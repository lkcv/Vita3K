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
<<<<<<< HEAD
=======
if(USE_DISCORD_RICH_PRESENCE)
  target_link_libraries(app PUBLIC discord-rpc)
endif()
>>>>>>> 986a4302a2b595ee8aa364da2388e368cbc79dbb
target_link_libraries(app PRIVATE gui)
