# CMakeLists.txt in UsageEnvironment

FILE(GLOB USAGE_ENVIRONMENT_SRCS
        include/*.hh
        *.hh
        *.h
        *.c
        *.cpp
        )

ADD_LIBRARY( UsageEnvironment STATIC ${USAGE_ENVIRONMENT_SRCS})
