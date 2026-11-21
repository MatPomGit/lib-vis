# Przepływ danych i granice zaufania

Planowany przebieg: **konsument → walidacja żądania → źródło / adapter → normalizacja + jednostki → zapis lub emisja u konsumenta**. Weryfikacja schematu i pochodzenia odbywa się przed zarejestrowaniem wyniku.

Jednostki i czas: piksele, klatki/s, sekundy monotoniczne, układ współrzędnych obrazu (początek w lewym górnym rogu). Zachowywać rozróżnienie czasu źródłowego, monotonicznego i systemowego, a także kolejność próbek. Nie interpolować po cichu brakujących klatek/próbek.

Źródła mogą pochodzić ze sprzętu lub z plików, dlatego przed wywołaniem należy zatwierdzić URI/ścieżkę, typ danych i maksymalny rozmiar. Surowe nagrania i dane uczestników nie trafiają do publicznych logów ani Github Actions. Transport i dostęp do urządzeń wymagają osobnej konfiguracji poza repo.

**Stan przepływu rzeczywistego: NOT_RUN.** Model zagrożeń: [security](../security/threat-model.md), [prywatność](../privacy.md).
