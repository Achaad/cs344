############################################################################
# <summary> CMakeLists.txt for OpenCV and CUDA. </summary>
# <date>    2012-02-07          </date>
# <author>  Quan Tran Minh. edit by Johannes Kast, Michael Sarahan </author>
# <email>   quantm@unist.ac.kr  kast.jo@googlemail.com msarahan@gmail.com</email>
############################################################################

# collect source files

file( GLOB  hdr *.hpp *.h )
file( GLOB  cu  *.cu)
SET (HW1_files main.cpp reference_calc.cpp compare.cpp)

CUDA_ADD_EXECUTABLE(HW1 ${HW1_files} ${hdr} ${cu})

#cmake_minimum_required(VERSION 3.13 FATAL_ERROR)

#project(udacity
#   LANGUAGES CXX CUDA
#       DESCRIPTION "Learning parallel computing way of life"
#       )

    #find_package(OpenCV REQUIRED)

    #list(APPEND cpp_sources
    #${CMAKE_CURRENT_LIST_DIR}/compare.cpp
    # ${CMAKE_CURRENT_LIST_DIR}/reference_calc.cpp
    #)

    #list(APPEND cu_sources
    #${CMAKE_CURRENT_LIST_DIR}/student_func.cu)

    #add_library(cu-obj
    #       OBJECT
    #       ${cu_sources}
    #      )

    #add_library(cu-static
    #       STATIC
    #       $<TARGET_OBJECTS:cu-obj>
    #      )

    #set_target_properties(cu-static
    #                 PROPERTIES
    #                 CUDA_SEPARABLE_COMPILATON ON
    #                )

    #add_executable(udacity_test main.cpp ${cpp_sources} ${cu_sources})
    #target_link_libraries(udacity_test ${OpenCV_LIBS})
