---
name: przeglad-github
description: Używaj, gdy użytkownik prosi o przegląd, uporządkowanie lub odświeżenie swoich repozytoriów na GitHubie — "przejrzyj profil", "ogarnij repo", "sprawdź, czy nic nie wyciekło", "co poprawić przed pokazaniem komuś". Także przed wrzuceniem nowego repozytorium publicznie.
---

# Przegląd repozytoriów na GitHubie

Procedura przeglądu profilu: co sprawdzić, w jakiej kolejności, co poprawić od
razu, a co zostawić do decyzji właściciela. Lista powstała z realnego sprzątania
profilu — każdy punkt odpowiada błędowi, który faktycznie się zdarzył.

## Zanim zaczniesz

Potrzebny jest dostęp do repozytoriów (konektor GitHub). Sklonuj każde
repozytorium, które masz przeglądać — pracuj na kopii, nie na podstawie samych
nazw plików z listingu.

Ustal z właścicielem, czy przegląd ma **raportować**, czy **poprawiać**. Domyślnie
poprawiaj rzeczy techniczne, a wszystko, co jest głosem właściciela — opisy,
README, nazwy — proponuj i pytaj.

## Kolejność

Zaczynaj od bezpieczeństwa. Reszta to kosmetyka, która może poczekać; wyciek
nie.

### 1. Sekrety i dane

- Przeszukaj drzewo pod kątem: `api_key`, `secret`, `token`, `password`,
  `bearer`, ciągów 24+ znaków wyglądających na klucz.
- Sprawdź, czy nie ma śledzonego `.env` (sam `.env.example` jest w porządku).
- **Zajrzyj do baz danych** (`*.db`, `*.sqlite`) — wylistuj tabele i policz
  wiersze. Pusta baza testowa jest nieszkodliwa; baza z adresami e-mail
  użytkowników to incydent.
- W repozytorium z promptami sprawdź dodatkowo kontekst firmowy: nazwy systemów,
  identyfikatory pól, przykłady na prawdziwych danych.
- Pamiętaj, że usunięcie pliku **nie usuwa go z historii**. Jeśli sekret był
  prawdziwy: najpierw unieważnić, potem dopiero sprzątać repozytorium.

### 2. Śmieci w repozytorium

Typowe: `.venv/`, `node_modules/`, `__pycache__/`, `*.pyc`, pliki baz,
`.DS_Store`, wgrane paczki `.zip`, katalogi `dist/` i `build/`.

**Sprawdź, czy `.gitignore` naprawdę działa.** Wpis w `.gitignore` nie przestaje
śledzić pliku, który trafił do repozytorium wcześniej — to najczęstsza pułapka.
Porównaj `git ls-files` z regułami; jeśli plik jest śledzony mimo wpisu, usuń go
ze śledzenia (`git rm --cached`), zostawiając na dysku.

### 3. Struktura

- README **w korzeniu** repozytorium — GitHub renderuje tylko ten.
- Czy pliki nie wjechały o poziom za głęboko (typowe po wgrywaniu przez stronę
  przez przeciągnięcie całego folderu zamiast jego zawartości).
- Czy w korzeniu nie leży coś, co powinno być w podkatalogu.

### 4. README

- Istnieje, nie jest pusty i nie jest zaślepką w stylu „Nothing here yet".
- Mówi, **co to jest, do czego służy i jak to uruchomić** — w tej kolejności.
- Wszystkie linki żyją; wszystkie obrazki istnieją pod wskazanymi ścieżkami
  (sprawdź przez odczyt plików, nie na oko).
- Przy projektach kursowych: uczciwie to nazwij. „Projekt kursowy" brzmi lepiej
  niż odkryte przez czytelnika udawanie produkcji.
- Sekcja o tym, czego świadomie nie ma (testów, danych, konfiguracji) zwykle
  dodaje wiarygodności, zamiast ujmować.

### 5. Nazewnictwo i spójność

- Jedna konwencja we wszystkich repozytoriach: małe litery i myślniki.
- Nazwa opisuje zawartość, nie technologię i nie etap nauki.
- **Po zmianie nazwy poszukaj starej w treści plików** — GitHub przekierowuje
  adresy, ale odnośniki zaszyte w plikach (badge Colab, linki w README) mogą
  wskazywać ścieżkę, która nie zostanie przekierowana przez narzędzie trzecie.

### 6. Opis i topics

Pola *About* na stronie repozytorium. Ich **nie da się ustawić z poziomu kodu**
w sesji z konektorem — przygotuj gotowe teksty do wklejenia i powiedz wprost, że
ten krok wymaga ręcznego kliknięcia.

### 7. Profil

- README profilu (repozytorium o nazwie równej loginowi) — czy istnieje i czy
  wiąże projekty w opowieść, zamiast powtarzać listę nazw.
- Czy przypięte repozytoria to te, które właściciel chce pokazać najpierw.
- Czy opisy na profilu zgadzają się z opisami w samych repozytoriach.

## Zasady przy poprawianiu

**Poprawiaj bez pytania:** usuwanie śmieci ze śledzenia, `.gitignore`, martwe
linki, literówki, spójność nazw plików wewnątrz repozytorium.

**Zapytaj najpierw:** treść README, opisy, nazwy repozytoriów, cokolwiek, co
brzmi jak głos właściciela, i wszystko, co kasuje historię.

**Nigdy sam:** zmiana widoczności repozytorium (publiczne/prywatne), usuwanie
repozytoriów, wymuszony push przepisujący historię.

## Commity

Jedna zmiana logiczna = jeden commit. W treści napisz **dlaczego**, nie tylko co:
„usuń .venv ze śledzenia — wpis w .gitignore nie działał, bo pliki były śledzone
wcześniej" niesie informację, której sam diff nie pokaże.

Przy plikach `.ipynb` **nie przepisuj JSON-a narzędziem** przy drobnej zmianie —
formatowanie zmieni się w całym pliku i diff spuchnie do tysięcy linii. Podmieniaj
tekst punktowo.

## Na koniec

Podsumuj w trzech częściach: co poprawione, co wymaga kliknięcia właściciela
(z gotowymi tekstami), co zostawione do decyzji i dlaczego. Bez ściany tekstu —
właściciel ma wiedzieć, czy coś go jeszcze czeka.
