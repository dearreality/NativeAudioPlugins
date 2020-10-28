cmake_minimum_required(VERSION 3.10)

project(NativeAudioPlugins)

add_library(NativeAudioPlugins INTERFACE)

target_include_directories(NativeAudioPlugins
    INTERFACE
    NativeCode)

target_compile_options(NativeAudioPlugins
    INTERFACE
    $<$<OR:$<CXX_COMPILER_ID:AppleClang>,$<CXX_COMPILER_ID:GNU>,$<CXX_COMPILER_ID:Clang>>:
        -Wno-self-assign
        -Wno-shorten-64-to-32>
    $<$<CXX_COMPILER_ID:MSVC>:
        /wd4458>
    )
