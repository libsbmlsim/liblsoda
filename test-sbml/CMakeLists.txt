cmake_minimum_required(VERSION 2.8)

add_executable(testSBML testSBML.cpp)
add_executable(testGiNaC testGiNaC.cpp)

# headers
include_directories(${LIBLSODA_INCLUDE_DIR})
include_directories(${LIBSBML_INCLUDE_DIR})
include_directories(${GINAC_INCLUDE_DIRS})

target_link_libraries(testSBML lsoda ${LIBSBML_LIBRARIES})
target_link_libraries(testGiNaC lsoda ${LIBSBML_LIBRARIES} ${GINAC_LIBRARIES})
