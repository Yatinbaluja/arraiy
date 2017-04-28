#=============================================================================#
# Author: QueezyTheGreat                                                      #
# Date:   26.04.2011                                                          #
#                                                                             #
# Description: Arduino CMake example                                          #
#                                                                             #
#=============================================================================#
set(CMAKE_TOOLCHAIN_FILE cmake/ArduinoToolchain.cmake) # Arduino Toolchain
set(PLATFOM avr)
set(ARDUINO_LIBRARIES_PATH /opt/arduino-1.6.12/hardware/arduino/avr/libraries)


cmake_minimum_required(VERSION 2.8)
#====================================================================#
#  Setup Project                                                     #
#====================================================================#
project(ArduinoExample C CXX)

register_hardware_platform("/opt/arduino-1.6.12/hardware/arduino/avr/")

print_board_list()
print_programmer_list()

add_subdirectory(example)   #add the example directory into build
