# PlatformIO Compatible ESP-IDF Project Example

PlatformIO Compatible ESP-IDF Project of [Hello World Example](https://github.com/espressif/esp-idf/tree/master/examples/get-started/hello_world)

## Run as PlatformIO Project

```sh
platformio run -t menuconfig
platformio run -t build
platformio run -t upload
platformio run -t monitor
```

## Run as ESP-IDF Project

ESP-IDF `v4.0` or more

```sh
idf.py menuconfig
idf.py build
idf.py flash
idf.py monitor
```

## What I changed

The difference from [Hello World Example](https://github.com/espressif/esp-idf/tree/master/examples/get-started/hello_world) is just the addition of the following two files.

platformio.ini

```ini
; PlatformIO Project Configuration File
;
;   Build options: build flags, source filter, extra scripting
;   Upload options: custom port, speed and extra flags
;   Library options: dependencies, extra library storages
;
; Please visit documentation for the other options and examples
; http://docs.platformio.org/page/projectconf.html

[platformio]
src_dir = main

[env:esp32dev]
platform = espressif32
framework = espidf
board = esp32dev

monitor_speed = 115200
monitor_filters = colorize
monitor_flags= --raw
```

.gitignore

```git
# PlatformIO
.pio
.pioenvs
.piolibdeps

# VSCode
.vscode

# ESP-IDF
sdkconfig
sdkconfig.old
build
```
