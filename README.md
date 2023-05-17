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
| NF1 | Niefunkcjonalne | Interfejs | Języ interfejsu | Interfejs użytkownika, komunikaty, powiadomienia, alerty przesyłane (pokazywane) użytkownikowi muszą być prezentowane w języku polskim. |1|
| NF2 | Niefunkcjonalne | Interfejs	| Logo | Logo firmy Rolldar zamieszczane w aplikacji jest zawsze widoczne w całości w wielkości dostosowanej do danego widoku.|1|
| NF3 | Niefunkcjonalne | Interfejs |  Poziom trudności obsługi | Aplikacja musi być możliwa do obsługi dla osób bez specjalistycznej wiedzy informatycznej i programistycznej, w tym umożliwiać pracę jedynie z poziomu interfejsu, bez konieczności pisania kodu. |1|
| NF4 | Niefunkcjonalne | Interfejs | Ergonomia | Moduły funkcjonalne muszą być wyposażone w estetyczny, spójny oraz intuicyjny interfejs użytkownika. Kolorystyka, grafika, kształty i czcionki muszą być jednakowe między różnymi widokami.|1|
| NF5 | Niefunkcjonalne | Interfejs | Responsywność | Interfejs aplikacji powinien dostosowywać się do wymiarów urządzenia, na którym wyświetlone zostają widoki.|1|
| NF6 | Niefunkcjonalne | Projektowe | Format daty| Data w systemie powinna być wyświetlana zgodnie z formatem dd.mm.yyyy|1|
| NF7 | Niefunkcjonalne | Projektowe |  Kopia zapasowa | Aplikacja powinna posiadać kopię zapasową tworzoną automatycznie raz w tygodniu tak, aby istniała możliwość odtworzenia środowiska i danych (w części lub w całości).  |1|
| NF8 | Niefunkcjonalne | Projektowe	 | Rozbudowa | Aplikacja powinna zostać napisana w taki sposób aby umożliwić ewentualną implementację kolejnych funkcjonalności lub modyfikację poszczególnych modułów w przyszłości. |1|
| NF9 | Niefunkcjonalne | Projektowe	 | Struktura kodu | Kod aplikacji powinien zostać napisany zgodnie z dobrymi zasadami pisania kodu, stosując konwencję nazewnictwa oraz wcięcia w kodzie zgodnie ze standardami przyjętymi dla danego języka programowania.|1|
| NF10 | Niefunkcjonalne | Projektowe | Dokumentacja | Do systemu (przed pierwszym wydaniem klientowi) powinna zostać dostarczona dedykowana dokumentacja techniczna stworzona w polskiej wersji językowej.
| NF11 | Niefunkcjonalne | Projektowe	 | Testowanie | Wymagane jest przeprowadzenie testów poszczególnych modułów aplikacji  z udziałem pracowników Rolldar do momentu poprawnego zakończenia wszystkich testów(UAT). | 1|
| NF12 | Niefunkcjonalne | Projektowe	| Repozytorium | Wszystkie wytworzone pliki (w szczególności całość kodu źródłowego) aplikacji muszą być zapisywane w repozytorium i aktualizowane w ramach przekazywania kolejnych wersji aplikacji. |1|
| N13 | Niefunkcjonalne | Bezpieczeństwo	 | Szyfrowanie danych | System powinien szyfrować wszystkie dane użytkowników przesyłane pomiędzy aplikacją a bazą danych. |1|
| NF14 | Niefunkcjonalne | Bezpieczeństwo	 | Zgodność z prawem | Standard bezpieczeństwa informacji zawartych w aplikacji powinien być zgodny z aktualnym prawem. |1|
| NF15 | Niefunkcjonalne | Bezpieczeństwo	| Zmiana hasła | Aplikacja powinna wymuszać zmianę hasła użytkownika co 60 dni. |1|
| NF16 | Niefunkcjonalne | Wydajnościowe	 | Liczba użytkowników | Jednocześnie ze strony może korzystać 500 osób znajdujących się w różnych lokalizacjach |1|
| NF17 | Niefunkcjonalne | Wydajnościowe	| Czas pracy| Aplikacja powinna być dostępna dla użytkowników 24/7/365 średnio 97% czasu. W ciągu kolejnych 4 lat korzystania z niej |1|
| NF18 | Niefunkcjonalne | Wydajnościowe	| Czas uruchomienia po awarii| W przypadku awarii aplikacja powinna zostać naprawiona w ciągu 5 godzin od pierwszego zgłoszenia niepożądanego zachowania systemu. |1|
| NF19 | Niefunkcjonalne | Utrzymanie	| Wersjonowanie | Nowe wersje aplikacji publikowane są zgodnie z konwencją: X.Y.Z, gdzie X oznacza numer znacznącej wprowadzonej zmiany najczęściej dodającej nowe funkcjonalności, y jest wersją, która wprowadziła niewielkie zmiany w funcjonalności (przyrosty funkcjonalności), a Z służy do wprowadzenia poprawek bezpieczeństwa krytycznych błędów. |1|
| NF20 | Niefunkcjonalne | Utrzymanie	| Aktualizacja | Nowe wydania systemu są publikowane w oparciu o przeprowadzoną analizę obciążenia systemu. Wydanie wprowadzane jest w momencie najmniejszego obciążenia systemu.  |1|
| NF21 | Niefunkcjonalne | Utrzymanie	| Wsparcie po aktualizacji | Po wprowadzeniu aktualizacji przez 24 godziny zzapewnione jest wsparcie techniczne na wypadek niepożądanych konsekwencji wprowadzenia nowych funkconalności.  |1|
| NF22 | Niefunkcjonalne | Dostęp	 | Sklepy z aplikacjami | Aplikacja powinna być dostępna do pobrania za darmo w sklepach z aplikacjami Google Play oraz Apple Store. |1|
| NF23 | Niefunkcjonalne | Dostęp	 | Systemy operacyjne  | Aplikacja powinna działać prawidłowo na urządzeniach zawierających mobilny system operacyjny Android (wersja 9.0 i wyższe) oraz iOS (wersja 12.0 i wyższe). |1|
| NF24 | Niefunkcjonalne | Czas reakcji |  | Maksymalny czas pomiędzy pobudzeniem przez użytkownika a odpowiedzią systemu nie powinien być dłuższy niż 4 sekundy. |1|
| NF25 | Niefunkcjonalne | Dostęp | Połączenie z Internetem| Do prawidłowego funkcjonowania systemu niezbędne jest stabilne połączenie internetowe wynoszące minimum 300 mb/s. |1|
| ------- | -------|------|------| -----| ----- |
| F1 | Funkcjonalne | Logowanie | Tworzenie konta| Użytkownik może założyć nowe konto w aplikacji jako klient po podaniu w odpowiednim formularzu swojego imienia, nazwiska, adresu email oraz hasła |1|
| 2 | Funkcjonalne | Logowanie | Walidacja rejestracji | Jeśli użytkownik podczas wypełniania formularza rejestracji poda dane w nieodpowiednim formacie, lub będzie chciał użyć istniejącego w bazie adresu email informacja o tym zostanie wyświetlona pod formularzem| 1 |
| 3 | Funkcjonalne | Logowanie | Przekierowanie po rejestracji | Użytkownik po udanym utworzeniu konta zostanie przekierowany na stronę z ofertą firmy Rolldar | 2 |
| 4 | Funkcjonalne |Logowanie| Logowanie klienta | Użytkownik może zalogować się do aplikacji na wcześniej założone konto po podaniu poprawnego adresu email oraz hasła| 1 |
| 5 | Funkcjonalne |  Logowanie | Walidacja logowania klienta| Jeśli użytkownik podczas próby logowania poda nieprawidłowe hasło lub adres email informacja o tym zostanie wyświetlona pod formularzem| 1 |
| 6 | Funkcjonalne | Logowanie | Przekierowanie po logowaniu | Użytkownik po udanym zalogowaniu zostanie przekierowany na stronę z ofertą firmy Rolldar | 2 |
| 7 | Funkcjonalne |Logowanie | Odzyskiwanie hasła | Użytkownik podając swój adres email w odpowiednim miejscu może wygenerować mail, który będzie zawierał link do formularza umożliwiającego zmianę hasła, jeśli podany email nie znajduje się w bazie zostanie wyświetlony stosowny komunikat | 2 |
| 8 | Funkcjonalne | Logowanie | Strona główna | Po wejściu do aplikacji użytkownik zostaje przekierowany na stronę główną, na której znajduje się logo firmy oraz dwa przyciski - jeden przekierowuje do strony logowania dla pracowników, a drugi do strony logowania dla klientów | 1 |
| 9 | Funkcjonalne | Logowanie | Logowanie pracownika | Użytkownik znajdujący się na stronie zawierającej formularz logowania dla pracowników po wpisaniu prawidłowo loginu oraz hasła zostaje przekierowany do strony "Panel pracownika" | 1  |
| 10 | Funkcjonalne | Logowanie | Walidacja logowania pracownika | Użytkownik znajdujący się na stronie zawierającej formularz logowania dla pracowników po wpisaniu nieprawidłowych danych w formularzu zostaje o tym poinformowany poprzez wyświetlenie stosownego komunikatu | 1 |
| 11 | Funkcjonalne | Oferta | Widok oferty| Użytkownik ma możliwość przeglądania oferty firmy Rolldar poprzez widok strony "Oferta", która zawiera wszystkie dostępne rodzaje dekoracji okien| 1 |
| 12 | Funkcjonalne | Oferta | Wyszukanie oferty| Poprzez pasek wyszukiwania znajdujący się na górze strony "Oferta" użytkownik ma możliwość wyszukania interesującego go elementu z oferty firmy| 3 |
| 13 | Funkcjonalne | Oferta | Szczegóły oferty | Użytkownik po kliknięciu na dany rodzaj dekoracji okiennej na stronie "Oferta" zostanie przeniesiony do strony zawierającej szczegółowe informacje oraz galerie zdjęć wybranej przez siebie opcji| 2 |
| 14 | Funkcjonalne | Oferta | Karuzela ze zdjęciami | Użytkownik na stronie ze szczegółami oferty widzi galerię zdjęć, które automatycznie się przewijają, ale może także przeglądać je samodzielnie poprzez nawigację w lewo lub w prawo| 3 |
| 15 | Funkcjonalne | Menu | Wyświetlenie bocznego menu | Użytkownik poprzez naciśnięcie przycisku menu znajdującego się w lewym górnym rogu aplikacji otwiera panel menu wyświetlający się po prawej stronie aplikacji | 1 |
| 16 | Funkcjonalne | Menu | Zawartość bocznego menu | Poprzez naciśnięcie na jedną z zakładek znajdującego się w bocznym menu: 'Oferta', 'Rezerwuj usługę' oraz 'Wyloguj się' użytkownik zostaje odpowiednio przekierowany do strony z ofertą, rezerwacją lub po wylogowaniu do strony głównej aplikacji | 1  |
| 17 | Funkcjonalne | Rezerwacja | Dokonanie rezerwacji | Użytkownik poprzez poprawne wypełnienie formularza rezerwacji ma możliwość umówienia się na wykonanie usługi przez firmę Rolldar, po udanej rezerwacji wyświetlone zostaje okno informujące o powodzeniu  | 1 |
| 18 | Funkcjonalne | Rezerwacja | Formularz rezerwacji | Użytkownik wypełnia poprawnie formularz poprzez podanie swojego: imienia i nazwiska, adresu email, numeru telefonu, adresu zamieszkania oraz po wybraniu intereującej go usługi, rodzaju rolet, dnia, oraz godziny od której i do której ma czas na daną usługę, jeśli podane dane będą nieprawidłowe pojawi się stosowny komunikat  | 1 |
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


# 5. Testy
