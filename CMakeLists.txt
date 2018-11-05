cmake_minimum_required(VERSION 3.12)

include_directories(./)
include_directories(/Usr/local/include/SDL2)

find_library(avutil avutil)
find_library(avformat avformat)
find_library(avdevice avdevice)
find_library(swscale swscale)
find_library(avcodec avcodec)
find_library(swresample swresample)
find_library(avfilter avfilter)
find_library(SDL2 SDL2)

add_executable(ffplay fftools/ffplay.c fftools/cmdutils.c)
target_link_libraries(ffplay avutil avformat avdevice swscale avcodec swresample avfilter SDL2)