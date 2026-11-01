# Dziennik review — Kafelki Wiedzy Monitora TK

Cel: trwała pamięć eksperymentu i kontrola skutków uwag przekazywanych do aktualizatora Monitora. Wpisy review nie są automatycznie poleceniami dla produkcyjnego aktualizatora.

## Statusy
- **obserwacja** — problem zidentyfikowany, bez decyzji o wdrożeniu;
- **propozycja** — sformułowano testowalne zalecenie;
- **zaakceptowane do inboxu** — użytkownik zatwierdził przekazanie;
- **weryfikacja** — czekamy na kolejną aktualizację i test JSON;
- **potwierdzone / nierozwiązane / odrzucone** — wynik sprawdzenia.

## Review R-001 — 1 listopada 2026
**Materiał:** eksperyment 0.1, snapshot Monitora `monitor-2026-11-01`, pliki wymienione w manifest.json. Wstępne review struktury JSON; bez niezależnego fact-checkingu i bez uruchamiania nowej konwersji.

**R-001-A — osoby jako indeksy, nie sieć działań.** Przykład: `tk-person-bogdan-swieczkowski` ma listę odsyłaczy, ale nie daje jeszcze bezpośredniego modelu jego działań, dokumentów i przypisanych stanowisk. Status: **obserwacja**. Hipoteza: wyraźniejsze oddzielenie działań, dokumentów i ocen w strukturze wpisów Monitora ułatwi ekstrakcję. Test: sprawdzić po następnej aktualizacji, czy można bez domysłów odtworzyć te powiązania. Nie wnioskować o sprawstwie z samej relacji `mentions`.

**R-001-B — dokumenty zbiorcze.** Przykład: `tk-dokumenty-przerwa-w-czynnosciach` łączy opisy dwóch zarządzeń. Status: **obserwacja**. Hipoteza: odrębne identyfikowalne opisy dokumentów ułatwią przypisanie autora, daty, źródła i relacji, przy zachowaniu wspólnej narracji na stronie. Test: czy konwersja tworzy dwa odrębne dokumenty bez sztucznego dopowiadania.

**R-001-C — źródła przypisane do całego kafelka.** Przykład: `tk-apel-siedmiu` łączy informację o oświadczeniu, podpisach, publikacji i niepewności co do spotkania. Status: **obserwacja**. Hipoteza: dokładniejsze przypisanie źródeł do poszczególnych ustaleń ułatwi kontrolę zgodności. Test: czy każde istotne twierdzenie da się przypisać do konkretnego źródła bez zgadywania.

**R-001-D — daty i etykiety czasu.** Przykład: `tk-oredzie-premiera` ma etykietę `31 października 2026Wieczór`, a daty publikacji i zdarzeń nie zawsze są oddzielone. Status: **obserwacja**. Test: czy przyszłe wersje pozwalają rozróżnić datę wydarzenia, dokumentu, publikacji i planowanego działania; ustalić, czy problem pochodzi ze strony, czy z ekstrakcji.

**R-001-E — relacje zbyt ogólne.** Aktualny model ma `mentions`, `comments_on`, `references`, `same_subject_as`. Status: **obserwacja**. Hipoteza: lepsza struktura źródłowych wpisów pomoże bezpiecznie odróżniać `issued_by`, `signed_by`, `responds_to` i inne związki. Test: relacje mają wynikać z tekstu i źródeł, nie z samej obecności nazwiska.

## Zasada przekazywania do Monitora
Nie wysyłaj automatycznie powyższych obserwacji do inboxu. Po zatwierdzeniu przez użytkownika dodaj do istniejącego inboxu konkretne zalecenie z numerem R-001-..., oczekiwanym skutkiem i warunkiem późniejszego testu. Po wykonaniu aktualizacji dopisz wynik testu tutaj; nie usuwaj historii nieudanych prób.

## Szablon kolejnego wpisu
**Review ID i data:**  
**Wersja strony / commit:**  
**Wersja JSON / commit:**  
**Problem i przykład:**  
**Czy źródłem problemu jest strona, ekstrakcja czy model JSON?:**  
**Propozycja i oczekiwany skutek:**  
**Status decyzji / przekazanie do inboxu:**  
**Test i wynik po kolejnej aktualizacji:**  
