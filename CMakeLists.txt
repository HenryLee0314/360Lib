CMAKE_MINIMUM_REQUIRED(VERSION 3.10)

PROJECT(TApp360Convert)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/bin)

SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/lib)

SET(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "-Wall -O -g -std=c++17 -pthread")

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)


INCLUDE_DIRECTORIES(App/utils/TApp360Convert)
INCLUDE_DIRECTORIES(Lib)
INCLUDE_DIRECTORIES(Lib/TAppCommon)

INCLUDE_DIRECTORIES(Lib/TLib360)
INCLUDE_DIRECTORIES(Lib/TLibCommon)
INCLUDE_DIRECTORIES(Lib/TLibVideoIO)

ADD_EXECUTABLE(TApp360Convert 
App/utils/TApp360Convert/convertmain.cpp        
App/utils/TApp360Convert/TApp360ConvertCfg.cpp  
App/utils/TApp360Convert/TApp360PicYuv.cpp 

Lib/TLib360/TCPPPSNRMetricCalc.cpp  
Lib/TLib360/TOctahedron.cpp        
Lib/TLib360/TEquiRect.cpp     
Lib/TLib360/TViewPort.cpp
Lib/TLib360/TCrastersParabolic.cpp  
Lib/TLib360/TPSNRMetricCalc.cpp    
Lib/TLib360/TGeometry.cpp     
Lib/TLib360/TViewPortPSNR.cpp
Lib/TLib360/TCubeMap.cpp            
Lib/TLib360/TSPSNRIMetricCalc.cpp  
Lib/TLib360/TIcosahedron.cpp  
Lib/TLib360/TWSPSNRMetricCalc.cpp
Lib/TLib360/TEqualArea.cpp          
Lib/TLib360/TSPSNRMetricCalc.cpp   

Lib/TAppCommon/program_options_lite.cpp

Lib/TLibVideoIO/TVideoIOYuv.cpp
)
