# Define the first application
set(TARGET_NAME app1)
add_executable(${TARGET_NAME} main.c)
# Link the NXP SDK components (adjust as necessary for your dependencies)
target_link_libraries(${TARGET_NAME} PRIVATE
${MCUX_SDK_PROJECT_NAME}.board
${MCUX_SDK_PROJECT_NAME}.drivers
${MCUX_SDK_PROJECT_NAME}.utilities
)
# Specify any additional compile definitions or flags for app1
target_compile_definitions(${TARGET_NAME} PRIVATE APP1_BUILD)