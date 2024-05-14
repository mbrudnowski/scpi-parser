cmake_minimum_required(VERSION 3.13)

add_library(scpilib "")

target_sources(scpilib 
  PRIVATE 
    ${CMAKE_CURRENT_LIST_DIR}/src/error.c
    ${CMAKE_CURRENT_LIST_DIR}/src/expression.c
    ${CMAKE_CURRENT_LIST_DIR}/src/fifo.c
    ${CMAKE_CURRENT_LIST_DIR}/src/ieee488.c
    ${CMAKE_CURRENT_LIST_DIR}/src/lexer.c
    ${CMAKE_CURRENT_LIST_DIR}/src/minimal.c
    ${CMAKE_CURRENT_LIST_DIR}/src/parser.c
    ${CMAKE_CURRENT_LIST_DIR}/src/units.c
    ${CMAKE_CURRENT_LIST_DIR}/src/utils.c
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/src/error.c
    ${CMAKE_CURRENT_LIST_DIR}/src/expression.c
    ${CMAKE_CURRENT_LIST_DIR}/src/fifo.c
    ${CMAKE_CURRENT_LIST_DIR}/src/ieee488.c
    ${CMAKE_CURRENT_LIST_DIR}/src/lexer.c
    ${CMAKE_CURRENT_LIST_DIR}/src/minimal.c
    ${CMAKE_CURRENT_LIST_DIR}/src/parser.c
    ${CMAKE_CURRENT_LIST_DIR}/src/units.c
    ${CMAKE_CURRENT_LIST_DIR}/src/utils.c
)

target_include_directories(scpilib
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/inc  
)

target_include_directories(scpilib
  PRIVATE
   inc
)