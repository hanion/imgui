project(imgui)




file(GLOB source_files "${PROJECT_SOURCE_DIR}/*.cpp")
file(GLOB include_files "${PROJECT_SOURCE_DIR}/*.h")


add_library(imgui SHARED ${source_files} ${sourceinclude_files_files})
target_include_directories(${PROJECT_NAME}
	PUBLIC
	$<INSTALL_INTERFACE:include>
	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
)