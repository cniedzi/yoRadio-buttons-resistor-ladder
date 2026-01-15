# yoRadio Multi-button input resistor ladder

This mod enables the use of multiple buttons to handle favorite stations in yoRadio using a resistor ladder. The favorite stations are stored in the ESP32 flash memory.
A short button press retrieves the station (if already stored), while a long press (>1 sec) saves the current station to the slot assigned to that button.

The required connections are shown in the file "Resistor ladder connection diagram.jpg".
<br><br>**IMPORTANT**:
- Since Espressif has changed analog reading mechanism started from ver.3x, this version works only on ESP Arduino Core version up to 2.0.17 max.
- For ESP32: GPIO for analog reading must belong to the ADC1 Group (32, 33, 34, 35, 36, 39). For ESP32-S3 is also recommended (but not required) to use ADC1 group pins (1, 2, 3, 4, 5, 6, 7, 8, 9, 10).

Installation:
1. Replace the "player.cpp" file in the "yoradio-main\yoRadio\src\core" directory with the provided one, or manually add the three required sections to the appropriate parts of your "player.cpp" file. Each section to be added is delimited by lines: /**************** EXTENDER ****************/ in the provided "player.cpp" file.
2. In the above mentioned file "player.cpp" set the expander parameters according to your configuration (section: EXPANDER CONFIGURATION)
3. Build & upload

Enjoy!

***************************************************************************

Ten mod umożliwia korzystanie z wielu przycisków do obsługi ulubionych stacji w yoRadio za pomocą drabinki rezystorowej. Ulubione stacje są przechowywane w pamięci flash procesora ESP32. Krótkie naciśnięcie przycisku wywołuje stację (jeśli została wcześniej zapisana), natomiast długie naciśnięcie (>1 sek.) zapisuje aktualną stację w slocie przypisanym do danego przycisku.

Wymagane połączenia zostały przedstawione w pliku "Resistor ladder connection diagram.jpg".

**WAŻNE**
- Ponieważ Espressif zmienił mechanizm odczytu analogowego poczynając od wersji 3.x, ta wersja działa wyłącznie z ESP Arduino Core w wersji maksymalnie do 2.0.17.
- Dla ESP32: GPIO do odczytu analogowego musi należeć do grupy ADC1 (32, 33, 34, 35, 36, 39). Dla ESP32-S3 również zaleca się (choć nie jest to wymagane) używanie pinów z grupy ADC1 (1, 2, 3, 4, 5, 6, 7, 8, 9, 10).

Instalacja:
1. Zastąp plik "player.cpp" w katalogu yoradio-main\yoRadio\src\core plikiem z tego repozytorium, lub ręcznie dodaj trzy wymagane sekcje w odpowiednich miejscach pliku "player.cpp". Każda z ww. sekcji jest ograniczona liniami: /**************** EXTENDER ****************/ w dostarczonym pliku "player.cpp".
2. W wyżej wymienionym pliku „player.cpp” ustaw parametry ekspandera zgodnie ze swoją konfiguracją (sekcja: EXPANDER CONFIGURATION).
3. Skompiluj i wgraj (Build & upload)

Miłego korzystania!
