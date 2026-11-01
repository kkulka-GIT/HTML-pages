# Kafelki Wiedzy Monitora TK — eksperyment 0.1

Status: materiał do review, nie model produkcyjny i nie wsad do istniejącego importera D1.

Zapis na podstawie dwóch publicznych stron Monitora odczytanych 1 listopada 2026 r. i porównanych bajt po bajcie ze źródłami Sites. Stan treści deklarowany przez Monitor: 1 listopada 2026, 07:11 czasu polskiego. SHA-256 stron i commit źródłowy znajdują się w `manifest.json`. Jest to model treści Monitora, **nie niezależne potwierdzenie opisanych wydarzeń ani opinii prawnych**. Przygotowano z pomocą AI.

## Układ

- `events.json`: 9 relacji o wydarzeniach, 2 zapowiedzi, 4 jednostki tła historycznego.
- `positions.json`: 10 stanowisk i 6 opinii. To wypowiedzi przypisane autorom, nie rozstrzygnięcia modelu.
- `context.json`: 3 opisy dokumentów, 3 pytania otwarte, podsumowanie i metodologia.
- `entities.json`: 30 osób i 8 instytucji jako indeks wystąpień, bez dodawania biografii.
- `sources.json`: 52 unikalne adresy materiałów przywołanych przez Monitor, z oryginalnymi etykietami. Ten rejestr nie jest liczony jako kafelki.
- `tiles.schema.json`: eksperymentalny JSON Schema Draft 2020-12 dla czterech zbiorów kafelków.
- `manifest.json`: pochodzenie, wersja i statystyka zbioru.
- `validation.json`: wyniki lokalnej kontroli i jawna lista pominiętych akapitów.

Łącznie **77 kafelków i 103 relacje**. Zbiory tematyczne ograniczają liczbę plików, zachowując samodzielne rekordy. Nie są dostosowane do obecnych tabel D1.

## Kafelek

`id` jest trwałym identyfikatorem, niezależnym od pozycji w tablicy. Przy pierwszym utworzeniu oparto go na kotwicy Monitora lub nazwie jednostki; po review nie należy regenerować go przy zmianie tytułu/nazwiska. Zmiana treści aktualizuje rekord pod tym samym ID. Podział/scalenie wymaga w przyszłości jawnej mapy następstwa, a nie cichego recyklingu ID.

`type` określa rodzaj jednostki. `title` i tablica `content` przechowują tytuł oraz akapity, bez przekształcania ich w nowe ustalenia. Teksty zachowują zastrzeżenia, a białe znaki zostały znormalizowane. Skrócone mobilne kopie tych samych akapitów pominięto.

`epistemic` określa sposób odczytania całego kafelka: relacja, przypisane twierdzenie/interpretacja, opis dokumentu, pytanie otwarte, synteza redakcyjna lub indeks podmiotu. Nie jest wynikiem oceny wiarygodności. Relacja prasowa może zawierać zarówno informację o wypowiedzi, jak i sporne twierdzenie jej autora; atrybucja i zastrzeżenia pozostają w tekście. Nie utożsamiać `reported_information` z bezspornym faktem.

`dates` rozróżnia koszyk chronologii Monitora (`monitor_timeline_bucket`), datę dokumentu i termin zapowiedziany (`scheduled_event`). Dla Zgromadzenia Ogólnego jawnie rozdzielono datę zarządzenia 30 października, wpis 31 października i zapowiedź 3 listopada. Pusta tablica oznacza brak normalizacji dat, nie brak dat w materiale. Oryginalne opisy czasu pozostają w treści i etykietach. Nie przypisano godzin publikacji zdarzeniom. Data snapshotu nie jest datą zdarzenia.

`source_ids` wskazuje rejestr adresów. ID źródła utworzono jako `src-` i pierwsze 16 znaków SHA-256 dokładnego URL; przy zmianie URL zachować stary wpis i dodać nowy lub w przyszłości alias. Nie zakładać, że dwa adresy są niezależnymi potwierdzeniami. U osób/instytucji źródła są sumą odnośników z kafelków, w których występują, nie źródłami biografii.

`provenance` wskazuje stronę, selektor miejsca pochodzenia, snapshot i metodę ekstrakcji. Selektor jest lokalizatorem dla tej wersji strony, nie trwałym ID. Etykieta `independent_fact_check: false` dotyczy tego eksperymentu; nie usuwa deklaracji wcześniejszych kontroli zapisanych w Monitorze.

