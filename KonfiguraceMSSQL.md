# Konfigurace SQL
## Disky a soubory
### Málo disků
SQL Server komunikuje se soubory dvěma směry, čtení a zápis dat z/do datových souborů, WAL (**W**rite **A**head **L**ogging) používaný u transakčního logu.

I ve virtuálním prostředí je potřeba vzít více disků. Jakmile SQL zjistí, že má k dispozici jeden diskový řadič, tak začne sám požadavky na disky sequencovat (ztráta 10-15%). SQLko běží v uživatelském režimu, nikoli kernel modu, takže vidí jen to, co mu ukáže OS.
### NTFS bloky dělat 64kB
SQL čte celé extenty (64kB) nebo segmenty neznámé velikosti.
### RAID level
0, 1, 5, 10

Největší problém je s RAID 5 s málo fyzickými disky. Je potřeba násobek 3 (aby to správně fungovalo).
RAID 5 na datové soubory.
### Umístění souborů
C: pro systém
D: pro data
E: transakční logy
T: tempdb
X: logy, trace files, audit logy
### Nastavení souborů databází
Malé soubory -> častý filegrowth => je jednodušší zvětšovat najednou po větších kusech.

Datové soubory v jedné filegroupě (**P**roportional **F**ill **A**lgothytm) - většímu dej víc, může se stát, že větší soubory ve filegroupě trpí větší zátěží. Na filegroupě je vlastnost *Autogrowth All Files*. Zátěž primárního datového souboru je mírně větší, než ostatní datové soubory. PFA pak zkurví výkon na primary file.
#### Automatic Filegrowth
**Nikdy v procentech**

Větší MB než default 64kB.

Report **Disk Usage**. Tam lze najít sekci Disk Autogrowth/Autoshrink, kde je vidět, jak se to zvětšovalo a jak to dlouho trvalo.
### *tempdb*
Potřebujou ji všichni. Je potřeba ji mít na vlastním disku.
### *tiering*
Co nejrychlejší přístup pro soubory transakčního logu, datové soubory mohou být na pomalejších discích.
### Malý soubor transakčního logu
Interně je rozdělen na sekce, tzv. **V**irtual **L**og **F**ile. Velikost VLF není známá, pokud jsou ve VLF všechny transakce promítnuty do datového souboru (Simple Recovery - checkpoint, záloha trlogu) - tj. jsou všechny transakce už neaktivní, tak SQL Server smajzne VLFko. Ale SQL Server pokračuje dál do dalšího VLFka. Když dojde na konec souboru, tak začne od začátku a používá smajznutý prostory. U větších DB jsou malé stovky VLFek v cajku, jak přelezeme 2000+, jsme v háji. SQLko se pak blbě orientuje, který VLFko je aktivní.

`dbcc loginf()`

Důležitý je počet zobrazených záznamů. Když je jich mooooc, tak přepnout recovery model na simple, chvilku počkat (větší chvilku) a pak `dbcc shrinkfile(2)`. Shrink soubor nemusí zmenšit, protože zrovna má aktivní VLFko na konci souboru a shrink uvolňuje pouze zezadu.
## Paměti
### Min a Max server memory
Omezení nejmenší a největší velikosti Buffer Poolu.
#### Min server memory
Až SQL Server postupně alokuje paměť, která přesáhne min. server memory, tak už to nevrátí.
#### Max server memory
SQL nebude mít Buffer Pool větší než max. server memory, ale ostatní komponenty omezeny nejsou.
#### Nastavovat nebo ne?
Pokud je jediná významná služba na OS, tak nenastavovat.

Když tam běží další komponenty (SSAS, SSRS, ...), tak např. max. server memory má smysl. SQL Server to má pak jednodušší.
#### Minimum Memory per Query
- V základním nastavení 1024kB
- Základní velikost paměti přidělené pro zpracování dotazu
- SQL Server si velikost paměti určuje na základě optimalizace
- Pro DWH je málo dotazů s velkým rancem dat, lze nastavit větší paměť (klidně na několik i desítek MB).
- Pro OLTP je zas hodně dotazů s malým objemem dat, tam je lepší na to nešahat.
- **Neléčit tím problém optimalizace (nejsou aktualizace statistik, developer blbě píše dotazy).**, když je zamlžená **cardinality estimation**.
  - Excessive Memory Grant - plýtvání pamětí, protože si SQL server myslí, že bude potřebovat raketu a pak potřebuje 2MB
  - Additional Memory Grants - naopak, za běhu dotazu potřebuje přidat paměť a to zdržuje.
### In-Memory OLTP
Nedá se omezit paměť. Je potřeba hooooodně paměti, daleko víc, než vyžaduje samotnej SQL server.

Od verze 2016 SP1 je to ve všech edicích SQL Serveru.

Když je In-Memory OLTP, tak je třeba počítat navíc 1/4 max velikosti buffer poolu.
- Standard až 32GB na jednu db.
- Enterprise až 2TB, na celou instanci
## Procesory
Nejlépe neřešit a nešahat.

Tam kde je více procesorů a více instancí SQL serveru, lze rozdělit na instance.

Už se nezakazuje CPU0. Od verze 2005 to je jedno.

SQL Server vidí logické procesory.
### Max. Worker Threads
- Max. Worker Threads = 512 (max. 4 CPU)
- Max. Worker Threads = (počet CPU - 4) * 16 + 512
- Worker Thread má 2MB
- `select * from sys.dm_os_workers` - kolik je workerů vytvořeno (vznikají dynamicky), po 15ti minutách nepoužívání je worker zgarbagován
- když jsou problémy s pamětí, tak nastavit na Max. Worker Threads
## Další vlastnosti instance
### Default Language
Default Language nemá nic společného s Collation!

Default Language definuje jen v jakém jazyce chodí na klienta chybová hlášení.

Default Language se nastavuje na login.

### Optimize for Ad-hoc Workloads
- Default: false
- Ovlivňuje, kdy se ukládá plán vykonání pro Plan Cache.
- Každý plán se uloží jako cache entry.
- Pokud je zapnuto, tak se plan ukládá až při druhém vykonání stejného plánu.
- `select * from sys.dm_exec_cached_plans` - size in bytes
- Report **Memory Consumption**
  - CACHESTORE_SQLCP - cache plany v grafu, čím víc, tím víc dynamickejch dotazů
  - CACHESTORE_OBJCP - cache plany procedur
- Zvyšuje míru rekompilací plánů
- Jen pro velké množství dynamického SQL, skládaných na klientu

### Cost Threshold for Parallelism
- Default 5
- Každý operátor na SQL Serveru má svou cenu - časoprostorové vyjádření náročnosti operace
- Prahová cena paralelismu udává, jakou cenu musí operátor překročit, aby jej SQL Server prováděl paralelně
- **Activity monitor** - Resource Waits, CXPACKET ukazuje, že je tam moc paralelismu
- Prahovou cenu zvyšujeme, když máme mnoho paralelních dotazů a naše instance trpí na nadměrná čekání CXPACKET
- Obecné pravidlo:
  - OLTP máme paralelismus méně rádi
  - OLAP databáze naopak jsou vhodnější pro paralelismy
- Vhodné přidávat po 5ti
### Max Degree of Parallelism
- Default 0
- Hodnota, která říká, kolik CPU může být najednou využíváno v rámci jednoho paralelního dotazu
  - Je-li MAXDOP 4, neznamená to, že si SQL Server nevyrobí víc workerů, ale vždy poběží jen 4. z nich
- Od SQL 2016 lze MAXDOP nastavovat per DB.
- Pro SharePoint DB se nastavuje MAXDOP 1 (zakazuje se paralelism).