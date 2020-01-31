set(CSMAN_CLI_SOURCE_DIR ${PROJECT_SOURCE_DIR}/csman-cli)
message(STATUS "Configuring csman-cli: module root path: ${CSMAN_CLI_SOURCE_DIR}")

include_directories(include)

#### Libraries
set(CSMAN_CLI_SRC
        include/dummy.hpp
        src/dummy.cpp)

add_executable(csman ${CSMAN_CLI_SRC})
target_link_libraries(csman mozart++)

