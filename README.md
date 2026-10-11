# MarkaPlan

Aplikacja do planowania rocznego budżetu marketingowego i obliczania prognozowanego zysku oraz ROI. Polski interfejs, bez backendu i kont użytkowników.

## Uruchomienie

Otwórz `MarkaPlan.html` w przeglądarce lub uruchom wersję modułową:

```sh
python3 -m http.server 8765
```

Następnie otwórz http://localhost:8765. Nie jest wymagana instalacja zależności ani budowanie aplikacji.

## Funkcje

- Edycja rocznego budżetu w PLN i kanałów marketingowych.
- Podział procentowy budżetu, walidacja i wykres.
- Oczekiwany ROI od −100%, bez górnego limitu.
- Automatyczne obliczanie inwestycji, prognozowanego zysku i ważonego ROI.
- Rozróżnienie pustego ROI i świadomie wpisanego 0%.
- Oznaczenie niepełnego lub przekroczonego podziału.
- Zapis planu w localStorage bieżącej przeglądarki.
- Responsywny układ i obsługa polskiego zapisu liczb.

## Obliczenia

Budżet kanału = budżet roczny × udział / 100.
Zysk kanału = budżet kanału × ROI / 100.
Łączny ROI = suma zysków / budżet roczny × 100.

Wyniki są prognozą opartą na założeniach użytkownika. Przy niepełnym planie prezentowane wartości są częściowe.

## Pliki

- `index.html`, `style.css`, `app.js` — interfejs aplikacji.
- `model.mjs` — parsowanie liczb i model obliczeń.
- `MarkaPlan.html` — samodzielna wersja z osadzonym CSS i JavaScript.

Czcionki są pobierane z Google Fonts; bez połączenia używane są czcionki systemowe. Dane planu pozostają w przeglądarce. Zapis przy otwieraniu samodzielnego pliku zależy od obsługi localStorage dla lokalnych plików przez przeglądarkę.
