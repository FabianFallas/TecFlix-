cmake_minimum_required(VERSION 3.14)
project(TecFlix)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17 -lcurl")
set(SOURCE_FILES main.cpp)

find_package(Qt5Widgets REQUIRED)
find_package( Qt5Core REQUIRED )
find_package( Qt5Gui REQUIRED )
add_executable(TecFlix main.cpp Clases/pelicula.cpp Clases/pelicula.h Lista/list.cpp Lista/list.h Lista/node.cpp Lista/node.h DesdeIMdB/leerIMdB.cpp DesdeIMdB/leerIMdB.h Paginacion/Pagina.cpp Paginacion/Pagina.h Grafica/ventana.h Grafica/ventana.cpp DesdeIMdB/descarga.cpp DesdeIMdB/descarga.h Grafica/ventana2.cpp Grafica/ventana2.h)
target_link_libraries(TecFlix Qt5::Widgets Qt5::Core Qt5::Gui )

target_link_libraries(TecFlix curl)
qt5_use_modules( TecFlix Core Widgets Gui )