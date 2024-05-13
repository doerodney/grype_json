message("reading /src/grype_json/CMakeLists.txt")

set(SOURCES grype_json.c)

add_library(grype_json STATIC ${SOURCES})
target_include_directories(grype_json PRIVATE ../include) 

