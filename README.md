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
[Test cases for polish version Scouts Panel based on User Story](https://docs.google.com/spreadsheets/d/1pktYOvva2EH0U7ixQA7B8eZjI_xEWv-k/edit?usp=sharing&ouid=102495179488717236756&rtpof=true&sd=true)
## Subtask 2
[Test cases for polish version Scouts Panel based on *own experience*](https://docs.google.com/spreadsheets/d/1nn6H2g1wuZ40Idh5qz9mLMMYqW_QeTGk/edit?usp=sharing&ouid=102495179488717236756&rtpof=true&sd=true)
## Subtask 3
### Po co piszemy test case’y?
 
We write test cases to verify the functionality and functions of the tested software in an orderly manner. Test cases verify if the developed software fulfill functional requirements. All members of the development team can use them (probably with the same results 🙂).
## Subtask 4
[Test cases for Pick.Eat.Up application](https://docs.google.com/spreadsheets/d/1k-rQZWu_euDSkjHRWvZbLn16pgFtxCoe/edit?usp=sharing&ouid=102495179488717236756&rtpof=true&sd=true)
 
Unfortunately I couldn't make order and testing *"order case"* because packages wasn't available. I checked few location and the respons was the same. 
 
# TASK 3
## Subtask 1
[Bug report for polish version Scouts Panel](https://docs.google.com/spreadsheets/d/1073vGUSzrlxxvDqCOZxLaYZnBjw61Y7Dt4xAeBSQcXA/edit?usp=sharing) :bug:
## Subtask 2
[Test results for polish version Scouts Panel](https://docs.google.com/spreadsheets/d/14bi1fve6uSGn19nEu3hWufCq5hRbhJiamhDKv2YWibU/edit?usp=sharing) :bookmark_tabs:
## Subtask 3
[Test report for polish version Scouts Panel](https://docs.google.com/document/d/1i9otL6GiEcbY270c3kWJ8xqT8NsKEJnEjCWlTiUwdeo/edit?usp=sharing) :soccer:

# TASK 4
## Subtask 2
[Bug report for polish version FOCUSLY APP](https://docs.google.com/spreadsheets/d/1OTbKdH6J0KUXovK25_keQevShC6WpW79u7h-hneiXs8/edit?usp=sharing) :pray:
## Subtask 3
### Do czego służy ta aplikacja? Jaki jest cel tej aplikacji?
The FOCUSLY APP is a collection of materials and audio files dedicated to the concept of mindfulness. FOCUSLY includes content which helps people consciously live and breath. 
 
With this APP users can take challenges, define goals which they want working with e.g. sleep, stress, emotions, relationships, mental health and take part in courses e.g. mindfulness, meditation, breath. 
 
FOCUSLY makes possible saving favorite practices thanks to which the user has faster and easier access to them.
 
Most content is available for a monthly or yearly subscription fee. Only some of them are available for free.
### Kto ma być użytkownikiem końcowym aplikacji?
FOCUSLY APP is dedicated for people of all ages. It also includes practices dedicated to children.
 
APP can be useful for people who are searching for life balance and looking for information on how to live and eat healthy.
 
FOCUSLY is dedicated for music lovers too because it contents sounds of nature playlists.
### Czy według Ciebie aplikacja jest user friendly?
On many levels, the FOCUSLY APP is user friendly. Being able to use it as a guest is a very good solution. “Practice reminder” option is very useful and it is not pushing too much.
 
FOCUSLY colors are muted and reflect the character of the APP. They are coherent with the content.
 
In FOCUSLY APP there is no linking or redirecting to external pages which is a good practice because everything the user needs is inside the application.
### Jak byś usprawnił aplikację? Co byś w niej poprawił. Czy masz jakiś pomysł na dodatkową funkcjonalność?
Unfortunately, in some places navigating the FOCUSLY APP is not intuitive. 
 
“Plus” button redirect user to the homepage instead to e.g. “Your goal” form.
 
After changing language to english APP loses part of its resources. Some functionalities are not available or are available only to a limited extent.
 
Using APP as a guest, “Sign up” and “Log in” functionalities are available from Settings level which makes it difficult to access. “Log out” button is available only from Settings level too. All these functionalities should be placed on the homepage.
 
Contact form contains a short note “Our support will help you within seconds” which should be changed right away because this information is not true.
 
“Changing password” form in APP and “Forgot password” functionality should be coherent but they are not. “Changing password” form in APP requires a minimum 6 characters password. Using “Forgot password” functionality, the user is obliged to use a minimum 8 characters password.
 
“Breathing exercises” should contain short sounds during the exercise that would signal the change of “breathe in” “breathe out” “hold”. Currently it is necessary to look at the phone all the time during practice.
 
An extra functionality in the FOCUSLY APP could be short videos with yoga sessions.
### Jakie dostrzegasz różnice pomiędzy testowaniem aplikacji internetowej, a natywnej?
Testing a native app requires more attention to detail from the tester. Native applications have more restrictions on access to selected functionalities.
 
In testing a native app, it is important to pay attention if all available content is visible on the screen. If not, swipe functionality has to work fast and reliably. It is crucial because in web app testing we have many tools like: touchpad, mouse and keyboard and in native app we have only our fingers.
 
Describing steps in a bug report is more difficult in case of native app. Tester can use only screenshots or screen scans but not links. 
 
![meditation](https://user-images.githubusercontent.com/116754129/203097417-e6493f85-af57-43ef-bb3b-d25395e272c0.jpg)
# TASK 5
## Subtask 1
wymień operatory/zapytania jakich się nauczyłe_aś
## Subtask 3
1. Wyświetl tabelę actors w kolejności alfabetycznej sortując po kolumnie surname.
 
**SELECT * FROM `actors` ORDER BY surname ASC;**
 
![surname_asc](https://user-images.githubusercontent.com/116754129/204270616-6fd345cd-4707-4151-a6ff-30dd8f0aabf9.jpg)
 
2. Wyświetl film, który powstał w 2019 roku.
 
**SELECT * FROM `movies` WHERE year_of_production='2019';**
 
 
3. Wyświetl wszystkie filmy, które powstały między 1900, a 1999 rokiem.
 
**SELECT * FROM `movies` WHERE year_of_production BETWEEN '1900' AND '1999';**
