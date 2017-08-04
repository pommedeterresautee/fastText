cmake_minimum_required(VERSION 3.8)
project(fastText)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        src/args.cc
        src/args.h
        src/dictionary.cc
        src/dictionary.h
        src/fasttext.cc
        src/fasttext.h
        src/main.cc
        src/matrix.cc
        src/matrix.h
        src/model.cc
        src/model.h
        src/productquantizer.cc
        src/productquantizer.h
        src/qmatrix.cc
        src/qmatrix.h
        src/real.h
        src/utils.cc
        src/utils.h
        src/vector.cc
        src/vector.h)


add_executable(fastText ${SOURCE_FILES})

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

target_link_libraries(fastText Threads::Threads)
