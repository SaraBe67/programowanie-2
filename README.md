# programowanie-2
1. **Cel analizy**

Głównym celem projektu jest przewidywanie poziomu stresu u studentów. Analiza bierze pod uwagę czynniki stresogenne typowe dla środowiska akademickiego oraz konstruktywne i niekonstruktywne sposoby radzenia sobie ze stresem. Finalnym zadaniem kodu jest zbudowanie i ocena modelu uczenia maszynowego, który najlepiej prognozuje ten poziom.


2. **Opis danych**

Analiza została przeprowadzona na zbiorze danych z pliku coping_with_stress.csv, zawierającym 200 640 wierszy i 15 kolumn. Każdy wiersz reprezentuje pojedynczego studenta, a kolumny opisują następujące cechy:
 
  a) Dane demograficzne i akademickie:
   * age: Wiek studenta,
   * academic_year: Rok studiów - od 1 do 4,
   * study_hours_per_day: Liczba godzin nauki dziennie - 0-14,
   * academic_performance: Wyniki w nauce / oceny 0-100 ,

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
    * screen_time: Czas spędzony przed ekranem - 0-12 (h)

Dane pochodzą ze strony Kaggle.com i zostały wygenerowane **syntetycznie** - mogą posłużyć jedynie do celów edukacyjnych, jak np. analiza danych, implementacja modeli uczenia maszynowego do przewidywania wybranych wartości. 
(Student Lifestyle, Mental Health & Burnout Insight; A comprehensive dataset analyzing student stress, lifestyle, and burnout pattern; autor - A.)


