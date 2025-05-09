# Version minima de CMake requerido
cmake_minimum_required(VERSION 3.22)

# Nombre del proyecto y lenguaje de programacion a utilizar
project(MALLADOR LANGUAGES Fortran)

message(STATUS "Making Grid")

# Definir el nombre del ejecutable
set(EXEC_NAME malla)

# Especificar el compilador de fortran a utilizar
set(CMAKE_Fortran_COMPILER gfortran)

# Variable para listar los archivos fuentes
set(SOURCE_FILES
    malla_irr.f90
    ../source/mod_malla.f90
    ../source/mod_postproceso.f90)

# Creacion del ejecutable
add_executable(${EXEC_NAME} ${SOURCE_FILES})
