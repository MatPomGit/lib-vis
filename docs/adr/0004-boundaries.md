# ADR-0004: granice Computer Vision

Data: 2026-11-21  
Status: proposed

## Kontekst

Akwizycja i klasyczne przetwarzanie obrazu często wymagają tych samych metadanych, kalibracji i transformacji. Detekcja obiektów i segmentacja dostarczają obserwacji, lecz nie są równoważne trackingowi.

## Propozycja

`lib-vis` odpowiada za warstwę computer vision: formaty obrazów, transformacje, parametry kamer, cechy, detekcję i segmentację pojedynczych klatek oraz podstawowe pomiary geometryczne. `lib-track` odpowiada za kojarzenie obserwacji i utrzymanie ścieżki w czasie; `lib-vlm` za multimodalne modele językowe. Przechwytywanie obrazu jest opcjonalnym adapterem, a nie zarządzaniem całą aparaturą.

## Alternatywy

- Umieszczenie trackingu w `lib-vis`: utrudnia nieobrazowe trackingi i ponowne wykorzystanie trajektorii z ROS2.
- Umieszczenie VLM w `lib-vis`: podwójny transport i kontrakt multimodalnej inferencji.

## Konsekwencje

Jeden format obserwacji geometrycznej, potrzeba jawnej kalibracji i testów z rzeczywistymi obrazami. Moduły pozostają planem do czasu ich implementacji i walidacji.
