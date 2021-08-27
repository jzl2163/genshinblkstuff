cmake_minimum_required(VERSION 3.10)

project(blkstuff VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED true)

add_executable(${PROJECT_NAME}
	# source
	main.cpp
	util.cpp
	3rdparty/aes/aes.c
	3rdparty/lz4/lz4.c
	# headers
	util.h
	magic_constants.h
	3rdparty/aes/aes.h
	3rdparty/lz4/lz4.h
	3rdparty/argh/argh.h
	3rdparty/ThreadPool/ThreadPool.h
	3rdparty/spdlog/spdlog.h
	)

target_include_directories(${PROJECT_NAME} PUBLIC
	${PROJECT_SOURCE_DIR}/3rdparty/
	${PROJECT_SOURCE_DIR}
	)
