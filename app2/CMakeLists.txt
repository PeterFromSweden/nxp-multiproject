# Define the first application
set(MCUX_SDK_PROJECT_NAME app2)
include(config.cmake)
set(ProjDirPath ${CMAKE_CURRENT_SOURCE_DIR})
include(flags.cmake)
add_executable(${MCUX_SDK_PROJECT_NAME} main.c pin_mux.c clock_config.c board.c)
# Include NXP MCUXpresso SDK
include(${SdkRootDirPath}/devices/MCXN947/all_lib_device.cmake)
