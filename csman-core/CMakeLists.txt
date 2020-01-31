set(CSMAN_CORE_SOURCE_DIR ${PROJECT_SOURCE_DIR}/csman-core)
message(STATUS "Configuring csman-core: module root path: ${CSMAN_CORE_SOURCE_DIR}")

include_directories(include)

#### Libraries
set(CSMAN_CORE_SRC
        include/dummy.hpp
        src/dummy.cpp)

add_library(csman-core STATIC ${CSMAN_CORE_SRC})
target_link_libraries(csman-core mozart++)

