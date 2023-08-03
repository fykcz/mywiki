# Kronos hacks
## Metronom v combi
+ Na nějaký timber nastavit program **BB022**
+ V *Timbre param* nastavit *MIDI Chanel* na **02**.
+ V *EQ/Vector* / *Drum track* nastavit
  + Pattern: **P417**
  + Shift: **17**
  + MIDI Output: **02** (stejný jako v Timbre param)
  + **Start immediately**
+ *IFX* / *Routing* odškrtnout *DKit* a nastavit Bus na **3/4**

## Přepínání timbrů na SWx
+ V *IFX* vyrobit 2 efekty *St. Graphics 7EQ*
+ Oba nastavit společný vlastnosti:
  + 1:Wide 1
  + Samý nuly na křivku
  + Trim 0
  + Source: SWx
+ Ten, co funguje bez SW:
  + Dry, Amount +100
+ Ten, co hraje se SWx:
  + Wet, Amount -100
