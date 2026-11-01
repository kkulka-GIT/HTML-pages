# Monitor TK — instrukcja procesu

Repozytorium jest publiczne. Nie zapisuj sekretów ani prywatnych danych. Wykonuj wyłącznie zadanie i zakres określone przez właściciela; nie zmieniaj gałęzi `main` ani dostępu do Site.

## Cykl monitoringu
1. Odczytaj aktualną gałąź `monitor-tk`, historię wpisów, wyniki poprzednich uruchomień i stan produkcyjnej strony Sites (numer wersji, status wdrożenia i tryb dostępu). Sprawdź, czy istnieje zaległa publikacja; nie twórz duplikatu.
2. Sprawdź wiarygodne źródła, zaczynając od dokumentów instytucji, a następnie niezależne media. Obejmuj zdarzenia od 30 października 2026. Weryfikuj bezpośrednie adresy i daty źródeł. Nie wymyślaj danych, cytatów ani godzin.
3. Oddziel fakty, relacje, opinie i kwestionowane twierdzenia. Przy ważnych twierdzeniach szukaj niezależnego potwierdzenia; brak potwierdzenia oznacz. Zapisz rozbieżności i krótkie cytaty z autorstwem.
   Przy każdym przeglądzie sprawdź także nowe opinie prawne i stanowiska stron. Powiąż wypowiedź z konkretnym wydarzeniem, podaj autora i źródło. W dzienniku odnotuj wynik sprawdzenia również wtedy, gdy nie dodano opinii.
4. Porównaj z istniejącymi wpisami, połącz źródła dotyczące tego samego zdarzenia; dopisuj nowe fakty i zachowuj historię zmian oraz widoczne sprostowania. Podaj odrębnie czas zdarzenia, publikacji źródła i zmiany serwisu, jeśli znany.
   Przy każdym przeglądzie wróć do wcześniejszych zapowiedzi. Sprawdź, czy działanie się odbyło, odwołano je lub opublikowano rezultat. Uzupełnij istniejący wpis i połącz go z późniejszym dokumentem. Rozróżniaj wejście na teren posesji i wejście do budynku. Nie utożsamiaj daty publikacji relacji z datą zdarzenia.
5. Bez istotnych nowych danych nie twórz wiadomości. Zapisz czas sprawdzenia i wynik, wyraźnie odróżniając go od czasu zmiany treści. Przed zapisem sprawdź bieżący SHA gałęzi, unikaj nadpisania cudzych zmian.
6. Publiczna strona produkcyjna działa od wersji 9. Po zmianie treści przygotuj kolejną wersję. Wdróż ją po odrębnej zgodzie właściciela na publikację tej wersji. Zachowaj dotychczasowy dostęp i historię. Potwierdź wersję oraz widoczność zmiany; w razie błędu zapisz zaległą publikację i ponów bez duplikowania. Nie twierdź, że publikacja się powiodła bez dowodu.
7. Raportuj rzeczywisty wynik każdego etapu, źródła, błędy i ograniczenia. Nie upubliczniaj witryny i nie twórz harmonogramu cyklicznego bez odrębnej zgody.

## Próba integracyjna
Historyczna procedura dla prywatnego demo. Nie wykonuj zmiany testowej na publicznej stronie. W teście jednorazowym wpisz do `data/test.json` wynik odczytu i zapisu, a na prywatnej demonstracji wykonaj wyraźnie oznaczoną niewielką zmianę testową, jeżeli dostęp i aktualne dane na to pozwalają. Zapisz dowody i porównaj stan GitHub oraz wdrożenia. Nie przedstawiaj danych testowych jako wiadomości.
