cmake_minimum_required(VERSION 3.13)
project(MultiTargetExample)
# Include NXP MCUXpresso SDK
set(MCUX_SDK_PROJECT_NAME ${PROJECT_NAME})
include($ENV{MCUX_SDK_PATH}/tools/cmake/sdk.cmake)
# Add subdirectories for each application
add_subdirectory(app1)
add_subdirectory(app2)