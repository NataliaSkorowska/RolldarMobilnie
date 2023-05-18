# RolldarMobilnie

# 1. Charakterystyka oprogramowania

Nazwa skrócona: RolldarMobilnie

Nazwa pełna: RolldarMobilnie - Twoja firma w jednym miejscu

Opis: Hybrydowa aplikacja mobilna stworzona z wykorzystaniem frameworka Ionic.
Przeznaczona do zarządzania zamówieniami dla pracowników firmy Rolldar zajmującej się montażem oraz serwisem dekoracji okiennych.
Aplikacja umożliwia użytkownikom zarządzanie zamówieniami poprzez może nadawać im statusy oraz może przechowywać w aplikacji zdjęcia faktur.

# 2. Prawa autorskie

a. Autor: Natalia Skórowska

b. Licencja: Uznanie autorstwa - użycie niekomercyjne 4.0

# 3. Specyfikacja wymagań

| ID | Kategoria | Podkategoria | Nazwa krótka | Opis | Priorytet |
| ------- | -------|------|------| -----| ----- |
| NF1 | Niefunkcjonalne | Interfejs | Języ interfejsu | Interfejs użytkownika, komunikaty, powiadomienia, alerty przesyłane (pokazywane) użytkownikowi muszą być prezentowane w języku polskim. | P1 |
| NF2 | Niefunkcjonalne | Interfejs	| Logo | Logo firmy Rolldar zamieszczane w aplikacji jest zawsze widoczne w całości w wielkości dostosowanej do danego widoku.|P2|
| NF3 | Niefunkcjonalne | Interfejs |  Poziom trudności obsługi | Aplikacja musi być możliwa do obsługi dla osób bez specjalistycznej wiedzy informatycznej i programistycznej, w tym umożliwiać pracę jedynie z poziomu interfejsu, bez konieczności pisania kodu. |P1|
| NF4 | Niefunkcjonalne | Interfejs | Ergonomia | Moduły funkcjonalne muszą być wyposażone w estetyczny, spójny oraz intuicyjny interfejs użytkownika. Kolorystyka, grafika, kształty i czcionki muszą być jednakowe między różnymi widokami.|P2|
| NF5 | Niefunkcjonalne | Interfejs | Responsywność | Interfejs aplikacji powinien dostosowywać się do wymiarów urządzenia, na którym wyświetlone zostają widoki.|P1|
| NF6 | Niefunkcjonalne | Projektowe | Format daty| Data w systemie powinna być wyświetlana zgodnie z formatem dd.mm.yyyy|P3|
| NF7 | Niefunkcjonalne | Projektowe |  Kopia zapasowa | Aplikacja powinna posiadać kopię zapasową tworzoną automatycznie raz w tygodniu tak, aby istniała możliwość odtworzenia środowiska i danych (w części lub w całości).  |P2|
| NF8 | Niefunkcjonalne | Projektowe	 | Rozbudowa | Aplikacja powinna zostać napisana w taki sposób aby umożliwić ewentualną implementację kolejnych funkcjonalności lub modyfikację poszczególnych modułów w przyszłości. |P2|
| NF9 | Niefunkcjonalne | Projektowe	 | Struktura kodu | Kod aplikacji powinien zostać napisany zgodnie z dobrymi zasadami pisania kodu, stosując konwencję nazewnictwa oraz wcięcia w kodzie zgodnie ze standardami przyjętymi dla danego języka programowania.|P2|
| NF10 | Niefunkcjonalne | Projektowe | Dokumentacja | Do systemu (przed pierwszym wydaniem klientowi) powinna zostać dostarczona dedykowana dokumentacja techniczna stworzona w polskiej wersji językowej.
| NF11 | Niefunkcjonalne | Projektowe	 | Testowanie | Wymagane jest przeprowadzenie testów poszczególnych modułów aplikacji  z udziałem pracowników Rolldar do momentu poprawnego zakończenia wszystkich testów(UAT). | 1|
| NF12 | Niefunkcjonalne | Projektowe	| Repozytorium | Wszystkie wytworzone pliki (w szczególności całość kodu źródłowego) aplikacji muszą być zapisywane w repozytorium i aktualizowane w ramach przekazywania kolejnych wersji aplikacji. |P1|
| N13 | Niefunkcjonalne | Bezpieczeństwo	 | Szyfrowanie danych | System powinien szyfrować wszystkie dane użytkowników przesyłane pomiędzy aplikacją a bazą danych. |P1|
| NF14 | Niefunkcjonalne | Bezpieczeństwo	 | Zgodność z prawem | Standard bezpieczeństwa informacji zawartych w aplikacji powinien być zgodny z aktualnym prawem. |P1|
| NF15 | Niefunkcjonalne | Bezpieczeństwo	| Zmiana hasła | Aplikacja powinna wymuszać zmianę hasła użytkownika co 60 dni. |1|
| NF16 | Niefunkcjonalne | Wydajnościowe	 | Liczba użytkowników | Jednocześnie ze strony może korzystać 500 osób znajdujących się w różnych lokalizacjach |P2|
| NF17 | Niefunkcjonalne | Wydajnościowe	| Czas pracy| Aplikacja powinna być dostępna dla użytkowników 24/7/365 średnio 97% czasu. W ciągu kolejnych 4 lat korzystania z niej |P2|
| NF18 | Niefunkcjonalne | Wydajnościowe	| Czas uruchomienia po awarii| W przypadku awarii aplikacja powinna zostać naprawiona w ciągu 5 godzin od pierwszego zgłoszenia niepożądanego zachowania systemu. | P2|
| NF19 | Niefunkcjonalne | Utrzymanie	| Wersjonowanie | Nowe wersje aplikacji publikowane są zgodnie z konwencją: X.Y.Z, gdzie X oznacza numer znacznącej wprowadzonej zmiany najczęściej dodającej nowe funkcjonalności, y jest wersją, która wprowadziła niewielkie zmiany w funcjonalności (przyrosty funkcjonalności), a Z służy do wprowadzenia poprawek bezpieczeństwa krytycznych błędów. |P3|
| NF20 | Niefunkcjonalne | Utrzymanie	| Aktualizacja | Nowe wydania systemu są publikowane w oparciu o przeprowadzoną analizę obciążenia systemu. Wydanie wprowadzane jest w momencie najmniejszego obciążenia systemu.  |P3|
| NF21 | Niefunkcjonalne | Utrzymanie	| Wsparcie po aktualizacji | Po wprowadzeniu aktualizacji przez 24 godziny zzapewnione jest wsparcie techniczne na wypadek niepożądanych konsekwencji wprowadzenia nowych funkconalności.  |1|
| NF22 | Niefunkcjonalne | Dostęp	 | Sklepy z aplikacjami | Aplikacja powinna być dostępna do pobrania za darmo w sklepach z aplikacjami Google Play oraz Apple Store. |1|
| NF23 | Niefunkcjonalne | Dostęp	 | Systemy operacyjne  | Aplikacja powinna działać prawidłowo na urządzeniach zawierających mobilny system operacyjny Android (wersja 9.0 i wyższe) oraz iOS (wersja 12.0 i wyższe). | P1|
| NF24 | Niefunkcjonalne | Wydajnościowe | Czas reakcji | Maksymalny czas pomiędzy pobudzeniem przez użytkownika a odpowiedzią systemu nie powinien być dłuższy niż 4 sekundy. | P2|
| NF25 | Niefunkcjonalne | Dostęp | Połączenie z Internetem| Do prawidłowego funkcjonowania systemu niezbędne jest stabilne połączenie internetowe wynoszące minimum 300 mb/s. |P2|
| NF26 | Niefunkcjonalne | Dostęp | Role | W systemie występują dwa rodzaje użytkowników: "Admin" oraz "User".|1|
| NF26 | Niefunkcjonalne | Dostęp | Administrator | Uprawnienia Admina umożliwiają mu tworzenie, edycję, usuwanie i zarządzanie dostępem dla "Userów". |1|
| NF26 | Niefunkcjonalne | Dostęp | User | |1|
| ------- | -------|------|------| -----| ----- |
| 8 | Funkcjonalne | Widok | Strona główna | Po wejściu do aplikacji użytkownik zostaje przekierowany na stronę główną, na której znajdują się wyśrodkowane logo firmy oraz formularz logowania| 1 |
| F1 | Funkcjonalne | Logowanie | Formularz logowania| Użytkownik może zalogować się do systemu poprzez prawidłowe wypełnienie formularza logowania znajdującego się w widoku "Strona główna" poprzez wpisanie nazwy użytkownika w pole "Nazwa" oraz przypisanego do tej nazwy hasła w pole "Hasło", a następnie zatwierdzenie wpisanych danych poprzez naciśnięcie przycisku "Zaloguj"  |1|
| 2 | Funkcjonalne | Logowanie | Walidacja logowania - nazwa użytkownika| Jeśli użytkownik podczas wypełniania formularza logowania poda nazwę użytkownika nie istniejącego w bazie danych informacja o tym zostanie wyświetlona pod formularzem po naciśnięciu przycisku "Zaloguj się" w postaci tekstu "Nieprawidłowa nazwa użytkownika" zapisanego czerwoną czcionką bezpośrednio pod polem "Nazwa" | 1 |
| 4 | Funkcjonalne |Logowanie| Walidacja logowania - hasło | Jeśli użytkownik podczas wypełniania formularza logowania poda nieprawidłowe hasło dla danego użytkownika informacja o tym zostanie wyświetlona pod formularzem po naciśnięciu przycisku "Zaloguj się" w postaci tekstu "Nieprawidłowe hasło" zapisanego czerwoną czcionką bezpośrednio pod polem "Hasło"| 1 |
| 3 | Funkcjonalne | Logowanie | Przekierowanie po logowaniu | Użytkownik po poprawnym wypełnieniu formularza rejestracji i zatwierdzeniu danych poprzez kliknięcie przycisku "Zaloguj" znajdującego się pod formualrzem zostanie przekierowany do widoku "Zamowienia". | 2 |
| 15 | Funkcjonalne | Menu | Dostępność menu bocznego | Przycisk hamburger menu odpowiadający za wyświetlenie menu bocznego jest dostępny w każdym widoku widocznym dla użytkownika zalogowanego i znajduje się po lewej stronie górnego panelu aplikacji.| 1 |
| 15 | Funkcjonalne | Menu | Wyświetlenie bocznego menu | Użytkownik poprzez naciśnięcie przycisku hamburger menu znajdującego się w lewym górnym rogu aplikacji otwiera panel menu wyświetlający się po lewej stronie aplikacji i zakrywający 75% szerokości strony oraz 100% jej wysokości. | 1 |
| 16 | Funkcjonalne | Menu | Zawartość bocznego menu | Poprzez naciśnięcie na jedną z zakładek znajdującego się w bocznym menu: 'Zamówienia', 'Klienci', 'Faktury' oraz 'Wyloguj się' użytkownik zostaje odpowiednio przekierowany do widoku 'Zamowienia', 'Klienci', 'Faktury' lub zostaje wylogowany i przekierowany do widoku 'Strona glowna'. | 1  |
| 15 | Funkcjonalne | Widok | Górny panel aplikacji  | Górny panel aplikacji znajduje się w każdym widoku dostępnym dla zalogowanych uzytkowników, zajmuje 100% szerokośći ekranu oraz 10% wysokości od górnej krawędzi. Górny panel zawiera wyśrodkowaną nazwę danego widoku oraz w lewym rogu ikonę hamburger menu.| 1 |
| 18 | Funkcjonalne | Widok | Zamówienia | Widok 'Zamówienia' składa się z wyśrodkowanych elementów wyświetlonych od góry w kolejności: pole "Wyszukaj", przycisk "Dodaj" oraz listy zawierającej wszystkie zamówienia. Po lewej stronie bezpośrednio nad listą zamieszczony jest przycisk z ikoną sortowania, a po prawej przycisk z ikoną filtrowania.   | 1 |
| 18 | Funkcjonalne | Zamówienia | Lista | Lista zamówień wyświetlana jest na 65% wysokości strony od dolnej krawędzi i zawiera listę zamówień domyślnie posortowaną od najnowszego do najstarszego. Z poziomu listy widoczne jest: Imię i nazwisko klienta, status zamówienia, rodzaj dekoracji okiennej.   | 1 |
| 18 | Funkcjonalne | Zamówienia | Paginacja listy | Lista wyświetla w jednym czasie 10 zamówień, która można przewijać w pionie, na dole listy pod ostatnim zamówieniem znajduje się panel paginacji zawierający od lewej: znak mniejszosci, numeracje stron (z pogrubieniem aktualnie wyświetlanej strony) zawierającą 5 cyfr, znak większości. Jeśli stron jest więcej niż 5 przekierowanie do stron o wyższym numerze następuje poprzez naciśnięcie znaku większości. Analogicznie przekierowanie do stron niższych. | 1 |
| 18 | Funkcjonalne | Zamówienia | Filtrowanie listy | Po naciśnięciu na ikonę filtrowania nad listą pod tą ikoną wyświetlona zostaje lista składająca się z trzech wierszy: 
1 - 'Status' - z checkboxami "Nowy", "Wymiary zebrane", "Oferta wysłana", "Oferta zaakceptowana", "W realizacji", "Usługa zrealizowana", "Usługa zakończona"
2 - 'Termin' - z możliwością wybrania przedziału czasowego z dokładnością do dnia. 
3 - 'Pracownik' - z checkboxami odpowiadającymi każdemu z aktualnie zatrudnionych w Rolldar pracowników technicznych. Po zaznaczeniu przynajmniej jednego pola aktywny staje się przycisk "Filtruj", po którego naciśnięciu wyświetlona zostaje zaktualizowana zgodnie z wybranymi kryteriami lista zamówieńm a lista z opcjami filtrowania zostaje ukryta. |2|
| 18 | Funkcjonalne | Zamówienia | Sortowanie listy | Po naciśnięciu na ikonę sortowania nad listą pod tą ikoną wyświetlona zostaje lista składająca się z sześciu opcji do wyboru wierszy: 
1 - "Według daty od najstarszych"
2 - "Według daty od najnowszych"
3 - "Według statusu od nowych"
4 - "Według statusu od zakończonych"
5 - "Według nazwiska klienta od A do Z"
6 - "Według nazwiska klienta od Z do A". Po naciśnięciu na jeden z wierszy wyświetlona zostaje posortowana zgodnie z wybranymi kryteriami lista zamówień, a lista z opcjami sortowania zostaje ukryta.|2|
| 18 | Funkcjonalne | Widok | Dodaj  zamówienie | Po nacisnieciu przycisku "Dodaj zamowienie" system przekierowuje użytkownika do widoku o tej samej nazwie, ktory zawiera formularz nowego zamowienia. | 1 |
| 18 | Funkcjonalne | Dodaj zamowienie| Formularz nowego zamówienia | Po nacisnieciu przycisku "Dodaj zamowienie" system przekierowuje użytkownika do widoku o tej samej nazwie, ktory zawiera formularz nowego zamowienia. | 1 |
| 17 | Funkcjonalne | Dodaj zamowienie | Zapisanie zamowienia | Użytkownik poprzez poprawne wypełnienie formularza nowego zamowienia ma możliwość dodania nowego zamowienia realizowanego przez firmę Rolldar, po poprawnym wypełnieniu wszystkich pól i naciśnięciu przycisku "Dodaj" wyświetlone zostaje okno z tekstem: "Dodano nowe zamówienie o numerze xxx", gdzie xxx - jest kolejnym, unikatowym numerem zamowienia, ktory jest inkrementowany przy dodaniu nowego rekordu. | 1 |

