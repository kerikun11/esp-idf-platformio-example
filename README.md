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
