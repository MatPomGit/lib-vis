# sync

Znaczniki czasu, sekwencje, kolejki z ograniczeniem pamięci.

Monotoniczny czas źródła i jawna niepewność synchronizacji.

Każdy rekord powinien przenosić jawny identyfikator źródła, czas i status, gdy dotyczą danej operacji. Nie zakładać dostępności sprzętu ani usług na podstawie dokumentacji. Interfejs ma deklarować błędy, timeout i zasady retencji danych.

**Status: PLANNED / NOT_IMPLEMENTED.** [Kontrakt](../../../docs/contracts.md) · [Testy](../../../docs/testing.md).
