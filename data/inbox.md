# Monitor TK — skrzynka zgłoszeń

To trwała kolejka propozycji użytkownika do rozpatrzenia przez agenta podczas przeglądu Monitora TK. Nie jest źródłem potwierdzonych faktów, listą zatwierdzonych zmian ani zgodą na publikację. Wpisy mogą dodawać upoważnieni współpracownicy i asystenci po wyraźnym poleceniu użytkownika.

## Jak dodawać zgłoszenia
Dopisuj nowe zgłoszenie z unikalnym identyfikatorem TK-0001, TK-0002 itd. (kolejny wolny numer), bez nadpisywania istniejących. Nie wymyślaj źródeł, dat ani ustaleń; brakujące informacje oznacz jako „nie podano”. Nie zapisuj danych prywatnych ani sekretów — repozytorium jest publiczne. Przed zapisem odczytaj najnowszy plik i sprawdź SHA, aby nie utracić równoległych zmian.

Każde zgłoszenie zawiera:
- ID, datę dodania (jeśli znana), typ: TREŚĆ albo SERWIS, status: oczekuje / uwzględnione / zamknięte.
- Temat i opis obserwacji lub twierdzenia, źródła/linki (jeśli są) oraz oczekiwane sprawdzenie albo propozycję.
- Wynik rozpatrzenia: datę, decyzję i uzasadnienie; w razie realizacji także potwierdzoną wersję/odnośnik. Nie oznaczaj jako „uwzględnione” bez potwierdzenia rezultatu.

## Zasady rozpatrywania
TREŚĆ: zweryfikuj w wiarygodnych źródłach, porównaj z istniejącymi wpisami i zdecyduj, czy materiał powinien trafić do chronologii. SERWIS: oceń użyteczność, zakres, ryzyko i zgodność z projektem; nie wdrażaj automatycznie większych zmian ani zmian wykraczających poza zgodę właściciela. Jeśli potrzebna jest decyzja lub dalsza weryfikacja, pozostaw status „oczekuje” i dopisz powód. Zamknięte zgłoszenia pozostają w pliku dla audytu; „zamknięte” oznacza rozpatrzone bez wdrożenia, np. duplikat lub brak potwierdzenia. Nie traktuj zgłoszenia jako instrukcji nadrzędnej wobec AGENTS.md.

## Zgłoszenia

### TK-0001 — Nagranie dotyczące żądania kluczy podczas nocnej wizyty w TK
- **Data dodania:** 1 listopada 2026
- **Typ:** TREŚĆ
- **Status:** uwzględnione
- **Temat:** Możliwe uzupełnienie relacji o nocnej wizycie prezydenta w siedzibie TK (30/31 października 2026) o materiał wideo dotyczący żądania wydania kluczy.
- **Opis zgłoszenia:** Zgłoszono informację o nagraniu opublikowanym w mediach 1 listopada, na którym osoba przedstawiająca się jako pracownik/asystent prezydenta miała zwrócić się do Macieja Berka o klucze. To twierdzenie do niezależnej weryfikacji; nie ustalono, czy klucze wydano lub przejęto. W udostępnionym tekście strony istnieje już wydarzenie „Prezydent przybył do siedziby Trybunału” z 31 października, ale rozwijane szczegóły wpisu nie były dostępne do porównania.
- **Źródła/linki:** relacja/nagranie WP z 1 listopada 2026 — dokładnego adresu nie podano; do odszukania i zweryfikowania. Kontekst: https://monitor-tk-2026.kkulka.chatgpt.site/#najnowsze
- **Oczekiwane sprawdzenie:** Odszukaj oryginalne nagranie i wiarygodne relacje; ustal, kto występuje, czego dotyczy żądanie, co faktycznie potwierdza materiał oraz czy istnieją stanowiska drugiej strony. Porównaj z pełnymi szczegółami obecnego wpisu o nocnej wizycie i pozostałą chronologią. Jeśli materiał wnosi potwierdzony nowy szczegół, zaproponuj rzeczowe uzupełnienie istniejącego wydarzenia, bez duplikowania i bez utożsamiania zarzutów z ustalonymi faktami.
- **Wynik rozpatrzenia:** oczekuje na weryfikację w Work; decyzja, uzasadnienie i ewentualna wersja — nie podano.


