# Moduły i odpowiedzialność

| Moduł | Zadanie | Ważny szczegół | Status |
| --- | --- | --- | --- |
| `lib_vis.capture` | Źródła klatek: kamery i pliki, kontrola buforów i timestampów | Otwarcie źródła wymaga jawnego device_id/URI; brak stałego zapisu w repo | PLANNED |
| `lib_vis.formats` | Dekodowanie obrazu i konwersje przestrzeni barw | MIME, format pikseli, orientacja, rozdzielczość, metadane wejścia/wyjścia | PLANNED |
| `lib_vis.transforms` | Skalowanie, kadrowanie, korekcja geometryczna i normalizacja | Zachowanie macierzy mapowania punktów i informacji o interpolacji | PLANNED |
| `lib_vis.quality` | Ocena jakości klatki i strumienia | Rozmycie, ekspozycja, kompletność klatek, jawne progi pomiarowe | PLANNED |
| `lib_vis.sync` | Znaczniki czasu, sekwencje, kolejki z ograniczeniem pamięci | Monotoniczny czas źródła i jawna niepewność synchronizacji | PLANNED |

Przetwarzanie obrazu i klatek bez inferencji językowej/VLM, estymacji ruchu ciała i sterowania urządzeniami. lib-vlm odpowiada za multimodalne modele, lib-track byłby właścicielem trackingu, a prywatny devices za konfiguracje aparatury.

Typy i wyjątki stanowią **propozycję** w [kontrakcie](../contracts.md). Nie tworzyć drugiej implementacji już dostępnego middleware lub modelu inferencji.
