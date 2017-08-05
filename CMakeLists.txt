cmake_minimum_required (VERSION 2.8.1)

######## Project settings ########
PROJECT(gateway_api)
SET(LICENSE "TBD")

######## Build and include settings ########
include_directories(
	inc
)

link_directories(
	${LINK_DIRECTORIES}
)


file(GLOB SOURCES
	"src/*.cpp"
)

add_library(
	gateway_api
	SHARED
	${SOURCES}
)

TARGET_LINK_LIBRARIES(
	gateway_api
)

######## Install targets ########
INSTALL(TARGETS gateway_api
	 DESTINATION usr/lib
)
