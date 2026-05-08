if (CONFIG_LIB_TELEMETRY)
zephyr_library()
zephyr_library_include_directories(include)
  zephyr_library_compile_definitions(
  VARIABLE_LIST_FILE=${CONFIG_TELEMETRY_VARIABLE_LIST_FILE}
)
zephyr_library_sources(
  command_parser.c
  command_processor.c
  registry.c
  telemetry.c
)
zephyr_include_directories(
  include
)

endif (CONFIG_LIB_TELEMETRY)
