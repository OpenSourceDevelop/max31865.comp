# max31865.comp
a max31865 modul for LinuxCNC

* SPI-Initialisierung: Passt das SPI-Protokoll für den MAX31865 an (8-Bit Transfers, Mode 0).
* Widerstands-zu-Temperatur-Umrechnung: Implementiert die Callendar-Van Dusen-Gleichung, die typisch für RTD-Sensoren ist.
* Fehlerbehandlung: Setzt ein Bit bei einem Fehler (z. B. Drahtbruch).
* Parameter: Ermöglicht die Anpassung an PT100 oder PT1000 und Referenzwiderstände.



halcompile --install max31865.comp



example:

loadrt max31865
addf max31865.update servo-thread
setp max31865.r_ref 430
setp max31865.rtd_nominal 100
setp max31865.wire_mode 3
