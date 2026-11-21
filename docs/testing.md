# Strategia testów

Weryfikację przeprowadzać etapami od syntetycznych fixture do rzeczywistego środowiska; wynik szablonu nie jest dowodem obsługi urządzeń.

1. Test syntetycznych obrazów RGB/BGR/grayscale i stride.
2. Test geometrycznego odwzorowania współrzędnych po resize/crop.
3. Test monotoniczności znaczników czasu, jitter i dropped frames.
4. Test błędów pustej klatki, błędnego MIME i limitu pamięci.
5. Test integracyjny ze wskazanym urządzeniem wyłącznie po preflight.

Planowany raport powinien zawierać finalny SHA, polecenie testowe, host/runtime, parametry i jednostki, źródło danych, `PASS/FAIL/NOT_RUN`, log ograniczony do metadanych oraz ewentualną niepewność pomiarową. Testy sprzętowe tylko po preflight i z jawnie wskazanym źródłem; nie używać stałych runnerów dla niezaufanego kodu.

Kontrole obecnego szkieletu:

```bash
python scripts/validate_repository.py --phase scaffold
python scripts/validate_documentation.py
python scripts/validate_pages.py
python -m unittest discover -s tests -v
```
