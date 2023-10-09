cmake_minimum_required (VERSION 3.5)
project (move_me_out CXX)
add_executable(move_me_out move_me_out.h move_me_out.cpp hello_world.cpp)

target_compile_features(move_me_out PUBLIC cxx_std_17)

if (MSVC)
    target_compile_options(move_me_out PUBLIC /W4 /WX)
else()
    target_compile_options(move_me_out PUBLIC -Wall -Wextra -Werror -pedantic)
endif()
