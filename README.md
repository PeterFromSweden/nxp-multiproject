# nxp-multiproject
VSCode based NXP build of multiple projects

# Background
Importing NXP examples does not give a cmake setup that can be expanded to two projects.

# Import project

# Fixes after import
## CMakeLists.txt
include(${SdkRootDirPath}/devices/MCXN947/all_lib_device.cmake)

## CMakePresets.json
"toolchainFile": "$env{SdkRootDirPath}/tools/cmake_toolchain_files/armgcc.cmake",
"SdkRootDirPath": "$env{SdkRootDirPath}"

## mcux_include.json
"SdkRootDirPath": "c:/Users/pliedholm/source/repos/nxp-sdk",

## .vscode/mcuexpresso-tools.json
"projectType": "sdk-freestanding",
  "sdk": {
    "version": "2.16.000",
    "path": "c:\\Users\\pliedholm\\source\\repos\\nxp-sdk",
    "boardId": "frdmmcxn947",
    "deviceId": "MCXN947",
    "coreId": "cm33_core0_MCXN947"
  }
