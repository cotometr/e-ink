cmake_minimum_required(VERSION 3.6)
project(eink)

set(CMAKE_CXX_STANDARD 11)

#include_directories(/usr/share/arduino/hardware/tools)
include_directories(/opt/arduino-1.8.2/libraries/SoftwareSerial)
include_directories(/opt/arduino-1.8.2/hardware/arduino/avr/cores/arduino)
include_directories(/opt/arduino-1.8.2/hardware/arduino/variants/micro)
include_directories(/opt/arduino-1.8.2/hardware/arduino/avr/libraries/EEPROM/src)
include_directories(/opt/arduino-1.8.2/hardware/arduino/avr/libraries/SPI/src)
#include_directories(../log)
set(SOURCE_FILES src/imagedata.cpp src/e-ink-display.cpp src/epdif.cpp src/font8.c
        src/font12.c
        src/font16.c
        src/font20.c
        src/font24.c
        src/e-ink.cpp
        src/fonts.h)
#set(SOURCE_FILES test/main.cpp )

add_executable(eink ${SOURCE_FILES})