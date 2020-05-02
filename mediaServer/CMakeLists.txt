# CMakeLists.txt mediaServer directory

# headers
SET(MEDIA_SERVER_HDRS
        DynamicRTSPServer.hh
        )

# source files for mediaServer
SET(MEDIA_SERVER_SRCS
        DynamicRTSPServer.cpp
        live555MediaServer.cpp
        )

ADD_COMPILE_OPTIONS(-I/usr/local/include -I. -O2 -DSOCKLEN_T=socklen_t -D_LARGEFILE_SOURCE=1 -D_FILE_OFFSET_BITS=64 -Wall -DBSD=1)

ADD_EXECUTABLE(mediaServer ${MEDIA_SERVER_HDRS} ${MEDIA_SERVER_SRCS})
TARGET_LINK_LIBRARIES(
        mediaServer
        liveMedia
        groupsock
        BasicUsageEnvironment
        UsageEnvironment
        ssl
        crypto
)
