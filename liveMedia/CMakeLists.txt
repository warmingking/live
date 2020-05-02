# CMakeLists.txt in liveMedia

INCLUDE_DIRECTORIES(
        ${live555Includes}
)

FILE(GLOB LIVE_MEDIA_SRCS
        include/*.hh
        *.hh
        *.h
        *.c
        *.cpp
        )

#AUX_SOURCE_DIRECTORY(. LIVE_MEDIA_SRCS)

MESSAGE("===========================")
MESSAGE(${LIVE_MEDIA_SRCS})
MESSAGE("===========================")

ADD_LIBRARY(liveMedia STATIC ${LIVE_MEDIA_SRCS})
