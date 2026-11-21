# Moduły Computer Vision

| Moduł | Odpowiedzialność | Status |
| --- | --- | --- |
| `lib_vis.capture` | Źródła obrazów, sekwencje i strumienie wideo | PLANNED |
| `lib_vis.formats` | Dekodowanie i konwersje formatów obrazu | PLANNED |
| `lib_vis.transforms` | Skalowanie, kadrowanie, normalizacja i przekształcenia | PLANNED |
| `lib_vis.calibration` | Parametry kamer, dystorsja, geometria projekcji | PLANNED |
| `lib_vis.features` | Cechy i punkty kluczowe obrazu | PLANNED |
| `lib_vis.detection` | Detekcja obiektów i pozycji w pojedynczej klatce | PLANNED |
| `lib_vis.segmentation` | Segmentacja semantyczna lub instancyjna jednej klatki | PLANNED |
| `lib_vis.geometry` | Geometria 2D/3D, głębia i przepływ optyczny | PLANNED |
| `lib_vis.quality` | Jakość obrazu, artefakty i kompletność | PLANNED |
| `lib_vis.sync` | Znaczniki czasu, kolejność i buforowanie | PLANNED |

Kolejność implementacji nie wymaga jednoczesnego wsparcia wszystkich modułów. Podstawą jest jednoznaczny model `Frame` i `CoordinateFrame`. Detekcja i segmentacja generują obserwacje, które mogą trafiać do `lib-track`. `lib-vis` nie przydziela stałych identyfikatorów obiektom w kolejnych klatkach. Wsparcie VLM pozostaje w `lib-vlm`.

[Kontrakty](../contracts.md) są projektowane, niezaimplementowane.
