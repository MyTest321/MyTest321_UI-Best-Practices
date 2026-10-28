# UI Best Practices

## Requirements
- Unreal Editor 5.3.2
- Visual Studio 2022
- MSVC v143 - VS 2022 C++ x64/x86 build tools (v14.38-17.8) (Out of support)
- .NET 6.0 Runtime (Out of support)

### Maybe manually select MSVC version for UBT
When you have multi MSVC version in VS2022, it default use higher version to compile. So UnrealBuildTool(UBT) may not happy.

- Open **%APPDATA%/Unreal Engine/UnrealBuildTool/BuildConfiguration.xml** and modify kind of
```xml
<?xml version="1.0" encoding="utf-8"?>
<Configuration xmlns="https://www.unrealengine.com/BuildConfiguration">
    <WindowsPlatform>
        <!-- Please Replace Your MSVC version !! -->
        <!-- Check Your MSVC version: "C:\Program Files\Microsoft Visual Studio\2022\Community\VC\Tools\MSVC" !!-->
        <CompilerVersion>14.38.33130</CompilerVersion>
    </WindowsPlatform>
</Configuration>
```

## Building
- Run `gen_vs2022.bat`
- Open `UIBestPractices.sln` and Compile/Run




 