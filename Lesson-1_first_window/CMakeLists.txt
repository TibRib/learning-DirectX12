# CMakeList.txt : projet CMake pour Lesson-1_first_window, incluez la source et définissez
# la logique spécifique au projet ici.
#
cmake_minimum_required (VERSION 3.8)

set( HEADER_FILES
    inc/d3dx12.h
    inc/Helpers.h
)


set( SRC_FILES
    src/main.cpp
)

add_executable( Lesson1 WIN32
    ${HEADER_FILES} 
    ${SRC_FILES}
)

target_include_directories( Lesson1
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/inc
) 

target_link_libraries( Lesson1
    d3d12.lib
    dxgi.lib
    dxguid.lib
)