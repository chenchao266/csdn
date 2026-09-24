```xml
<?xml version="1.0" encoding="utf-8"?>
<Project DefaultTargets="Build" ToolsVersion="15.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <ItemGroup Label="ProjectConfigurations">
    <ProjectConfiguration Include="Debug|x64">
      <Configuration>Debug</Configuration>
      <Platform>x64</Platform>
    </ProjectConfiguration>
    <ProjectConfiguration Include="Release|x64">
      <Configuration>Release</Configuration>
      <Platform>x64</Platform>
    </ProjectConfiguration>
    <ProjectConfiguration Include="MinSizeRel|x64">
      <Configuration>MinSizeRel</Configuration>
      <Platform>x64</Platform>
    </ProjectConfiguration>
    <ProjectConfiguration Include="RelWithDebInfo|x64">
      <Configuration>RelWithDebInfo</Configuration>
      <Platform>x64</Platform>
    </ProjectConfiguration>
  </ItemGroup>
  <PropertyGroup Label="Globals">
    <ProjectGuid>{4DBE2B18-F8E3-3CD8-A754-07C5532B687F}</ProjectGuid>
    <ProjectName>mxnet</ProjectName>
    <VCProjectUpgraderObjectName>NoUpgrade</VCProjectUpgraderObjectName>
    <WindowsTargetPlatformVersion>10.0.17763.0</WindowsTargetPlatformVersion>
    <PreferredToolArchitecture>x64</PreferredToolArchitecture>
  </PropertyGroup>
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.Default.props" />
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|x64'" Label="Configuration">
    <ConfigurationType>DynamicLibrary</ConfigurationType>
    <CharacterSet>MultiByte</CharacterSet>
    <PlatformToolset>v141</PlatformToolset>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|x64'" Label="Configuration">
    <ConfigurationType>DynamicLibrary</ConfigurationType>
    <CharacterSet>MultiByte</CharacterSet>
    <PlatformToolset>v141</PlatformToolset>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'" Label="Configuration">
    <ConfigurationType>DynamicLibrary</ConfigurationType>
    <CharacterSet>MultiByte</CharacterSet>
    <PlatformToolset>v141</PlatformToolset>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'" Label="Configuration">
    <ConfigurationType>DynamicLibrary</ConfigurationType>
    <CharacterSet>MultiByte</CharacterSet>
    <PlatformToolset>v141</PlatformToolset>
  </PropertyGroup>
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings">
      <Import Project="$(VCTargetsPath)\BuildCustomizations\CUDA 9.2.props" />
  </ImportGroup>
  <ImportGroup Label="PropertySheets">
    <Import Project="$(UserRootDir)\Microsoft.Cpp.$(Platform).user.props" Condition="exists('$(UserRootDir)\Microsoft.Cpp.$(Platform).user.props')" Label="LocalAppDataPlatform" />
  </ImportGroup>
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup>
    <_ProjectFileVersion>10.0.20506.1</_ProjectFileVersion>
    <OutDir Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(MXNET_ROOT)\x64\Debug\</OutDir>
    <IntDir Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">mxnet.dir\Debug\</IntDir>
    <TargetName Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">libmxnet</TargetName>
    <TargetExt Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">.dll</TargetExt>
    <LinkIncremental Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">true</LinkIncremental>
    <GenerateManifest Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">true</GenerateManifest>
    <OutDir Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(MXNET_ROOT)\x64\Release\</OutDir>
    <IntDir Condition="'$(Configuration)|$(Platform)'=='Release|x64'">mxnet.dir\Release\</IntDir>
    <TargetName Condition="'$(Configuration)|$(Platform)'=='Release|x64'">libmxnet</TargetName>
    <TargetExt Condition="'$(Configuration)|$(Platform)'=='Release|x64'">.dll</TargetExt>
    <LinkIncremental Condition="'$(Configuration)|$(Platform)'=='Release|x64'">false</LinkIncremental>
    <GenerateManifest Condition="'$(Configuration)|$(Platform)'=='Release|x64'">true</GenerateManifest>
    <OutDir Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">$(MXNET_ROOT)\x64\MinSizeRel\</OutDir>
    <IntDir Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">mxnet.dir\MinSizeRel\</IntDir>
    <TargetName Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">libmxnet</TargetName>
    <TargetExt Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">.dll</TargetExt>
    <LinkIncremental Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">false</LinkIncremental>
    <GenerateManifest Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">true</GenerateManifest>
    <OutDir Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">$(MXNET_ROOT)\x64\RelWithDebInfo\</OutDir>
    <IntDir Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">mxnet.dir\RelWithDebInfo\</IntDir>
    <TargetName Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">libmxnet</TargetName>
    <TargetExt Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">.dll</TargetExt>
    <LinkIncremental Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">true</LinkIncremental>
    <GenerateManifest Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">true</GenerateManifest>
  </PropertyGroup>
  <ItemDefinitionGroup Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">
    <ClCompile>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <AdditionalOptions>%(AdditionalOptions) /bigobj</AdditionalOptions>
      <AssemblerListingLocation>Debug/</AssemblerListingLocation>
      <BasicRuntimeChecks>EnableFastChecks</BasicRuntimeChecks>
      <CompileAs>CompileAsCpp</CompileAs>
      <DebugInformationFormat>ProgramDatabase</DebugInformationFormat>
      <ExceptionHandling>Sync</ExceptionHandling>
      <InlineFunctionExpansion>Disabled</InlineFunctionExpansion>
      <MultiProcessorCompilation>true</MultiProcessorCompilation>
      <OpenMPSupport>true</OpenMPSupport>
      <Optimization>Disabled</Optimization>
      <PrecompiledHeader>NotUsing</PrecompiledHeader>
      <RuntimeLibrary>MultiThreadedDebug</RuntimeLibrary>
      <PreprocessorDefinitions>WIN32_LEAN_AND_MEAN;DMLC_USE_CXX11;MSHADOW_IN_CXX11;_SCL_SECURE_NO_WARNINGS;_CRT_SECURE_NO_WARNINGS;MXNET_EXPORTS;NNVM_EXPORTS;DMLC_STRICT_CXX11;NOMINMAX;MSHADOW_USE_CUDA=1;MXNET_USE_NCCL=0;MSHADOW_INT64_TENSOR_SIZE=0;MSHADOW_USE_CBLAS=1;MSHADOW_USE_MKL=0;MXNET_USE_BLAS_OPEN=1;MSHADOW_USE_SSE=0;MSHADOW_USE_F16C=0;MSHADOW_FORCE_STREAM;USE_CUDNN;MXNET_USE_OPENCV=0;MXNET_USE_OPENMP=1;MXNET_USE_LAPACK=1;MSHADOW_USE_CUDNN=1;MXNET_USE_CUDA=1;MXNET_USE_SIGNAL_HANDLER=1;USE_CPP_PACKAGE=1;CMAKE_INTDIR="Debug";mxnet_EXPORTS;%(PreprocessorDefinitions)</PreprocessorDefinitions>
      <ObjectFileName>$(IntDir)</ObjectFileName>
    </ClCompile>
    <ResourceCompile>
      <PreprocessorDefinitions>WIN32;_DEBUG;WIN32_LEAN_AND_MEAN;DMLC_USE_CXX11;MSHADOW_IN_CXX11;_SCL_SECURE_NO_WARNINGS;_CRT_SECURE_NO_WARNINGS;MXNET_EXPORTS;NNVM_EXPORTS;DMLC_STRICT_CXX11;NOMINMAX;MSHADOW_USE_CUDA=1;MXNET_USE_NCCL=0;MSHADOW_INT64_TENSOR_SIZE=0;MSHADOW_USE_CBLAS=1;MSHADOW_USE_MKL=0;MXNET_USE_BLAS_OPEN=1;MSHADOW_USE_SSE=0;MSHADOW_USE_F16C=0;MSHADOW_FORCE_STREAM;USE_CUDNN;MXNET_USE_OPENCV=0;MXNET_USE_OPENMP=1;MXNET_USE_LAPACK=1;MSHADOW_USE_CUDNN=1;MXNET_USE_CUDA=1;MXNET_USE_SIGNAL_HANDLER=1;USE_CPP_PACKAGE=1;CMAKE_INTDIR=\"Debug\";mxnet_EXPORTS;%(PreprocessorDefinitions)</PreprocessorDefinitions>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
    </ResourceCompile>
    <Midl>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <OutputDirectory>$(ProjectDir)/$(IntDir)</OutputDirectory>
      <HeaderFileName>%(Filename).h</HeaderFileName>
      <TypeLibraryName>%(Filename).tlb</TypeLibraryName>
      <InterfaceIdentifierFileName>%(Filename)_i.c</InterfaceIdentifierFileName>
      <ProxyFileName>%(Filename)_p.c</ProxyFileName>
    </Midl>
    <Link>
      <AdditionalDependencies>$(OPENBLAS_ROOT)\lib\Release\libopenblas.dll.a;$(CUDA_PATH)\lib\x64\cudart.lib;$(CUDA_PATH)\lib\x64\curand.lib;$(CUDA_PATH)\lib\x64\cublas.lib;$(CUDA_PATH)\lib\x64\cudart.lib;$(CUDA_PATH)\lib\x64\curand.lib;$(CUDA_PATH)\lib\x64\cublas.lib;$(CUDA_PATH)\lib\x64\cudnn.lib;$(CUDA_PATH)\lib\x64\cudnn.lib;$(CUDA_PATH)\lib\x64\cufft.lib\..\cufft.lib;$(CUDA_PATH)\lib\x64\cusolver.lib\..\cusolver.lib;3rdparty\dmlc-core\Debug\dmlc.lib;kernel32.lib;user32.lib;gdi32.lib;winspool.lib;shell32.lib;ole32.lib;oleaut32.lib;uuid.lib;comdlg32.lib;advapi32.lib</AdditionalDependencies>
      <AdditionalLibraryDirectories>$(CUDA_PATH)/lib/win32;$(CUDA_PATH)/lib/win32/$(Configuration);$(CUDA_PATH)/lib/x64;$(CUDA_PATH)/lib/x64/$(Configuration);%(AdditionalLibraryDirectories)</AdditionalLibraryDirectories>
      <AdditionalOptions>%(AdditionalOptions) /machine:x64</AdditionalOptions>
      <GenerateDebugInformation>true</GenerateDebugInformation>
      <IgnoreSpecificDefaultLibraries>%(IgnoreSpecificDefaultLibraries)</IgnoreSpecificDefaultLibraries>
      <ImportLibrary>$(MXNET_ROOT)/x64/Debug/libmxnet.lib</ImportLibrary>
      <ProgramDataBaseFile>$(MXNET_ROOT)/x64/Debug/libmxnet.pdb</ProgramDataBaseFile>
      <SubSystem>Console</SubSystem>
    </Link>
    <CudaCompile>
      <CodeGeneration>compute_50,sm_50;compute_52,sm_52;compute_60,sm_60;compute_61,sm_61;compute_70,sm_70;compute_75,sm_75</CodeGeneration>
      <TargetMachinePlatform>64</TargetMachinePlatform>
      <AdditionalCompilerOptions>/bigobj</AdditionalCompilerOptions>
    </CudaCompile>
    <ProjectReference>
      <LinkLibraryDependencies>false</LinkLibraryDependencies>
    </ProjectReference>
  </ItemDefinitionGroup>
  <ItemDefinitionGroup Condition="'$(Configuration)|$(Platform)'=='Release|x64'">
    <ClCompile>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <AdditionalOptions>%(AdditionalOptions) /bigobj</AdditionalOptions>
      <AssemblerListingLocation>Release/</AssemblerListingLocation>
      <CompileAs>CompileAsCpp</CompileAs>
      <ExceptionHandling>Sync</ExceptionHandling>
      <FunctionLevelLinking>true</FunctionLevelLinking>
      <InlineFunctionExpansion>AnySuitable</InlineFunctionExpansion>
      <MultiProcessorCompilation>true</MultiProcessorCompilation>
      <OpenMPSupport>true</OpenMPSupport>
      <Optimization>MaxSpeed</Optimization>
      <PrecompiledHeader>NotUsing</PrecompiledHeader>
      <RuntimeLibrary>MultiThreaded</RuntimeLibrary>
      <PreprocessorDefinitions>NDEBUG;WIN32_LEAN_AND_MEAN;DMLC_USE_CXX11;MSHADOW_IN_CXX11;_SCL_SECURE_NO_WARNINGS;_CRT_SECURE_NO_WARNINGS;MXNET_EXPORTS;NNVM_EXPORTS;DMLC_STRICT_CXX11;NOMINMAX;MSHADOW_USE_CUDA=1;MXNET_USE_NCCL=0;MSHADOW_INT64_TENSOR_SIZE=0;MSHADOW_USE_CBLAS=1;MSHADOW_USE_MKL=0;MXNET_USE_BLAS_OPEN=1;MSHADOW_USE_SSE=0;MSHADOW_USE_F16C=0;MSHADOW_FORCE_STREAM;USE_CUDNN;MXNET_USE_OPENCV=0;MXNET_USE_OPENMP=1;MXNET_USE_LAPACK=1;MSHADOW_USE_CUDNN=1;MXNET_USE_CUDA=1;MXNET_USE_SIGNAL_HANDLER=1;USE_CPP_PACKAGE=1;CMAKE_INTDIR="Release";mxnet_EXPORTS;%(PreprocessorDefinitions)</PreprocessorDefinitions>
      <ObjectFileName>$(IntDir)</ObjectFileName>
      <DebugInformationFormat>
      </DebugInformationFormat>
    </ClCompile>
    <ResourceCompile>
      <PreprocessorDefinitions>WIN32;NDEBUG;WIN32_LEAN_AND_MEAN;DMLC_USE_CXX11;MSHADOW_IN_CXX11;_SCL_SECURE_NO_WARNINGS;_CRT_SECURE_NO_WARNINGS;MXNET_EXPORTS;NNVM_EXPORTS;DMLC_STRICT_CXX11;NOMINMAX;MSHADOW_USE_CUDA=1;MXNET_USE_NCCL=0;MSHADOW_INT64_TENSOR_SIZE=0;MSHADOW_USE_CBLAS=1;MSHADOW_USE_MKL=0;MXNET_USE_BLAS_OPEN=1;MSHADOW_USE_SSE=0;MSHADOW_USE_F16C=0;MSHADOW_FORCE_STREAM;USE_CUDNN;MXNET_USE_OPENCV=0;MXNET_USE_OPENMP=1;MXNET_USE_LAPACK=1;MSHADOW_USE_CUDNN=1;MXNET_USE_CUDA=1;MXNET_USE_SIGNAL_HANDLER=1;USE_CPP_PACKAGE=1;CMAKE_INTDIR=\"Release\";mxnet_EXPORTS;%(PreprocessorDefinitions)</PreprocessorDefinitions>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
    </ResourceCompile>
    <Midl>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <OutputDirectory>$(ProjectDir)/$(IntDir)</OutputDirectory>
      <HeaderFileName>%(Filename).h</HeaderFileName>
      <TypeLibraryName>%(Filename).tlb</TypeLibraryName>
      <InterfaceIdentifierFileName>%(Filename)_i.c</InterfaceIdentifierFileName>
      <ProxyFileName>%(Filename)_p.c</ProxyFileName>
    </Midl>
    <Link>
      <AdditionalDependencies>$(OPENBLAS_ROOT)\lib\Release\libopenblas.dll.a;$(CUDA_PATH)\lib\x64\cudart.lib;$(CUDA_PATH)\lib\x64\curand.lib;$(CUDA_PATH)\lib\x64\cublas.lib;$(CUDA_PATH)\lib\x64\cudart.lib;$(CUDA_PATH)\lib\x64\curand.lib;$(CUDA_PATH)\lib\x64\cublas.lib;$(CUDA_PATH)\lib\x64\cudnn.lib;$(CUDA_PATH)\lib\x64\cudnn.lib;$(CUDA_PATH)\lib\x64\cufft.lib\..\cufft.lib;$(CUDA_PATH)\lib\x64\cusolver.lib\..\cusolver.lib;3rdparty\dmlc-core\Release\dmlc.lib;kernel32.lib;user32.lib;gdi32.lib;winspool.lib;shell32.lib;ole32.lib;oleaut32.lib;uuid.lib;comdlg32.lib;advapi32.lib</AdditionalDependencies>
      <AdditionalLibraryDirectories>$(CUDA_PATH)/lib/win32;$(CUDA_PATH)/lib/win32/$(Configuration);$(CUDA_PATH)/lib/x64;$(CUDA_PATH)/lib/x64/$(Configuration);%(AdditionalLibraryDirectories)</AdditionalLibraryDirectories>
      <AdditionalOptions>%(AdditionalOptions) /machine:x64</AdditionalOptions>
      <EnableCOMDATFolding>true</EnableCOMDATFolding>
      <GenerateDebugInformation>false</GenerateDebugInformation>
      <IgnoreSpecificDefaultLibraries>%(IgnoreSpecificDefaultLibraries)</IgnoreSpecificDefaultLibraries>
      <ImportLibrary>$(MXNET_ROOT)/x64/Release/libmxnet.lib</ImportLibrary>
      <OptimizeReferences>true</OptimizeReferences>
      <ProgramDataBaseFile>$(MXNET_ROOT)/x64/Release/libmxnet.pdb</ProgramDataBaseFile>
      <SubSystem>Console</SubSystem>
    </Link>
    <CudaCompile>
      <CodeGeneration>compute_50,sm_50;compute_52,sm_52;compute_60,sm_60;compute_61,sm_61;compute_70,sm_70;compute_75,sm_75</CodeGeneration>
      <TargetMachinePlatform>64</TargetMachinePlatform>
      <AdditionalCompilerOptions>/bigobj</AdditionalCompilerOptions>
    </CudaCompile>
    <ProjectReference>
      <LinkLibraryDependencies>false</LinkLibraryDependencies>
    </ProjectReference>
  </ItemDefinitionGroup>
  <ItemDefinitionGroup Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">
    <ClCompile>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <AdditionalOptions>%(AdditionalOptions) /bigobj</AdditionalOptions>
      <AssemblerListingLocation>MinSizeRel/</AssemblerListingLocation>
      <CompileAs>CompileAsCpp</CompileAs>
      <ExceptionHandling>Sync</ExceptionHandling>
      <FunctionLevelLinking>true</FunctionLevelLinking>
      <InlineFunctionExpansion>OnlyExplicitInline</InlineFunctionExpansion>
      <MultiProcessorCompilation>true</MultiProcessorCompilation>
      <OpenMPSupport>true</OpenMPSupport>
      <Optimization>MinSpace</Optimization>
      <PrecompiledHeader>NotUsing</PrecompiledHeader>
      <RuntimeLibrary>MultiThreaded</RuntimeLibrary>
      <PreprocessorDefinitions>NDEBUG;WIN32_LEAN_AND_MEAN;DMLC_USE_CXX11;MSHADOW_IN_CXX11;_SCL_SECURE_NO_WARNINGS;_CRT_SECURE_NO_WARNINGS;MXNET_EXPORTS;NNVM_EXPORTS;DMLC_STRICT_CXX11;NOMINMAX;MSHADOW_USE_CUDA=1;MXNET_USE_NCCL=0;MSHADOW_INT64_TENSOR_SIZE=0;MSHADOW_USE_CBLAS=1;MSHADOW_USE_MKL=0;MXNET_USE_BLAS_OPEN=1;MSHADOW_USE_SSE=0;MSHADOW_USE_F16C=0;MSHADOW_FORCE_STREAM;USE_CUDNN;MXNET_USE_OPENCV=0;MXNET_USE_OPENMP=1;MXNET_USE_LAPACK=1;MSHADOW_USE_CUDNN=1;MXNET_USE_CUDA=1;MXNET_USE_SIGNAL_HANDLER=1;USE_CPP_PACKAGE=1;CMAKE_INTDIR="MinSizeRel";mxnet_EXPORTS;%(PreprocessorDefinitions)</PreprocessorDefinitions>
      <ObjectFileName>$(IntDir)</ObjectFileName>
      <DebugInformationFormat>
      </DebugInformationFormat>
    </ClCompile>
    <ResourceCompile>
      <PreprocessorDefinitions>WIN32;NDEBUG;WIN32_LEAN_AND_MEAN;DMLC_USE_CXX11;MSHADOW_IN_CXX11;_SCL_SECURE_NO_WARNINGS;_CRT_SECURE_NO_WARNINGS;MXNET_EXPORTS;NNVM_EXPORTS;DMLC_STRICT_CXX11;NOMINMAX;MSHADOW_USE_CUDA=1;MXNET_USE_NCCL=0;MSHADOW_INT64_TENSOR_SIZE=0;MSHADOW_USE_CBLAS=1;MSHADOW_USE_MKL=0;MXNET_USE_BLAS_OPEN=1;MSHADOW_USE_SSE=0;MSHADOW_USE_F16C=0;MSHADOW_FORCE_STREAM;USE_CUDNN;MXNET_USE_OPENCV=0;MXNET_USE_OPENMP=1;MXNET_USE_LAPACK=1;MSHADOW_USE_CUDNN=1;MXNET_USE_CUDA=1;MXNET_USE_SIGNAL_HANDLER=1;USE_CPP_PACKAGE=1;CMAKE_INTDIR=\"MinSizeRel\";mxnet_EXPORTS;%(PreprocessorDefinitions)</PreprocessorDefinitions>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
    </ResourceCompile>
    <Midl>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <OutputDirectory>$(ProjectDir)/$(IntDir)</OutputDirectory>
      <HeaderFileName>%(Filename).h</HeaderFileName>
      <TypeLibraryName>%(Filename).tlb</TypeLibraryName>
      <InterfaceIdentifierFileName>%(Filename)_i.c</InterfaceIdentifierFileName>
      <ProxyFileName>%(Filename)_p.c</ProxyFileName>
    </Midl>
    <Link>
      <AdditionalDependencies>$(OPENBLAS_ROOT)\lib\Release\libopenblas.dll.a;$(CUDA_PATH)\lib\x64\cudart.lib;$(CUDA_PATH)\lib\x64\curand.lib;$(CUDA_PATH)\lib\x64\cublas.lib;$(CUDA_PATH)\lib\x64\cudart.lib;$(CUDA_PATH)\lib\x64\curand.lib;$(CUDA_PATH)\lib\x64\cublas.lib;$(CUDA_PATH)\lib\x64\cudnn.lib;$(CUDA_PATH)\lib\x64\cudnn.lib;$(CUDA_PATH)\lib\x64\cufft.lib\..\cufft.lib;$(CUDA_PATH)\lib\x64\cusolver.lib\..\cusolver.lib;3rdparty\dmlc-core\MinSizeRel\dmlc.lib;kernel32.lib;user32.lib;gdi32.lib;winspool.lib;shell32.lib;ole32.lib;oleaut32.lib;uuid.lib;comdlg32.lib;advapi32.lib</AdditionalDependencies>
      <AdditionalLibraryDirectories>$(CUDA_PATH)/lib/win32;$(CUDA_PATH)/lib/win32/$(Configuration);$(CUDA_PATH)/lib/x64;$(CUDA_PATH)/lib/x64/$(Configuration);%(AdditionalLibraryDirectories)</AdditionalLibraryDirectories>
      <AdditionalOptions>%(AdditionalOptions) /machine:x64</AdditionalOptions>
      <EnableCOMDATFolding>true</EnableCOMDATFolding>
      <GenerateDebugInformation>false</GenerateDebugInformation>
      <IgnoreSpecificDefaultLibraries>%(IgnoreSpecificDefaultLibraries)</IgnoreSpecificDefaultLibraries>
      <ImportLibrary>$(MXNET_ROOT)/x64/MinSizeRel/libmxnet.lib</ImportLibrary>
      <OptimizeReferences>true</OptimizeReferences>
      <ProgramDataBaseFile>$(MXNET_ROOT)/x64/MinSizeRel/libmxnet.pdb</ProgramDataBaseFile>
      <SubSystem>Console</SubSystem>
    </Link>
    <ProjectReference>
      <LinkLibraryDependencies>false</LinkLibraryDependencies>
    </ProjectReference>
  </ItemDefinitionGroup>
  <ItemDefinitionGroup Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">
    <ClCompile>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <AdditionalOptions>%(AdditionalOptions) /bigobj</AdditionalOptions>
      <AssemblerListingLocation>RelWithDebInfo/</AssemblerListingLocation>
      <CompileAs>CompileAsCpp</CompileAs>
      <DebugInformationFormat>ProgramDatabase</DebugInformationFormat>
      <ExceptionHandling>Sync</ExceptionHandling>
      <FunctionLevelLinking>true</FunctionLevelLinking>
      <InlineFunctionExpansion>OnlyExplicitInline</InlineFunctionExpansion>
      <MultiProcessorCompilation>true</MultiProcessorCompilation>
      <OpenMPSupport>true</OpenMPSupport>
      <Optimization>MaxSpeed</Optimization>
      <PrecompiledHeader>NotUsing</PrecompiledHeader>
      <RuntimeLibrary>MultiThreaded</RuntimeLibrary>
      <PreprocessorDefinitions>NDEBUG;WIN32_LEAN_AND_MEAN;DMLC_USE_CXX11;MSHADOW_IN_CXX11;_SCL_SECURE_NO_WARNINGS;_CRT_SECURE_NO_WARNINGS;MXNET_EXPORTS;NNVM_EXPORTS;DMLC_STRICT_CXX11;NOMINMAX;MSHADOW_USE_CUDA=1;MXNET_USE_NCCL=0;MSHADOW_INT64_TENSOR_SIZE=0;MSHADOW_USE_CBLAS=1;MSHADOW_USE_MKL=0;MXNET_USE_BLAS_OPEN=1;MSHADOW_USE_SSE=0;MSHADOW_USE_F16C=0;MSHADOW_FORCE_STREAM;USE_CUDNN;MXNET_USE_OPENCV=0;MXNET_USE_OPENMP=1;MXNET_USE_LAPACK=1;MSHADOW_USE_CUDNN=1;MXNET_USE_CUDA=1;MXNET_USE_SIGNAL_HANDLER=1;USE_CPP_PACKAGE=1;CMAKE_INTDIR="RelWithDebInfo";mxnet_EXPORTS;%(PreprocessorDefinitions)</PreprocessorDefinitions>
      <ObjectFileName>$(IntDir)</ObjectFileName>
    </ClCompile>
    <ResourceCompile>
      <PreprocessorDefinitions>WIN32;NDEBUG;WIN32_LEAN_AND_MEAN;DMLC_USE_CXX11;MSHADOW_IN_CXX11;_SCL_SECURE_NO_WARNINGS;_CRT_SECURE_NO_WARNINGS;MXNET_EXPORTS;NNVM_EXPORTS;DMLC_STRICT_CXX11;NOMINMAX;MSHADOW_USE_CUDA=1;MXNET_USE_NCCL=0;MSHADOW_INT64_TENSOR_SIZE=0;MSHADOW_USE_CBLAS=1;MSHADOW_USE_MKL=0;MXNET_USE_BLAS_OPEN=1;MSHADOW_USE_SSE=0;MSHADOW_USE_F16C=0;MSHADOW_FORCE_STREAM;USE_CUDNN;MXNET_USE_OPENCV=0;MXNET_USE_OPENMP=1;MXNET_USE_LAPACK=1;MSHADOW_USE_CUDNN=1;MXNET_USE_CUDA=1;MXNET_USE_SIGNAL_HANDLER=1;USE_CPP_PACKAGE=1;CMAKE_INTDIR=\"RelWithDebInfo\";mxnet_EXPORTS;%(PreprocessorDefinitions)</PreprocessorDefinitions>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
    </ResourceCompile>
    <Midl>
      <AdditionalIncludeDirectories>$(MXNET_ROOT)\include;$(MXNET_ROOT)\src;$(MXNET_ROOT)\3rdparty\mshadow;$(MXNET_ROOT)\3rdparty\nvidia_cub;$(MXNET_ROOT)\3rdparty\tvm\nnvm\include;$(MXNET_ROOT)\3rdparty\tvm\include;$(MXNET_ROOT)\3rdparty\dmlc-core\include;$(MXNET_ROOT)\3rdparty\dlpack\include;$(OPENBLAS_ROOT)\include\openblas;$(CUDA_PATH)\include;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <OutputDirectory>$(ProjectDir)/$(IntDir)</OutputDirectory>
      <HeaderFileName>%(Filename).h</HeaderFileName>
      <TypeLibraryName>%(Filename).tlb</TypeLibraryName>
      <InterfaceIdentifierFileName>%(Filename)_i.c</InterfaceIdentifierFileName>
      <ProxyFileName>%(Filename)_p.c</ProxyFileName>
    </Midl>
    <Link>
      <AdditionalDependencies>$(OPENBLAS_ROOT)\lib\Release\libopenblas.dll.a;$(CUDA_PATH)\lib\x64\cudart.lib;$(CUDA_PATH)\lib\x64\curand.lib;$(CUDA_PATH)\lib\x64\cublas.lib;$(CUDA_PATH)\lib\x64\cudart.lib;$(CUDA_PATH)\lib\x64\curand.lib;$(CUDA_PATH)\lib\x64\cublas.lib;$(CUDA_PATH)\lib\x64\cudnn.lib;$(CUDA_PATH)\lib\x64\cudnn.lib;$(CUDA_PATH)\lib\x64\cufft.lib\..\cufft.lib;$(CUDA_PATH)\lib\x64\cusolver.lib\..\cusolver.lib;3rdparty\dmlc-core\RelWithDebInfo\dmlc.lib;kernel32.lib;user32.lib;gdi32.lib;winspool.lib;shell32.lib;ole32.lib;oleaut32.lib;uuid.lib;comdlg32.lib;advapi32.lib</AdditionalDependencies>
      <AdditionalLibraryDirectories>$(CUDA_PATH)/lib/win32;$(CUDA_PATH)/lib/win32/$(Configuration);$(CUDA_PATH)/lib/x64;$(CUDA_PATH)/lib/x64/$(Configuration);%(AdditionalLibraryDirectories)</AdditionalLibraryDirectories>
      <AdditionalOptions>%(AdditionalOptions) /machine:x64</AdditionalOptions>
      <EnableCOMDATFolding>true</EnableCOMDATFolding>
      <GenerateDebugInformation>true</GenerateDebugInformation>
      <IgnoreSpecificDefaultLibraries>%(IgnoreSpecificDefaultLibraries)</IgnoreSpecificDefaultLibraries>
      <ImportLibrary>$(MXNET_ROOT)/x64/RelWithDebInfo/libmxnet.lib</ImportLibrary>
      <OptimizeReferences>true</OptimizeReferences>
      <ProgramDataBaseFile>$(MXNET_ROOT)/x64/RelWithDebInfo/libmxnet.pdb</ProgramDataBaseFile>
      <SubSystem>Console</SubSystem>
    </Link>
    <ProjectReference>
      <LinkLibraryDependencies>false</LinkLibraryDependencies>
    </ProjectReference>
  </ItemDefinitionGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\common\random_generator.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\common\utils.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\kvstore\gradient_compression.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\kvstore\kvstore_utils.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\ndarray\ndarray_function.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\batch_norm_v1.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\bilinear_sampler.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\adamw.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\adaptive_avg_pooling.cu"/> 
    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\all_finite.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\bilinear_resize.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\boolean_mask.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\bounding_box.cu"/> 
    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\count_sketch.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\deformable_convolution.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\deformable_psroi_pooling.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\dgl_graph.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\fft.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\gradient_multiplier_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\hawkes_ll.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\ifft.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\index_array.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\index_copy.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\multi_proposal.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\multibox_detection.cu"/>
      
    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\multibox_prior.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\multibox_target.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\optimizer_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\proposal.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\psroi_pooling.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\quadratic_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\roi_align.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\sync_batch_norm.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\contrib\transformer.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\convolution_v1.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\correlation.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\crop.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\custom\native_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\grid_generator.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\identity_attach_KL_sparse_reg.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\image\image_random.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\image\resize.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\instance_norm.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\l2_normalization.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\leaky_relu.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\loss_binary_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\make_loss.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\activation.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\batch_norm.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\concat.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\convolution.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\ctc_loss.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_batch_norm.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\deconvolution.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\dropout.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\fully_connected.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\layer_norm.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\lrn.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\moments.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\pooling.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\softmax.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\softmax_activation.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\nn\upsampling.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\optimizer_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\pad.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\pooling_v1.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\quantization\dequantize.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantize.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantize_v2.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_conv.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_flatten.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_fully_connected.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_pooling.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\quantization\requantize.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\random\multisample_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\random\sample_multinomial_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\random\sample_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\random\shuffle_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\regression_output.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\rnn.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\roi_pooling.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\sequence_last.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\sequence_mask.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\sequence_reverse.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\slice_channel.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\softmax_output.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\spatial_transformer.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\subgraph\tensorrt\tensorrt.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\svm_output.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\swapaxis.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\amp_cast.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\broadcast_reduce_op_index.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\broadcast_reduce_op_value.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\cast_storage.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\control_flow_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\diag_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\dot.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_broadcast_op_basic.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_broadcast_op_extended.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_broadcast_op_logic.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op_basic.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op_extended.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op_logic.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_scalar_op_basic.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_scalar_op_extended.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_scalar_op_logic.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_scatter_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_sum.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_unary_op_basic.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_unary_op_trig.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\histogram.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\indexing_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\init_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\la_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\matrix_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\ordering_op.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\ravel.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\sparse_retain.cu"/>

    
  </ItemGroup>
  <ItemGroup>
    <CudaCompile Include="$(MXNET_ROOT)\src\operator\tensor\square_sum.cu"/>

    
  </ItemGroup>
  <ItemGroup>
 
  </ItemGroup>
  <ItemGroup>
    <ClInclude Include="$(MXNET_ROOT)\include\mkldnn\mkldnn.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mkldnn\mkldnn_types.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\base.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\c_api.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\c_api_error.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\c_api_test.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\c_predict_api.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\engine.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\executor.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\graph_attr_types.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\imperative.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\io.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\kvstore.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\libinfo.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\ndarray.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\op_attr_types.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\operator.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\operator_util.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\random_generator.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\resource.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\rtc.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\storage.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\tensor_blob.h" />
    <ClInclude Include="$(MXNET_ROOT)\include\mxnet\tuple.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_api.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\c_api\c_api_common.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_api_error.cc">
      <ObjectFileName>$(IntDir)/src/c_api/c_api_error.cc.obj</ObjectFileName>
    </ClCompile>
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_api_executor.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_api_function.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_api_ndarray.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_api_profile.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_api_symbolic.cc">
      <ObjectFileName>$(IntDir)/src/c_api/c_api_symbolic.cc.obj</ObjectFileName>
    </ClCompile>
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_api_test.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\c_api\c_predict_api.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\common\cuda_utils.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\common\exec_utils.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\common\lazy_alloc_array.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\common\object_pool.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\common\rtc.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\common\static_array.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\common\utils.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\common\utils.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\engine\engine.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\engine\engine_impl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\engine\naive_engine.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\engine\openmp.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\engine\openmp.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\engine\stream_manager.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\engine\thread_pool.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\engine\threaded_engine.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\engine\threaded_engine.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\engine\threaded_engine_perdevice.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\engine\threaded_engine_pooled.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\executor\attach_op_execs_pass.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\executor\attach_op_resource_pass.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\executor\exec_pass.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\executor\graph_executor.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\executor\graph_executor.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\executor\infer_graph_attr_pass.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\executor\inplace_addto_detect_pass.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\imperative\cached_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\imperative\cached_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\imperative\imperative.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\imperative\imperative_utils.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\imperative\imperative_utils.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\initialize.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\image_aug_default.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\image_augmenter.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\image_det_aug_default.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\image_io.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\image_iter_common.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\image_recordio.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\inst_vector.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\io.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\iter_batchloader.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\iter_csv.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\iter_image_det_recordio.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\iter_image_recordio.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\iter_image_recordio_2.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\iter_libsvm.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\io\iter_mnist.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\iter_normalize.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\iter_prefetcher.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\iter_sparse.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\iter_sparse_batchloader.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\iter_sparse_prefetcher.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\io\opencv_compatibility.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\comm.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\comm_tree.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\gpu_topology.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\gradient_compression-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\kvstore\gradient_compression.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\gradient_compression.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\kvstore\kvstore.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\kvstore_dist.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\kvstore_dist_server.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\kvstore_local.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\kvstore_nccl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\kvstore\kvstore_utils.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\kvstore\kvstore_utils.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\libinfo.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\ndarray\ndarray.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\ndarray\ndarray_function-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\ndarray\ndarray_function.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\ndarray\ndarray_function.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\nnvm\gradient.cc">
      <ObjectFileName>$(IntDir)/src/nnvm/gradient.cc.obj</ObjectFileName>
    </ClCompile>
    <ClInclude Include="$(MXNET_ROOT)\src\nnvm\graph_algorithm.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\nnvm\graph_editor.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\nnvm\legacy_json_util.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\nnvm\legacy_op_util.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\nnvm\plan_memory.cc">
      <ObjectFileName>$(IntDir)/src/nnvm/plan_memory.cc.obj</ObjectFileName>
    </ClCompile>
    <ClCompile Include="$(MXNET_ROOT)\src\nnvm\tvm_bridge.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\batch_norm_v1-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\batch_norm_v1.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\bilinear_sampler-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\bilinear_sampler.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\c_lapack_api.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\c_lapack_api.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\channel_op_common.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\adamw-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\adamw.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\adaptive_avg_pooling-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\adaptive_avg_pooling.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\all_finite-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\all_finite.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\amp_graph_pass.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\bilinear_resize-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\bilinear_resize.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\boolean_mask-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\boolean_mask.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\bounding_box-common.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\bounding_box-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\bounding_box.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\count_sketch-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\count_sketch.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\deformable_convolution-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\deformable_convolution.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\deformable_psroi_pooling-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\deformable_psroi_pooling.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\dgl_graph-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\dgl_graph.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\erfinv-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\fft-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\fft.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\gradient_multiplier_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\hawkes_ll-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\hawkes_ll.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\ifft-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\ifft.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\index_array-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\index_array.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\index_copy-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\index_copy.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\krprod.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\krprod.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\multi_proposal-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\multi_proposal.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\multibox_detection-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\multibox_detection.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\multibox_prior-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\multibox_prior.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\multibox_target-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\multibox_target.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\nn\deformable_im2col.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\nnz.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\optimizer_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\optimizer_op.cc">
      <ObjectFileName>$(IntDir)/src/operator/contrib/optimizer_op.cc.obj</ObjectFileName>
    </ClCompile>
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\proposal-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\proposal.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\psroi_pooling-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\psroi_pooling.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\quadratic_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\quadratic_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\roi_align-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\roi_align.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\sync_batch_norm-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\sync_batch_norm.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\contrib\transformer-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\contrib\transformer.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\control_flow.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\convolution_v1-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\convolution_v1.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\correlation-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\correlation.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\crop-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\crop.cc">
      <ObjectFileName>$(IntDir)/src/operator/crop.cc.obj</ObjectFileName>
    </ClCompile>
    <ClCompile Include="$(MXNET_ROOT)\src\operator\cross_device_copy.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\cudnn_bilinear_sampler-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\cudnn_lrn-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\cudnn_spatial_transformer-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\custom\custom-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\custom\custom.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\custom\native_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\custom\native_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\custom\ndarray_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\custom\ndarray_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\elemwise_op_common.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\grid_generator-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\grid_generator.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\identity_attach_KL_sparse_reg-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\identity_attach_KL_sparse_reg.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\image\crop-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\image\crop.cc">
      <ObjectFileName>$(IntDir)/src/operator/image/crop.cc.obj</ObjectFileName>
    </ClCompile>
    <ClInclude Include="$(MXNET_ROOT)\src\operator\image\image_random-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\image\image_random.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\image\image_utils.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\image\resize-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\image\resize.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\instance_norm-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\instance_norm.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\l2_normalization-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\l2_normalization.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\leaky_relu-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\leaky_relu.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\linalg.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\linalg_impl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\loss_binary_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\loss_binary_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\make_loss-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\make_loss.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\math_functions-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\mkl_functions-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\mshadow_op.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\mxnet_op.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\activation-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\activation.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\batch_norm-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\batch_norm.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\concat-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\concat.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\convolution-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\convolution.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\ctc_loss-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\ctc_loss.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_activation-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_algoreg-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_algoreg.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_batch_norm-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_batch_norm.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_convolution-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_deconvolution-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_pooling-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\cudnn\cudnn_softmax_activation-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\deconvolution-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\deconvolution.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\depthwise_convolution-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\dropout-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\dropout.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\fully_connected-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\fully_connected.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\im2col.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\layer_norm-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\layer_norm.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\lrn-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\lrn.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_act-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_act.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_base-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_base.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_batch_norm-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_concat-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_concat.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_convolution-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_convolution.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_copy.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_deconvolution.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_fully_connected-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_fully_connected.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_lrn-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_ops-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_pooling-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_pooling.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_reshape.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_rnn_impl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_slice-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_slice.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_softmax.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_softmax_output.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_sum.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\mkldnn\mkldnn_transpose.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\moments-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\moments.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\pool.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\pool_utils.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\pooling-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\pooling.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\sequence_mask-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\softmax-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\softmax.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\softmax_activation-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\softmax_activation.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nn\upsampling-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nn\upsampling.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nnpack\nnpack_convolution-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nnpack\nnpack_fully_connected-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nnpack\nnpack_pooling-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\nnpack\nnpack_util.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\nnpack\nnpack_util.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\operator.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\operator_common.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\operator_tune-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\operator_tune.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\operator_tune.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\operator_util.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\optimizer_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\optimizer_op.cc">
      <ObjectFileName>$(IntDir)/src/operator/optimizer_op.cc.obj</ObjectFileName>
    </ClCompile>
    <ClInclude Include="$(MXNET_ROOT)\src\operator\pad-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\pad.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\pooling_v1-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\pooling_v1.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\dequantize-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\dequantize.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_dequantize-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantize-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantize_v2-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantized_act.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantized_concat.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantized_conv.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantized_elemwise_add.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantized_fully_connected.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantized_ops-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_quantized_pooling.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\mkldnn\mkldnn_requantize-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\quantization_utils.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\quantize-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantize.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantize_graph_pass.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\quantize_v2-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantize_v2.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_activation.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_concat.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_conv.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\quantized_elemwise_add-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_elemwise_add.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\quantized_flatten-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_flatten.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_fully_connected.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\quantized_pooling.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\quantization\requantize-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\quantization\requantize.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\random\multisample_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\random\multisample_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\random\sample_multinomial_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\random\sample_multinomial_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\random\sample_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\random\sample_op.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\random\sampler.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\random\shuffle_op.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\random\unique_sample_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\random\unique_sample_op.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\regression_output-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\regression_output.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\rnn-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\rnn.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\rnn_impl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\roi_pooling-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\roi_pooling.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\sequence_last-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\sequence_last.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\sequence_mask-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\sequence_mask.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\sequence_op_common.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\sequence_reverse-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\sequence_reverse.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\slice_channel-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\slice_channel.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\softmax_output-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\softmax_output.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\spatial_transformer-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\spatial_transformer.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\special_functions-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\build_subgraph.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\common.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\default_subgraph_property.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\default_subgraph_property_v2.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_conv-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_conv.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_conv_property.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_fc.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_fc_post_quantize_property.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_fc_property.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_post_quantize_align_scale_property.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_post_quantize_property.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\mkldnn\mkldnn_subgraph_property.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\subgraph_property.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\tensorrt\nnvm_to_onnx-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\tensorrt\nnvm_to_onnx.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\tensorrt\onnx_to_tensorrt.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\tensorrt\onnx_to_tensorrt.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph\tensorrt\tensorrt-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph\tensorrt\tensorrt.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\subgraph_op_common.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\subgraph_op_common.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\svm_output-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\svm_output.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\swapaxis-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\swapaxis.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\amp_cast.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\amp_cast.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\broadcast_reduce-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\broadcast_reduce_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\broadcast_reduce_op_index.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\broadcast_reduce_op_value.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\cast_storage-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\cast_storage.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\control_flow_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\control_flow_op.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\diag_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\diag_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\dot-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\dot.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_broadcast_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_broadcast_op_basic.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_broadcast_op_extended.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_broadcast_op_logic.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op_basic.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op_extended.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_op_logic.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_scalar_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_scalar_op_basic.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_scalar_op_extended.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_scalar_op_logic.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_scatter_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_scatter_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_sum.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_sum.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_unary_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_unary_op_basic.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_unary_op_trig.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\histogram-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\histogram.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\indexing_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\indexing_op.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\init_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\init_op.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\la_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\la_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\la_op.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\matrix_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\matrix_op.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\ordering_op-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\ordering_op.cc" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\ravel.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\ravel.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\slice-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\sort_op.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\sparse_retain-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\sparse_retain.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\square_sum-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\operator\tensor\square_sum.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\operator\tensor\util\tensor_util-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\optimizer\sgd-inl.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\profiler\aggregate_stats.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\profiler\aggregate_stats.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\profiler\nvtx.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\profiler\nvtx.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\profiler\profiler.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\profiler\profiler.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\profiler\storage_profiler.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\profiler\vtune.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\profiler\vtune.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\resource.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\storage\cpu_device_storage.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\storage\cpu_shared_storage_manager.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\storage\gpu_device_storage.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\storage\naive_storage_manager.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\storage\pinned_memory_storage.h" />
    <ClInclude Include="$(MXNET_ROOT)\src\storage\pooled_storage_manager.h" />
    <ClCompile Include="$(MXNET_ROOT)\src\storage\storage.cc" />
    <ClInclude Include="$(MXNET_ROOT)\src\storage\storage_manager.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\base.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\c_api.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\compiler\op_attr_types.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\compiler\packed_func_ext.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\compiler\util.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\graph.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\graph_attr_types.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\layout.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\node.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\op.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\op_attr_types.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\pass.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\pass_functions.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\symbolic.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\top\nn.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\top\tensor.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\include\nnvm\tuple.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\c_api\c_api_common.h" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\c_api\c_api_error.cc">
      <ObjectFileName>$(IntDir)/3rdparty/tvm/nnvm/src/c_api/c_api_error.cc.obj</ObjectFileName>
    </ClCompile>
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\c_api\c_api_graph.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\c_api\c_api_symbolic.cc">
      <ObjectFileName>$(IntDir)/3rdparty/tvm/nnvm/src/c_api/c_api_symbolic.cc.obj</ObjectFileName>
    </ClCompile>
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\core\graph.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\core\node.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\core\op.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\core\pass.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\core\symbolic.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\correct_layout.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\gradient.cc">
      <ObjectFileName>$(IntDir)/3rdparty/tvm/nnvm/src/pass/gradient.cc.obj</ObjectFileName>
    </ClCompile>
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\graph_algorithm.h" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\infer_shape_type.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\order_mutation.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\place_device.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\plan_memory.cc">
      <ObjectFileName>$(IntDir)/3rdparty/tvm/nnvm/src/pass/plan_memory.cc.obj</ObjectFileName>
    </ClCompile>
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\print_graph_ir.cc" />
    <ClCompile Include="$(MXNET_ROOT)\3rdparty\tvm\nnvm\src\pass\saveload_json.cc" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\base.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\dot_engine-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\expr_engine-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\expr_scalar-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\expression.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\broadcast.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\broadcast_with_axis.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\channel_pool.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\channel_unpool.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\choose.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\complex.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\concat.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\crop.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\fill.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\flip.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\implicit_gemm.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\mask.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\mirror.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\one_hot.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\pack_col2patch.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\pad.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\range.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\reduce_with_axis.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\reduceto1d.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\reshape.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\slice.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\slice_ex.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\spatial_pool.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\spatial_unpool.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\spatial_upsampling_nearest.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\swapaxis.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\take.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\take_grad.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\transpose.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\extension\unpack_patch2col.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\half.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\half2.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\io.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\logging.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\packet-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\packet\plain-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\packet\sse-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\random.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\stream_gpu-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\tensor.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\tensor_container.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\tensor_cpu-inl.h" />
    <ClInclude Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\tensor_gpu-inl.h" /> 
    <None Include="$(MXNET_ROOT)\src\ndarray\ndarray_function-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\contrib\bilinear_resize-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\contrib\bounding_box-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\contrib\nn\deformable_im2col.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\nn\depthwise_convolution_tf.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\nn\im2col.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\nn\pool.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\tensor\broadcast_reduce-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\tensor\cast_storage-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\tensor\dot-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\tensor\elemwise_binary_broadcast_op-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\tensor\indexing_op-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\tensor\sort_op-inl.cuh" />
    <None Include="$(MXNET_ROOT)\src\operator\tensor\util\tensor_util-inl.cuh" />
    <None Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\cuda\reduce.cuh" />
    <None Include="$(MXNET_ROOT)\3rdparty\mshadow\mshadow\cuda\tensor_gpu-inl.cuh" />
  </ItemGroup>
  <ItemGroup>
    <ProjectReference Include="$(MXNET_ROOT)\x64\3rdparty\dmlc-core\dmlc.vcxproj">
      <Project>{91A0A9DB-8213-3584-8660-2DF56756B058}</Project>
      <Name>dmlc</Name>
    </ProjectReference>
  </ItemGroup>
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets">
    <Import Project="$(VCTargetsPath)\BuildCustomizations\CUDA 9.2.targets" />
  </ImportGroup>
</Project>
```
mxnet.vcxproj
cmake生成的编译太慢。
 如果要用cpp-package，需要`USE_CPP_PACKAGE=1`
如果没有 PreferredToolArchitecture ，会报错C1060。
/bigobj需要在两个地方设置，如果没有会报错C1128。
.vcxproj.user 配置一下 `MXNET_ROOT`及`OPENBLAS_ROOT`
这里cuda用的是`9.2`，也可以使用`10.1`、`10.2`等等
mxnet 对应的python库 为[gluoncv](https://gluon-cv.mxnet.io/)，需要安装Pillow(python imaging library)。

tuple.h还要[改个地方](https://github.com/apache/incubator-mxnet/issues/15143)，把`#if !defined(_MSC_VER)` 改成`#if !(defined(_MSC_VER) && _MSC_VER < 1900)`，否则生成的op.h不正确。
相比libtorch，mxnet还是容易编译的，不过用的人少。
使用c++方式之前，需要先[export_network](https://gluon-cv.mxnet.io/build/examples_deployment/export_network.html) 。
悲剧的是在win7下，dll退出时[有个bug](https://github.com/apache/incubator-mxnet/issues/11163)。