# __Task 1__
## Subtask 1
9 punktów :blush:
## Subtask 2
- [x] repozytorium w GitHub zostało utworzone
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
## Subtask 1
- [x] bug report form was created
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
### Wymień operatory/zapytania jakich się nauczyłaś:
 
- [x] SELECT

- [x] SELECT DISTINCT

- [x] WHERE

- [x] ORDER BY

- [x] LIKE

- [x] IN

- [x] BETWEEN

- [x] AND, OR, NOT

- [x] NULL VALUES

- [x] INSERT INTO

- [x] UPDATE
## Subtask 2
- [x] xampp was installed
## Subtask 3
### SQL tasks
**1. Wyświetl tabelę actors w kolejności alfabetycznej sortując po kolumnie surname.**
 
SELECT * FROM `actors` ORDER BY surname ASC;
 
![surname_asc](https://user-images.githubusercontent.com/116754129/204270616-6fd345cd-4707-4151-a6ff-30dd8f0aabf9.jpg)
 
**2. Wyświetl film, który powstał w 2019 roku.**
 
SELECT * FROM `movies` WHERE year_of_production='2019';
 
![movie_2019](https://user-images.githubusercontent.com/116754129/204273859-0fc800db-3abc-4ca7-bbc5-72ff74b02dbc.jpg)
 
**3. Wyświetl wszystkie filmy, które powstały między 1900, a 1999 rokiem.**
 
SELECT * FROM `movies` WHERE year_of_production BETWEEN '1900' AND '1999';
 
![movies_1900_1999](https://user-images.githubusercontent.com/116754129/204273937-02b4ebd9-e5eb-4d0e-bd7f-12a7cdf17fd1.jpg)
 
**4. Wyświetl JEDYNIE tytuł i cenę filmów, które kosztują poniżej 7$**
 
SELECT title, price FROM `movies` WHERE price<'7';
 
![price_7](https://user-images.githubusercontent.com/116754129/204276527-c43f3953-fac2-4c2b-8a9e-c4bb63d94012.jpg)
 
**5. Użyj operatora logicznego AND, aby wyświetlić aktorów o actor_id pomiędzy 4-7 (4 i 7 powinny się wyświetlać). NIE UŻYWAJ operatora BETWEEN.**
 
SELECT * FROM `actors` WHERE actor_id>='4' AND actor_id<='7';
 
![actors_4_7](https://user-images.githubusercontent.com/116754129/204278009-fe48977b-70a7-4880-8382-69dbc7986cdd.jpg)
 
**6. Wyświetl klientów o id 2,4,6 wykorzystaj do tego warunek logiczny.**
 
SELECT * FROM `customers` WHERE customer_id='2' OR customer_id='4' OR customer_id='6';
 
![customers_2_4_6](https://user-images.githubusercontent.com/116754129/204279023-f1e4fbb1-e81d-471e-ba3d-567de4f0167a.jpg)
 
**7. Wyświetl klientów o id 1,3,5 wykorzystaj do tego operator IN.**
 
SELECT * FROM `customers` WHERE customer_id IN (1,3,5);
 
![customers_1_3_5](https://user-images.githubusercontent.com/116754129/204280008-fed33def-da12-4b29-83f7-358a15a273eb.jpg)
 
**8. Wyświetl dane wszystkich osób z tabeli ‘actors’, których imię zaczyna się od ciągu “An”.**
 
SELECT * FROM `actors` WHERE name LIKE 'An%';
 
![name_An](https://user-images.githubusercontent.com/116754129/204320688-9980817f-a7fd-4537-9e4f-52f45dd4417b.jpg)
 
**9. Wyświetl dane klienta, który nie ma podanego adresu email.**
 
SELECT * FROM `customers` WHERE email IS NULL;
 
![null](https://user-images.githubusercontent.com/116754129/204322150-5c01442b-50a4-4e67-ba03-d4bab1a83edf.jpg)

**10. Wyświetl wszystkie filmy, których cena wynosi powyżej 9$ oraz ich ID mieści się pomiędzy 2 i 8 movie_id.**
 
SELECT * FROM `movies` WHERE price>'9' AND (movie_id BETWEEN '2' AND '8');
 
![movie](https://user-images.githubusercontent.com/116754129/204324667-469bda85-d5fb-4dca-8b9b-7317080e14a5.jpg)
 
# TASK 5
## Subtask 1
### SQL tasks - cont.
**11. Popełniłam błąd wpisując nazwisko Ani Miler – wpisałam Muler. Znajdź i zastosuj funkcję, która poprawi mój karkołomny błąd**

UPDATE customers SET surname='Miler' WHERE customer_id='3'

![surname_change](https://user-images.githubusercontent.com/116754129/205654815-05d59cbd-22d9-48a1-9c10-fd62fbf27419.jpg)

**12. Pobrałam za dużo pieniędzy od klienta, który kupił w ostatnim czasie film o id 4. Korzystając z funkcji join sprawdź, jak ma na imię klient i jakiego ma maila. W celu napisania mu wiadomości o pomyłce fantastycznej szefowej.**

SELECT customers.name, customers.email FROM customers INNER JOIN sale ON customers.customer_id = sale.customer_id WHERE sale.movie_id='4';

![movie id_4](https://user-images.githubusercontent.com/116754129/205691137-52c0105f-0013-4336-b36b-7a39aab7fcd7.jpg)

**13. Na pewno zauważył_ś, że sprzedawca zapomniał wpisać emaila klientce Patrycji. Uzupełnij ten brak wpisując: pati@mail.com**

UPDATE customers SET email='pati@mail.com' WHERE customer_id='4'

![email_null](https://user-images.githubusercontent.com/116754129/205656618-e0d11338-43c5-478e-93a2-9c6d0e8c10cb.jpg)

**14. Dla każdego zakupu wyświetl, imię i nazwisko klienta, który dokonał wypożyczenia oraz tytuł wypożyczonego filmu. (wykorzystaj do tego funkcję inner join, zastanów się wcześniej, które tabele Ci się przydadzą do wykonania ćwiczenia).**

SELECT sale.*, customers.name, customers.surname, movies.title FROM ((sale INNER JOIN customers ON customers.customer_id = sale.customer_id) INNER JOIN movies ON sale.movie_id = movies.movie_id);

![sale_customer_movie](https://user-images.githubusercontent.com/116754129/205708720-0eefc0d9-2195-44f6-b1d5-9040f9d6987d.jpg)

**15. W celu anonimizacji danych, chcesz stworzyć pseudonimy swoich klientów. - Dodaj kolumnę o nazwie ‘pseudonym’ do tabeli customer,- Wypełnij kolumnę w taki sposób, aby pseudonim stworzył się z dwóch pierwszych liter imienia i ostatniej litery nazwiska. Np. Natalie Pilling → Nag**

ALTER TABLE customers ADD pseudonym VARCHAR(255)

**16. Wyświetl tytuły filmów, które zostały zakupione, wyświetl tabelę w taki sposób, aby tytuły się nie powtarzały.**

SELECT DISTINCT movies.title FROM movies INNER JOIN sale ON movies.movie_id = sale.movie_id;

![movies](https://user-images.githubusercontent.com/116754129/205716642-229627da-08ae-4523-8bcf-7a1a9c26159d.jpg)

**17. Wyświetl wspólną listę imion wszystkich aktorów i klientów, a wynik uporządkuj alfabetycznie. (Wykorzystaj do tego funkcji UNION)**

SELECT name FROM actors UNION ALL SELECT name FROM customers ORDER BY name ASC;

![name_actors_customers](https://user-images.githubusercontent.com/116754129/205718196-493cfe76-3083-4e94-aae9-c91b5ad88163.jpg)

**18. Polskę opanowała inflacja i nasz sklepik z filmami również dotknął ten problem. Podnieś cenę wszystkich filmów wyprodukowanych po 2000 roku o 2,5 $ (Pamiętaj, że dolar to domyślna jednostka- nie używaj jej nigdzie).**

**19. Wyświetl imię i nazwisko aktora o id 4 i tytuł filmu, w którym zagrał**

**20. A gdzie nasza HONIA!? Dodaj do tabeli customers nową krotkę, gdzie customer_id = 7, name = Honia, surname = Stuczka-Kucharska, email = honia@mail.com oraz pseudonym = Hoa**

## Subtask 2
### Test
10 points :first_quarter_moon:

## Subtask 3
### My brand new [QA_portfolio](https://github.com/JoannaKonik-Karczewska/QA-portfolio)
 
