# winda
PROJEKT WINDY
mjura@student.agh.edu.pl

Opis Modelu

Model Windy przedstawia układ połączonych systemów, którego celem jest realizacja działania inteligentnej windy obsługującej kabinę, piętra, elementy bezpieczeństwa oraz system sterowania, wraz z obsługą nagrań wideo i sygnałów sterujących. Wszystkie zadania realizowane jest przez processor CPU, który połączony jest przez pętlę sprzężenia zwrotnego z głownymi magistralami każdego systemu.  Każde z urządzeń połączone jest do magistrali zasilającej, elementy sterujące do magistrali CAN.


SCHEMAT CAŁEGO UKŁADU:
![image alt](https://github.com/MaxymJ/winda/blob/main/winda3p.png)

W systemie głównym znajdują się:

2 magistrale

a) Magistrala zasilająca: 
bus Szyna_Zasilania;

b) Magistrala sterująca:
bus Kabel_CAN;

1 urządzenie

c) zasilacz główny:
device Glowne_Zasilanie;

2 podsystemy

d) System Kabiny windy:
system Kabina;

e) System maszynowni sterujacej:
system Maszynownia;

PODSYSTEM KABINA:
![image alt](https://github.com/MaxymJ/winda/blob/main/kabina.png)

1 procesor

a) Jednostka obliczeniowa kabiny:
processor cpu;

1 pamięć

b) Pamięć lokalna: 
memory pamiec;

1 magistrala

c) Magistrala lokalna danych: 
bus szyna_lok;

1 proces

d) Aplikacja sterująca kabiną: 
process aplikacja;

4 urządzenia

e) Mechanizm otwierania drzwi: 
device drzwi;

f) Oświetlenie wewnętrzne: 
device swiatlo;

g) Kamera monitoringu: 
device kamera;

h) Panel przycisków pasażera:
device panel;

PODSYSTEM MASZYNOWNIA:
![image alt](https://github.com/MaxymJ/winda/blob/main/maszynownia.png)

1 procesor

a) Główny procesor sterujący:
processor cpu;

1 pamięć

b) Złożona pamięć sterownika (Flash/RAM):
memory pamiec;

1 magistrala

c) Magistrala systemowa:
bus szyna_sys;

1 proces

d) Aplikacja logiki sterowania windą:
process aplikacja;

2 urządzenia

e) Silnik wciągarki:
device silnik;

f) Wyświetlacz numeru piętra:
device lcd_pietra;

a) CPU – procesor realizujący sterowanie i planowanie wątków;

Wykonane analizy:

a)Computing Electrical Power for Szyna_Zasilania

<img width="1791" height="121" alt="image" src="https://github.com/user-attachments/assets/6b613d59-bb79-4a3e-a37b-380142fc5937" />

b)Resource Budget Analysis

<img width="1306" height="1321" alt="image" src="https://github.com/user-attachments/assets/3a6ece3e-300a-4e01-9f5b-2fcf57981fb0" />

LITERATURA:
[1] OSATE 2 - Open Source AADL Tool Environment - https://osate.org/
[2] AADL Community Resources and Examples - https://github.com/osate <br [3] SAE International, "AS5506C: Architecture Analysis & Design Language (AADL)," SAE International Standard, 2017 - https://www.sae.org/standards/content/as5506c/>
[3] Introduction to AADLa and OSATE - https://www.youtube.com/watch?v=MjUQZaqaTA4


