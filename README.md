# __Task 1__
## Subtask 1
9 punktów :blush:
## Subtask 3
Cześć! Biorę udział w projekcie Dare IT Challenge "Zostań Testerem Manualnym" bo daje mi on możliwość usystematyzowania i poszerzenia wiedzy w temacie testowania. Cenię sobie, że projekt w dużym stopniu opiera się na pracy własnej. To bardzo rozwijające i zarazem ciekawe doświadczenie.
 
 W związku z tym, że kilka miesięcy temu podjęłam decyzję o zmianie branży i obecnie aktywnie poszukuję pracy jako tester manualny liczę, że stworzone podczas Challenge'u porfolio i zdobyta wiedza przyśpieszą ten proces. Ostatni, ale nie mniej ważny jest dla mnie fakt, że program Dare IT wspiera kobiety w przebranżowieniu się. Osobiście to dla mnie jedna z ważniejszych wartości :rocket:
 
Dobrego dnia, Joanna
## Subtask 4
### Scouts Panel
Aplikacja służy do gromadzenia informacji o graczach, zapisywania informacji o meczach oraz do tworzenia raportów. Zawiera szereg funkcjonalności 
### Funkcjonalności aplikacji: 
* dostępne z poziomu widoku "Gracze":
  * *wyszukiwanie* - działa w sposób intuicyjny
  * *filtrowanie* - działa w sposób intuicyjny, ale dodałabym w tym widoku dodatkowy przycisk "Szukaj" lub dała użytkownikowi możliwość przejścia do widoku z wyfiltrowanymi danymi po kliknięciu "Enter"
  * *wybór kolumn, które mają być prezentowane w tabeli "Gracze"* - działa w sposób intuicyjny
  * *drukowanie* - działa w sposób intuicyjny
  * *pobieranie pliku .csv* - działa w sposób intuicyjny
* zarządzanie dostępem: *logowanie, wylogowanie, przypomnienie hasła* działają w sposób intuicyjny; panel logowania jest prosty i czytelny
* możliwość sortowania wybranych kolumn w tabeli "Gracze" - ???
* możliwość dodania gracza - działa w sposób intuicyjny; dodałabym tą funkcjonalność również w widoku "Gracze" (teraz dostępna tylko ze strony głównej)
* możliwość dodania meczu
* możliwość edycji meczu
* możliwość dodania raportu - z poziomu widoku "Mecze" funkcjonalność działa intuicyjnie; z poziomu widoku "Raporty" po kliknięciu "Dodaj raport" użytkownik zostaje przekierowany do widoku "Mecze" bez komunikatu dlaczego tak się dzieje -> dodałabym komunikat np. "Wybierz mecz, aby dodać raport"; po dodaniu raportu użytkownik ma możliwość jego edytowania, bez możliwości obejrzenia -> dodałabym funkcjonalność "Pokaż" i wyświetliła raport w formie przyjaznej dla użytkownika
* możliwość edycji raportu
* możliwość zapisania danych statystycznych meczu - nazwa tej funkcjonalności (*Rozpocznij mecz*) jest nieczytelna dla użytkownika; poruszanie się po tym widoku nie jest intuicyjne; brak jest komunikatu, w którym miejscu dane zostają zapisane;
* możliwość zmiany języka - działa w sposób intuicyjny niemniej wybierając język polski, wszystkie komunikaty/polecenia powinny być wyświetlane użytkownikowi w języku polskim co obecnie się nie dzieje dotyczy m.in. "Submit" "Clear" "Save" "Required" "Next page" etc.
### Oceń interfejs aplikacji (wygląd) – czy Ci się podoba, czy nie?
Mimo, iż wiele funkcjonalności działa w aplikacji intuicyjnie to interfejs jest mało czytelny. Dane pszczególnych graczy prezentowane są jedynie w formie "do edycji" co powoduje, że nie są one czytelne. Otwarcie widoku "Edytuj raport" powoduje zmianę rozdzielczości strony.
### Czy aplikacja jest intuicyjna? (Intuicyjna, czyli np. nie masz problemu ze zrozumieniem, co należy kliknąć, żeby wejść do formularza dodawania nowego zawodnika piłki nożnej do systemu)
W wielu miejscach aplikacja jest intuicyjna niemniej znajdują się w niej funkcjonalności, które sprawiają trudność użytkownikowi. Brak jest możliwości szybkiego przejścia w tabeli graczy do konkretnej strony lub na koniec tabeli. Wypełnianie pół w formularzach też bywa nieintuicyjne jak na przykład w widoku "Dodawanie meczu" pola  Web MAtch lub General
### Co błędem jest / lub co może nim być?
  * widok "Dodaj gracza":
    * pole *"Imię"* przyjmuje inne znaki (cyfry, znaki specjalne) niż litery
    * pole *"Nazwisko"* przyjmuje inne znaki (cyfry, znaki specjalne) niż litery
    * pole *"Telefon"* przyjmuje inne znaki niż cyfry
    * pole *"Waga"* przyjmuje wartości ujemne
    * pole *"Wzrost"* przyjmuje wartości ujemne
    * pole *"Data urodzenia"* przyjmuje datę przyszłą
    * pole *"Data urodzenia"* umożliwia wpisanie 6-cio cyfrowej wartości w polu rok, ale aplikacja takiej wartości nie zapisze 
    * pole *"Języki"* przyjmuje inne znaki (cyfry, znaki specjalne) niż litery
    * pola *"Łączy nas piłka"* *"90 minut"* *"Profil facebook"* *"Link do Youtuba"* przyjmują dowolne wartości
  * widok "Dodaj mecz":
    * pole *"Czas gry"* przyjmuje wartości ujemne
    * pole *"Data"* przyjmuje datę przyszłą
    * pole *"Zdobyte gole"* *"Stracone gole"* przyjmują nieograniczoną liczbę znaków
  * do aplikacji można dodać dwóch graczy posiadających te same dane
