# Monitor TK — instrukcja procesu

Repozytorium jest publiczne. Nie zapisuj sekretów ani prywatnych danych. Wykonuj wyłącznie zadanie i zakres określone przez właściciela; nie zmieniaj gałęzi `main` ani dostępu do Site.

## Cykl monitoringu
1. Odczytaj aktualną gałąź `monitor-tk`, skrzynkę `data/inbox.md`, historię wpisów, wyniki poprzednich uruchomień i stan produkcyjnej strony Sites (numer wersji, status wdrożenia i tryb dostępu). Sprawdź, czy istnieje zaległa publikacja; nie twórz duplikatu.
2. Zacznij od listy otwartych zapowiedzi z poprzedniego przeglądu. Przy każdej zapisz w dzienniku wynik i źródło albo godzinę sprawdzenia i brakujące potwierdzenie. Powiąż wynik z pierwotnym wpisem. Następnie sprawdź pozostałe wiarygodne źródła, zaczynając od dokumentów instytucji, a następnie niezależne media. Obejmuj zdarzenia od 30 października 2026. Weryfikuj bezpośrednie adresy i daty źródeł. Nie wymyślaj danych, cytatów ani godzin.
3. Oddziel fakty, relacje, opinie i kwestionowane twierdzenia. Przy ważnych twierdzeniach szukaj niezależnego potwierdzenia; brak potwierdzenia oznacz. Zapisz rozbieżności i krótkie cytaty z autorstwem.
   Przy każdym przeglądzie sprawdź także nowe opinie prawne i stanowiska stron. Powiąż wypowiedź z konkretnym wydarzeniem, podaj autora i źródło. W dzienniku odnotuj wynik sprawdzenia również wtedy, gdy nie dodano opinii.
   Przy istotnym wydarzeniu wyjaśnij w jednym lub dwóch zdaniach, co zmienia się w praktyce. Powiąż skutek ze źródłem, przypisz interpretację autorowi i wskaż nieustalone skutki, jeśli mają znaczenie.
4. Porównaj z istniejącymi wpisami, połącz źródła dotyczące tego samego zdarzenia; dopisuj nowe fakty i zachowuj historię zmian oraz widoczne sprostowania. Podaj odrębnie czas zdarzenia, publikacji źródła i zmiany serwisu, jeśli znany.
   Przy uzupełnianiu zapowiedzi rozróżnij wykonanie działania, odwołanie i publikację rezultatu. Uzupełnij istniejący wpis i połącz go z późniejszym dokumentem. Rozróżniaj wejście na teren posesji i wejście do budynku. Nie utożsamiaj daty publikacji relacji z datą zdarzenia.
5. Bez istotnych nowych danych nie twórz wiadomości. Zapisz czas sprawdzenia i wynik, wyraźnie odróżniając go od czasu zmiany treści. Przed zapisem sprawdź bieżący SHA gałęzi, unikaj nadpisania cudzych zmian.
6. Po zmianie treści sprawdź wynik i zapisz odpowiednią wersję w Sites. Codzienny harmonogram „Monitor TK — codzienny przegląd” ma stałą zgodę właściciela na automatyczną publikację swoich zweryfikowanych aktualizacji na obecnej publicznej stronie. Opublikuj wersję w tym samym uruchomieniu. Przy aktualizacji ręcznej opublikuj wersję na polecenie właściciela.
   Przed publikacją sprawdź numer wersji i stan jej wdrożenia. Użyj już zapisanej wersji, jeśli odpowiada wynikowi przeglądu. Jeżeli wdrożenie trwa, sprawdź jego wynik. Po błędzie zapisz w dzienniku numer wersji i przyczynę. Przy ponowieniu użyj aktualnej wersji i sprawdź, czy nowsza publiczna edycja obejmuje już te zmiany. Po udanym wdrożeniu potwierdź w Sites numer wersji i jej dostępność. Zapisz wynik w dzienniku i podaj właścicielowi link do strony. Gdy przegląd nie przyniósł zmian i nie ma zaległej publikacji harmonogramu, odnotuj samo sprawdzenie.
