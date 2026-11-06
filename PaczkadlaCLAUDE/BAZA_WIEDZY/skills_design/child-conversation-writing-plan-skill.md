---
name: child-conversation-writing-plan
description: Zamienia doprecyzowane założenia w plan wdrożenia projektu trenażowego rozmowy z dzieckiem (struktura plików, kolejność pracy, kryteria gotowości).
version: 1.0.0
based_on:
  - spec-interview.md
  - skill-creator.md
  - superpowers/writing-plans
---

# Child Conversation Writing Plan Skill

## Cel
Po fazie wywiadu przygotuj egzekwowalny plan budowy projektu, krok po kroku, z artefaktami i kryteriami akceptacji.

## Wejście
- Ustalone założenia projektu.
- Dostępne materiały źródłowe.
- Preferencje użytkownika (tempo, szczegółowość, styl oceny).

## Wyjście
Plan zawierający:
1. Etapy realizacji.
2. Konkretne pliki do utworzenia/uzupełnienia.
3. Definicję „done” dla każdego etapu.
4. Kolejność testów jakości.

## Szablon planu
### Etap 1 — Fundament
- `README-projektu.md`
- `core/system-instructions.md`
- `core/safety-and-boundaries.md`

### Etap 2 — Ocena i metryki
- `docs/evaluation-rubric-child.md`
- `docs/feedback-format.md`
- `tests/evaluation-cases.md`

### Etap 3 — Scenariusze
- `scenarios/catalog.yaml`
- `scenarios/01...md` do `scenarios/05...md`

### Etap 4 — Stan i historia
- `state/current-progress.md`
- `sessions/session-template.md`
- `sessions/history.md`

### Etap 5 — Kalibracja
- 3 sesje testowe
- analiza rozjazdu intencja vs efekt
- korekta rubryki

## Kryteria jakości planu
- Każdy etap ma cel, wynik i warunek zakończenia.
- Każdy plik ma rolę i właściciela logicznego.
- Plan nie pomija warstwy oceny (to element obowiązkowy).
- Plan jest realistyczny do wykonania iteracyjnie.
