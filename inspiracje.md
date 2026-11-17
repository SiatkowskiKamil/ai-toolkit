# Inspiracje

Cudze prompty i skille, z których korzystam. Nie są tu skopiowane — są linki do
oryginałów, bo tam są aktualizowane i tam należy im się ruch. Moja część to
notatka, do czego tego użyłem i co z tego wyszło.

| Co | Autor | Do czego mi się przydało |
|---|---|---|
| [ponytail](https://github.com/DietrichGebert/ponytail) | Dietrich Gebert | Plugin do Claude Code, który hamuje dopisywanie zbędnego kodu: każe najpierw sięgnąć po bibliotekę standardową i natywne funkcje, a każdy skrót oznacza komentarzem `ponytail:`. Instalacja (dwa osobne polecenia w Claude Code, wymaga `node` w PATH):<br>`/plugin marketplace add DietrichGebert/ponytail`<br>`/plugin install ponytail@ponytail`<br>W praktyce kodu faktycznie powstaje mniej, a ponieważ każda kolejna iteracja pracuje na mniejszym kodzie, realnie spada też zużycie tokenów. |
| [pptx](https://github.com/anthropics/skills/tree/main/skills/pptx) | Anthropic | Tworzy, czyta i poprawia prezentacje PowerPoint. Instalacja (w terminalu):<br>`npx skills add anthropics/skills --skill pptx`<br>Jeszcze nie używałem przy własnym zadaniu — uzupełnię, jak się sprawdzi. |
| [hyperframes](https://github.com/heygen-com/hyperframes/tree/main/skills/hyperframes) | HeyGen | Składa film z napisami, animacjami i muzyką z kodu HTML, bez programu do montażu. Wymaga Node.js 22+ i FFmpeg; wysyła do HeyGen sygnał użycia (da się wyłączyć), a lektor korzysta z płatnych usług. Instalacja (w terminalu):<br>`npx skills add heygen-com/hyperframes --skill hyperframes`<br>Jeszcze nie używałem przy własnym zadaniu — uzupełnię, jak się sprawdzi. |
| [frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) | Anthropic | Pilnuje, żeby strona miała własny charakter, a nie wyglądała jak kolejny szablon z AI. Instalacja (w terminalu):<br>`npx skills add anthropics/skills --skill frontend-design`<br>Jeszcze nie używałem przy własnym zadaniu — uzupełnię, jak się sprawdzi. |
| [copywriting](https://github.com/coreyhaines31/marketingskills/tree/main/skills/copywriting) | Corey Haines | Pisze teksty na stronę — główną, ofertę, cennik — i najpierw dopytuje o klienta i produkt. Instalacja (w terminalu):<br>`npx skills add coreyhaines31/marketingskills --skill copywriting`<br>Jeszcze nie używałem przy własnym zadaniu — uzupełnię, jak się sprawdzi. |
| [grill-me](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me) | Matt Pocock | Wypytuje o plan runda po rundzie, aż wszystko będzie jasne — zanim AI zacznie budować. Sam `grill-me` tylko przekazuje pracę do `grilling`, dlatego instaluje się oba. Instalacja (w terminalu):<br>`npx skills add mattpocock/skills --skill grill-me --skill grilling`<br>Jeszcze nie używałem przy własnym zadaniu — uzupełnię, jak się sprawdzi. |

## Jak to uzupełniam

Trzecia kolumna jest tu najważniejsza. Sama lista linków istnieje już w setkach
egzemplarzy; wartość dokłada dopiero zdanie o tym, że coś zadziałało przy
konkretnym zadaniu albo że zawiodło i dlaczego.

Jeżeli zmieniłem cudzy prompt na tyle, że to już moja wersja — trafia do
`prompts/` jako mój plik, z linkiem do pierwowzoru w sekcji *Uwagi*.
