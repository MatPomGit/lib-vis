# Docelowy kontrakt danych i API

**Status: PROPOSED / NOT_IMPLEMENTED.** `contracts/api.json` zachowuje puste `public_entrypoints`, ponieważ biblioteka nie udostępnia jeszcze wykonywalnych symboli.

| Typ logiczny | Zakres pól | Kontrakt |
| --- | --- | --- |
| `Frame` | buffer/URI, width, height, pixel_format, timestamp_monotonic_s, source_id | PLANNED |
| `StreamInfo` | frame_rate_hz, resolution_px, codec, calibration_ref, timebase | PLANNED |
| `VisionTransform` | operation, parameters, interpolation, source_to_output geometry | PLANNED |
| `QualityReport` | blur_metric, exposure_metric, dropped_frames, valid_flags | PLANNED |

Wspólne wymagania: jawne źródło danych i identyfikator żądania, model błędów (`INVALID_INPUT`, `UNAVAILABLE`, `TIMEOUT`, `UNSUPPORTED`, `DATA_LOSS`), limit bufora i granica odpowiedzialności za zapis. Jednostki muszą być określone w schemacie: piksele, klatki/s, sekundy monotoniczne, układ współrzędnych obrazu (początek w lewym górnym rogu).

Nie zakładać prawidłowego timestampu przy odbiorze. Zwracany status ma rozróżniać brak źródła, pusty wynik, niską jakość oraz brak danych. Wersjonowanie i publiczne symbole zostaną zatwierdzone przy pierwszej implementacji. Zmiana niekompatybilna po pojawieniu się odbiorców wymaga kontroli SemVer i migracji.
