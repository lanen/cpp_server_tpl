cmake_minimum_required (VERSION 2.8)

# 查找当前目录下的所有源文件
set (exe agent_server)
set (SRCS main.cpp

#    ../include/protoc/agent.pb.h
#    ../include/protoc/agent.pb.cc

#    Agent.hpp
#    Agent.cpp
)

configure_file( ../etc/log.properties etc/log.properties COPYONLY)

add_executable (${exe} ${SRCS})

#target_link_libraries(${exe} framework netutil protobuf log4cplusU ev)

install (TARGETS ${exe} RUNTIME DESTINATION bin)

