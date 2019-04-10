cmake_minimum_required(VERSION 3.10)

project(NativeAudioPlugins)

target_include_directories(NativeAudioPlugins
	INTERFACE
	NativeCode)

target_compile_features(NativeAudioPlugins PRIVATE cxx_std_14)


