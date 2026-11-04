# Skille

| Skill | Do czego |
|---|---|
| [`przeglad-github/`](przeglad-github/) | przegląd i porządkowanie repozytoriów: sekrety, śmieci, README, spójność nazw |
| [`przyklad-skilla/`](przyklad-skilla/) | szablon — skopiuj folder przy dodawaniu nowego |

## Format

Jeden folder na skill, w środku `SKILL.md` zaczynający się nagłówkiem YAML:

```yaml
---
name: nazwa-skilla
description: Jedno zdanie o tym, KIEDY ten skill ma zostać użyty.
---
```

`description` to nie opis zawartości, tylko warunek uruchomienia — po nim Claude
rozpoznaje, że to jest moment na ten skill. „Formatuje raporty" nie wystarczy;
„Używaj, gdy użytkownik prosi o raport miesięczny w formacie zespołu finansowego"
już tak.

Pod nagłówkiem idzie treść: instrukcje krok po kroku, zasady, przykłady. Do folderu
można dołożyć pliki pomocnicze (szablony, skrypty, przykładowe dane) i odwoływać
się do nich z `SKILL.md`.

Tak przygotowany folder pakuje się do ZIP-a i wgrywa do Claude bez przeróbek.
