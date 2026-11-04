# ai-toolkit

Prompty i skille do pracy z Claude, których faktycznie używam, każdy z notatką,
kiedy i do czego był wykorzystywany.

```
prompts/        pojedyncze prompty, jeden plik = jeden prompt
skills/         skille w formacie Claude Skills, gotowe do wgrania
inspiracje.md   cudze rzeczy, z których korzystam — linki, nie kopie
```

## Zasada

Trafia tu tylko to, co zrozumie ktoś z zewnątrz. Prompty z pracy prawie zawsze
mają w środku nazwy systemów, identyfikatory pól albo przykłady na prawdziwych
danych — takie zostają tam, gdzie powstały. To repozytorium jest publiczne.

## Czyje to jest

W `prompts/` i `skills/` są wyłącznie moje rzeczy. Cudze trafiają do
[`inspiracje.md`](inspiracje.md) jako linki do oryginałów — tam są aktualizowane
i tam należy im się ruch.

Gdyby kiedyś znalazło się tu coś cudzego w całości, będzie leżeć w osobnym
folderze razem z licencją oryginału i nagłówkiem mówiącym, skąd pochodzi, kto
jest autorem i co zmieniłem. Podanie autora nie zastępuje licencji: bez niej
kopia pozostaje kopią bez zgody, więc wtedy linkuję albo pytam autora.

## Jak korzystać

**Prompty** — otwórz plik, skopiuj blok kodu, wklej. Każdy ma opis sytuacji,
w której działa, i przykład tego, co z niego wychodzi.

**Skille** — każdy folder zawiera `SKILL.md` z nagłówkiem `name` i `description`.
Taki folder można spakować i wgrać do Claude bez żadnych przeróbek; `description`
decyduje o tym, kiedy Claude po skill sięgnie, więc to w nim jest cała robota.
