# Dashboard postępów — raport skumulowany
Okres: {{period_start}} -> {{period_end}} | Liczba rozmów: **{{sessions_count}}**

## 1) Trend ogólny
- Średnia z okresu: **{{global_avg}}/10**
- Trend: **{{trend_label}}**

```text
Sesje:  01 02 03 04 05 06 07 08 09 10
Wynik:  {{sparkline_scores}}
```

## 2) Kryteria (0-4) — zmiana vs poprzedni okres
```text
Trafność      {{dot_trafnosc}} {{avg_trafnosc}}  (Δ {{delta_trafnosc}})
Walidacja     {{dot_walidacja}} {{avg_walidacja}}  (Δ {{delta_walidacja}})
Granice       {{dot_granice}} {{avg_granice}}  (Δ {{delta_granice}})
Współpraca    {{dot_wspolpraca}} {{avg_wspolpraca}}  (Δ {{delta_wspolpraca}})
Język wieku   {{dot_jezyk}} {{avg_jezyk}}  (Δ {{delta_jezyk}})
```

## 3) Heatmapa kategorii scenariuszy
```text
ekrany               {{cat_ekrany_score}}  {{cat_ekrany_level}}
poranek/szkoła       {{cat_szkola_score}}  {{cat_szkola_level}}
rodzeństwo/zazdrość  {{cat_rodzenstwo_score}}  {{cat_rodzenstwo_level}}
jedzenie             {{cat_jedzenie_score}}  {{cat_jedzenie_level}}
granice              {{cat_granice_score}}  {{cat_granice_level}}
```

## 4) Co wzmacniać / co ograniczać
- Top 3 dobre reakcje:
  1. {{good_1}}
  2. {{good_2}}
  3. {{good_3}}
- Top 3 ryzyka:
  1. {{risk_1}}
  2. {{risk_2}}
  3. {{risk_3}}

## 5) Plan na następne 5 rozmów
- Priorytet #1: {{priority_1}}
- Priorytet #2: {{priority_2}}
- Priorytet #3: {{priority_3}}
