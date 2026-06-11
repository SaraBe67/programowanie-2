# programowanie-2
## 1. **Cel analizy**

Głównym celem projektu jest przewidywanie poziomu stresu u studentów. Analiza bierze pod uwagę czynniki stresogenne typowe dla środowiska akademickiego oraz konstruktywne i niekonstruktywne sposoby radzenia sobie ze stresem. Finalnym zadaniem kodu jest zbudowanie i ocena modelu uczenia maszynowego, który najlepiej prognozuje ten poziom.

## 2. **Opis danych**

Analiza została przeprowadzona na zbiorze danych z pliku coping_with_stress.csv, zawierającym 200 640 wierszy i 15 kolumn. Każdy wiersz reprezentuje pojedynczego studenta, a kolumny opisują następujące cechy:
 
a) Dane demograficzne i akademickie:
 * age: Wiek studenta,
 * academic_year: Rok studiów - od 1 do 4,
 * study_hours_per_day: Liczba godzin nauki dziennie - 0-14,
 * academic_performance: Wyniki w nauce / oceny 0-100,

b) Czynniki psychologiczne i samopoczucie:
 * stress_level: Poziom stresu (zmienna docelowa / objaśniana) - 0-10,
 * anxiety_score: Wynik określający poziom lęku - 0-10,
 * depression_score: Wynik określający poziom depresji - 0-10,
 * burnout_score: Wynik określający poziom wypalenia - 0-10,
   
c) Czynniki stresogenne i środowiskowe:
 * exam_pressure: Presja związana z egzaminami - 0-10,
 * financial_stress: Stres finansowy - 0-10,
 * family_expectation: Oczekiwania rodziny - 0-10,
  
d) Styl życia i wsparcie (czynniki radzenia sobie ze stresem):
 * sleep_hours: Liczba godzin snu - 0-10,
 * physical_activity: Aktywność fizyczna - 0-7 (h),
 * social_support: Wsparcie społeczne - 0-10,
 * screen_time: Czas spędzony przed ekranem - 0-12 (h).

Wyniki 0-10 zostały wyrażone jako skala punktowa od 0 do 10 (0 to wartość minimalna, 10 to wartość maksymalna), chyba że z opisu wynika inaczej.

Dane pochodzą ze strony Kaggle.com i zostały wygenerowane **syntetycznie** - mogą posłużyć jedynie do celów edukacyjnych, jak np. analiza danych, implementacja modeli uczenia maszynowego do przewidywania wybranych wartości. 
(*Student Lifestyle, Mental Health & Burnout Insight; A comprehensive dataset analyzing student stress, lifestyle, and burnout pattern*; autor - A.)

## 3. **Wyniki analizy**

Komenda "stress.info" ujawniła brak pustych wartości. 

**Wykresy pudełkowe "Rozkład zmiennych wyrażonych w godzinach" i "Rozkład zmiennych w skalach punktowych (0-10)"**

Z analizy obu wykresów wyłania się obraz studenta, który znajduje się pod silną presją zewnętrzną (egzaminy, rodzina) i spędza bardzo dużo czasu statycznie (na nauce i przed ekranem). Mimo że ogólne wskaźniki depresji i lęku w całej populacji utrzymują się na niskim poziomie, wysoka presja i brak ruchu stanowią bezpośredni czynnik ryzyka dla grupy studentów znajdujących się w skrajnych częściach rozkładu (długie wąsy wykresów zdrowia psychicznego).

**Histogramy dla zmiennych "stress_stats"**

- Prawie wszystkie zmienne mają rozkład płaski (jednostajny) - zbiór danych jest **wygenerowany sztucznie**.
- **Brak problemu z klasami rzadkimi** (Imbalance): Ponieważ stress_level ma płaski rozkład, Twój model uczy się na tak samo licznej reprezentacji osób o niskim, średnim, jak i wysokim stresie. Model nie będzie "faworyzował" żadnej grupy.
- Brak wartości odstających (Outliers).
- **Wyzwanie dla korelacji liniowych**: Ponieważ zmienne losowe z rozkładów jednostajnych bez naturalnego szumu potrafią zachowywać się bardzo matematycznie, modele nieliniowe mogą na tych danych osiągać podejrzanie dobre wyniki, łatwo mapując zależności.
