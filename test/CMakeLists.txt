FetchContent_Declare(
  Catch2
  GIT_REPOSITORY https://github.com/catchorg/Catch2.git
  GIT_TAG        v3.3.1
)
FetchContent_MakeAvailable(Catch2)

add_executable(test_lib test_lib.cpp)
target_link_libraries(test_lib PRIVATE Catch2::Catch2WithMain)

add_test(NAME testlibraryintegration COMMAND test_lib)