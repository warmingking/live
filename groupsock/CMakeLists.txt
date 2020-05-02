# CMakeLists.txt in groupsock

FILE(GLOB GROUPSOCK_SRCS
        include/*.hh
        *.hh
        *.h
        *.c
        *.cpp
        )

ADD_LIBRARY(groupsock STATIC ${GROUPSOCK_SRCS})
