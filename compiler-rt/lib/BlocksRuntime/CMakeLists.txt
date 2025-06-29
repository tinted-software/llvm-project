set(BLOCK_SOURCES
  data.c
  runtime.c
)

set(BLOCK_HEADERS
  Block.h
)

add_compiler_rt_component(blocks)

add_compiler_rt_runtime(
  BlocksRuntime
  SOURCES ${BLOCK_SOURCES}
  ADDITIONAL_HEADERS ${BLOCK_HEADERS}
  PARENT_TARGET blocks
)
