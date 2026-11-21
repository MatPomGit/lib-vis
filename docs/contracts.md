# Docelowy kontrakt danych Computer Vision

**PROPOSED / NOT_IMPLEMENTED.** Rejestr `contracts/api.json` celowo ma puste `public_entrypoints`.

| Typ | Zakres pól / wymagania |
| --- | --- |
| `Frame` | `buffer_or_ref`, `width`, `height`, `pixel_format`, `timestamp_monotonic_s`, `source_id` |
| `StreamInfo` | `frame_rate_hz`, `resolution_px`, `codec`, `calibration_ref?`, `timebase` |
| `VisionTransform` | `operation`, `parameters`, `source_to_output_transform`, `interpolation` |
| `CameraCalibration` | `intrinsics`, `distortion`, `extrinsics?`, `reprojection_error?`, `frame_id` |
| `Detection2D` | `bbox_xywh_px`, `class_id?`, `confidence?`, `source_frame_ref` |
| `Keypoints` | `points_xy_px`, `visibility?`, `source_frame_ref`, `model_version?` |
| `SegmentationMask` | `mask_ref`, `labels`, `geometry`, `encoding` |
| `GeometryResult` | `coordinate_frame`, `units`, `points_or_flow`, `calibration_ref?` |
| `QualityReport` | `blur_metric`, `exposure_metric`, `dropped_frames`, `validity_flags` |

Przestrzeń obrazu: jednostka px, początek w lewym górnym rogu, jawnie określona orientacja osi. Przestrzeń metryczna: m, wymaga potwierdzonej kalibracji i `frame_id`. Confidence i błąd kalibracji są opcjonalne i nie mogą być wytwarzane sztucznie. Brak `track_id` w typach obserwacji: ścieżki należą do `lib-track`.

Docelowe błędy: `INVALID_IMAGE`, `UNSUPPORTED_FORMAT`, `CALIBRATION_REQUIRED`, `FRAME_MISMATCH`, `TIMEOUT`, `DATA_LOSS`. Nie ma jeszcze działającego SDK ani kontraktów ABI.
