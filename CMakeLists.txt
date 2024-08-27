cmake_minimum_required(VERSION 3.29)
project(progressbar)

# set cpp 11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# find wxWidgets
find_package(wxWidgets REQUIRED COMPONENTS core base)

# add wxWidgets header files
include(${wxWidgets_USE_FILE})

# Aggiungi i file sorgente del progetto
add_executable(progressbar main.cpp
                ProgressBarFrame.cpp
                ProgressBarFrame.h
                ResourceLoader.cpp
                ResourceLoader.h)

# Linka wxWidgets con il tuo progetto
target_link_libraries(progressbar ${wxWidgets_LIBRARIES})