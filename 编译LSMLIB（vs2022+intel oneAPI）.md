[LSMLIB](https://github.com/velexi-research/LSMLIB)

.vcxproj

```xml
<?xml version="1.0" encoding="utf-8"?>
<Project DefaultTargets="Build" ToolsVersion="17.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <PropertyGroup>
    <PreferredToolArchitecture>x64</PreferredToolArchitecture>
  </PropertyGroup>
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
    <ProjectGuid>{35454A9E-AFF5-37EC-87E1-6D24D84D6CDA}</ProjectGuid>
    <Keyword>Win32Proj</Keyword>
    <WindowsTargetPlatformVersion>10.0.26100.0</WindowsTargetPlatformVersion>
    <Platform>x64</Platform>
    <ProjectName>lsm</ProjectName>
    <VCProjectUpgraderObjectName>NoUpgrade</VCProjectUpgraderObjectName>
  </PropertyGroup>
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.Default.props" />
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|x64'" Label="Configuration">
    <ConfigurationType>StaticLibrary</ConfigurationType>
    <CharacterSet>MultiByte</CharacterSet>
    <PlatformToolset>v143</PlatformToolset>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|x64'" Label="Configuration">
    <ConfigurationType>StaticLibrary</ConfigurationType>
    <CharacterSet>MultiByte</CharacterSet>
    <PlatformToolset>v143</PlatformToolset>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'" Label="Configuration">
    <ConfigurationType>StaticLibrary</ConfigurationType>
    <CharacterSet>MultiByte</CharacterSet>
    <PlatformToolset>v143</PlatformToolset>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'" Label="Configuration">
    <ConfigurationType>StaticLibrary</ConfigurationType>
    <CharacterSet>MultiByte</CharacterSet>
    <PlatformToolset>v143</PlatformToolset>
  </PropertyGroup>
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings">
  </ImportGroup>
  <ImportGroup Label="PropertySheets">
    <Import Project="$(UserRootDir)\Microsoft.Cpp.$(Platform).user.props" Condition="exists('$(UserRootDir)\Microsoft.Cpp.$(Platform).user.props')" Label="LocalAppDataPlatform" />
  </ImportGroup>
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup>
    <_ProjectFileVersion>10.0.20506.1</_ProjectFileVersion>
    <OutDir Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\lib\Debug\</OutDir>
    <IntDir Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">lsm.dir\Debug\</IntDir>
    <TargetName Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">lsm</TargetName>
    <TargetExt Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">.lib</TargetExt>
    <OutDir Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\lib\Release\</OutDir>
    <IntDir Condition="'$(Configuration)|$(Platform)'=='Release|x64'">lsm.dir\Release\</IntDir>
    <TargetName Condition="'$(Configuration)|$(Platform)'=='Release|x64'">lsm</TargetName>
    <TargetExt Condition="'$(Configuration)|$(Platform)'=='Release|x64'">.lib</TargetExt>
    <OutDir Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">N:\works\LSMLIB-2.0.1\x64\lib\MinSizeRel\</OutDir>
    <IntDir Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">lsm.dir\MinSizeRel\</IntDir>
    <TargetName Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">lsm</TargetName>
    <TargetExt Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">.lib</TargetExt>
    <OutDir Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">N:\works\LSMLIB-2.0.1\x64\lib\RelWithDebInfo\</OutDir>
    <IntDir Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">lsm.dir\RelWithDebInfo\</IntDir>
    <TargetName Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">lsm</TargetName>
    <TargetExt Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">.lib</TargetExt>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|x64'">
    <IncludePath>C:\Program Files (x86)\Intel\oneAPI\compiler\2023.2.0\windows\compiler\include;$(IncludePath)</IncludePath>
    <LibraryPath>C:\Program Files (x86)\Intel\oneAPI\compiler\2023.2.0\windows\compiler\lib\intel64_win;$(LibraryPath)</LibraryPath>
  </PropertyGroup>
  <ItemDefinitionGroup Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">
    <ClCompile>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\x64\include/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\boundary_conditions/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\fast_marching_method/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\field_extension/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\geometry/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\reinitialization/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\toolbox/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\utils;N:\works\LSMLIB-2.0.1\src\utils/$(ConfigurationName);%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <AdditionalOptions>%(AdditionalOptions) -r8</AdditionalOptions>
      <AssemblerListingLocation>$(IntDir)</AssemblerListingLocation>
      <BasicRuntimeChecks>Default</BasicRuntimeChecks>
      <ExceptionHandling>
      </ExceptionHandling>
      <MinimalRebuild>
      </MinimalRebuild>
      <Optimization>
      </Optimization>
      <PrecompiledHeader>NotUsing</PrecompiledHeader>
      <RuntimeLibrary>
      </RuntimeLibrary>
      <SupportJustMyCode>
      </SupportJustMyCode>
      <UseFullPaths>false</UseFullPaths>
      <PreprocessorDefinitions>%(PreprocessorDefinitions);CMAKE_INTDIR="Debug"</PreprocessorDefinitions>
      <ObjectFileName>$(IntDir)</ObjectFileName>
      <DebugInformationFormat>
      </DebugInformationFormat>
      <ScanSourceForModuleDependencies>false</ScanSourceForModuleDependencies>
    </ClCompile>
    <ResourceCompile>
      <PreprocessorDefinitions>%(PreprocessorDefinitions);WIN32;_DEBUG;CMAKE_INTDIR=\"Debug\"</PreprocessorDefinitions>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\utils;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
    </ResourceCompile>
    <Midl>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\utils;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <OutputDirectory>$(ProjectDir)/$(IntDir)</OutputDirectory>
      <HeaderFileName>%(Filename).h</HeaderFileName>
      <TypeLibraryName>%(Filename).tlb</TypeLibraryName>
      <InterfaceIdentifierFileName>%(Filename)_i.c</InterfaceIdentifierFileName>
      <ProxyFileName>%(Filename)_p.c</ProxyFileName>
    </Midl>
    <Lib>
      <AdditionalOptions>%(AdditionalOptions) /machine:x64</AdditionalOptions>
    </Lib>
  </ItemDefinitionGroup>
  <ItemDefinitionGroup Condition="'$(Configuration)|$(Platform)'=='Release|x64'">
    <ClCompile>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\x64\include/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\boundary_conditions/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\fast_marching_method/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\field_extension/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\geometry/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\reinitialization/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\toolbox/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\utils;N:\works\LSMLIB-2.0.1\src\utils/$(ConfigurationName);%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <AdditionalOptions>%(AdditionalOptions) -r8</AdditionalOptions>
      <AssemblerListingLocation>$(IntDir)</AssemblerListingLocation>
      <BasicRuntimeChecks>Default</BasicRuntimeChecks>
      <ExceptionHandling>
      </ExceptionHandling>
      <MinimalRebuild>
      </MinimalRebuild>
      <Optimization>
      </Optimization>
      <PrecompiledHeader>NotUsing</PrecompiledHeader>
      <RuntimeLibrary>
      </RuntimeLibrary>
      <SupportJustMyCode>
      </SupportJustMyCode>
      <UseFullPaths>false</UseFullPaths>
      <PreprocessorDefinitions>%(PreprocessorDefinitions);CMAKE_INTDIR="Release"</PreprocessorDefinitions>
      <ObjectFileName>$(IntDir)</ObjectFileName>
      <DebugInformationFormat>
      </DebugInformationFormat>
      <ScanSourceForModuleDependencies>false</ScanSourceForModuleDependencies>
    </ClCompile>
    <ResourceCompile>
      <PreprocessorDefinitions>%(PreprocessorDefinitions);WIN32;CMAKE_INTDIR=\"Release\"</PreprocessorDefinitions>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\utils;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
    </ResourceCompile>
    <Midl>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\utils;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <OutputDirectory>$(ProjectDir)/$(IntDir)</OutputDirectory>
      <HeaderFileName>%(Filename).h</HeaderFileName>
      <TypeLibraryName>%(Filename).tlb</TypeLibraryName>
      <InterfaceIdentifierFileName>%(Filename)_i.c</InterfaceIdentifierFileName>
      <ProxyFileName>%(Filename)_p.c</ProxyFileName>
    </Midl>
    <Lib>
      <AdditionalOptions>%(AdditionalOptions) /machine:x64</AdditionalOptions>
    </Lib>
  </ItemDefinitionGroup>
  <ItemDefinitionGroup Condition="'$(Configuration)|$(Platform)'=='MinSizeRel|x64'">
    <ClCompile>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\x64\include/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\boundary_conditions/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\fast_marching_method/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\field_extension/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\geometry/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\reinitialization/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\toolbox/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\utils;N:\works\LSMLIB-2.0.1\src\utils/$(ConfigurationName);%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <AdditionalOptions>%(AdditionalOptions) -r8</AdditionalOptions>
      <AssemblerListingLocation>$(IntDir)</AssemblerListingLocation>
      <BasicRuntimeChecks>Default</BasicRuntimeChecks>
      <ExceptionHandling>
      </ExceptionHandling>
      <MinimalRebuild>
      </MinimalRebuild>
      <Optimization>
      </Optimization>
      <PrecompiledHeader>NotUsing</PrecompiledHeader>
      <RuntimeLibrary>
      </RuntimeLibrary>
      <SupportJustMyCode>
      </SupportJustMyCode>
      <UseFullPaths>false</UseFullPaths>
      <PreprocessorDefinitions>%(PreprocessorDefinitions);CMAKE_INTDIR="MinSizeRel"</PreprocessorDefinitions>
      <ObjectFileName>$(IntDir)</ObjectFileName>
      <DebugInformationFormat>
      </DebugInformationFormat>
      <ScanSourceForModuleDependencies>false</ScanSourceForModuleDependencies>
    </ClCompile>
    <ResourceCompile>
      <PreprocessorDefinitions>%(PreprocessorDefinitions);WIN32;CMAKE_INTDIR=\"MinSizeRel\"</PreprocessorDefinitions>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\utils;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
    </ResourceCompile>
    <Midl>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\utils;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <OutputDirectory>$(ProjectDir)/$(IntDir)</OutputDirectory>
      <HeaderFileName>%(Filename).h</HeaderFileName>
      <TypeLibraryName>%(Filename).tlb</TypeLibraryName>
      <InterfaceIdentifierFileName>%(Filename)_i.c</InterfaceIdentifierFileName>
      <ProxyFileName>%(Filename)_p.c</ProxyFileName>
    </Midl>
    <Lib>
      <AdditionalOptions>%(AdditionalOptions) /machine:x64</AdditionalOptions>
    </Lib>
  </ItemDefinitionGroup>
  <ItemDefinitionGroup Condition="'$(Configuration)|$(Platform)'=='RelWithDebInfo|x64'">
    <ClCompile>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\x64\include/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\boundary_conditions/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\fast_marching_method/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\field_extension/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\geometry/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\reinitialization/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\toolbox/$(ConfigurationName);N:\works\LSMLIB-2.0.1\src\utils;N:\works\LSMLIB-2.0.1\src\utils/$(ConfigurationName);%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <AdditionalOptions>%(AdditionalOptions) -r8</AdditionalOptions>
      <AssemblerListingLocation>$(IntDir)</AssemblerListingLocation>
      <BasicRuntimeChecks>Default</BasicRuntimeChecks>
      <ExceptionHandling>
      </ExceptionHandling>
      <MinimalRebuild>
      </MinimalRebuild>
      <Optimization>
      </Optimization>
      <PrecompiledHeader>NotUsing</PrecompiledHeader>
      <RuntimeLibrary>
      </RuntimeLibrary>
      <SupportJustMyCode>
      </SupportJustMyCode>
      <UseFullPaths>false</UseFullPaths>
      <PreprocessorDefinitions>%(PreprocessorDefinitions);CMAKE_INTDIR="RelWithDebInfo"</PreprocessorDefinitions>
      <ObjectFileName>$(IntDir)</ObjectFileName>
      <DebugInformationFormat>
      </DebugInformationFormat>
      <ScanSourceForModuleDependencies>false</ScanSourceForModuleDependencies>
    </ClCompile>
    <ResourceCompile>
      <PreprocessorDefinitions>%(PreprocessorDefinitions);WIN32;CMAKE_INTDIR=\"RelWithDebInfo\"</PreprocessorDefinitions>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\utils;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
    </ResourceCompile>
    <Midl>
      <AdditionalIncludeDirectories>N:\works\LSMLIB-2.0.1\x64\include;N:\works\LSMLIB-2.0.1\src\boundary_conditions;N:\works\LSMLIB-2.0.1\src\fast_marching_method;N:\works\LSMLIB-2.0.1\src\field_extension;N:\works\LSMLIB-2.0.1\src\geometry;N:\works\LSMLIB-2.0.1\src\reinitialization;N:\works\LSMLIB-2.0.1\src\toolbox;N:\works\LSMLIB-2.0.1\src\utils;%(AdditionalIncludeDirectories)</AdditionalIncludeDirectories>
      <OutputDirectory>$(ProjectDir)/$(IntDir)</OutputDirectory>
      <HeaderFileName>%(Filename).h</HeaderFileName>
      <TypeLibraryName>%(Filename).tlb</TypeLibraryName>
      <InterfaceIdentifierFileName>%(Filename)_i.c</InterfaceIdentifierFileName>
      <ProxyFileName>%(Filename)_p.c</ProxyFileName>
    </Midl>
    <Lib>
      <AdditionalOptions>%(AdditionalOptions) /machine:x64</AdditionalOptions>
    </Lib>
  </ItemDefinitionGroup>
  <ItemGroup>
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\boundary_conditions\lsm_boundary_conditions.c" />
  
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\boundary_conditions\lsm_boundary_conditions1d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\boundary_conditions\lsm_boundary_conditions2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
   <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\boundary_conditions\lsm_boundary_conditions3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\fast_marching_method\FMM_Core.c" />
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\fast_marching_method\FMM_Heap.c" />
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\fast_marching_method\lsm_FMM_eikonal2d.c" />
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\fast_marching_method\lsm_FMM_eikonal3d.c" />
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\fast_marching_method\lsm_FMM_field_extension2d.c" />
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\fast_marching_method\lsm_FMM_field_extension3d.c" />
  
       <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\field_extension\lsm_field_extension1d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
     <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\field_extension\lsm_field_extension2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
     <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\field_extension\lsm_field_extension3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\geometry\lsm_geometry3d_c.c" />
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\geometry\lsm_curvature2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\geometry\lsm_curvature2d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
       <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\geometry\lsm_curvature3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\geometry\lsm_curvature3d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\geometry\lsm_geometry1d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\geometry\lsm_geometry2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\geometry\lsm_geometry2d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\geometry\lsm_geometry3d_fort.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\reinitialization\lsm_reinitialization1d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\reinitialization\lsm_reinitialization2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
   
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\reinitialization\lsm_reinitialization2d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\reinitialization\lsm_reinitialization3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\reinitialization\lsm_reinitialization3d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_initialization2d.c" />
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_initialization3d.c" />
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_calculus_toolbox.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_localization2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_localization3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_tvd_runge_kutta1d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_tvd_runge_kutta2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_tvd_runge_kutta2d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_tvd_runge_kutta3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\src\toolbox\lsm_tvd_runge_kutta3d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
      <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_calculus_toolbox2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_calculus_toolbox2d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_calculus_toolbox3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
       <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_level_set_evolution1d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
     <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_level_set_evolution2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
     <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_level_set_evolution2d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
     <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_level_set_evolution3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
   
     <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_level_set_evolution3d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
    
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_math_utils1d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
   
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_math_utils2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_math_utils2d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_math_utils3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
  
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_math_utils3d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_spatial_derivatives1d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_spatial_derivatives2d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_spatial_derivatives2d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_spatial_derivatives3d.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
 
    <CustomBuild Include="N:\works\LSMLIB-2.0.1\x64\src\toolbox\lsm_spatial_derivatives3d_local.f">
      <FileType>Document</FileType>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <AdditionalInputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">$(IFDIR)\ifort.exe;%(AdditionalInputs)</AdditionalInputs>
      <Message Condition="'$(Configuration)|$(Platform)'=='Release|x64'">ifort.exe %(Identity)...</Message>
      <Outputs Condition="'$(Configuration)|$(Platform)'=='Release|x64'">N:\works\LSMLIB-2.0.1\x64\src\%(Filename).obj;%(Outputs)</Outputs>
      <Command Condition="'$(Configuration)|$(Platform)'=='Release|x64'">"$(IFDIR)\ifort.exe" -r8 /c "%(FullPath)"</Command>
      <SubType>Designer</SubType>
    </CustomBuild>
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\utils\lsm_data_arrays.c" />
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\utils\lsm_file.c" />
    <ClCompile Include="N:\works\LSMLIB-2.0.1\src\utils\lsm_grid.c" />
  </ItemGroup>
  <ItemGroup />
  <ItemGroup>
    <ProjectReference Include="N:\works\LSMLIB-2.0.1\x64\ZERO_CHECK.vcxproj">
      <Project>{77015F72-4972-3B35-A387-E4D2632C6EC6}</Project>
      <Name>ZERO_CHECK</Name>
      <ReferenceOutputAssembly>false</ReferenceOutputAssembly>
      <CopyToOutputDirectory>Never</CopyToOutputDirectory>
    </ProjectReference>
  </ItemGroup>
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets">
  </ImportGroup>
</Project>


```


.vcxproj.user

```xml
<?xml version="1.0" encoding="utf-8"?>
<Project ToolsVersion="Current" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">
    <IFDIR>C:\Program Files (x86)\Intel\oneAPI\compiler\2023.2.0\windows\bin\intel64</IFDIR> 
    
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|x64'">
    <IFDIR>C:\Program Files (x86)\Intel\oneAPI\compiler\2023.2.0\windows\bin\intel64</IFDIR> 
     
  </PropertyGroup>
</Project>

```
