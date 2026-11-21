# Plan walidacji Computer Vision

Początkowe testy używają syntetycznych obrazów, masek i wzorców kalibracji.

1. Dekodowanie RGB/BGR/gray, stride, skala obrazu i zachowanie orientacji.
2. Resize i crop: odwracalne mapowanie współrzędnych detekcji i punktów.
3. Kalibracja kamery z syntetycznym wzorcem, błąd reprojekcji i przypadek bez kalibracji.
4. Ekstrakcja punktów kluczowych z kontrolowanego obrazu oraz granice współrzędnych.
5. Detekcje bbox/pose i poprawność danych wejściowych do `lib-track`.
6. Maska segmentacji i transformacja jej geometrii przy zmianie rozdzielczości.
7. Głębia/przepływ optyczny dla znanego przesunięcia i jakości danych.
8. Kolejność ramek, monotoniczne timestampy, dropped frames, timeout i limit pamięci.
9. E2E z rzeczywistą kamerą dopiero po weryfikacji sprzętu i uprawnień.

Raport na exact SHA musi podać metody, parametry, jednostki, wersje adapterów, źródło danych, wynik `PASS/FAIL/NOT_RUN` i ograniczenia. Testy CI szkieletu nie oznaczają zweryfikowanego działania algorytmów wizji.

```bash
python scripts/validate_repository.py --phase scaffold
python scripts/validate_documentation.py
python scripts/validate_pages.py
python -m unittest discover -s tests -v
```
