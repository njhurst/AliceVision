# Headers
set(system_files_headers
  cpu.hpp
  gpu.hpp
  MemoryInfo.hpp
  system.hpp
  Timer.hpp
  Logger.hpp
)

# Sources
set(system_files_sources
  cpu.cpp
  MemoryInfo.cpp
  Timer.cpp
  Logger.cpp
)

alicevision_add_library(aliceVision_system
  SOURCES ${system_files_headers} ${system_files_sources}
  PUBLIC_LINKS
    ${Boost_LOG_LIBRARY}
    ${Boost_THREAD_LIBRARY}
    ${Boost_LOG_SETUP_LIBRARY}
    ${Boost_DETAIL_LIBRARY}
    ${Boost_SYSTEM_LIBRARY}
    ${Boost_DATE_TIME_LIBRARY}
    ${Boost_PROGRAM_OPTIONS_LIBRARY}
  PUBLIC_INCLUDE_DIRS
    ${Boost_INCLUDE_DIR}
)
