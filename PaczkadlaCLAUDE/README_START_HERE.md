# Paczka dla Claude — Rozmowa z dzieckiem

## Jak użyć w Claude Project
1. Dodaj cały folder `PaczkadlaCLAUDE` do projektu.
2. Jako główną instrukcję projektu ustaw plik: `INSTRUKCJE/PROJECT_INSTRUCTIONS.md`.
3. Wszystkie pliki z `BAZA_WIEDZY/` traktuj jako kontekst pomocniczy.
4. Raporty generuj po każdej sesji i skumulowanie co 5 sesji.

## Struktura
- `INSTRUKCJE/` — pliki nadrzędne, jak model ma działać.
- `BAZA_WIEDZY/` — rubryki, algorytmy, szablony i przykładowe dane.

## Priorytet interpretacji
1. `INSTRUKCJE/PROJECT_INSTRUCTIONS.md`
2. `INSTRUKCJE/STAN-GRY.md`
3. `BAZA_WIEDZY/reporting/*`
4. `BAZA_WIEDZY/data_examples/*`

## Uwaga
To jest paczka startowa. Pliki scenariuszy (30 sztuk z reakcjami) trzeba jeszcze doszczegółowić w osobnym etapie.
