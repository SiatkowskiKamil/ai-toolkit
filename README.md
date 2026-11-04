# ai-toolkit

Prompty i skille do pracy z Claude, których faktycznie używam, każdy z notatką,
kiedy i do czego był wykorzystywany.

```
prompts/   pojedyncze prompty, jeden plik = jeden prompt
skills/    skille w formacie Claude Skills, gotowe do wgrania
```

## Zasada

Trafia tu tylko to, co zrozumie ktoś z zewnątrz. Prompty z pracy prawie zawsze
mają w środku nazwy systemów, identyfikatory pól albo przykłady na prawdziwych
danych — takie zostają tam, gdzie powstały. To repozytorium jest publiczne.

## Jak korzystać

**Prompty** — otwórz plik, skopiuj blok kodu, wklej. Każdy ma opis sytuacji,
w której działa, i przykład tego, co z niego wychodzi.

**Skille** — każdy folder zawiera `SKILL.md` z nagłówkiem `name` i `description`.
Taki folder można spakować i wgrać do Claude bez żadnych przeróbek; `description`
decyduje o tym, kiedy Claude po skill sięgnie, więc to w nim jest cała robota.
