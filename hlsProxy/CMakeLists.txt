# CMakeLists.txt proxyServer directory

# source files for proxyServer
SET(HLS_PROXY_SRCS
        live555HLSProxy.cpp
        )

ADD_COMPILE_OPTIONS(-I/usr/local/include -I. -O2 -DSOCKLEN_T=socklen_t -D_LARGEFILE_SOURCE=1 -D_FILE_OFFSET_BITS=64 -Wall -DBSD=1)

ADD_EXECUTABLE(hlsProxt ${HLS_PROXY_SRCS})
TARGET_LINK_LIBRARIES(
        hlsProxt
        BasicUsageEnvironment
        groupsock
        liveMedia
        UsageEnvironment
)
