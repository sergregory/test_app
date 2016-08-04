set(target "${TEST_APP_TOOLS}")

FILE(GLOB hdrs "*.h*")
FILE(GLOB srcs "*.cpp")

# VS2012 doesn't support correctly the tuples yet,
# see http://code.google.com/p/googletest/issues/detail?id=412
if(MSVC)
    ADD_DEFINITIONS(/D _VARIADIC_MAX=10)
endif()

ADD_EXECUTABLE(${target} ${srcs} ${hdrs})
TARGET_LINK_LIBRARIES(${target} ${TEST_APP_LIBRARY})
