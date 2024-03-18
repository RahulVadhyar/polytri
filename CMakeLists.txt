cmake_minimum_required(VERSION 3.13)

project(polytri VERSION 0.1 LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 14)



# -----------------------------------------------------------------------------

set(Sources
  src/trapezoidal_decomposition.cc
  src/monotone_partitioning.cc
  src/polygon_triangulation.cc
)

set(Headers
  src/polygon_triangulation.h
)

# -----------------------------------------------------------------------------

add_library(${PROJECT_NAME} STATIC ${Sources} ${Headers})
target_include_directories(${PROJECT_NAME} PRIVATE ${SOURCE_DIR})
