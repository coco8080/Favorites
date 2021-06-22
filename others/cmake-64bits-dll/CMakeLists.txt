set(BUILD_USE_64BITS on)
SET (LIBHELLO_SRC image_processing.c)       // image_processing 为目标文件
ADD_LIBRARY (image_processing SHARED ${LIBHELLO_SRC})
INSTALL(TARGETS image_processing RUNTIME DESTINATION F:\work\open-source\oled_display_gui\python_gui\image_processing\C_dll_source_code\lib)
SET_TARGET_PROPERTIES(image_processing PROPERTIES LINKER_LANGUAGE C)
