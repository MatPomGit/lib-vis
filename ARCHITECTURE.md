# Architektura lib-vis

Przechwytywanie, dekodowanie, transformacje i kontrola jakości obrazu oraz strumieni wideo.

**Wejście:** jawnie nazwane źródło danych i jego konfiguracja. **Wyjście:** wersjonowany, zwalidowany rekord z metadanymi, czasem, jednostkami i statusem. Warstwy: `src/lib_vis/` → adapter sprzętu/systemu → kontrolowany odbiorca. Katalogi w `src/` zawierają obecnie tylko dokumentację planowanej implementacji.

Przetwarzanie obrazu i klatek bez inferencji językowej/VLM, estymacji ruchu ciała i sterowania urządzeniami. lib-vlm odpowiada za multimodalne modele, lib-track byłby właścicielem trackingu, a prywatny devices za konfiguracje aparatury.

Wspólny standard pomiarowy: piksele, klatki/s, sekundy monotoniczne, układ współrzędnych obrazu (początek w lewym górnym rogu). Konwersje jednostek i czasu muszą być jawne; brak niezbędnych metadanych skutkuje błędem zamiast niejawnego przybliżenia.

Szczegóły: [komponenty](docs/architecture/components.md), [przepływy danych](docs/architecture/data-flow.md), [kontrakt](docs/contracts.md), [ADR-0004](docs/adr/0004-boundaries.md).

**Status:** architektura PROPOSED; implementacja NOT_IMPLEMENTED, E2E NOT_RUN, release NOT_RELEASED.
