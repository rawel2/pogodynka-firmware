# Pogodynka – wydania programu

Gotowe wersje programu „Pogodynki” – zegara pogodowego na płytce **STM32H7B3I-DK** (ekran 4,3" 480 × 272,
Wi-Fi na płytce). Pogodynka sama sprawdza to repozytorium i instaluje nowsze wersje: w nocy (ok. 3:00) albo po
„Sprawdź teraz” → „Zainstaluj” na swojej stronie www (zakładka „Urządzenie”).

| Plik | Zawartość |
|---|---|
| `wersja.txt` | numer wersji, rozmiar pliku w bajtach, suma CRC32 (szesnastkowo) – po jednej w wierszu |
| `pogodynka.bin` | program do wgrania (aktualizacja przez Wi-Fi albo `0x08000000` przez ST-LINK) |
| `zmiany.txt` | historia wersji |

Program trafia do drugiego banku pamięci flash; pogodynka przełącza się na niego dopiero po sprawdzeniu rozmiaru
i sumy kontrolnej, a poprzednia wersja zostaje w zapasie („Wróć do poprzedniego” na stronie www).

Made with AI.
