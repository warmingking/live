# CMakeLists.txt in BasicUsageEnvironment

FILE(GLOB BASIC_USAGE_ENVIRONMENT_SRCS
        include/*.hh
        *.hh
        *.h
        *.c
        *.cpp
        )

ADD_LIBRARY( BasicUsageEnvironment STATIC ${BASIC_USAGE_ENVIRONMENT_SRCS})
