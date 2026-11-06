# Ranking scenariuszy v2 (tempo postępu)

## Cel
Pokazać, które scenariusze najszybciej poprawiają umiejętności i które blokują postęp.

## Metryki
- `gain_per_session` = średni przyrost wyniku po każdej sesji danego scenariusza.
- `criteria_gain` = przyrost najsłabszego kryterium po sesji.
- `stability` = odchylenie wyników (niższe = stabilniej).

## Tabela rankingowa
```text
#  Scenariusz                     Gain  Stability  Najbardziej rośnie
1  S03 Nie chce iść do szkoły     +0.42   0.58     Walidacja
2  S22 Faworyzowane rodzeństwo    +0.36   0.61     Granice
3  S19 Nie odłożę telefonu        +0.29   0.74     Współpraca
...
```

## Reguła doboru kolejnej sceny
1. Weź 2 kryteria najsłabsze globalnie.
2. Wybierz scenariusz z TOP rankingu, który historycznie poprawia te kryteria.
3. Unikaj 2 razy pod rząd scen z malejącym `gain_per_session`.
