# winda
PROJEKT WINDY
mjura@student.agh.edu.pl

Opis Modelu

Model Windy przedstawia układ połączonych systemów, którego celem jest realizacja działania inteligentnej windy obsługującej kabinę, piętra, elementy bezpieczeństwa oraz system sterowania, wraz z obsługą nagrań wideo i sygnałów sterujących. Wszystkie zadania realizowane jest przez processor CPU, który połączony jest przez pętlę sprzężenia zwrotnego z głownymi magistralami każdego systemu. 

Spis komponentów:

SYSTEM:

A) Winda_Proj - główny system zawierający cały projekt;

B) Kabina - podsystem systemu Winda_Proj;

C) Przyciski_Pieter - podsystem systemu Kabina;

D) Przyciski_Funkcjonalne - podsystem systemu Kabina;

E) Pietra - podsystem systemu Winda_Proj;

F) Pietro0 - podsystem systemu Pietra;

G) Pietro1 - podsystem systemu Pietra;

H) Pietro2 - podsystem systemu Pietra;

I) Pietro3 - podsystem systemu Pietra;

J) Sterowanie - podsystem systemu Winda_Proj;

DEVICE:

a) Przycisk_Pietra_0 – urządzenie wyboru piętra 0;

b) Przycisk_Pietra_1 – urządzenie wyboru piętra 1;

c) Przycisk_Pietra_2 – urządzenie wyboru piętra 2;

d) Przycisk_Pietra_3 – urządzenie wyboru piętra 3;

e) Przyciski_Awarii – przycisk zgłoszenia awarii;

f) Przycisk_STOP – przycisk awaryjnego zatrzymania;

g) Przycisk_Pomoc – przycisk wezwania pomocy;

h) Przycisk_Otworz_Drzwi – przycisk otwierania drzwi;

i) Przycisk_Zamknij_Drzwi – przycisk zamykania drzwi;

j) Przycisk_Komunikatow_Glosowych – przycisk komunikatów głosowych;

k) Wentylator – przycisk wentylacji;

l) Wentylator_Windy – wentylator kabiny windy;

m) Drzwi – drzwi windy;

n) Glosnik – głośnik w kabinie;

o) Mikrofon – mikrofon w kabinie;

p) Wyswietlacz – wyświetlacz informacyjny;

q) Swiatla_Winda – oświetlenie kabiny;

r) Kamera_Winda – kamera w kabinie;

s) Waga – czujnik masy w kabinie;

t) Swiatla_Korytarz – oświetlenie korytarza piętra;

u) Kamera_Korytarz – kamera korytarzowa;

v) Czujnik_Ruchu – czujnik ruchu na piętrze;

BUS:

a) wylaczanie – magistrala sterowania wyłączaniem i zbierania danych;

b) sygnaly – magistrala sygnałów pomiędzy piętrami i sterowaniem;

c) kryzys – magistrala sygnałów kryzysowych;

d) element – magistrala sterowania urządzeniami (wentylator, głośnik);

e) element2 – magistrala sterowania zasilaniem urządzeń;

f) polaczanie – magistrala sterowania urządzeniami pięter;

g) pietra1 – magistrala agregacji nagrań z pięter;

h) sygnal – magistrala sygnałowa pomocnicza;

i) Nagrania – magistrala przesyłania danych nagrań;

j) ster – magistrala sterowania systemem;

k) sygnaly – magistrala sygnałów pomiędzy systemami;

PROCESS:

a) nagryw – proces odpowiedzialny za obsługę nagrań wideo;

THREAD:

a) nagrywanie – wątek odpowiedzialny za odbiór i zapisy nagrań;

b) zgrywanie – wątek odpowiedzialny za przekazywanie nagrań;

MEMORY

a) Materialy_Video – pamięć przechowująca materiały wideo;

PROCESSOR:

a) CPU – procesor realizujący sterowanie i planowanie wątków;