| 7? | Funkcjonalne |Logowanie | Odzyskiwanie hasła | Użytkownik podając swój adres email w odpowiednim miejscu może wygeneować mail, który będzie zawierał link do formularza umożliwiającego zmianę hasła, jeśli podany email nie znajduje się w bazie zostanie wyświetlony stosowny komunikat | 2 |

| 9 | Funkcjonalne | Logowanie | Logowanie pracownika | Użytkownik znajdujący się na stronie zawierającej formularz logowania dla pracowników po wpisaniu prawidłowo loginu oraz hasła zostaje przekierowany do strony "Panel pracownika" | 1  |
| 10 | Funkcjonalne | Logowanie | Walidacja logowania pracownika | Użytkownik znajdujący się na stronie zawierającej formularz logowania dla pracowników po wpisaniu nieprawidłowych danych w formularzu zostaje o tym poinformowany poprzez wyświetlenie stosownego komunikatu | 1 |
| 11 | Funkcjonalne | Oferta | Widok oferty| Użytkownik ma możliwość przeglądania oferty firmy Rolldar poprzez widok strony "Oferta", która zawiera wszystkie dostępne rodzaje dekoracji okien| 1 |
| 12 | Funkcjonalne | Oferta | Wyszukanie oferty| Poprzez pasek wyszukiwania znajdujący się na górze strony "Oferta" użytkownik ma możliwość wyszukania interesującego go elementu z oferty firmy| 3 |
| 13 | Funkcjonalne | Oferta | Szczegóły oferty | Użytkownik po kliknięciu na dany rodzaj dekoracji okiennej na stronie "Oferta" zostanie przeniesiony do strony zawierającej szczegółowe informacje oraz galerie zdjęć wybranej przez siebie opcji| 2 |
| 14 | Funkcjonalne | Oferta | Karuzela ze zdjęciami | Użytkownik na stronie ze szczegółami oferty widzi galerię zdjęć, które automatycznie się przewijają, ale może także przeglądać je samodzielnie poprzez nawigację w lewo lub w prawo| 3 |

