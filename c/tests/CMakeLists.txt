project(${PROJECT_NAME}_tests CXX)


Include(FetchContent)

FetchContent_Declare(
        Catch2
        GIT_REPOSITORY https://github.com/catchorg/Catch2.git
        GIT_TAG v2.13.1)

FetchContent_MakeAvailable(Catch2)

add_executable(${PROJECT_NAME} main.cpp
               node.test.cpp
               binary-search-tree.test.cpp
               )

target_link_libraries(${PROJECT_NAME} ${CMAKE_PROJECT_NAME})

target_link_libraries(${PROJECT_NAME} Catch2::Catch2)