## Relacje

- `comments_on`: opinia lub stanowisko umieszczone pod konkretnym wpisem Monitora.
- `references`: jawny link Monitora do innej wydzielonej jednostki.
- `mentions`: jawna nazwa lub skrót w tytule/treści; nie oznacza uczestnictwa ani sprawstwa.
- `same_subject_as`: dwie prezentacje tej samej opinii Matczaka; nie dwa niezależne potwierdzenia.

Relacje są skierowane i mają pole `basis`. Nie zapisujemy automatycznie ich odwrotności. Np. `tk-ocena-korwin` komentuje `tk-zarzadzenia`, a wpis o zarządzeniach odsyła do kafelka dokumentów `tk-dokumenty-przerwa-w-czynnosciach`. Relacje osób z materiałami są obecnie ostrożnym indeksem, nie grafem urzędów.

## Zakres i luki

Przeniesiono wszystkie 13 wpisów chronologii, 14 zagnieżdżonych ocen/stanowisk, 3 karty dokumentów, 3 pytania sporne, 4 historyczne sekcje oraz podsumowanie i metodologię. Zachowano 55 z 62 sprawdzonych akapitów `main` (po wyłączeniu kopii mobilnych i komunikatu pustych filtrów). Pozostałe wymieniono w `validation.json`: opis serwisu, metadane czasu (zapisane również w manifeście), pusty akapit, informacja nawigacyjna i wstępne dwuzdaniowe streszczenie historii. Zasadnicze rozwinięcie historii zachowano w całości.

Nie pobierano pełnych tekstów dokumentów zewnętrznych, PDF ani nagrań. Informacja o niepotwierdzonym odczycie skanów TK została zachowana. Źródła to wskazania z Monitora; ich aktualnej dostępności i treści nie zweryfikowano ponownie. Nie modelowano wyglądu, nawigacji, filtrów ani indeksu opinii jako dodatkowych faktów. Nie dopisano bieżących wiadomości spoza snapshotu.

## Kontrola

Sprawdzono składnię wszystkich JSON-ów, schemat czterech zbiorów, formaty dat/URI, niepuste wymagane pola, unikalność ID i URL, istnienie celów wszystkich relacji, odwołania do źródeł i pokrycie akapitów. Wynik: `validation.json`.

Minimalna ponowna walidacja (Python z pakietem `jsonschema`, uruchomiony w tym katalogu):

```python
import json
from pathlib import Path
from jsonschema import Draft202012Validator, FormatChecker
read = lambda name: json.loads(Path(name).read_text(encoding='utf-8'))
m = read('manifest.json')
v = Draft202012Validator(read('tiles.schema.json'), format_checker=FormatChecker())
tiles = []
for name in m['tile_files']:
    data = read(name)
    v.validate(data)
    tiles.extend(data['tiles'])
ids = [t['id'] for t in tiles]
assert len(ids) == len(set(ids))
sources = read('sources.json')['sources']
sids = {s['id'] for s in sources}
assert len(sids) == len(sources) == len({s['url'] for s in sources})
for tile in tiles:
    assert set(tile['source_ids']) <= sids
    for rel in tile['relations']:
        assert rel['target_id'] in ids and rel['target_id'] != tile['id']
assert len(tiles) == m['tile_count']
assert sum(len(t['relations']) for t in tiles) == m['relation_count']
print('OK')
```

Schemat nie kontroluje globalnych odwołań — robią to dodatkowe asercje. Nie ma jeszcze odrębnych schematów rejestru źródeł/manifesta ani walidacji merytorycznej.

## Pytania do następnego review