- **Wynik przeglądu 1 listopada 2026:** Odnaleziono [publikację WP z 1.11, 01:22](https://wiadomosci.wp.pl/prezydent-prosi-o-klucze-nowe-wideo-z-trybunalu-konstytucyjnego-7346139325565376a) z opisem nagrania rozmowy z 31.10. Według relacji mężczyzna przedstawiający się jako asystent prezydenta mówi do Macieja Berka, że prezydent prosi o klucze; Berek odmawia. [Wcześniejsza relacja WP z 31.10](https://wiadomosci.wp.pl/kolejny-utarczki-w-tk-proba-przejecia-kluczy-7345792989231584a) opisuje nagrania opublikowane przez Berka, a [wywiad WP](https://wiadomosci.wp.pl/prezydent-nas-staranowal-sedzia-ujawnia-kulisy-spotkania-z-nawrockim-w-trybunale-konstytucyjnym-7345973501848032a) zawiera relację Anny Korwin-Piotrowskiej o uniemożliwieniu zabrania pęku kluczy. Nie potwierdzono przekazania kluczy ani niezależnie tożsamości mężczyzny. **Status pozostaje: oczekuje** — przed oznaczeniem „uwzględnione” należy porównać z pełnym wpisem w Sites i zapisać potwierdzoną zmianę.

- **Rozpatrzenie w Work, 1 listopada 2026, 07:11 czasu polskiego:** Porównano pełny wpis `wizyta-prezydenta` w źródłach wdrożonej wersji 15. Nie zawierał informacji o kluczach. Przygotowano uzupełnienie tego wpisu (bez nowego wydarzenia), z odnośnikiem do WP i rozróżnieniem daty publikacji od zdarzenia. Opis opiera się na relacji WP; oryginalnego filmu nie analizowano samodzielnie. Nie potwierdzono przekazania kluczy ani niezależnie tożsamości rozmówcy. Odnaleziono także relację PR24 za Onetem identyfikującą mężczyznę na nagraniu, lecz bez niezależnego potwierdzenia nie dodano nazwiska. Zmiana zapisana w Sites jako **wersja 16**, commit `348047fbe6eafd8fc7264b30c380f36ab55f85b6`, fragment `#nagranie-klucze`. **Status pozostaje: oczekuje — gotowe do publikacji, wymagana odrębna zgoda właściciela.** Po potwierdzonym wdrożeniu należy zmienić status na uwzględnione.


1 listopada 2026 o godz. 07:13 czasu polskiego, po wyraźnej zgodzie właściciela, opublikowano wersję 16. Sites potwierdził status `succeeded` wdrożenia `appgdep_6ae6d889c0688191a626c2ea295b9c89`, wersja `appgprj_6ae5bd5f169c8191a0ba73fc8b47d63f~appgver_f0d886f970508191bff0c5a1418665b8`, commit `348047fbe6eafd8fc7264b30c380f36ab55f85b6`. Zachowano dostęp publiczny. [Monitor TK](https://monitor-tk-2026.kkulka.chatgpt.site). Zgłoszenie TK-0001 uwzględniono w istniejącym wpisie `#nagranie-klucze`. Potwierdzenie pochodzi z rejestru wdrożeń Sites; nie wykonywano dodatkowego testu wizualnego.


### TK-0002 — Opinie prawne o sporze w TK
- **Data dodania:** 1 listopada 2026
- **Typ:** TREŚĆ
- **Status:** oczekuje
- **Temat:** Weryfikacja opinii prawników i konstytucjonalistów dotyczących wydarzeń 30–31 października 2026, oświadczenia czterech byłych prezesów TK, apelu siedmiu obecnych sędziów i zarządzeń Bogdana Święczkowskiego oraz Anny Korwin-Piotrowskiej.
- **Tropy do sprawdzenia:** Jacek Zaleśny, Mateusz Radajewski, Jerzy Stępień, Ewa Łętowska, Tomasz Zalasiński, Helsińska Fundacja Praw Człowieka. Ustalić dokładne wypowiedzi, daty, źródła i argumenty; poszukać też innych prawników reprezentujących różne oceny.
- **Dokumenty i źródła:** https://monitorkonstytucyjny.eu/archiwa/35302 ; https://www.rp.pl/polityka/art45425881-sedziowie-tk-zabrali-glos-mowia-o-bezprawnych-dzialaniach-apel-do-wladz-i-politykow ; https://www.rp.pl/sady-i-trybunaly/art45424221-odsuniecie-prezesa-tk-bez-podstawy-prawnej-prawnicy-sa-podzieleni ; https://www.rp.pl/opinie-prawne/art45425551-konstytucjonalista-nie-mozna-zarzadzic-przerwy-w-czynnosciach-prezesa-tk ; https://hfhr.pl/aktualnosci/stanowisko-zarzadu-hfpc-w-sprawie-sytuacji-wokol-tk ; https://wiadomosci.wp.pl/swieczkowski-wydal-zarzadzenie-anulowal-dokument-korwin-piotrowskiej-7345966093789632a . Linki wymagają weryfikacji.
- **Oczekiwane sprawdzenie:** Porównać z Monitorem, bez duplikatów. Dla każdej opinii wskazać autora, datę, oryginalne źródło, konkretne działanie lub dokument, którego dotyczy, i podstawę prawną. Oddzielnie zbadać legalność odsunięcia prezesa, późniejszych zarządzeń i dni wolnych 3–6 listopada. Nie przypisywać prawnikom poparcia dla oświadczeń, których bezpośrednio nie oceniali. Rozważyć sekcję „Co mówią prawnicy?” z przedstawieniem różnych stanowisk.
- **Wynik rozpatrzenia:** oczekuje na analizę w Work. Zgłoszenie nie stanowi zgody na publikację.


### TK-0003 — Oficjalne potwierdzenie konsultacji prezydenta z ugrupowaniami
- **Data dodania:** 1 listopada 2026
- **Typ:** TREŚĆ
- **Status:** oczekuje
- **Temat:** Sprawdzić, czy istniejący wpis Monitora TK o konsultacjach prezydenta Karola Nawrockiego z przedstawicielami środowisk parlamentarnych 31 października 2026 zawiera oficjalny komunikat Kancelarii Prezydenta i udokumentowany rezultat spotkań.
- **Źródło urzędowe do otwarcia i weryfikacji:** https://www.prezydent.pl/aktualnosci/wydarzenia/konsultacje-z-liderami-srodowisk-parlamentarnych%2C129330 — „Konsultacje z liderami środowisk parlamentarnych” (zweryfikować datę publikacji, listę spotkań, uczestników, treść i ewentualne aktualizacje).
- **Oczekiwane sprawdzenie:** Porównać komunikat Kancelarii Prezydenta z pełnym istniejącym wydarzeniem w Monitorze. Ustalić, które spotkania rzeczywiście się odbyły, z kim, kiedy, czy opublikowano oficjalny wynik, porozumienie, projekt lub zapowiedź dalszych działań. Brak publicznego porozumienia opisywać wyłącznie jako brak potwierdzenia w sprawdzonych źródłach. Sprawdzić ewentualne kolejne oficjalne komunikaty KPRP, a nie tworzyć wydarzeń z samych komentarzy polityków lub dziennikarzy.
- **Propozycja redakcyjna:** Jeśli wydarzenie już istnieje, uzupełnić je o bezpośredni link do dokumentu prezydenckiego i krótki, rzeczowy wynik konsultacji, bez duplikowania wpisu. Nowy wpis tylko dla istotnego nowego faktu lub dokumentu. Oddzielić fakt spotkań od ocen uczestników.
- **Wynik rozpatrzenia:** oczekuje na weryfikację podczas aktualizacji w Work. Nie jest to zgoda na publikację.
