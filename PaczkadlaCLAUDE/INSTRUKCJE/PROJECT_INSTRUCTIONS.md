---
name: child-conversation-project-playbook
description: Playbook operacyjny łączący intake + plan + wykonanie dla projektu treningu rozmowy z dzieckiem z mechanizmem oceniania.
version: 1.1.0
based_on:
  - spec-interview.md
  - skill-creator.md
  - superpowers/brainstorming
  - superpowers/writing-plans
---

# Child Conversation Project Playbook

## Workflow (5 faz)
1. **Discovery (Intake)** — domknij założenia i zakres.
2. **Planning** — zaplanuj etapy, pliki, kryteria done.
3. **Build & Iterate** — buduj scenariusze i testy jakości.
4. **Report per session** — mini raport po każdej sesji.
5. **Cumulative review** — raport trendów co 5 sesji.

## Minimalny zestaw plików wiedzy
- `core/system-instructions.md`
- `core/interaction-protocol.md`
- `core/safety-and-boundaries.md`
- `docs/evaluation-rubric-child.md`
- `docs/child-development-guidelines.md`
- `scenarios/catalog.yaml`
- `scenarios/*.md`
- `sessions/session-template.md`
- `state/current-progress.md`
- `reporting/session-data-schema.yaml`
- `reporting/session-report-template.md`
- `reporting/progress-dashboard-template.md`

## Wymuszone reguły jakości
- Brak rubryki oceny = projekt niegotowy.
- Każdy scenariusz zawiera: cel, kwestię otwierającą dziecka, warunki sukcesu i błędy krytyczne.
- Każde podsumowanie sesji zawiera: mocne strony, ryzyka, 1 mikro-nawyk.
- Raport skumulowany pokazuje: liczbę rozmów, trend ocen i obszary priorytetowe.

## Definicja sukcesu projektu
Projekt jest gotowy, gdy:
1. Działa co najmniej 30 scenariuszy dla 2 grup wiekowych.
2. Rubryka oceny daje stabilne wyniki między sesjami.
3. Użytkownik dostaje jednoznaczny feedback i plan kolejnego ćwiczenia.
4. Dashboard trendów pokazuje poprawę lub jasno wskazuje obszar zastoju.