1. Czy rozbić wielowątkowe wpisy (wizyta prezydenta, konsultacje, nagranie kluczy) na osobne zdarzenia i twierdzenia? Obecnie priorytetem było zachowanie treści i jej kontekstu.
2. Czy każdemu twierdzeniu przypisać osobne źródło, autora i status? To precyzyjniejsze niż wspólny zestaw źródeł całego kafelka, lecz wymaga redakcyjnego review.
3. Rozdzielić dokument od jego opisu i publikacji; obecna karta skanów zawiera dwa zarządzenia. Ujednolicić daty zdarzenia, publikacji, obowiązywania i aktualizacji, z zakresem i niepewnością.
4. Rozszerzyć relacje po ręcznej ocenie o `issued_by`, `signed_by`, `contradicts` i role z czasem obowiązywania. Nie wyciągać ich wyłącznie z wystąpienia nazwiska.
5. Rozważyć wariant atomowy: osobne encje, zdarzenia, dokumenty i przypisane twierdzenia; kafelek prezentacyjny byłby wtedy widokiem wielu rekordów. Na tym etapie nie wybieramy rozwiązania docelowego.
6. Dodać wersjonowanie treści, historię korekt i reguły deduplikacji między źródłami. Git przechowuje historię plików, ale nie zastępuje semantycznej historii twierdzeń.

## Izolacja eksperymentu

Pliki utworzono wyłącznie w `knowledge/monitor-tk/` na `main`. Nie zmieniono `knowledge/d1-import-lab.json`, workflow, gałęzi `monitor-tk`, Sites ani D1. Nie wywołano endpointu importu. Istniejący workflow importu ma filtr wyłącznie na plik testowy; ten katalog nie jest jego wejściem. Publikacja tych plików w GitHub nie jest wdrożeniem modelu do usług.


## Plan przyszłych aktualizacji i migracji — notatka robocza (1 listopada 2026)

**Decyzja na obecnym etapie:** Monitor TK pozostaje głównym, redakcyjnie aktualizowanym źródłem opublikowanej treści. Kafelki Wiedzy są eksperymentalnym, pochodnym indeksem wersji Monitora, a nie drugim niezależnym systemem redakcyjnym. Nie zmieniać z tego powodu bieżącego promptu aktualizacji strony, publikacji Sites ani istniejącego importu D1.

**Zadanie do rozważenia po każdej kolejnej aktualizacji Monitora (jeszcze nie automatyzować):**
- Odczytać konkretną, zakończoną wersję Monitora oraz jej identyfikator/commit, czas aktualizacji i dostępne źródła.
- Porównać ją z wersją Monitora, na podstawie której powstał poprzedni zestaw JSON. Ustalić, które fragmenty dodano, poprawiono, usunięto lub przeniesiono.
- Na tej podstawie zaproponować dodanie, zmianę, oznaczenie jako nieaktualne albo zachowanie kafelków. Nie wykonywać ponownego niezależnego researchu w celu „uzupełnienia” JSON-ów. Każde nowe twierdzenie musi wynikać z określonego fragmentu wersji Monitora; brakujące informacje oznaczać jako brak, a nie zgadywać.
- Zachować stabilne ID, źródłowe lokalizatory fragmentów, identyfikator snapshotu, historię zmian i powiązania. Przy podziale/scaleniu zapisać jawne następstwo identyfikatorów; nie usuwać po cichu historii korekt.
- Wygenerować raport różnic: dodane/zmienione/wycofane kafelki, zmiany relacji i źródeł, nieodwzorowane fragmenty strony, miejsca niejednoznaczne wymagające review. Uruchomić walidację schematu i odwołań oraz kontrolę zgodności z opublikowaną wersją Monitora.
- Dopiero po review zdecydować, czy przyjąć nową wersję JSON. Samo opublikowanie Monitora nie oznacza zatwierdzenia nowych kafelków.

**Granica zgodności:** nie oczekujemy identycznego brzmienia narracji i pól strukturalnych, ale wymagamy identyfikowalnego pochodzenia każdego twierdzenia z konkretnej wersji Monitora. Nie można zagwarantować zgodności semantycznej samą walidacją JSON; potrzebna jest kontrola merytoryczna. Indeks nie powinien zawierać informacji wykraczających poza treść i źródła przypisane do tej wersji Monitora.

**Przygotowanie do ewentualnej migracji:** zachować manifesty wersji, mapę identyfikatorów, historię zmian, reguły ekstrakcji, wyniki walidacji i listę nierozstrzygniętych problemów. Nie zakładać dziś, że JSON stanie się źródłem strony lub że jego schemat odpowiada przyszłemu D1. Przed migracją wykonać próbę na jednej aktualizacji i sprawdzić odtwarzalność, kompletność oraz zgodność. Migracja wymaga odrębnej decyzji i planu, nie wynika automatycznie z tej notatki.

**Status:** propozycja procesu do przetestowania; bez zmian w Actions, Sites, D1 i bieżącym procesie publikacji.
