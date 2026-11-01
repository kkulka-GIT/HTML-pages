# Reviewer Kafelków Wiedzy — instrukcja eksperymentalna

Status: instrukcja do uruchamiania review na żądanie. Nie jest instrukcją produkcyjnego aktualizatora Monitora TK.

## Cel
Ocenić, czy istniejąca, opublikowana treść Monitora TK nadaje się do wiernego odwzorowania w uporządkowanych JSON-ach, bez utraty narracji, źródeł, dat, zastrzeżeń i rozróżnienia faktów od ocen. Uczyć się na kolejnych próbach i formułować propozycje ulepszeń struktury przyszłych wpisów Monitora.

## Wejścia
- Publiczny Monitor TK: https://monitor-tk-2026.kkulka.chatgpt.site/ oraz jego podstrony.
- Ten katalog: README.md, manifest.json, validation.json, tiles.schema.json, events.json, positions.json, context.json, entities.json, sources.json.
- REVIEW_LOG.md: wcześniejsze problemy, hipotezy, decyzje i wyniki.
- Gdy dostępne: poprzedni snapshot strony, poprzedni zestaw JSON oraz odpowiadające im commity. Nie porównuj wersji bez ustalenia ich pochodzenia.

## Przebieg review
1. Ustal dokładną wersję strony i JSON-ów, daty oraz commity. Wyraźnie zaznacz brak dostępu do którejkolwiek wersji.
2. Oceń zachowanie znaczenia: wydarzenia, osoby, instytucje, dokumenty, stanowiska, opinie, kwestie sporne, chronologię i kontekst.
3. Sprawdź, czy kafelki są zbyt zbiorcze albo sztucznie rozdrobnione; czy można prześledzić każde istotne twierdzenie do konkretnego fragmentu Monitora i jego źródła; czy nie pomylono relacji o twierdzeniu z potwierdzeniem samego twierdzenia.
4. Sprawdź stabilność identyfikatorów, relacje, autorstwo, daty wydarzeń i publikacji, deduplikację, korekty i brakujące fragmenty. Oddziel walidację techniczną od oceny semantycznej.
5. Jeśli przeprowadzasz próbę konwersji, użyj wyłącznie wskazanego snapshotu Monitora; nie prowadź niezależnego researchu w celu dopisywania faktów. Zapisz wersję wejścia, metodę, wynik, walidację i rozbieżności. Nie nadpisuj zatwierdzonych JSON-ów bez odrębnej zgody.
6. Porównaj wynik z wcześniejszymi próbami i sprawdź, czy zaakceptowane wcześniej zalecenia poprawiły reprezentację. Nie ogłaszaj sukcesu wyłącznie dlatego, że JSON przechodzi schemat.
7. Zapisz w REVIEW_LOG.md konkretne ustalenia: dowód/przykład, skutek dla przyszłej migracji, propozycję, priorytet, status, sposób sprawdzenia w kolejnej aktualizacji.

## Dwie oddzielne ścieżki
Reviewer analizuje i proponuje. Produkcyjny aktualizator Monitora nadal działa według swoich instrukcji. Reviewer nie zmienia automatycznie strony, AGENTS.md, inboxu, D1, Sites ani workflow GitHub Actions.

Propozycje zmian dotyczących sposobu redagowania lub struktury strony trafiają do istniejącego inboxu Monitora TK **dopiero po akceptacji użytkownika**. Do inboxu przenosi się zwięzłe, wykonalne zalecenie z uzasadnieniem i identyfikatorem wpisu review, a nie cały raport. Aktualizator powinien zachować naturalną czytelność strony; nie należy podporządkowywać narracji sztywnemu formatowi JSON.

Po kolejnej aktualizacji Reviewer ponownie sprawdza tę samą uwagę i oznacza ją jako potwierdzoną, nierozwiązaną albo wymagającą korekty. Żadna uwaga nie staje się automatycznie obowiązującą regułą.

## Kryterium gotowości
Migrację można rozważyć dopiero po powtarzalnych testach na kolejnych wersjach: brak istotnych pominięć i dopisanych faktów, identyfikowalne źródła twierdzeń, poprawne role i daty, stabilne ID, odtwarzalna narracja oraz brak regresji. Decyzja o migracji jest odrębna od review.

## Format wyniku
Podaj: analizowane wersje; co działa; problemy z konkretnymi ID lub fragmentami; zalecenia dla struktury strony versus zalecenia dla ekstraktora JSON; wynik porównania z poprzednią próbą; otwarte pytania; propozycje do zatwierdzenia i ewentualnego przekazania do inboxu.
