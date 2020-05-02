# CMakeLists.txt proxyServer directory

# source files for proxyServer
SET(PROXY_SERVER_SRCS
        live555ProxyServer.cpp
        )

ADD_COMPILE_OPTIONS(-I/usr/local/include -I. -O2 -DSOCKLEN_T=socklen_t -D_LARGEFILE_SOURCE=1 -D_FILE_OFFSET_BITS=64 -Wall -DBSD=1)

ADD_EXECUTABLE(proxyServer ${PROXY_SERVER_SRCS})
TARGET_LINK_LIBRARIES(
        proxyServer
        liveMedia
        groupsock
        BasicUsageEnvironment
        UsageEnvironment
        ssl
        crypto
)
