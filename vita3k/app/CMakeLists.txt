add_library(
	app
	STATIC
	include/app/functions.h
	include/app/screen_render.h
	src/app_init.cpp
	src/app.cpp
	src/screen_render.cpp
)

target_include_directories(app PUBLIC include)
target_link_libraries(app PUBLIC host)
target_link_libraries(app PRIVATE gui)
