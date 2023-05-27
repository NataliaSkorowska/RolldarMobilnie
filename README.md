# RolldarMobilnie

---

## Spis treści
* [1. Charakterystyka oprogramowania](#charakterystyka-oprogramowania)
* [2. Prawa autorskie](#prawa-autorskie)
* [3. Specyfikacja wymagań](#specyfikacja-wymagań)
* [4. Architetura systemu](#Architektura-systemu)
* [5. Testy](#Testy)
* [6. Słownik pojęć](#Słownik-pojęć)
* [7. Projekt widoków](#Projekt-widoków)

---

## Charakterystyka oprogramowania

<b> Nazwa skrócona: </b> Rolldar Mobilnie

<b> Nazwa pełna: </b> RolldarMobilnie - Twoja firma w jednym miejscu

<b> Opis: </b> 
- Rolldar Mobilnie to hybrydowa aplikacja mobilna stworzona z wykorzystaniem frameworka Ionic.
- Jej głównym celem jest usprawnienie procesu zarządzania zamówieniami, który jest realizowany przez pracowników firmy Rolldar. Firma ta specjalizuje się w montażu oraz serwisie dekoracji okiennych.
- Jest to pierwszy w firmie system, który zbiera wszystkie informacje o zamówieniach w jednym miejscu dokonując integracji realizacji wykonywanych przez różnych pracowników.
- W ofercie firmy znajdują się następujące dekoracje okienne: markizy, moskitiery, plisy, żaluzje pionowe oraz poziome, rolety zewnętrzne, wolnowiszące, zasłony, firany, bramy.
- <b> Zalety płynące z wykorzystania aplikacji przez pracowników technicznych: </b> Podczas pracy w terenie (która zajmuje 80% czasu ich pracy) pracownicy techniczni mają informacje niezbędne do efektywnej pracy zawsze przy sobie niezależnie od miejsca i czasu. Dzięki aplikacji pracownicy nie muszą codziennie przebywać w biurze po wykonaniu zlecenia, a zyskany czas mogą przeznaczyć na realizację większej liczby zamówień by maksymalizować zyski w firmie.
- <b> Zalety płynące z wykorzystania aplikacji przez kierowanika firmy: </b> Kierownik ma na bieżąco wgląd do zamówień wszystkich pracowników dzięki czemu może skuteczniej monitorować ich pracę. Zapewnia to większą możliwość kontroli tego jakie zamówienia zostały zrealizowane oraz jakie są zaplanowane. Umożliwi to także nadzór nad efektywnością pracy pracowników technicznych.  

<b> Interesariusze </b>:
- Pracownicy techniczni firmy Rolldar
- Kierownik firmy Rolldar
- (Pośrednio) klienci firmy Rolldar, których dane przechowywane będą w bazie danych połączonej z dostarczonym systemem

<b> Sposób pozyskania wymagań: </b>
- Wywiady z pracownikami oraz kierownikiem Rolldar
- Obserwacja ich pracy w terenie oraz biurze

---

## Prawa autorskie

<b> a. Autor: </b> Natalia Skórowska

<b> b. Licencja: </b> Uznanie autorstwa - użycie niekomercyjne 4.0

---

## Specyfikacja wymagań

### A. Wymagania niefunkcjonalne

| ID | Kategoria | Podkategoria | Nazwa krótka | Opis | Priorytet |
| ------- | -------|------|------| -----| ----- |
| NF1 | Niefunkcjonalne | Wydajnościowe | Liczba użytkowników | Jednocześnie ze strony może korzystać 500 osób znajdujących się w różnych lokalizacjach. |P2|
| NF2 | Niefunkcjonalne | Wydajnościowe | Czas reakcji | Maksymalny czas pomiędzy pobudzeniem przez użytkownika a odpowiedzią systemu nie powinien być dłuższy niż 4 sekundy. | P2|
| NF3 | Niefunkcjonalne | Wydajnościowe	| Czas pracy| Aplikacja powinna być dostępna dla użytkowników 24/7/365 średnio 97% czasu. W ciągu kolejnych 4 lat korzystania z niej. |P1|
| NF4 | Niefunkcjonalne | Wydajnościowe	| Czas uruchomienia po awarii| W przypadku awarii aplikacja powinna zostać naprawiona w ciągu 5 godzin od pierwszego zgłoszenia niepożądanego zachowania systemu. | P2|
| NF5 | Niefunkcjonalne | Interfejs | Języ interfejsu | Interfejs użytkownika, komunikaty, powiadomienia, alerty przesyłane (pokazywane) użytkownikowi muszą być prezentowane w języku polskim. | P1 |
| NF6 | Niefunkcjonalne | Interfejs	| Logo | Logo firmy Rolldar zamieszczone w aplikacji powinno być zawsze widoczne w całości w wielkości dostosowanej do danego widoku.|P2|
| NF7 | Niefunkcjonalne | Interfejs |  Poziom trudności obsługi | Aplikacja jest możliwa do obsługi dla osób bez specjalistycznej wiedzy informatycznej i programistycznej, w tym umożliwiać pracę jedynie z poziomu interfejsu, bez konieczności pisania kodu. |P1|
| NF8 | Niefunkcjonalne | Interfejs | Ergonomia | Moduły funkcjonalne muszą być wyposażone w estetyczny, spójny oraz intuicyjny interfejs użytkownika. Kolorystyka (czerwono-biała), grafika, kształty i czcionki muszą być jednakowe między różnymi widokami.|P2|
| NF9 | Niefunkcjonalne | Interfejs | Responsywność | Interfejs aplikacji powinien dostosowywać się do wymiarów urządzenia, na którym wyświetlone zostają widoki.|P1|
| NF10 | Niefunkcjonalne | Projektowe | Format daty| Data w systemie powinna być wyświetlana zgodnie z formatem dd.mm.yyyy. |P3|
| NF11 | Niefunkcjonalne | Projektowe |  Kopia zapasowa | Aplikacja powinna posiadać kopię zapasową tworzoną automatycznie raz w tygodniu tak, aby istniała możliwość odtworzenia środowiska i danych (w części lub w całości). |P1|
| NF12 | Niefunkcjonalne | Projektowe | Rozbudowa | Aplikacja powinna zostać napisana w taki sposób aby umożliwić ewentualną implementację kolejnych funkcjonalności lub modyfikację poszczególnych modułów w przyszłości. |P2|
| NF13 | Niefunkcjonalne | Projektowe	 | Struktura kodu | Kod aplikacji powinien zostać napisany zgodnie z dobrymi zasadami pisania kodu, stosując konwencję nazewnictwa oraz wcięcia w kodzie zgodnie ze standardami przyjętymi dla danego języka programowania.|P2|
| NF14 | Niefunkcjonalne | Projektowe | Dokumentacja | Do systemu (przed pierwszym wydaniem klientowi) powinna zostać dostarczona dedykowana dokumentacja techniczna stworzona w polskiej wersji językowej. | P1|
| NF15 | Niefunkcjonalne | Projektowe	| Repozytorium | Wszystkie wytworzone pliki (w szczególności całość kodu źródłowego) aplikacji muszą być zapisywane w repozytorium i aktualizowane w ramach przekazywania kolejnych wersji aplikacji. |P1|
| N16 | Niefunkcjonalne | Bezpieczeństwo	 | Szyfrowanie danych | System powinien szyfrować wszystkie dane użytkowników przesyłane pomiędzy aplikacją a bazą danych. |P1|
| NF17 | Niefunkcjonalne | Bezpieczeństwo	 | Zgodność z prawem | Standard bezpieczeństwa informacji zawartych w aplikacji powinien być zgodny z aktualnym prawem (Stan na 21.05.2023 - oznacza to zgodność z Narodowym Standardem Bezpieczeństwa NSC 200 wer. 2.1).|P1|
| NF18 | Niefunkcjonalne | Bezpieczeństwo	| Zmiana hasła | Aplikacja powinna wymuszać zmianę hasła użytkownika co 60 dni. |P2|
| NF19 | Niefunkcjonalne | Utrzymanie	| Wersjonowanie | Nowe wersje aplikacji wersjonowane są zgodnie z konwencją: X.Y.Z, gdzie X oznacza numer znacznącej wprowadzonej zmiany najczęściej dodającej nowe funkcjonalności, y jest wersją, która wprowadziła niewielkie zmiany w funcjonalności (przyrosty funkcjonalności), a Z służy do wprowadzenia poprawek bezpieczeństwa krytycznych błędów. |P3|
| NF20 | Niefunkcjonalne | Utrzymanie	| Aktualizacja | Nowe wydania systemu są publikowane w oparciu o przeprowadzoną analizę obciążenia systemu. Wydanie wprowadzane jest w momencie najmniejszego obciążenia systemu.  |P3|
| NF21 | Niefunkcjonalne | Utrzymanie	| Wsparcie po aktualizacji | Po wprowadzeniu aktualizacji przez 24 godziny zapewnione jest wsparcie techniczne na wypadek niepożądanych konsekwencji wprowadzenia nowych funkconalności.  |P2|
| NF22 | Niefunkcjonalne | Dostęp	 | Sklepy z aplikacjami | Aplikacja powinna być dostępna do pobrania za darmo w sklepach z aplikacjami Google Play oraz Apple Store. |P1|
| NF23 | Niefunkcjonalne | Dostęp	 | Systemy operacyjne  | Aplikacja powinna działać prawidłowo na urządzeniach opartych na mobilnym systemie operacyjnym Android (wersja 9.0 i wyższe) oraz iOS (wersja 12.0 i wyższe). | P1|
| NF24 | Niefunkcjonalne | Dostęp | Połączenie z Internetem| Do prawidłowego funkcjonowania systemu niezbędne jest stabilne połączenie internetowe wynoszące minimum 300 mb/s. |P1|
| NF25 | Niefunkcjonalne | Dostęp | Role | W ramach projektu i dostarczonego systemu przekazane są dostępy dla dwóch rodzaje użytkowników: "Admin" oraz "User".|P1|
| NF26 | Niefunkcjonalne | Dostęp | Administrator | Uprawnienia Admina umożliwiają mu tworzenie, edycję, usuwanie i zarządzanie dostępem dla "Userów" poprzez zapewnienie bezpośredniego dostępu do bazy danych aplikacji. |P1|
| NF27 | Niefunkcjonalne | Dostęp | Użytkownik | Uprawnienia użytkownika pozwalają mu na obsługiwanie widoków 'Strona główna', 'Zamówienia', 'Dodaj zamówienie', 'Nowe zamówienie', 'Szczegóły zamówienia'. |P1|

---

### B. Wymagania funkcjonalne

| ID | Kategoria | Podkategoria | Nazwa krótka | Opis | Priorytet |
| ------- | -------|------|------| -----| ----- |
| F1 | Funkcjonalne | Widok | Strona główna | Po wejściu do aplikacji system przekierowuje użytkownika na stronę główną, na której znajdują się wyśrodkowane logo firmy oraz formularz logowania.| P1 |
| F2 | Funkcjonalne | Logowanie | Formularz logowania| System umożliwia zalogowanie się do aplikacji poprzez prawidłowe wypełnienie przez użytkownika formularza logowania znajdującego się w widoku "Strona główna" poprzez wpisanie nazwy użytkownika w pole "Nazwa" oraz przypisanego do tej nazwy hasła w pole "Hasło", a następnie zatwierdzenie wpisanych danych poprzez naciśnięcie przycisku "Zaloguj".  |P1|
| F3 | Funkcjonalne | Logowanie | Walidacja logowania - nazwa użytkownika| Jeśli użytkownik podczas wypełniania formularza logowania poda nazwę użytkownika nie istniejącego w bazie danych system wyświetli informację o tym pod formularzem po naciśnięciu przycisku "Zaloguj się" w postaci tekstu "Nieprawidłowa nazwa użytkownika" zapisanego czerwoną czcionką bezpośrednio pod polem "Nazwa". | P1 |
| F4 | Funkcjonalne |Logowanie| Walidacja logowania - hasło | Jeśli użytkownik podczas wypełniania formularza logowania poda nieprawidłowe hasło dla danego użytkownika system wyświetli informację o tym pod formularzem po naciśnięciu przycisku "Zaloguj się" w postaci tekstu "Nieprawidłowe hasło" zapisanego czerwoną czcionką bezpośrednio pod polem "Hasło".| P1 |
| F5 | Funkcjonalne | Logowanie | Przekierowanie po logowaniu |Po poprawnym wypełnieniu formularza rejestracji przez użytkownika i zatwierdzeniu danych poprzez kliknięcie przycisku "Zaloguj" znajdującego się pod formularzem system przekierowuje do widoku "Zamówienia". | P1 |
| F6 | Funkcjonalne | Menu | Dostępność menu bocznego | Przycisk hamburger menu odpowiadający za wyświetlenie menu bocznego jest dostępny w każdym widoku widocznym dla użytkownika zalogowanego i znajduje się po lewej stronie górnego panelu aplikacji.| P1 |
| F7 | Funkcjonalne | Menu | Wyświetlenie bocznego menu | Użytkownik poprzez naciśnięcie przycisku hamburger menu znajdującego się w lewym górnym rogu aplikacji otwiera panel menu wyświetlający się po lewej stronie aplikacji i zakrywający 75% szerokości strony oraz 100% jej wysokości. | P1 |
| F8 | Funkcjonalne | Menu | Zawartość bocznego menu | Poprzez naciśnięcie na jedną z zakładek znajdującego się w bocznym menu: "Zamówienia" oraz "Wyloguj się" użytkownik zostaje odpowiednio przekierowany do widoku "Zamówienia", lub zostaje wylogowany i przekierowany do widoku "Strona główna". | P1 |
| F9 | Funkcjonalne | Widok | Górny panel aplikacji  | Górny panel aplikacji jest widoczny dla użytkowników znajdujących się w każdym widoku dostępnym dla zalogowanych uzytkowników, zajmuje 100% szerokośći ekranu oraz 10% wysokości od górnej krawędzi. Górny panel zawiera wyśrodkowaną nazwę danego widoku oraz w lewym rogu ikonę hamburger menu.| P1 |
| F10 | Funkcjonalne | Widok | Zamówienia | Widok "Zamówienia" składa się z wyśrodkowanych elementów wyświetlonych od góry w kolejności: pole "Wyszukaj", przycisk "Dodaj" oraz listy zawierającej wszystkie zamówienia. Po lewej stronie bezpośrednio nad listą zamieszczony jest przycisk z ikoną sortowania, a po prawej przycisk z ikoną filtrowania.   | P1 |
| F11 | Funkcjonalne | Zamówienia | Lista | System wyświetla listę zamówień na 65% wysokości strony od dolnej krawędzi. Lista jest domyślnie posortowana od najnowszego do najstarszego. Z poziomu listy widoczne jest po lewej stronie wiersza: status zamówienia, na środku wiersza: Imię i nazwisko klienta, rodzaj dekoracji okiennej, data złożenia zamówienia (kolejno pod sobą), po prawej stronie wiersza ikona kosza, oczu oraz edycji.| P1 |
| F12 | Funkcjonalne | Zamówienia | Usuwanie zamowienia | Po naciśnięciu na ikonę kosza (aktywną tylko dla pracownika, który dodał dane zamówienie) znajdującą się przy danym zamówieniu z listy system wyswietla na srodku strony okienko z tekstem: "Czy na pewno chcesz usunac to zamowienie?" i z dwoma przyciskami "Tak, usuń", "Anuluj". Po nacisnieciu na przycisk "Tak, usuń" system przenosi informacje do archiwum (niedostepnego z poziomu aplikacji dla Usera). Po naciśnięciu przycisku "Anuluj" okno się zamyka i wyświetlony zostaje widok "Zamówienia".| P3 |
| F13 | Funkcjonalne | Zamówienia | Szczegóły zamówienia | Po naciśnięciu na ikonę oka znajdującą się przy danym zamówieniu z listy użytkownik zostaje przekierowany na stronę zawierającą szczegóły danego zamówienia - dane z formularza wyświetlone są jako nieedytowalny tekst w kolejności zgodnej z tą z formularza. Ilość wyświetlonych danych zależy od statusu zamówienia.  | P2 |
| F14 | Funkcjonalne | Zamówienia | Edycja zamowienia | Po naciśnięciu na ikonę edycji w danym wierszu listy zamówień użytkownik zostaje przekierowany do widoku "Edycja zamówienia", w którym może dokonać edycji danych zawartych w danym zamówieniu - wyświetlone zostają w formie edytowalnych pól wszystkie dane wprowadzone o zamówieniu (w zależności do statusu zamówienia), edycji nie podlega data złożenia zamówienia.| P1 |
| F15 | Funkcjonalne | Zamówienia | Zatwierdzanie edycji| System aktywuje przycisk "Zapisz zmiany" znajdujący się pod formularzem edycji zamówienia jeśli użytkownik wprowadzi zmiany w formularzu.| P1 |
| F16 | Funkcjonalne | Zamówienia | Zmiana statusu zamówienia | W widoku "Edycja zamówienia" system umożliwia wybranie z listy rozwijanej statusu zamówienia i jego zmianę.| P1 |
| F17 | Funkcjonalne | Zamówienia | Status "Zebrano wymiary" | Po zmianie statusu zamówienia na "Zebrano wymiary" wyświetlone zostaje pola umożlwiające wpisanie: wysokości okna oraz szerokości okna oraz pole umożliwiające wybór dekoracji okiennej z rozwijanej listy.|P1 |
| F18 | Funkcjonalne | Zamówienia | Edycja daty każdego etapu zamówienia | W widoku "Edycja zamówienia" po wyborze nowego statusu zamówienia z listy system wyświetla pole do wyboru daty otrzymania danego statusu, która zostaje zapisana poprzez naciśnięciu przycisku "Zapisz edycję" znajdującego się pod formularzem edycji zamówienia. | P1 |
| F19| Funkcjonalne | Zamówienia | Paginacja listy | Lista wyświetla w jednym czasie 10 zamówień, która można przewijać w pionie, na dole listy pod ostatnim zamówieniem znajduje się panel paginacji zawierający od lewej: znak mniejszosci, numeracje stron (z pogrubieniem aktualnie wyświetlanej strony) zawierającą 5 cyfr, znak większości. | P3 |
| F20 | Funkcjonalne | Zamówienia | Filtrowanie listy | Po naciśnięciu na ikonę filtrowania nad listą pod tą ikoną wyświetlona zostaje lista z dostępnymi opcjami filtrowania. Po zaznaczeniu przynajmniej jednego pola aktywny staje się przycisk "Filtruj", po którego naciśnięciu wyświetlona zostaje zaktualizowana zgodnie z wybranymi kryteriami lista zamówieńm a lista z opcjami filtrowania zostaje ukryta. |P3|
| F21 | Funkcjonalne | Zamówienia | Sortowanie listy | Po naciśnięciu na ikonę sortowania nad listą pod tą ikoną wyświetlona zostaje lista składająca się z sześciu opcji do wyboru wierszy:  1 - "Według daty od najstarszych" 2 - "Według daty od najnowszych" 3 - "Według statusu od nowych" 4 - "Według statusu od zakończonych" 5 - "Według nazwiska klienta od A do Z" 6 - "Według nazwiska klienta od Z do A". Po naciśnięciu na jeden z wierszy wyświetlona zostaje posortowana zgodnie z wybranymi kryteriami lista zamówień, a lista z opcjami sortowania zostaje ukryta.|P3|
| F22 | Funkcjonalne | Widok | Dodaj  zamówienie | Po naciśnięciu przycisku "Dodaj zamówienie" system przekierowuje użytkownika do widoku o tej samej nazwie, który zawiera formularz nowego zamówienia. | P1 |
| F23 | Funkcjonalne | Dodaj zamówienie| Formularz nowego zamówienia | Po naciśnięciu przycisku "Dodaj zamówienie" system przekierowuje użytkownika do widoku o tej samej nazwie, który zawiera formularz nowego zamówienia. Formularz składa się z następujacych pól: Imię i nazwisko klienta, miejscowość, ulica, kod pocztowy, numer budynku/mieszkania, numer telefonu, data złożenia zamówienia, data pierwszej wizyty, status zamówienia, notatka oraz przycisku "Zapisz" znajdującego się pod formularzem.| P1 |
| F24 | Funkcjonalne | Dodaj zamówienie| Walidacja formularza zamówienia |Jeśli użytkownik podczas wypełniania formularza zamówienia poda dane w nieprawidłowym formacie informacja o tym zostanie wyświetlona pod formularzem po naciśnięciu przycisku "Zapisz" w postaci tekstu "Nieprawidłowy format danych" zapisanego czerwoną czcionką bezpośrednio pod błędnie wypełnionym polem.| P1 |
| F25 | Funkcjonalne | Dodaj zamówienie | Zapisanie zamówienia | Użytkownik poprzez poprawne wypełnienie formularza nowego zamówienia ma możliwość dodania nowego zamówienia realizowanego przez firmę Rolldar, po poprawnym wypełnieniu wszystkich pól i naciśnięciu przycisku "Dodaj" wyświetlone zostaje okno z tekstem: "Dodano nowe zamówienie o numerze xxx" (gdzie xxx - jest kolejnym, unikatowym numerem zamowienia, który jest inkrementowany przy dodaniu nowego rekordu). | P1 |
| F25 | Funkcjonalne | Zamówienia | Wyszukanie oferty |  Poprzez pasek wyszukiwania znajdujący się w widoku "Zamówienia" użytkownik ma możliwość wyszukania interesującego go zamówienia - wpisując adres, numer telefonu, imię lub nazwisko klienta.| P2 |
| F26 | Funkcjonalne | Zamówienia | Usuwanie filtru wyszukiwania |  Po naciśnięciu na ikonę "x" znajdującą się po prawej stronie na pasku wyszukiwania zamówień system usuwa frazę wpisaną w pasku wyszukiwania i przywraca domyślny widok listy zamówień.| P3 |

---

# Architektura systemu

<b> a. Architektura rozwoju - stos technologiczny </b>

| ID | Nazwa | Zastosowanie | Wersja |
| ------- | -------|------|------| 
| 1 | Ionic | Framework aplikacji, struktura projektu | 7.5.0 |
| 2 | Angular | Framework aplikacji | 16.0.2 |
| 3 | AngularFire | Komunikacja aplikacji z bazą danych (przechowywanie danych, logowanie) | 7.5.0 |
| 4 | HTML5 | Struktura aplikacji |  - |
| 5 | Figma | Stworzenie prototypu aplikacji |  107.0.0 |
| 6 | Visual Studio Code | Środowisko programistyczne | 17.5.5 |
| 7 | Git | System kontroli wersji | 2.40.1 |
| 8 | GitHub | Przechowywanie repozytorium w chmurze | 3.8.3 |

<b> b. Architektura uruchomieniowa - stos technologiczny </b>


| ID | Nazwa | Zastosowanie | Wersja |
| ------- | -------|------|------|
| 1 | Firebase | Baza danych |  31.5.0 |
| 2 | Node.js | Serwer do uruchomienia aplikacji |  18.12.0 |
| 3A | iOS | Oprogramowanie mobilne, na którym zainstalowana została aplikacja |  12.0 i wyższe |
| 3B | Android | Oprogramowanie mobilne, na którym zainstalowana została aplikacja |  9.0 i wyższe |

3A i 3B - wymagane jedno z dwóch 

---

# Testy

| Lp. | Nazwa | Warunki wstępne| Kroki wykonania | Oczekiwany rezultat |
| ------------- | ------------- |------|------|-------|
1| Widoczność strony głównej | Serwer, na którym zamieszczona jest aplikacja jest uruchomiony i poprawnie skonfigurowany. | 1. Wejdź w aplikację "RolldarMobilnie". <br> 2. Przyjrzyj się jak wygląda widok strony głównej aplikacji. | Strona główna aplikacji Rolldar zawierająca wyśrodkowane logo firmy oraz formularz logowania zostaje wyświetlona. |
| 2 | Formularz logowania|Widok "Strona główna" jest widoczny i zawiera formularz logowania.|1. Wpisz nazwę użytkownika w pole "Nazwa". <br> 2. Wpisz odpowiadające temu użytkownikowi hasło w pole "Hasło".  |Użytkownik może wpisać tekst w pola formularza logowania. Wpisane hasło zostaje wyświetlone w postaci kropek.|
| 3 | Walidacja logowania - nazwa użytkownika|Użytkownik znajduje się na widoku "Strona główna". Widok "Strona główna" zawiera formularz logowania z polami "Nazwa" i "Hasło".|1. Wpisz w pole "Nazwa" nieistniejącą nazwę użytkownika. <br> 2. Naciśnij przycisk "Zaloguj się" znajdujący się pod formularzem.|Tekst zapisany czerwoną czcionką "Nieprawidłowa nazwa użytkownika" zostaje wyświetlony bezpośrednio pod polem "Nazwa".|
| 4 |  Walidacja logowania - hasło |Użytkownik znajduje się na widoku "Strona główna". Widok "Strona główna" zawiera formularz logowania z polami "Nazwa" i "Hasło".| 1. Wpisz w pole "Nazwa" istniejącą nazwę użytkownika. <br> 2. Wpisz w pole "Hasło" błędne dla danego użytkownika hasło. <br> 3. Naciśnij przycisk "Zaloguj się" znajdujący się pod formularzem.|Tekst zapisany czerwoną czcionką "Nieprawidłowe hasło" zostaje wyświetlony bezpośrednio pod polem "Nazwa".
| 5 | Przekierowanie po logowaniu |Użytkownik posiada aktywne konto w aplikacji. W bazie danych przechowywane są Nazwa oraz Hasło użytkownika zgodne z tymi, które użytkownik wpisał w formularzu| 1. Wpisz nazwy użytkownika w pole "Nazwa". <br> 2. Wpisz odpowiadające temu użytkownikowi hasło w pole "Hasło". <br> 3. Kliknij przycisk "Zaloguj się". <br> 4. Przyjrzyj się czy zostałeś przekierowany na stronę "Zamówienia". |Widok "Zamówienia" zostaje wyświetlony.|
| 6 |  Dostępność menu bocznego  |Użytkownik jest zalogowany do aplikacji Rolldar.|1. Sprawdź czy widzisz ikonę hamburger menu będąc w widoku: "Zamówienia", "Szczegóły zamówienia", "Dodaj zamówienie", "Edytuj zamówienie". |Ikona menu bocznego jest widoczna w panelu górnym.|
| 7 |Wyświetlenie bocznego menu | Użytkownik jest zalogowany. Ikona hamburger menu jest widoczna w widokach: "Zamówienia", "Szczegóły zamówienia", "Dodaj zamówienie", "Edytuj zamówienie". | 1. Naciśnij przycisk hamburger menu znajdując się w lewym górnym rogu aplikacji. |Otwarty zostaje panel menu wyświetlający się po lewej stronie aplikacji i zakrywający 75% szerokości strony oraz 100% jej wysokości. |
| 8 | Zawartość bocznego menu | Użytkownik jest zalogowany. Górny panel jest widoczny. Ikona hamburger menu jest aktywna. | 1. Naciśnij na ikonę hamburger menu w lewym górnym rogu aplikacji. <br> 2. Naciśnij na zakładkę "Zamówienia". <br> 3. Naciśnij ponownie na ikonę hamburger menu. <br> 4. Naciśnij na zakładkę "Wyloguj się". | Po naciśnięciu na zakładkę "Zamówienia" użytkownik zostaje przekierowany do widoku "Zamowienia". Po naciśnięciu "Wyloguj się" zostaje wylogowany i przekierowany do widoku "Strona główna".| 
| 9 | Górny panel aplikacji | Użytkownik jest zalogowany.|  1. Nawiguj kolejno między widokami: "Dodaj zamówienie", "Szczegóły zamówienia", "Zamówienia", "Edytuj zamówienie".<br> 2. Zweryfikuj czy górny panel aplikacji jest widoczny. | Górny panel aplikacji jest cały czas widoczny dla użytkowników, zajmuje 100% szerokośći ekranu oraz 10% wysokości od górnej krawędzi. Górny panel zawiera wyśrodkowaną nazwę danego widoku oraz w lewym rogu ikonę hamburger menu.|
| 10 | Zamówienia widok | Użytkownik jest zalogowany i znajduje się w widoku "Zamówienia". Na liście zamówień znajduje się co najmniej jedno zamówienie.  |1. Zaloguj się do systemu przez formularz logowania. <br>2. Zweryfikuj, że widzisz widok "Zamówienia". | Widok "Zamówienia" składa się z wyśrodkowanych elementów wyświetlonych od góry w kolejności: pole "Wyszukaj", przycisk "Dodaj zamówienie," oraz listy zawierającej wszystkie zamówienia. Po lewej stronie bezpośrednio nad listą zamieszczony jest przycisk z ikoną sortowania, a po prawej przycisk z ikoną filtrowania. | 
| 11 | Lista zamówień| Użytkownik jest zalogowany i znajduje się w widoku "Zamówienia".  Na liście zamówień znajdują się co najmniej dwa zamówienia.| 1. Zaloguj się przez formularz logowania. <br> 2. Zweryfikuj widok listy zamówień. | Lista zamówień wyświetlana jest na 65% wysokości strony od dolnej krawędzi i zawiera listę zamówień domyślnie posortowaną od najnowszego do najstarszego. Z poziomu listy widoczne jest po lewej stronie wiersza: status zamówienia, na środku wiersza: Imię i nazwisko klienta, rodzaj dekoracji okiennej, data złożenia zamówienia (kolejno pod sobą), po prawej stronie wiersza ikona kosza, oczu oraz edycji. |
| 12 | Usuwanie zamówienia | Użytkownik jest zalogowany i znajduje się w widoku "Zamówienia". Na liście zamówień znajduje się co najmniej jedno zamówienie. Użytkownik zalogowany jest tym który dodał wybrane zamówienie. | 1. Naciśnij na ikonę kosza znajdującą się przy danym zamówieniu z listy. <br> 2. Wybierz przycisk "Anuluj". <br> 3. Naciśnij ponownie na ikonkę koszta. <br> 4. Wybierz opcję "Tak, usuń". <br> 5. Zweryfikuj czy wybrane zamówienie zostało usunięte.|  Na środu strony wyświetlone zostaje okienko z tekstem: "Czy na pewno chcesz usunac to zamowienie?" i z dwoma przyciskami "Tak, usuń", "Anuluj". Po naciśnięciu na przycisk "Tak, usuń" system usuwa dane zamówienie z listy zamówień. Po naciśnięciu przycisku "Anuluj" okno się zamyka i wyświetlony zostaje widok "Zamówienia". |
| 13 | Szczegóły zamówienia | Użytkownik jest zalogowany i znajduje się w widoku "Zamówienia". Na liście zamówień znajduje się co najmniej jedno zamówienie. | 1. Naciśnij na ikonę oka znajdującą się przy danym zamówieniu z listy. <br> 2. Zweryfikuj, że widzisz widok "Szczegóły zamówienia". | Przekierowanie na stronę zawierającą szczegóły danego zamówienia - dane przypisane do danego zamówienia zostają wyświetlone jako wyśrodkowany nieedytowalny tekst. 
| 14 | Edycja zamowienia | Użytkownik jest zalogowany i znajduje się w widoku "Zamówienia". Na liście zamówień znajduje się co najmniej jedno zamówienie.|  1. Naciśnij na ikonę edycji w danym wierszu listy zamówień. <br> 2. Zmień status zamówienia. <br> 3. Zmień nazwę klienta. <br> 4. Edytuj datę złożenia zamówienia. | Użytkownik zostaje przekierowany do widoku "Edycja zamówienia", w którym może dokonać edycji danych zawartych w danym zamówieniu - wyświetlone zostają w formie edytowalnych pól wszystkie dane wprowadzone o zamówieniu (w zależności do statusu zamówienia), edycji nie podlega data złożenia zamówienia.|
| 15 |  Zatwierdzanie edycji| Użytkownik jest zalogowany. Na liście zamówień znajduje się co najmniej jedno zamówienie. Użytkownik znajduje się w widoku "Edycja zamówienia". Użytkownik wprowadził zmianę w formularzu edycji zamówienia. | 1. Wprowadź zmiany w formularzu edycji zamówienia. <br> 2. Naciśnij przycisk "Zapisz zmiany". <br>3. Wróć do widoku "Zamówienia". <br> 4. Wejdź ponownie w tryb edycji edytowanego przed chwilą zamówienia z listy zamówień. <br> 5. Zweryfikuj, że dane zostały zmienione.| System aktywuje przycisk "Zapisz zmiany" znajdujący się pod formularzem edycji zamówienia jeśli użytkownik wprowadzi zmiany w formularzu. Zmiany zostają zapisane po naciśnięciu przycisku "Zapisz zmiany".|
| 16 | Zmiana statusu zamówienia |Użytkownik jest zalogowany. Na liście zamówień znajduje się co najmniej jedno zamówienie. Użytkownik znajduje się w widoku "Edycja zamówienia". | 1. W widoku "Edycja zamówienia" wybierz nowy status z listy rozwijanej.  <br> 2. Kliknij "Zapisz edycję". | Po wyborze listy rozwijanej nowego statusu zamówienia wyświetlają się następujące dostępne statusy: 1.Wymiary zebrane, 2.Oferta wysłana, 3.Oferta zaakceptowana, 4.W realizacji 5.Usługa wykonana, 6. Usługa zakończona, 7.Usługa z zastrzeżeniami.
| 17 | Status "Zebrano wymiary" | Użytkownik jest zalogowany. Na liście zamówień znajduje się co najmniej jedno zamówienie. Użytkownik znajduje się w widoku "Edycja zamówienia".| 1. Zmień status zamówień wybierając z rozwijanej listy "Zebrano wymiary". <br> 2. Wpisz w pole "wysokość" wartość liczbową.  <br> 3. Wpisz w pole "szerokość" wartość liczbową. <br> 4. Wybierz z listy rozwijanej typ dekoracji okiennej. <br> 5. Naciśnij przycisk "Zapisz edycję". | Po zmianie statusu zamówienia na "Zebrano wymiary" wyświetlone zostaje pole umożlwiające wpisanie: wysokości okna oraz szerokości okna oraz pole umożliwiające wybór dekoracji okiennej z rozwijanej listy. Lista dekoracji zawiera opcje: "Markizy", "Plisy", "Zasłony", "Moskitiery", "Zewnętrzne", "Żaluzje", "Wolnowiszące", "Bramy".|
| 18 | Edycja daty każdego etapu zamówienia | Użytkownik jest zalogowany. Na liście zamówień znajduje się co najmniej jedno zamówienie. Użytkownik znajduje się w widoku "Edycja zamówienia".| 1. Wybierz nowy status zamówienia z listy. <br> 2. Wybierz datę nowego statusu. <br> 3. Kliknij przycisk "Zapisz edycję". <br> 4. Zweryfikuj czy data nowego statusu została zapisana. | Po wyborze nowego statusu system wyświetla pole do wyboru daty otrzymania danego statusu, która zostaje zapisana poprzez naciśnięciu przycisku "Zapisz edycję" znajdującego się pod formularzem edycji zamówienia.|
| 19| Paginacja listy |Użytkownik jest zalogowany. Na liście zamówień znajduje się co najmniej 20 zamówień. Użytkownik znajduje się w widoku "Zamówienia".|   1. Zjedź na dół listy zamówień. <br>  2. Kliknij na przycisk znaku większości. <br> 3. Sprawdź czy zostałeś przekierowany na drugą stronę listy zamówień. <br> 4.Kliknij na znak mniejszości. | Lista wyświetla w jednym czasie 10 zamówień, która można przewijać w pionie, na dole listy pod ostatnim zamówieniem znajduje się panel paginacji zawierający od lewej: znak mniejszości, numeracje stron (z pogrubieniem aktualnie wyświetlanej strony) zawierającą 5 cyfr, znak większości. Jeśli stron jest więcej niż 5 przekierowanie do stron o wyższym numerze następuje poprzez naciśnięcie znaku większości. Analogicznie przekierowanie do stron niższych. |
| 20 |Filtrowanie listy | Użytkownik jest zalogowany. Na liście zamówień znajdują się co najmniej dwa zamówienia. Użytkownik znajduje się w widoku "Zamówienia".| 1. Naciśnij na ikonę filtrowania. <br> 2. Wybierz dowolną kombinację filtrów. <br> 3. Sprawdź czy lista zamówień jest zmieniona zgdnie z filtrami. |Po naciśnięciu na ikonę filtrowania nad listą pod tą ikoną wyświetlona zostaje lista składająca się z trzech wierszy:  1 - "Status" - z checkboxami "Nowy", "Wymiary zebrane", "Oferta wysłana", "Oferta zaakceptowana", "W realizacji", "Usługa zrealizowana", "Usługa zakończona" 2 - "Termin" - z możliwością wybrania przedziału czasowego z dokładnością do dnia.  3 - "Pracownik" - z checkboxami odpowiadającymi każdemu z aktualnie zatrudnionych w Rolldar pracowników technicznych. Po zaznaczeniu przynajmniej jednego pola aktywny staje się przycisk "Filtruj", po którego naciśnięciu wyświetlona zostaje zaktualizowana zgodnie z wybranymi kryteriami lista zamówień, a lista z opcjami filtrowania zostaje ukryta.|
| 21 | Sortowanie listy | Użytkownik jest zalogowany. Na liście zamówień znajdują się co najmniej dwa zamówienia. Użytkownik znajduje się w widoku "Zamówienia" | 1. Naciśnij na ikonę sortowania nad listą zamówień. <br>  2. Wybierz jedną z dostępnych opcji. <br> 3. Sprawdź czy zamówienia z listy zamówień są prawidłowo posortowane. <br> 4. Powtórz kroki 1-3 wybierając za każdym razem w kroku drugim inną z dostępnych opcji. |Pod ikoną sortowania wyświetlona zostaje lista składająca się z sześciu opcji do wyboru wierszy:  1 - "Według daty od najstarszych", 2 - "Według daty od najnowszych", 3 - "Według statusu od nowych", 4 - "Według statusu od zakończonych", 5 - "Według nazwiska klienta od A do Z" 6 - "Według nazwiska klienta od Z do A". Wyświetlona zostaje posortowana zgodnie z wybranymi kryteriami lista zamówień, a lista z opcjami sortowania zostaje ukryta.|
| 22 | Dodaj  zamówienie |Użytkownik jest zalogowany. Użytkownik znajduje się w widoku "Zamówienia".| 1. Naciśnij przycisk "Dodaj zamówienie". | System przekierowuje użytkownika do widoku "Dodaj zamówienie", który zawiera formularz nowego zamówienia. |
| 23 |  Formularz nowego zamówienia |Użytkownik jest zalogowany. Użytkownik znajduje się w widoku "Dodaj zamówienie".| 1. Uzupełnij formularz następującymi danymi: Imię i nazwisko klienta (obowiązkowe pole tekstowe min 5 znaków, max 50), miejscowość (obowiązkowe pole, min 4 znaki, max 40), ulica (obowiązkowe, min 3 znaki, max 50), kod pocztowy (obowiązkowe pole, zgodny z formatem kodu pocztowego 00-000), numer budynku/mieszkania (obowiązkowe pole tekstowe, min 1 znak, max 10), numer telefonu (obowiązkowe,9 cyfr), data złożenia zamówienia, data pierwszej wizyty, notatka (pole tekstowe nieobowiązkowe, maximum 400 slow). <br> 2. Naciśnij "Zapisz". | Użytkownik może wpisać dane do formularza nowego zamówienia. Po zapisaniu zamówienie jest widoczne w widoku "Zamówienia". |
| 24 | Zapisanie zamowienia | Użytkownik jest zalogowany. Użytkownik znajduje się w widoku "Dodaj zamówienie". Użytkownik uzupełnił dane formularza nowego zamówienia danymi w prawidłowym formacie. | 1. Wpisz do formularza nowego zamówienia wymagane dane w prawidłowym formacie. <br> 2. Kliknij przycisk "Zapisz".  | Wyświetlone zostaje okno z tekstem: "Dodano nowe zamówienie o numerze xxx". |
| 25 | Wyszukanie oferty | Użytkownik jest zalogowany. Użytkownik znajduje się w widoku "Zamówienia". Pasek wyszukiwania zamówień jest widoczny. Na liście zamówień znajdują się co najmniej dwa zamówienia. | 1. Wpisz w pasek wyszukiwania numer telefonu klienta. <br> 2. Zweryfikuj zawartość listy. <br> 3. Powtórz kroki 1-2 zmieniając numer telefonu na: imię klienta, nazwisko klienta, adres klienta.  | Lista zamówień wyświetla tylko zamówienia zawierające daną frazę. |
| 26 |  Usuwanie filtru wyszukiwania | Użytkownik jest zalogowany. Użytkownik znajduje się w widoku "Zamówienia". Pasek wyszukiwania zamówień jest widoczny.| 1. Wpisz tekst w pasku wyszukiwania. <br> 2. Naciśnj na ikonę "x" znajdującą się po prawej stronie na pasku wyszukiwania. | System usuwa frazę wpisaną w pasku wyszukiwania i przywraca domyślny widok listy zamówień.|
# Słownik pojęć

<ins> <b> Widok </b> </ins>

Jest to warstwa interfejsu użytkownika (UI) odpowiedzialna za wyświetlanie informacji i umożliwianie interakcji z użytkownikiem na ekranie urządzenia mobilnego, takiego jak smartphone czy tablet. Widok stanowi reprezentacje konkretne złożenie elementó, które tworzą interfejs użytkownika. Użytkownik może przemieszczać się pomiędzy widokami.

<ins> <b> Zamówienie </b></ins>

Zlecenie zawarte przez umowę ustną obejmujące wszystkie etapy dostarczenia dekoracji okiennej wraz z usługą jej montażu lub serwisu. W rach Zamówienia w aplikacji Rolldar przechowywane są następujące dane:
- Imię i nazwisko klienta
- Adres wykonania zlecenia
- Numer telefonu klienta
- Obecny status zamówienia. 
Do wyboru 6 statusów: "Nowy", "Wymiary zebrane", "Oferta wysłana", "Oferta zaakceptowana", "W realizacji", "Usługa zrealizowana", "Usługa zakończona"
- Imię i nazwisko pracownika odpowiedzialnego za realizację zlecenia
- Wysokość oraz szerokość okna (wymiary okna)
- Rodzaj dekoracji okiennej dostarczonej w ramach zamówienia.

<ins> <b> System </b></ins>

Wszystkie elementy i powiązania między nimi tworzące aplikację mobilną Rolldar Mobilnie.
  
<ins> <b> Klient </b></ins>

Osoba zlecająca realizację zamówienia przez firmę Rolldar.

<ins> <b> Użytkownik </b></ins>

Pracownik firmy Rolldar obsługujący aplikację mobilną Rolldar Mobilnie dostarczaną w ramach niniejszego projektu.

# Możliwości rozbudowy

1) Funkcjonalność dodawania zdjęć do zamówienia.
2) Przechowywanie w ramach oddzielnej zakładki listy klientów z możliwością filtrowania, sortowania i wyszukiwania w ramach tej listy.

# Projekt widoków
![Zrzut ekranu (1773)](https://github.com/NataliaSkorowska/RolldarAplikacjaMobilna/assets/56688592/19d49870-e0c1-4eea-ad8c-8ba562a3ee25)
![Zrzut ekranu (1774)](https://github.com/NataliaSkorowska/RolldarAplikacjaMobilna/assets/56688592/a975e4b3-0af5-4325-9f20-166735f835eb)

![Zrzut ekranu (1776)](https://github.com/NataliaSkorowska/RolldarAplikacjaMobilna/assets/56688592/989f4119-4947-4a40-9f5e-dea7eae68d50)
