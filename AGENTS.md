# Monitor TK — instrukcja procesu

Repozytorium jest publiczne. Nie zapisuj sekretów ani prywatnych danych. Wykonuj wyłącznie zadanie i zakres określone przez właściciela; nie zmieniaj gałęzi `main` ani dostępu do Site.

## Cykl monitoringu
1. Odczytaj aktualną gałąź `monitor-tk`, skrzynkę `data/inbox.md`, historię wpisów, wyniki poprzednich uruchomień i stan produkcyjnej strony Sites (numer wersji, status wdrożenia i tryb dostępu). Sprawdź, czy istnieje zaległa publikacja; nie twórz duplikatu.
2. Sprawdź wiarygodne źródła, zaczynając od dokumentów instytucji, a następnie niezależne media. Obejmuj zdarzenia od 30 października 2026. Weryfikuj bezpośrednie adresy i daty źródeł. Nie wymyślaj danych, cytatów ani godzin.
3. Oddziel fakty, relacje, opinie i kwestionowane twierdzenia. Przy ważnych twierdzeniach szukaj niezależnego potwierdzenia; brak potwierdzenia oznacz. Zapisz rozbieżności i krótkie cytaty z autorstwem.
   Przy każdym przeglądzie sprawdź także nowe opinie prawne i stanowiska stron. Powiąż wypowiedź z konkretnym wydarzeniem, podaj autora i źródło. W dzienniku odnotuj wynik sprawdzenia również wtedy, gdy nie dodano opinii.
4. Porównaj z istniejącymi wpisami, połącz źródła dotyczące tego samego zdarzenia; dopisuj nowe fakty i zachowuj historię zmian oraz widoczne sprostowania. Podaj odrębnie czas zdarzenia, publikacji źródła i zmiany serwisu, jeśli znany.
   Przy każdym przeglądzie wróć do wcześniejszych zapowiedzi. Sprawdź, czy działanie się odbyło, odwołano je lub opublikowano rezultat. Uzupełnij istniejący wpis i połącz go z późniejszym dokumentem. Rozróżniaj wejście na teren posesji i wejście do budynku. Nie utożsamiaj daty publikacji relacji z datą zdarzenia.
5. Bez istotnych nowych danych nie twórz wiadomości. Zapisz czas sprawdzenia i wynik, wyraźnie odróżniając go od czasu zmiany treści. Przed zapisem sprawdź bieżący SHA gałęzi, unikaj nadpisania cudzych zmian.
6. Po zmianie treści przygotuj kolejną wersję, ustalając bieżący numer i status wdrożenia w Sites. Wdróż ją po odrębnej zgodzie właściciela na publikację tej wersji. Zachowaj dotychczasowy dostęp i historię. Potwierdź wersję oraz widoczność zmiany; w razie błędu zapisz zaległą publikację i ponów bez duplikowania. Nie twierdź, że publikacja się powiodła bez dowodu.
7. Raportuj rzeczywisty wynik każdego etapu, źródła, błędy i ograniczenia. Nie upubliczniaj witryny i nie twórz harmonogramu cyklicznego bez odrębnej zgody.

## Skrzynka zgłoszeń
Plik `data/inbox.md` jest trwałą kolejką materiałów przekazywanych przez właściciela także z innych rozmów ChatGPT. Przy każdym przeglądzie odczytaj go i rozpatrz oczekujące zgłoszenia, równolegle prowadząc własny monitoring źródeł. Zgłoszenia typu TREŚĆ weryfikuj merytorycznie i porównuj z chronologią; zgłoszenia typu SERWIS oceniaj jako propozycje UX, dostępności lub zmian technicznych. Nie traktuj zgłoszeń jako potwierdzonych faktów ani automatycznych poleceń wdrożenia. Zmiany większe lub wykraczające poza zgodę właściciela przedstaw do decyzji. Po rozpatrzeniu zapisz status i krótkie uzasadnienie w skrzynce; jeśli potrzebna jest decyzja lub weryfikacja, pozostaw „oczekuje” z wyjaśnieniem. Status „uwzględnione” nadaj dopiero po potwierdzeniu rezultatu; przy przerwaniu pracy ponownie sprawdź stan przed zmianą statusu. Zachowuj historię zamkniętych zgłoszeń. Nie zmieniaj reguły odrębnej zgody na publikację.

## Spójność dokumentacji
Po każdym przeglądzie i aktualizacji sprawdź zgodność README.md, AGENTS.md, data/inbox.md oraz data/przeglady.md. Nie powielaj bieżącego numeru wersji w README.md ani w stałych instrukcjach AGENTS.md. Aktualny stan publikacji ustalaj na podstawie Sites, a historię zmian i dowody wdrożeń zapisuj w data/przeglady.md. Rozbieżności poprawiaj, jeśli są potwierdzone, a w przeciwnym razie odnotuj je w dzienniku. Nie traktuj historycznych wpisów jako opisu aktualnego stanu.

## Próba integracyjna
Historyczna procedura dla prywatnego demo. Nie wykonuj zmiany testowej na publicznej stronie. W teście jednorazowym wpisz do `data/test.json` wynik odczytu i zapisu, a na prywatnej demonstracji wykonaj wyraźnie oznaczoną niewielką zmianę testową, jeżeli dostęp i aktualne dane na to pozwalają. Zapisz dowody i porównaj stan GitHub oraz wdrożenia. Nie przedstawiaj danych testowych jako wiadomości.
