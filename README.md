# RolldarMobilnie

---

## Spis treści
* [1. Charakterystyka oprogramowania](#charakterystyka-oprogramowania)
* [2. Prawa autorskie](#prawa-autorskie)
* [3. Specyfikacja wymagań](#specyfikacja-wymagań)
* [4. Architetura systemu](#Architektura-systemu)
* [5. Testy](#Testy)
* [6. Słownik pojęć](#Słownik-pojęć)

---

## Charakterystyka oprogramowania

<b> Nazwa skrócona: </b> RolldarMobilnie

<b> Nazwa pełna: </b> RolldarMobilnie - Twoja firma w jednym miejscu

<b> Opis: </b> Hybrydowa aplikacja mobilna stworzona z wykorzystaniem frameworka Ionic.
Przeznaczona do zarządzania zamówieniami dla pracowników firmy Rolldar zajmującej się montażem oraz serwisem dekoracji okiennych.
Aplikacja umożliwia użytkownikom zarządzanie zamówieniami poprzez przechowywanie danych związanych z każdym zamówieniem i śledzenie ich postępu poprzez nadawanie statusów. Dzięki aplikacji pracownicy techniczni działający w terenie mają informacje niezbędne do efektywnej pracy zawsze przy sobie, a kierownik ma na bieżąco wgląd do zamówień wszystkich pracowników dzięki czemu może skuteczniej monitorować ich pracę.

---

## Prawa autorskie

<b> a. Autor: </b> Natalia Skórowska

<b> b. Licencja: </b> Uznanie autorstwa - użycie niekomercyjne 4.0

---

## Specyfikacja wymagań

### A. Wymagania niefunkcjonalne

| ID | Kategoria | Podkategoria | Nazwa krótka | Opis | Priorytet |
| ------- | -------|------|------| -----| ----- |
| NF1 | Niefunkcjonalne | Interfejs | Języ interfejsu | Interfejs użytkownika, komunikaty, powiadomienia, alerty przesyłane (pokazywane) użytkownikowi muszą być prezentowane w języku polskim. | P1 |
| NF2 | Niefunkcjonalne | Interfejs	| Logo | Logo firmy Rolldar zamieszczane w aplikacji jest zawsze widoczne w całości w wielkości dostosowanej do danego widoku.|P2|
| NF3 | Niefunkcjonalne | Interfejs |  Poziom trudności obsługi | Aplikacja musi być możliwa do obsługi dla osób bez specjalistycznej wiedzy informatycznej i programistycznej, w tym umożliwiać pracę jedynie z poziomu interfejsu, bez konieczności pisania kodu. |P1|
| NF4 | Niefunkcjonalne | Interfejs | Ergonomia | Moduły funkcjonalne muszą być wyposażone w estetyczny, spójny oraz intuicyjny interfejs użytkownika. Kolorystyka, grafika, kształty i czcionki muszą być jednakowe między różnymi widokami.|P2|
| NF5 | Niefunkcjonalne | Interfejs | Responsywność | Interfejs aplikacji powinien dostosowywać się do wymiarów urządzenia, na którym wyświetlone zostają widoki.|P1|
| NF6 | Niefunkcjonalne | Projektowe | Format daty| Data w systemie powinna być wyświetlana zgodnie z formatem dd.mm.yyyy|P3|
| NF7 | Niefunkcjonalne | Projektowe |  Kopia zapasowa | Aplikacja powinna posiadać kopię zapasową tworzoną automatycznie raz w tygodniu tak, aby istniała możliwość odtworzenia środowiska i danych (w części lub w całości).  |P1|
| NF8 | Niefunkcjonalne | Projektowe	 | Rozbudowa | Aplikacja powinna zostać napisana w taki sposób aby umożliwić ewentualną implementację kolejnych funkcjonalności lub modyfikację poszczególnych modułów w przyszłości. |P2|
| NF9 | Niefunkcjonalne | Projektowe	 | Struktura kodu | Kod aplikacji powinien zostać napisany zgodnie z dobrymi zasadami pisania kodu, stosując konwencję nazewnictwa oraz wcięcia w kodzie zgodnie ze standardami przyjętymi dla danego języka programowania.|P2|
| NF10 | Niefunkcjonalne | Projektowe | Dokumentacja | Do systemu (przed pierwszym wydaniem klientowi) powinna zostać dostarczona dedykowana dokumentacja techniczna stworzona w polskiej wersji językowej. | P1|
| NF11 | Niefunkcjonalne | Projektowe	 | Testowanie | Wymagane jest przeprowadzenie testów poszczególnych modułów aplikacji  z udziałem pracowników Rolldar do momentu poprawnego zakończenia wszystkich testów(UAT). | P2|
| NF12 | Niefunkcjonalne | Projektowe	| Repozytorium | Wszystkie wytworzone pliki (w szczególności całość kodu źródłowego) aplikacji muszą być zapisywane w repozytorium i aktualizowane w ramach przekazywania kolejnych wersji aplikacji. |P1|
| N13 | Niefunkcjonalne | Bezpieczeństwo	 | Szyfrowanie danych | System powinien szyfrować wszystkie dane użytkowników przesyłane pomiędzy aplikacją a bazą danych. |P1|
| NF14 | Niefunkcjonalne | Bezpieczeństwo	 | Zgodność z prawem | Standard bezpieczeństwa informacji zawartych w aplikacji powinien być zgodny z aktualnym prawem. |P1|
| NF15 | Niefunkcjonalne | Bezpieczeństwo	| Zmiana hasła | Aplikacja powinna wymuszać zmianę hasła użytkownika co 60 dni. |P2|
| NF16 | Niefunkcjonalne | Wydajnościowe	 | Liczba użytkowników | Jednocześnie ze strony może korzystać 500 osób znajdujących się w różnych lokalizacjach |P2|
| NF24 | Niefunkcjonalne | Wydajnościowe | Czas reakcji | Maksymalny czas pomiędzy pobudzeniem przez użytkownika a odpowiedzią systemu nie powinien być dłuższy niż 4 sekundy. | P2|
| NF17 | Niefunkcjonalne | Wydajnościowe	| Czas pracy| Aplikacja powinna być dostępna dla użytkowników 24/7/365 średnio 97% czasu. W ciągu kolejnych 4 lat korzystania z niej |P2|
| NF18 | Niefunkcjonalne | Wydajnościowe	| Czas uruchomienia po awarii| W przypadku awarii aplikacja powinna zostać naprawiona w ciągu 5 godzin od pierwszego zgłoszenia niepożądanego zachowania systemu. | P2|
| NF19 | Niefunkcjonalne | Utrzymanie	| Wersjonowanie | Nowe wersje aplikacji publikowane są zgodnie z konwencją: X.Y.Z, gdzie X oznacza numer znacznącej wprowadzonej zmiany najczęściej dodającej nowe funkcjonalności, y jest wersją, która wprowadziła niewielkie zmiany w funcjonalności (przyrosty funkcjonalności), a Z służy do wprowadzenia poprawek bezpieczeństwa krytycznych błędów. |P3|
| NF20 | Niefunkcjonalne | Utrzymanie	| Aktualizacja | Nowe wydania systemu są publikowane w oparciu o przeprowadzoną analizę obciążenia systemu. Wydanie wprowadzane jest w momencie najmniejszego obciążenia systemu.  |P3|
| NF21 | Niefunkcjonalne | Utrzymanie	| Wsparcie po aktualizacji | Po wprowadzeniu aktualizacji przez 24 godziny zzapewnione jest wsparcie techniczne na wypadek niepożądanych konsekwencji wprowadzenia nowych funkconalności.  |P2|
| NF22 | Niefunkcjonalne | Dostęp	 | Sklepy z aplikacjami | Aplikacja powinna być dostępna do pobrania za darmo w sklepach z aplikacjami Google Play oraz Apple Store. |P1|
| NF23 | Niefunkcjonalne | Dostęp	 | Systemy operacyjne  | Aplikacja powinna działać prawidłowo na urządzeniach zawierających mobilny system operacyjny Android (wersja 9.0 i wyższe) oraz iOS (wersja 12.0 i wyższe). | P1|
| NF25 | Niefunkcjonalne | Dostęp | Połączenie z Internetem| Do prawidłowego funkcjonowania systemu niezbędne jest stabilne połączenie internetowe wynoszące minimum 300 mb/s. |P1|
| NF26 | Niefunkcjonalne | Dostęp | Role | W systemie występują dwa rodzaje użytkowników: "Admin" oraz "User".|P1|
| NF27 | Niefunkcjonalne | Dostęp | Administrator | Uprawnienia Admina umożliwiają mu tworzenie, edycję, usuwanie i zarządzanie dostępem dla "Userów". |P1|
| NF28 | Niefunkcjonalne | Dostęp | Użytkownik | Uprawnienia użytkownika pozwalają mu na obsługiwanie widoków 'Strona główna', 'Zamówienia', 'Dodaj zamówienie', 'Nowe zamówienie', 'Szczegóły zamówienia'. |P1|

---

### B. Wymagania funkcjonalne

| ID | Kategoria | Podkategoria | Nazwa krótka | Opis | Priorytet |
| ------- | -------|------|------| -----| ----- |
| F1 | Funkcjonalne | Widok | Strona główna | Po wejściu do aplikacji system przekierowuje użytkownika na stronę główną, na której znajdują się wyśrodkowane logo firmy oraz formularz logowania.| P1 |
| F2 | Funkcjonalne | Logowanie | Formularz logowania| System umożliwia zalogowania do aplikacji poprzez prawidłowe wypełnienie przez użytkownika formularza logowania znajdującego się w widoku "Strona główna" poprzez wpisanie nazwy użytkownika w pole "Nazwa" oraz przypisanego do tej nazwy hasła w pole "Hasło", a następnie zatwierdzenie wpisanych danych poprzez naciśnięcie przycisku "Zaloguj".  |P1|
| F3 | Funkcjonalne | Logowanie | Walidacja logowania - nazwa użytkownika| Jeśli użytkownik podczas wypełniania formularza logowania poda nazwę użytkownika nie istniejącego w bazie danych system wyświetli informację o tym pod formularzem po naciśnięciu przycisku "Zaloguj się" w postaci tekstu "Nieprawidłowa nazwa użytkownika" zapisanego czerwoną czcionką bezpośrednio pod polem "Nazwa". | P1 |
| F4 | Funkcjonalne |Logowanie| Walidacja logowania - hasło | Jeśli użytkownik podczas wypełniania formularza logowania poda nieprawidłowe hasło dla danego użytkownika system wyświetli informację o tym pod formularzem po naciśnięciu przycisku "Zaloguj się" w postaci tekstu "Nieprawidłowe hasło" zapisanego czerwoną czcionką bezpośrednio pod polem "Hasło"| P1 |
| F5 | Funkcjonalne | Logowanie | Przekierowanie po logowaniu |Po poprawnym wypełnieniu formularza rejestracji przez użytkownika i zatwierdzeniu danych poprzez kliknięcie przycisku "Zaloguj" znajdującego się pod formualrzem system przekierowuje do widoku "Zamowienia". | P1 |
| F6 | Funkcjonalne | Menu | Dostępność menu bocznego | Przycisk hamburger menu odpowiadający za wyświetlenie menu bocznego jest dostępny w każdym widoku widocznym dla użytkownika zalogowanego i znajduje się po lewej stronie górnego panelu aplikacji.| P1 |
| F7 | Funkcjonalne | Menu | Wyświetlenie bocznego menu | Użytkownik poprzez naciśnięcie przycisku hamburger menu znajdującego się w lewym górnym rogu aplikacji otwiera panel menu wyświetlający się po lewej stronie aplikacji i zakrywający 75% szerokości strony oraz 100% jej wysokości. | 1 |
| F8 | Funkcjonalne | Menu | Zawartość bocznego menu | Poprzez naciśnięcie na jedną z zakładek znajdującego się w bocznym menu: 'Zamówienia' oraz 'Wyloguj się' użytkownik zostaje odpowiednio przekierowany do widoku 'Zamowienia', lub zostaje wylogowany i przekierowany do widoku 'Strona glowna'. | 1  |
| F9 | Funkcjonalne | Widok | Górny panel aplikacji  | Górny panel aplikacji jest widocznyy dla użytkownikó znajdujących się w każdym widoku dostępnym dla zalogowanych uzytkowników, zajmuje 100% szerokośći ekranu oraz 10% wysokości od górnej krawędzi. Górny panel zawiera wyśrodkowaną nazwę danego widoku oraz w lewym rogu ikonę hamburger menu.| 1 |
| F10 | Funkcjonalne | Widok | Zamówienia | Widok 'Zamówienia' składa się z wyśrodkowanych elementów wyświetlonych od góry w kolejności: pole "Wyszukaj", przycisk "Dodaj" oraz listy zawierającej wszystkie zamówienia. Po lewej stronie bezpośrednio nad listą zamieszczony jest przycisk z ikoną sortowania, a po prawej przycisk z ikoną filtrowania.   | 1 |
| F11 | Funkcjonalne | Zamówienia | Lista | Lista zamówień wyświetlana jest na 65% wysokości strony od dolnej krawędzi i zawiera listę zamówień domyślnie posortowaną od najnowszego do najstarszego. Z poziomu listy widoczne jest po lewej stronie wiersza: status zamowienia, na srodku wiersza: Imię i nazwisko klienta, rodzaj dekoracji okiennej, data zlozenia zamowienia (kolejno pod soba), po prawej stronie wiersza ikona kosza, oczu oraz edycji.| 1 |
| F12 | Funkcjonalne | Zamówienia | Usuwanie zamowienia | Po  po naciśnięciu na ikonę kosza (aktywna tylko dla pracownika, ktory dodal dane zamowienie) znajdującą się przy danym zamówieniu z listy system wyswietla na srodku strony okienko z tekstem: "Czy na pewno chcesz usunac to zamowienie?" i z dwoma przyciskami "Tak, usuń", "Anuluj". Po nacisnieciu na przycisk "Tak, usuń" system przenosi informacje do archiwum (niedostepnego z poziomu aplikacji dla Usera),. Po naciśnięciu przycisku "Anuluj" okno się zamyka i wyświetlony zostaje widok 'Zamówienia'.| P1 |
| F13 | Funkcjonalne | Zamówienia | Szczegóły zamówienia | Po naciśnięciu na ikonę oka znajdującą się przy danym zamówieniu z listy użytkownik zostaje przekierowany na stronę zawierającą szczegóły danego zamówienia - dane z formularza wyświetlone są jako nieedytowalny tekst w kolejności zgodnej z tej z formularza. Ilość wyświetlonych danych zależy od statusu zamówienia.  | P2 |
| F14 | Funkcjonalne | Zamówienia | Edycja zamowienia | Po naciśnięciu na ikonę edycji w danym wierszu listy zamówień użytkownik zostaje przekierowany do widoku "Edycja zamowienia", w ktorym moze dokonać edycji danych zawartych w danym zamówieniu - wyświetlone zostają w formie edytowalnych pól wszystkie dane wprowadzone o zamówieniu (w zależności do statusu zamówienia), edycji nie podlega data złożenia zamówienia.| P1 |
| F14 | Funkcjonalne | Zamówienia | Zatwierdzanie edycji| System aktywuje przycisk "Zapisz zmiany" znajdujący się pod formularzem edycji zamówienia jeśli użytkownik wprowadzi zmiany w formularzu.| P1 |
| F15 | Funkcjonalne | Zamówienia | Zmiana statusu zamówienia | W widoku "Edycja zamówienia" system umożliwia wybranie z listy rozwijanej statusu zamówienia i jego zmianę. Dostępne statusy zamówienia: 1.Wymiary zebrane, 2.Oferta wysłana, 3.Oferta zaakceptowana, 4.W realizacji 5.Usługa wykonana, 6. Usługa zakończona, 7.Usługa z zastrzeżeniami| 1 |
| F14 | Funkcjonalne | Zamówienia | Status "Zebrano wymiary" | Po zmianie statusu zamówienia na "Zebrano wymiary" wyświetlone zostaje pola umożlwiiające wpisanie: wysokości okna oraz szerokości okna oraz pole umożliwiające wybór dekoracji okiennej z rozwijanej listy.|P1 |
| F15 | Funkcjonalne | Zamówienia | Edycja daty każdego etapu zamówienia | W widoku "Edycja zamówienia" po wyborze nowego statusu zamówienia z listy system wyświetla pole do wyboru daty otrzymania danego statusu, która zostaje zapisana poprzez naciśnięciu przycisku "Zapisz edycję" znajdującego się pod formularzem edycji zamówienia. 1 |
| F22| Funkcjonalne | Zamówienia | Paginacja listy | Lista wyświetla w jednym czasie 10 zamówień, która można przewijać w pionie, na dole listy pod ostatnim zamówieniem znajduje się panel paginacji zawierający od lewej: znak mniejszosci, numeracje stron (z pogrubieniem aktualnie wyświetlanej strony) zawierającą 5 cyfr, znak większości. Jeśli stron jest więcej niż 5 przekierowanie do stron o wyższym numerze następuje poprzez naciśnięcie znaku większości. Analogicznie przekierowanie do stron niższych. | P3 |
| F23 | Funkcjonalne | Zamówienia | Filtrowanie listy | Po naciśnięciu na ikonę filtrowania nad listą pod tą ikoną wyświetlona zostaje lista składająca się z trzech wierszy:  1 - 'Status' - z checkboxami "Nowy", "Wymiary zebrane", "Oferta wysłana", "Oferta zaakceptowana", "W realizacji", "Usługa zrealizowana", "Usługa zakończona" 2 - 'Termin' - z możliwością wybrania przedziału czasowego z dokładnością do dnia.  3 - 'Pracownik' - z checkboxami odpowiadającymi każdemu z aktualnie zatrudnionych w Rolldar pracowników technicznych. Po zaznaczeniu przynajmniej jednego pola aktywny staje się przycisk "Filtruj", po którego naciśnięciu wyświetlona zostaje zaktualizowana zgodnie z wybranymi kryteriami lista zamówieńm a lista z opcjami filtrowania zostaje ukryta. |P3|
| F24 | Funkcjonalne | Zamówienia | Sortowanie listy | Po naciśnięciu na ikonę sortowania nad listą pod tą ikoną wyświetlona zostaje lista składająca się z sześciu opcji do wyboru wierszy:  1 - "Według daty od najstarszych" 2 - "Według daty od najnowszych" 3 - "Według statusu od nowych" 4 - "Według statusu od zakończonych" 5 - "Według nazwiska klienta od A do Z" 6 - "Według nazwiska klienta od Z do A". Po naciśnięciu na jeden z wierszy wyświetlona zostaje posortowana zgodnie z wybranymi kryteriami lista zamówień, a lista z opcjami sortowania zostaje ukryta.|P3|
| F25 | Funkcjonalne | Widok | Dodaj  zamówienie | Po nacisnieciu przycisku "Dodaj zamowienie" system przekierowuje użytkownika do widoku o tej samej nazwie, ktory zawiera formularz nowego zamowienia. | P1 |
| F26 | Funkcjonalne | Dodaj zamowienie| Formularz nowego zamówienia | Po nacisnieciu przycisku "Dodaj zamowienie" system przekierowuje użytkownika do widoku o tej samej nazwie, ktory zawiera formularz nowego zamowienia. Formularz sklada sie z nastepujacych pol: Imie i nazwisko klienta (obowiazkowe pole tekstowe min 5 znakow, max 50), miejscowosc (obowiazkowe pole, min 4 znaki, max 40), ulica (obowiazkowe, min 3 znaki, max 50), kod pocztowy (obowiazkowe pole, zgodny z formatem kodu pocztowego 00-000), numer budynku/mieszkania (obowiazkowe pole tekstowe, min 1 znak, max 10), numer telefonu (obowiazkowe,9 cyfr), data zlozenia zamowienia, data pierwszej wizyty, notatka (pole tekstowe nieobowiązkowe, maximum 400 slow). Oraz przycisku "Zapisz" znajdujacego sie pod formularzem.| P1 |
| F27 | Funkcjonalne | Dodaj zamowienie| Walidacja formularza zamowienia |Jeśli użytkownik podczas wypełniania formularza zamówienia poda dane w nieprawidłowym formacie informacja o tym zostanie wyświetlona pod formularzem po naciśnięciu przycisku "Zapisz" w postaci tekstu "Nieprawidłowy format danych" zapisanego czerwoną czcionką bezpośrednio pod błędnie wypełnionym polem.| P1 |
| F28 | Funkcjonalne | Dodaj zamowienie | Zapisanie zamowienia | Użytkownik poprzez poprawne wypełnienie formularza nowego zamowienia ma możliwość dodania nowego zamowienia realizowanego przez firmę Rolldar, po poprawnym wypełnieniu wszystkich pól i naciśnięciu przycisku "Dodaj" wyświetlone zostaje okno z tekstem: "Dodano nowe zamówienie o numerze xxx" (gdzie xxx - jest kolejnym, unikatowym numerem zamowienia, ktory jest inkrementowany przy dodaniu nowego rekordu) | P1 |
| F29 | Funkcjonalne | Zamowienia | Wyszukanie oferty |  Poprzez pasek wyszukiwania znajdujący się w widoku "Zamowienia" użytkownik ma możliwość wyszukania interesującego go zamowienia - wpisujac adres, numer telefonu, imie lub nazwisko klienta.| P2 |
| F30 | Funkcjonalne | Zamowienia | Usuwanie filtru wyszukiwania |  Po naciśnięciu na ikonę "x" znajdującą się po prawej stronie na pasku wyszukiwania zamowien system usuwa frazę wpisaną w pasku wyszukiwania i przywraca domyślny widok listy zamowien.| P3 |

---

# Architektura systemu

a. Architektura rozwoju - stos technologiczny

| ID | Nazwa | Zastosowanie | Wersja |
| ------- | -------|------|------| 
| 1 | Ionic | Framework aplikacji, struktura projektu | 7.5.0 |
| 2 | Angular | Framework aplikacji | 16.0.2 |
| 3 | AngularFire | Komunikacja aplikacji z bazą danych (przechowywanie danych, logowanie) | 7.5.0 |
| 4 | Firebase | Baza danych |  31.5.0 |
| 5 | HTML5 | Struktura aplikacji |  - |
| 6 | Figma | Stworzenie prototypu aplikacji |  107.0.0 |
| 7 | Node.js | Serwer do uruchomienia aplikacji |  18.12.0 |


b. Architektura uruchomieniowa - stos technologiczny


| ID | Nazwa | Zastosowanie | Wersja |
| ------- | -------|------|------|
| 1 | Visual Studio Code | Środowisko programistyczne | 17.5.5 |
| 2 | Git | System kontroli wersji | 2.40.1 |
| 3 | GitHub | Przechowywanie repozytorium w chmurze | 3.8.3 |




---

# Testy

# Słownik pojęć
Widok
Zamowienie
System
# Możliwości rozbudowy
1) Umieszczanie zdjęć do każdego zamówienia
2) Lista klientów
