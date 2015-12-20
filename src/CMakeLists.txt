set(target ${TEST_APP_LIBRARY})

FILE(GLOB hdrs "*.h*" "${TEST_APP_INCLUDE}/*.h*")
FILE(GLOB srcs "*.cpp")

ADD_LIBRARY(${target} STATIC ${srcs} ${hdrs})
TARGET_LINK_LIBRARIES(${target} ${LIBRARY_DEPS})
