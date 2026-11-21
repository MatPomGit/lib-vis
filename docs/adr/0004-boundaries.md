# ADR-0004: odpowiedzialność lib-vis

Data: 2026-11-21  
Status: proposed

## Kontekst

Przechwytywanie, dekodowanie, transformacje i kontrola jakości obrazu oraz strumieni wideo. Bez odrębnej granicy repozytorium podobne funkcje byłyby powielane w aplikacjach i bibliotekach.

## Proponowana decyzja

Przetwarzanie obrazu i klatek bez inferencji językowej/VLM, estymacji ruchu ciała i sterowania urządzeniami. lib-vlm odpowiada za multimodalne modele, lib-trac byłby właścicielem trackingu, a prywatny devices za konfiguracje aparatury. Repozytorium utrzymuje jedynie warstwę adaptacji i spójne metadane. Wykorzystuje istniejące SDK/backendy po weryfikacji ich licencji. Szczegóły jednostek: piksele, klatki/s, sekundy monotoniczne, układ współrzędnych obrazu (początek w lewym górnym rogu).

## Alternatywy

- Implementacja wszystkiego w konsumentach: duplikacja i brak wspólnego kontraktu.
- Jeden megaprojekt dla wszystkich sensorów i inferencji: rozmyte granice oraz nadmierne zależności.

## Konsekwencje

Osobne testy wersjonowanego API; żadne wsparcie sprzętowe nie jest zadeklarowane przed testem. Ryzyko utrzymania adapterów i konieczność synchronizacji wersji z konsumentami.