| 17 | Funkcjonalne | Rezerwacja | Dokonanie rezerwacji | Użytkownik poprzez poprawne wypełnienie formularza rezerwacji ma możliwość umówienia się na wykonanie usługi przez firmę Rolldar, po udanej rezerwacji wyświetlone zostaje okno informujące o powodzeniu  | 1 |

| 19 | Funkcjonalne | Zamówienia | Lista zamówień |  Użytkownik zalogowany jako pracownik znajdując się na stronie "Zamówienia" wyświetla listę zamówień złożonych przez klientów - widoczne jest imię i nazwisko osoby zamawiającej oraz status zamówienia | 1 |
| 20 | Funkcjonalne | Zamówienia | Usuwanie zamówienia | Użytkownik zalogowany jako pracownik znajdując się na stronie "Zamówienia" po naciśnięciu na ikonę kosza znajdującą się przy danym zamówieniu z listy ma możliwość usunięcia wszystkich informacji o danym zamówieniu z bazy. Po naciśnięciu ikony wyświetla się okno, które prosi użytkownika o potwierdzenie swojej decyzji  | 2  |
| 21 | Funkcjonalne | Zamówienia | Szczegóły zamówienia | Użytkownik zalogowany jako pracownik znajdując się na stronie "Zamówienia" po naciśnięciu na ikonę z ołówkiem znajdującą się przy danym zamówieniu z listy zostaje przekierowany na stronę zawierającą szczegóły danego zamówienia  | 1 |
| 22 | Funkcjonalne | Zamówienia | Edycja zamówienia | Użytkownik zalogowany jako pracownik znajdując się na stronie zawierającej szczegóły danego zamówienia może edytować umieszczone tam dane, w tym zmieniać status zamówienia. Dostępne statusy: "Nowy", "W realizacji", "Ukończono"   | 2 |
| 23 | Funkcjonalne | Zamówienia | Walidacja edycji zamówienia | Użytkownik zalogowany jako pracownik znajdując się na stronie zawierającej szczegóły danego zamówienia może dokonać edycji danych tylko jeśli poprawnie przejdzie walidację wprowadzonych zmian  | 3 |
| 24 | Funkcjonalne | Zamówienia | Wyszukiwanie zamówień | Użytkownik zalogowany jako pracownik znajdując się na stronie "Zamówienia" poprzez wpisanie interesującej go frazy w pasku wyszukiwania na górze strony ma możliwość wyszukanie zamówień, które zawierają wpisane słowa|  |
| 25 | Funkcjonalne | Faktury | Lista faktur | Użytkownik zalogowany jako pracownik znajdując się na stronie "Faktury" ma możliwość przeglądania listy dodanych zdjęć faktur - wyświetla się nazwa oraz miniaturka zdjęcia każdej z faktur| 3 |
| 26 | Funkcjonalne | Faktury | Dodanie zdjęcia faktury | Użytkownik zalogowany jako pracownik znajdując się na stronie "Faktury" po naciśnięciu przycisku "Wybierz plik" ma możliwość wgrania na listę faktur zdjęcie w formacie .png lub .jpg poprzez wybranie go z urządzenia | 3 |
| 27 | Funkcjonalne | Faktury | Pobranie zdjęcia | Użytkownik zalogowany jako pracownik znajdując się na stronie "Faktury" po naciśnięciu ikony pobierania znajdującej się pod każdym ze zdjęć na liście ma możliwość wyświetlenia zdjęcia w pełnym formacie i pobrania go na swoje urządzenie | 3 |
| 28 | Funkcjonalne | Panel pracownika | Widok panelu pracownika | Użytkownik zalogowany jako pracownik znajdujący się na stronie "panel pracownika" widzi dwa przyciski, które po naciśnięciu przekierują go odpowiednio: pierwszy "zamówienia" - do strony zawierającej listę zamówień, drugi "faktury" - do strony zawierającej listę faktur | 1 |
# 4. Architektura systemu

a. Architektura rozwoju - stos technologiczny

b. Architektura uruchomieniowa - stos technologiczny

Widok
Zamowienie

# 5. Testy
