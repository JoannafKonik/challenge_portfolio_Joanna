# __Task 1__
## Subtask 1
9 punktów :blush:
## Subtask 3
Cześć! Biorę udział w projekcie Dare IT Challenge "Zostań Testerem Manualnym" bo daje mi on możliwość usystematyzowania i poszerzenia wiedzy związanej z przeprowadzaniem testów oprogramowania. Cenię sobie, że projekt w dużym stopniu opiera się na pracy własnej. To bardzo rozwijające i zarazem ciekawe doświadczenie.
 
 W związku z tym, że kilka miesięcy temu podjęłam decyzję o zmianie branży i obecnie aktywnie poszukuję pracy jako tester manualny liczę, że stworzone podczas Challenge'u porfolio i zdobyta wiedza przyśpieszą ten proces. Ostatni, ale nie mniej ważny jest fakt, że program Dare IT wspiera kobiety w przebranżowieniu się. Osobiście to dla mnie jedna z ważniejszych wartości :rocket:
 
Dobrego dnia, Joanna
## Subtask 4
### Scouts Panel
Aplikacja służy do gromadzenia szczegółowych danych o graczach, zapisywania informacji o meczach oraz tworzenia raportów meczowych. Ponadto umożliwia przeglądanie tych danych oraz ich edytowanie.
### Funkcjonalności aplikacji: 
* dostępne z poziomu widoku "Gracze":
  * *wyszukiwanie* - działa w sposób intuicyjny
  * *filtrowanie* - działa w sposób intuicyjny, ale dodałabym w tym widoku dodatkowy przycisk "Szukaj" lub dała użytkownikowi możliwość przejścia do widoku z wyfiltrowanymi danymi po kliknięciu "Enter"
  * *wybór kolumn, które mają być prezentowane w tabeli "Gracze"* - działa w sposób intuicyjny
  * *drukowanie* - proces wydruku nie jest przeprowadzony optymalnie; układ wydruku nie jest tożsamy z widokiem strony
  * *pobieranie pliku .csv* - działa w sposób intuicyjny, ale zawiera błędy (szczegóły poniżej)
