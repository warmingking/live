cmake_minimum_required(VERSION 3.16)

PROJECT( live555 )

SET(CMAKE_CXX_STANDARD 11)

INCLUDE_DIRECTORIES(
        liveMedia/include
        groupsock/include
        UsageEnvironment/include
        BasicUsageEnvironment/include
)

ADD_DEFINITIONS(-DSOCKLEN_T=socklen_t -D_LARGEFILE_SOURCE=1 -D_FILE_OFFSET_BITS=64)
ADD_COMPILE_OPTIONS(-I/usr/local/include -I. -O2 -Wall -DBSD=1)

ADD_SUBDIRECTORY(liveMedia)
ADD_SUBDIRECTORY(groupsock)
ADD_SUBDIRECTORY(UsageEnvironment)
ADD_SUBDIRECTORY(BasicUsageEnvironment)
ADD_SUBDIRECTORY(testProgs)
ADD_SUBDIRECTORY(mediaServer)
ADD_SUBDIRECTORY(proxyServer)
ADD_SUBDIRECTORY(hlsProxy)
