cmake_minimum_required(VERSION 3.10.2)

# 项目名称
project("mycppapp")

# 添加 C++ 文件
add_library( native-lib
             SHARED
             src/main/cpp/native-lib.cpp )

# 查找日志库（通常需要在 Android 项目中链接日志库）
find_library( log-lib
              log )

# 链接日志库
target_link_libraries( native-lib
                       ${log-lib} )
