# STAN GRY — Child Conversation Trainer
Data aktualizacji: 2026-11-06
Status: W TRAKCIE (fundament i raportowanie gotowe, silnik decyzyjny częściowo gotowy)

## 1) Etap projektu
Projekt jest na etapie:
- domknięcia założeń metodycznych,
- wdrożenia warstwy raportowania v1/v2,
- przygotowania struktury danych do zapisu sesji,
- przygotowania playbooka i skilli projektowych.

Nie jest jeszcze zakończony etap:
- pełnej implementacji silnika „drzewa scenariuszowego” (HSM + reguły przejść) jako wykonywalnego modułu,
- uzupełnienia 30 scenariuszy o kompletne reakcje `reactions[]`.

## 2) Co zostało stworzone
### Skille i playbook
- C:\Skill\child-conversation-intake-skill.md
- C:\Skill\child-conversation-writing-plan-skill.md
- C:\Skill\child-conversation-project-playbook.md
- C:\Skill\README.md

### Raportowanie v1
- C:\Skill\reporting\session-data-schema.yaml
- C:\Skill\reporting\session-report-template.md
- C:\Skill\reporting\progress-dashboard-template.md
- C:\Skill\reporting\progress-algorithm.md

### Raportowanie v2
- C:\Skill\reporting\v2\text-radar-template.md
- C:\Skill\reporting\v2\scenario-ranking-template.md
- C:\Skill\reporting\v2\storage-model.md

### Przykłady raportów
- C:\Skill\reporting\examples\session-report-example.md
- C:\Skill\reporting\examples\cumulative-dashboard-example.md

### Dane (model zapisu bez DB)
- C:\Skill\data\sessions\SESSION_2026-11-06_001.yaml
- C:\Skill\data\aggregates\progress-summary.json
- C:\Skill\data\aggregates\scenario-ranking.json

## 3) Założenia merytoryczne już ustalone
- Grupy wiekowe: 7-9 oraz 10-12.
- Tryb główny: feedback po każdej odpowiedzi użytkownika.
- Ocena wielokryterialna (co dobre + co poprawić + mikro-krok).
- Komenda „Mój przypadek” (praca na realnej sytuacji użytkownika).
- Cel katalogu: 30 scenariuszy (dynamiczne przebiegi jak w grze).

## 4) Co zostało do wykonania (najbliższe kroki)
1. Dokończyć spec silnika reakcji i przejść fazowych (wykonywalne reguły).
2. Utworzyć katalog 30 scenariuszy z pełnym `state_init`, `focus_weights` i `reactions[]`.
3. Zaimplementować generator raportów, który czyta `data/sessions/*` i automatycznie aktualizuje agregaty.
4. Dodać walidację jakości: spójność ocen, stabilność trendu, wykrywanie regresu.
5. Rozpocząć serię sesji testowych (min. 10) dla kalibracji skali.

## 5) Decyzja architektoniczna (ważne)
- Na tym etapie nie jest wymagana baza danych.
- Zapis plikowy YAML/JSON jest wystarczający i prostszy operacyjnie.
- Migracja na SQLite/PostgreSQL dopiero przy dużej skali (wielu użytkowników / dashboard online).

## 6) Ryzyka
- Bez kompletu `reactions[]` system będzie zbyt szablonowy.
- Bez automatycznego generatora agregatów raporty będą ręczne.
- Bez kalibracji na realnych sesjach możliwe rozjazdy punktacji między scenami.

## 7) Definicja „gotowe v1”
V1 uznajemy za gotowe, gdy:
- działa 30 scenariuszy w 2 grupach wiekowych,
- każdy scenariusz ma dynamiczne warianty reakcji,
- raport sesyjny i skumulowany generują się automatycznie,
- użytkownik dostaje jednoznaczny plan rozwoju po każdej sesji.
