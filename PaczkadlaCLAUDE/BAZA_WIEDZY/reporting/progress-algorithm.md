# Algorytm oceny postępów (sesja + skumulowany)

## A. Metryki bazowe
- `score_turn` (0-10) = wynik tury po wagach kryteriów.
- `score_session` = średnia z tur.
- `score_criteria_avg` = średnia każdej cechy 0-4.

## B. Metryki skumulowane
- `sessions_count` = liczba zarejestrowanych rozmów.
- `global_avg` = średnia `score_session`.
- `rolling_5` = średnia z ostatnich 5 rozmów.
- `trend_slope` = nachylenie prostej regresji dla ostatnich 10 wyników.

Interpretacja trendu:
- `trend_slope >= +0.08` => „rosnący”
- `-0.08 < trend_slope < +0.08` => „stabilny”
- `trend_slope <= -0.08` => „spadkowy”

## C. Indeks postępu
`progress_index = 0.45*global_avg + 0.35*rolling_5 + 0.20*consistency`

Gdzie:
- `consistency = 10 - std_dev(last_10_scores)` (clamp 0..10)

## D. Ocena obszarów do pracy
Dla każdego kryterium 0-4:
- `>= 3.2` => mocna strona
- `2.4 .. 3.19` => stabilne, rozwijać
- `< 2.4` => priorytet treningowy

## E. Wizualizacje tekstowe
- Kropki: `●` = 0.5 punktu (skala 0-4).
- Kolumny tur: `█` = 0.5 punktu (skala 0-10).
- Sparkline trendu: `▁▂▃▄▅▆▇█` mapowane na wynik sesji.

## F. Reguły rekomendacji
- Jeśli 2 kolejne sesje mają spadek i to samo kryterium < 2.4 => ustaw to kryterium jako Priorytet #1.
- Jeśli kryterium > 3.2 przez 5 sesji => dodaj nową trudność scenariusza.
- Co 5 rozmów generuj raport skumulowany; co 1 rozmowę raport sesyjny.
