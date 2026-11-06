# Storage model v2 — gdzie zapisywać wyniki

## Czy trzeba bazę danych?
Nie na start.

Dla v1/v2 wystarczy zapis plikowy (YAML/JSONL/Markdown), bo:
- łatwo wersjonować,
- łatwo przeglądać ręcznie,
- zero kosztu utrzymania.

## Struktura zapisu
- `data/sessions/SESSION_YYYY-MM-DD_NNN.yaml` — pełny rekord jednej rozmowy.
- `data/aggregates/progress-summary.json` — liczby skumulowane i trendy.
- `data/aggregates/scenario-ranking.json` — ranking scenariuszy.
- `sessions/history.md` — czytelny log dla użytkownika.

## Minimalny rekord sesji
```yaml
session_id: SESSION_2026-11-06_001
date: 2026-11-06
scenario_id: S03
age_band: 7-9
difficulty: medium
score_mean_0_10: 6.8
criteria_avg:
  trafnosc: 2.5
  walidacja: 3.0
  granice: 2.0
  wspolpraca: 2.8
  jezyk_wieku: 3.5
```

## Kiedy przejść na DB
Przejdź na DB dopiero gdy:
- >1000 sesji,
- wielu użytkowników równolegle,
- potrzebne filtrowanie i dashboard online.

Wtedy najlepiej: SQLite (lokalnie) -> PostgreSQL (wielu użytkowników).
