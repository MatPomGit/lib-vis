# lib-vis

**Computer vision:** biblioteka akwizycji, przetwarzania i analizy obrazów oraz strumieni wideo, obejmująca także detekcję, segmentację i geometrię komputerowego widzenia.

**Status: ARCHITECTURE_ONLY / NOT_IMPLEMENTED / NOT_RELEASED.** Moduły są zaprojektowane, lecz nie istnieje wykonywalny pakiet.

## Moduły

| Moduł | Zakres | Status |
| --- | --- | --- |
| [capture](src/lib_vis/capture/README.md) | Źródła obrazów, sekwencje i strumienie wideo | PLANNED |
| [formats](src/lib_vis/formats/README.md) | Dekodowanie i konwersje formatów obrazu | PLANNED |
| [transforms](src/lib_vis/transforms/README.md) | Skalowanie, kadrowanie, normalizacja i przekształcenia | PLANNED |
| [calibration](src/lib_vis/calibration/README.md) | Parametry kamer, dystorsja, geometria projekcji | PLANNED |
| [features](src/lib_vis/features/README.md) | Cechy i punkty kluczowe obrazu | PLANNED |
| [detection](src/lib_vis/detection/README.md) | Detekcja obiektów i pozycji w pojedynczej klatce | PLANNED |
| [segmentation](src/lib_vis/segmentation/README.md) | Segmentacja semantyczna lub instancyjna jednej klatki | PLANNED |
| [geometry](src/lib_vis/geometry/README.md) | Geometria 2D/3D, głębia i przepływ optyczny | PLANNED |
| [quality](src/lib_vis/quality/README.md) | Jakość obrazu, artefakty i kompletność | PLANNED |
| [sync](src/lib_vis/sync/README.md) | Znaczniki czasu, kolejność i buforowanie | PLANNED |

`lib-vis` odpowiada za obserwacje obrazu w pojedynczych klatkach i pomiary geometryczne. **Wieloobiektowy tracking, identyfikatory ścieżek, ich kojarzenie i historię ruchu utrzymuje `lib-track`.** Inferencję językowo-wizualną i modele multimodalne obsługuje `lib-vlm`; `lib-sig` odpowiada za ogólne DSP; prywatne `devices` zawiera kontrakty aparatury.

[Architektura](ARCHITECTURE.md) · [Kontrakt API](docs/contracts.md) · [Plan testów](docs/testing.md) · [Roadmap](docs/roadmap.md).

Wszystkie funkcje są planowane. Nie opublikowano API, instalowalnego pakietu ani wydania.
