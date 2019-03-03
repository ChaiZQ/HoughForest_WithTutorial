cmake_minimum_required(VERSION 2.8.3)
project(HoughForest)

set(CUDA_USE_STATIC_CUDA_RUNTIME OFF)
find_package( OpenCV 2.4.8 REQUIRED )
include_directories(${OpenCV_INCLUDE_DIRS})

#-------------------------executables-----------------------------#
add_executable(CRForest-Detector CRForest-Detector.cpp  CRForestDetector.cpp CRPatch.cpp CRTree.cpp HoG.cpp)
target_link_libraries(CRForest-Detector ${OpenCV_LIBS})
