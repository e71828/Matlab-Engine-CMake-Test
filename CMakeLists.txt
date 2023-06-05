cmake_minimum_required(VERSION 3.13)
project(MEX)

set(CMAKE_INSTALL_PREFIX ${CMAKE_SOURCE_DIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

set(MATLAB_ROOT C:/Program\ Files/MATLAB/R2023a CACHE PATH "")
set(MATLAB_INCLUDE_DIR ${MATLAB_ROOT}/extern/include)
message(STATUS "MATLAB Found, MATLAB MEX will be compiled.")
message(STATUS "MATLAB Found, ${MATLAB_INCLUDE_DIR}.")

INCLUDE_DIRECTORIES(${MATLAB_INCLUDE_DIR})
add_executable (${PROJECT_NAME} src/matlab_engine.cpp)
target_link_libraries(${PROJECT_NAME} "C:/Program Files/MATLAB/R2023a/extern/lib/win64/mingw64/libMatlabEngine.lib")
target_link_libraries(${PROJECT_NAME} "C:/Program Files/MATLAB/R2023a/extern/lib/win64/mingw64/libMatlabDataArray.lib")

#add_custom_command(TARGET ${PROJECT_NAME} POST_BUILD
#    COMMAND ${CMAKE_COMMAND} -E copy_directory
#        "${MATLAB_ROOT}/extern/bin/win64"
#        $<TARGET_FILE_DIR:${PROJECT_NAME}>)
