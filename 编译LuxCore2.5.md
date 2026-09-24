
[LuxCore](https://github.com/LuxCoreRender/LuxCore)
依赖
[OpenEXR](https://github.com/AcademySoftwareFoundation/openexr)
[OpenImageIO](https://github.com/OpenImageIO/oiio)
[c-blosc](https://github.com/Blosc/c-blosc)
[embree](https://github.com/embree/embree)
[OpenImageDenoise](https://github.com/OpenImageDenoise/oidn)
[tbb](https://github.com/oneapi-src/oneTBB)
boost
zlib
libpng
libjpeg-turbo
libtiff

------
静态库
需要定义
OIIO_STATIC_DEFINE
去掉
OPENEXR_DLL
BOOST_ALL_DYN_LINK
BOOST_ALL_NO_LIB



---------

去掉python相关
去掉boost.python、boost.numpy依赖
修改CMakeLists.txt

```powershell
#	MESSAGE(FATAL_ERROR "--> Could not locate required Boost files - Please check ${BOOST_SEARCH_PATH}")

#add_subdirectory(src/pyluxcoretools)
```

修改src\luxcore\CMakeLists.txt

```powershell
#add_library(pyluxcore MODULE ${PYLUXCORE_SRCS} ${LUXCORE_LIB_SRCS} ${LUX_PARSER_SRC})

	#target_link_libraries(pyluxcore -Wl,-undefined -Wl,dynamic_lookup slg-core slg-film slg-kernels luxrays bcd opensubdiv openvdb ${BLOSC_LIBRARY} ${EMBREE_LIBRARY} ${OIDN_LIBRARY} ${TBB_LIBRARY} ${TIFF_LIBRARIES} ${TIFF_LIBRARIES} ${OPENEXR_LIBRARIES} ${PNG_LIBRARIES} ${JPEG_LIBRARIES})
    #SET_TARGET_PROPERTIES(pyluxcore PROPERTIES XCODE_ATTRIBUTE_DEPLOYMENT_POSTPROCESSING NO) # exclude pylux from strip, not possible
    #target_link_libraries(pyluxcore PRIVATE slg-core slg-film slg-kernels luxrays bcd opensubdiv openvdb ${BLOSC_LIBRARY} ${EMBREE_LIBRARY} ${OIDN_LIBRARY} ${TBB_LIBRARY} ${TIFF_LIBRARIES} ${TIFF_LIBRARIES} ${OPENEXR_LIBRARIES} ${PNG_LIBRARIES} ${JPEG_LIBRARIES})
    #set_target_properties(pyluxcore PROPERTIES PREFIX "")
 
	#set_target_properties(pyluxcore PROPERTIES SUFFIX ".pyd")
```
