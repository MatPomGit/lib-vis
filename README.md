# lib-vis

Przechwytywanie, dekodowanie, transformacje i kontrola jakości obrazu oraz strumieni wideo.

**Status:** architektura i struktura źródeł, **NOT_IMPLEMENTED**. To biblioteka planowana, bez zainstalowanego pakietu, urządzeń podłączonych do testów i wydania.

## Moduły

| Moduł | Zakres | Status |
| --- | --- | --- |
| [capture](src/lib_vis/capture/README.md) | Źródła klatek: kamery i pliki, kontrola buforów i timestampów | PLANNED |
| [formats](src/lib_vis/formats/README.md) | Dekodowanie obrazu i konwersje przestrzeni barw | PLANNED |
| [transforms](src/lib_vis/transforms/README.md) | Skalowanie, kadrowanie, korekcja geometryczna i normalizacja | PLANNED |
| [quality](src/lib_vis/quality/README.md) | Ocena jakości klatki i strumienia | PLANNED |
| [sync](src/lib_vis/sync/README.md) | Znaczniki czasu, sekwencje, kolejki z ograniczeniem pamięci | PLANNED |

Przetwarzanie obrazu i klatek bez inferencji językowej/VLM, estymacji ruchu ciała i sterowania urządzeniami. lib-vlm odpowiada za multimodalne modele, lib-track byłby właścicielem trackingu, a prywatny devices za konfiguracje aparatury.

Dokumentacja techniczna: [architektura](ARCHITECTURE.md), [kontrakt API](docs/contracts.md), [walidacja](docs/testing.md), [roadmap](docs/roadmap.md), [prywatność](docs/privacy.md). Rejestr publicznego API w [contracts/api.json](contracts/api.json) pozostaje pusty, dopóki nie powstanie kod. Nie opublikowano wydania ani Pages.