* zarządzanie dostępem: *logowanie, wylogowanie, przypomnienie hasła* działają w sposób intuicyjny; panel logowania jest prosty i czytelny
* możliwość sortowania wybranych kolumn w tabeli "Gracze" - działa w sposób intuicyjny, ale zawiera błędy (szczegóły poniżej)
* możliwość dodania gracza - działa w sposób intuicyjny; dodałabym tą funkcjonalność również w widoku "Gracze" (teraz dostępna tylko ze strony głównej)
* możliwość dodania meczu
* możliwość edycji meczu
* możliwość dodania raportu - z poziomu widoku "Mecze" funkcjonalność działa intuicyjnie; z poziomu widoku "Raporty" po kliknięciu "Dodaj raport" użytkownik zostaje przekierowany do widoku "Mecze" bez komunikatu dlaczego tak się dzieje -> dodałabym komunikat np. "Wybierz mecz, aby dodać raport"; po dodaniu raportu użytkownik ma możliwość jego edytowania, bez możliwości obejrzenia -> dodałabym funkcjonalność "Pokaż" i wyświetliła raport w formie przyjaznej dla użytkownika
* możliwość edycji raportu
* możliwość zapisania danych statystycznych meczu - nazwa tej funkcjonalności (*Rozpocznij mecz*) jest nieczytelna dla użytkownika; poruszanie się po tym widoku nie jest intuicyjne; brak jest komunikatu, w którym miejscu dane zostają zapisane;
* możliwość zmiany języka - działa w sposób intuicyjny niemniej wybierając język polski, wszystkie komunikaty/polecenia powinny być wyświetlane użytkownikowi w języku polskim co obecnie się nie dzieje dotyczy m.in. "Submit" "Clear" "Save" "Required" "Next page" etc.
### Interfejs aplikacji - moja ocena:
Mimo, iż wiele funkcjonalności działa w aplikacji intuicyjnie to interfejs jest mało czytelny. Informacje o graczach, meczach i raportach prezentowane są w formie tabel "do edycji" co jest formą mało przyjazną użytkownikowi. Brakuje elementów graficznych oraz opcji pozwalającej na przykład na porównanie dwóch lub większej ilości graczy. W sytuacji kiedy w polu tekstowym wprowadzona jest duża ilość znaków strona nie skaluje się do wielkości ekranu co powoduje rozciągnięcie strony i konieczność przesuwania ekranu suwakiem.
### Czy aplikacja jest intuicyjna?
W wielu miejscach aplikacja jest intuicyjna niemniej znajdują się w niej funkcjonalności, które sprawiają użytkownikowi trudności w poruszaniu się po niej. W tabeli "Gracze" brak jest możliwości szybkiego przejścia do konkretnej strony lub na koniec tabeli. Nieintuicyjne bywa też wypełnianie pól w formularzach. Podczas dodawania lub edytowania Gracza pojawia się komunikat "Nie udało się dodać / zaktualizować gracza" bez informacji, które pola zostały błędnie wypełnione. Najmniej intuicyjne jest poruszanie się po widoku *"Rozpocznij mecz"*. 
### Co błędem jest / lub co może nim być?
  * widok "Dodaj gracza":
    * pole *"Imię"* przyjmuje inne znaki (cyfry, znaki specjalne) niż litery
    * pole *"Nazwisko"* przyjmuje inne znaki (cyfry, znaki specjalne) niż litery
    * pole *"Telefon"* przyjmuje inne znaki niż cyfry
    * pole *"Waga"* przyjmuje wartości ujemne
    * pole *"Wzrost"* przyjmuje wartości ujemne
    * pole *"Data urodzenia"* przyjmuje datę przyszłą
    * pole *"Data urodzenia"* umożliwia wpisanie 6-cio cyfrowej wartości w polu rok, mimo, iż aplikacja takiej wartości nie zapisuje
    * pole *"Języki"* przyjmuje inne znaki (cyfry, znaki specjalne) niż litery
    * pola *"Łączy nas piłka"* *"90 minut"* *"Profil facebook"* *"Link do Youtuba"* przyjmują dowolne wartości
  * widok "Dodaj mecz":
    * pole *"Czas gry"* przyjmuje wartości ujemne
    * pole *"Data"* przyjmuje datę przyszłą
    * pole *"Zdobyte gole"* *"Stracone gole"* przyjmują nieograniczoną ilości znaków
  * aplikacja zezwala na wprowadzenie nieograniczonej ilości znaków w większości pól w formatce *"Dodaj gracza"* i *"Dodaj mecz"* co powinno być uznane za błąd ponieważ prowadzi do tego, że tabele z danymi stają się mało czytelne
  * do aplikacji można dodać dwóch graczy posiadających te same dane
  * sortowanie - funkcja sortowania działa, ale metoda sortowania jest nieprawidłowa (np. nierozpoznawanie małej i dużej litery, odwrotne sortowanie w kolumnie "Wiek")
  * pobieranie pliku .csv - brak funkcji "Pobierz wszystko"; pobranie pliku możliwe jest tylko w obrębie danego widoku (10 wierszy)
  * pobieranie pliku .csv - próba odczytania pliku .csv wskazuje na to, że podczas eksportu nie przeniosły się poprawne wszystkie wartości; dotyczy kolumn: Wiek, Mecze, Recenzja, Raporty
  * brak funkcjonalności usuwania gracza, meczu, raportu
  * nie działa opcja *"Wróć do raportu"*, która wyświetlona jest w widoku "Niezapisany mecz" na stronie głównej aplikacji
  * konsola wyświetla błąd *"Params `start` and `limit` are deprecated."*

# Task 2
## Subtask 1
[Test cases for Scouts Panel based on User Story](https://docs.google.com/spreadsheets/d/1pktYOvva2EH0U7ixQA7B8eZjI_xEWv-k/edit?usp=sharing&ouid=102495179488717236756&rtpof=true&sd=true)
## Subtask 2
[Test cases for Scouts Panel based on own experience](...)
## Subtask 3
sdfghj
## Subtask 4
[Test cases for Pick.Eat.Up application](https://docs.google.com/spreadsheets/d/1k-rQZWu_euDSkjHRWvZbLn16pgFtxCoe/edit?usp=sharing&ouid=102495179488717236756&rtpof=true&sd=true)
 
Unfortunately I couldn't make order because packages wasn't available. I checked few location and the respons was the same. 
