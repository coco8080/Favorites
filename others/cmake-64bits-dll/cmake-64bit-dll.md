<!--
 * @Author: your name
 * @Date: 2021-06-22 13:25:28
 * @LastEditTime: 2021-06-22 13:34:31
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \Favorites\others\cmake_64bit_dll.md
-->
### Use CMake to build the 64-bits dll(windowns 下cmake生成动态链接库dll)

+ 在需要生成的 *dll* 目录下新建 *CMakeLists.tx* 文件
```
CMakeLists.tx
set(BUILD_USE_64BITS on)                                            // 设置 64 bits
SET (LIBHELLO_SRC ../erase.h)                                       // 后面那个参数填你自己需要构建dll的文件
ADD_LIBRARY (mylib0713 SHARED ${LIBHELLO_SRC})                      //  第一个参数为你需要构建的dll的名字，第二个为类型
INSTALL(TARGETS mylib0713 RUNTIME DESTINATION D:/mylib)             //指定dll的生成目录这里目录是D:/mylib，注意linux下是LIBRARY DESTINATION  windows下是 RUNTIME DESTINATION
SET_TARGET_PROPERTIES(mylib0713 PROPERTIES LINKER_LANGUAGE C)       //为你的dll设置linker
```
+ 在当前目录下执行 *cmake .*，注意后面有个点

+ 在当前目录下运行 *cmake --build .*
