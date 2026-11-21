# capture

Źródła klatek: kamery i pliki, kontrola buforów i timestampów.

Otwarcie źródła wymaga jawnego device_id/URI; brak stałego zapisu w repo.

Każdy rekord powinien przenosić jawny identyfikator źródła, czas i status, gdy dotyczą danej operacji. Nie zakładać dostępności sprzętu ani usług na podstawie dokumentacji. Interfejs ma deklarować błędy, timeout i zasady retencji danych.

**Status: PLANNED / NOT_IMPLEMENTED.** [Kontrakt](../../../docs/contracts.md) · [Testy](../../../docs/testing.md).
