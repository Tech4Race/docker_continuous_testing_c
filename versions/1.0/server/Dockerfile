FROM alpine:3.6

# -- Build Tools
# Install package as build-base dependencies but without g++, fortify-headers
# THis give a step at 97Mo instead of 159Mo
RUN apk --no-cache add gcc=6.3.0-r4 musl-dev=1.1.16-r14 libc-dev=0.7.1-r0 make=4.2.1-r0 

# -- Continuous Testing Tools (235Mo)
#     - cmocka for unit test
#     - valgrind for memory leak detection
#     - gcovr for test coverage information
RUN apk --no-cache add cmocka=1.1.0-r4 valgrind=3.12.0-r1 gcovr=3.3-r0

# Bash (usefull for developer to log inside the container)
RUN apk --no-cache add bash=4.3.48-r1
