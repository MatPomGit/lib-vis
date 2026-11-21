# Architektura lib-vis

`lib-vis` to domenowo neutralna biblioteka **computer vision**. Łączy akwizycję obrazu, dekodowanie, transformacje, kalibrację, ekstrakcję cech, detekcję, segmentację oraz geometrię i analizę jakości.

```text
Kamera / plik / strumień
        |
 capture → formats → transforms / calibration
        |
    features / detection / segmentation / geometry
        |
       quality + sync
        |
Obserwacje 2D/3D dla aplikacji, lib-track lub lib-vlm
```

Detekcja pozycji i sylwetek w pojedynczej klatce należy do `lib-vis`; długotrwałe wiązanie obserwacji z jednym `track_id` należy do `lib-track`. Model VLM odpowiada za interpretację multimodalną w `lib-vlm`, nie za geometrię kamery. `lib-vis` może korzystać z OpenCV lub innych silników detekcji poprzez opcjonalne adaptery; biblioteka nie implementuje własnego silnika głębokiej inferencji.

Wszystkie operacje powinny ujawniać układ współrzędnych, rozmiar źródła, jednostki px/m, kalibrację (gdy potrzebna), timestamp i niepewność pomiarową. Sam obraz nie pozwala wnioskować o fizycznej skali 3D bez odpowiedniej kalibracji i metody rekonstrukcji.

Opis szczegółowy: [komponenty](docs/architecture/components.md), [przepływ danych](docs/architecture/data-flow.md), [kontrakty](docs/contracts.md), [ADR-0004](docs/adr/0004-boundaries.md). **Implementacja NOT_IMPLEMENTED; E2E NOT_RUN.**
