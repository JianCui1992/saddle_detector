cmake_minimum_required(VERSION 2.8)
PROJECT( saddle_detector_project )
FIND_PACKAGE( OpenCV REQUIRED )

#IF(CMAKE_COMPILER_IS_GNUCXX)
  #SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wno-strict-aliasing")
  #SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wextra -Wno-write-strings")
  #SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wno-deprecated -ansi")
  ##SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -ftree-vectorize -funroll-loops")
    #add_definitions(-std=c++11)
#ENDIF(CMAKE_COMPILER_IS_GNUCXX)

message("OCV includes: ${OpenCV_INCLUDE_DIRS}")
add_executable( saddlepts saddlepts.cpp anyoption.cpp sorb.cpp fast.cpp fast_score.cpp )
TARGET_LINK_LIBRARIES( saddlepts ${OpenCV_LIBS} )
