# Raport sesji — {{session_id}}
Data: {{date}} | Scenariusz: {{scenario_title}} ({{scenario_id}}) | Wiek: {{age_band}} | Trudność: {{difficulty}}

## 1) Wynik sesji
- Średnia: **{{score_mean_0_10}}/10**
- Liczba tur: **{{turns_count}}**
- Poziom sesji: {{level_label}}

### Wykres kolumnowy (tury)
```text
T1 {{bar_t1}} {{score_t1}}
T2 {{bar_t2}} {{score_t2}}
T3 {{bar_t3}} {{score_t3}}
T4 {{bar_t4}} {{score_t4}}
T5 {{bar_t5}} {{score_t5}}
```

## 2) Ocena kryteriów (średnie 0-4)
```text
Trafność      {{dot_trafnosc}} {{avg_trafnosc}}
Walidacja     {{dot_walidacja}} {{avg_walidacja}}
Granice       {{dot_granice}} {{avg_granice}}
Współpraca    {{dot_wspolpraca}} {{avg_wspolpraca}}
Język wieku   {{dot_jezyk}} {{avg_jezyk}}
```

## 3) Co działało
- {{strong_1}}
- {{strong_2}}

## 4) Co ryzykowne
- {{risk_1}}

## 5) Jeden mikro-nawyk na kolejną sesję
- {{micro_habit_next}}

## 6) Lepsze wersje (najważniejsze)
- Oryginał: "{{raw_line_1}}"
- Lepsza wersja: "{{better_line_1}}"