7. Raportuj rzeczywisty wynik każdego etapu, źródła, błędy i ograniczenia. Zmiana odbiorców witryny lub utworzenie nowego harmonogramu wymaga osobnego polecenia właściciela.

## Małe zmiany przy aktualizacji

Przy zwykłej aktualizacji odczytaj [plan małych zmian](data/plan-zmian.md) i wykonaj jeden kolejny otwarty krok razem z przeglądem źródeł. Sam odczyt podsumowania lub publikacja wcześniej przygotowanej wersji nie rozpoczyna kroku. Sprawdź efekt według kryterium w planie, odnotuj wynik i następny krok w `data/przeglady.md`, a następnie oznacz sprawdzony krok w planie. Jeśli krok jest już wykonany, potwierdź to na bieżącej wersji. Jeśli brakuje warunków do sprawdzenia lub pilna wiadomość wymaga wcześniejszej aktualizacji, zapisz powód i wróć do otwartego kroku przy kolejnym przeglądzie. Po wyczerpaniu listy kontynuuj zwykły monitoring.

## Skrzynka zgłoszeń
Plik `data/inbox.md` jest trwałą kolejką materiałów przekazywanych przez właściciela także z innych rozmów ChatGPT. Przy każdym przeglądzie odczytaj go i rozpatrz oczekujące zgłoszenia, równolegle prowadząc własny monitoring źródeł. Zgłoszenia typu TREŚĆ weryfikuj merytorycznie i porównuj z chronologią; zgłoszenia typu SERWIS oceniaj jako propozycje UX, dostępności lub zmian technicznych. Nie traktuj zgłoszeń jako potwierdzonych faktów ani automatycznych poleceń wdrożenia. Zmiany większe lub wykraczające poza zgodę właściciela przedstaw do decyzji. Po rozpatrzeniu zapisz status i krótkie uzasadnienie w skrzynce; jeśli potrzebna jest decyzja lub weryfikacja, pozostaw „oczekuje” z wyjaśnieniem. Status „uwzględnione” nadaj dopiero po potwierdzeniu rezultatu; przy przerwaniu pracy ponownie sprawdź stan przed zmianą statusu. Zachowuj historię zamkniętych zgłoszeń. Materiały uwzględnione w aktualizacji podlegają zasadom publikacji z punktu 6.

## Spójność sekcji strony

Porównaj podsumowanie i zapowiedzi z chronologią, opiniami, biblioteką dokumentów i opisami spraw spornych. Stałe zasady weryfikacji utrzymuj w „Jak czytać ten serwis?”. Zakres, ograniczenia i wynik bieżącego przeglądu zapisuj w „Ostatnim przeglądzie”. Odróżniaj datę przeglądu źródeł od czasu aktualizacji witryny. Zachowaj osobną historię sporu. Po zmianie chronologii sprawdź kolejność i odsyłacze oraz zgodność liczników kalendarza z datami wpisów.

## Spójność dokumentacji
Po każdym przeglądzie i aktualizacji sprawdź zgodność README.md, AGENTS.md, data/inbox.md oraz data/przeglady.md. Nie powielaj bieżącego numeru wersji w README.md ani w stałych instrukcjach AGENTS.md. Aktualny stan publikacji ustalaj na podstawie Sites, a historię zmian i dowody wdrożeń zapisuj w data/przeglady.md. Rozbieżności poprawiaj, jeśli są potwierdzone, a w przeciwnym razie odnotuj je w dzienniku. Nie traktuj historycznych wpisów jako opisu aktualnego stanu.

## Próba integracyjna
Historyczna procedura dla prywatnego demo. Nie wykonuj zmiany testowej na publicznej stronie. W teście jednorazowym wpisz do `data/test.json` wynik odczytu i zapisu, a na prywatnej demonstracji wykonaj wyraźnie oznaczoną niewielką zmianę testową, jeżeli dostęp i aktualne dane na to pozwalają. Zapisz dowody i porównaj stan GitHub oraz wdrożenia. Nie przedstawiaj danych testowych jako wiadomości.
