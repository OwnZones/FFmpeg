cmake_minimum_required(VERSION 3.11)
project(OwnzonesFFmpeg)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_VERBOSE_MAKEFILE ON)

add_custom_command(OUTPUT ffmpeg_g
                    COMMAND make -j4
                    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/)

add_custom_target(ffmpeg
                    COMMAND make -j4
                    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/)


add_custom_command(OUTPUT ffprobe_g
        COMMAND make -j4
        WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/)

add_custom_target(ffprobe
        COMMAND make -j4
        WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/)
