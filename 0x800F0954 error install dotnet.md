# Error 0x800F0954 Installing .NET Framework 3.5 or Any Optional Feature
[Dobrej článek](https://www.winhelponline.com/blog/error-0x800f0954-net-framework-3-5-optional-feature-dism)

Pomohl následující scénář:
1. Spustit `regedit.exe`
2. Najít klíč `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU`
3. Proměnnou `UseWUServer` nastavit na `0`.
4. Ukončit Regedit
5. Restartovat Windows