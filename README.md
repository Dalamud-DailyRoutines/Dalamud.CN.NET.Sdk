# Dalamud.CN.NET.Sdk
Dalamud 插件开发专用 .NET SDK, 主要方便国服开发者

## 使用

将你的插件 `.csproj` 项目文件的开头由

```
<Project Sdk="Microsoft.NET.Sdk">
```

替换为

```
<Project Sdk="Dalamud.CN.NET.Sdk/11.3.0">
```

即可

注意 API 对应版本, 版本号首位为 11 则为 API 11 / .NET 8.0, 首位为 12 则为 API 12 / .NET 9.0

## 引用与配置

无特殊说明情况下, 下方配置项均默认启用

- DalamudPackager (可配置, 配置项 `Use_DalamudPackager`)
- DotNet.ReproducibleBuilds
- Dalamud
- ImGui.NET
- ImGuiScene
- PInvoke.User32
- PInvoke.Windows.Core
- FFXIVClientStructs (可配置, 配置项 `Use_Dalamud_FFXIVClientStructs`)
- InteropGenerator.Runtime (可配置, 配置项 `Use_Dalamud_FFXIVClientStructs`)
- Newtonsoft.Json (可配置, 配置项 `Use_Dalamud_Newtonsoft_Json`)
- Lumina (可配置, 配置项 `Use_Dalamud_Lumina`)
- Lumina.Excel (可配置, 配置项 `Use_Dalamud_Lumina_Excel`)
- Serilog (可配置, 配置项 `Use_Dalamud_Serilog`)

特殊

- DalamudHome (可配置, 配置项 `Use_Dalamud_CN`)
  - 若为 true, 则使用 `$(appdata)\XIVLauncherCN\addon\Hooks\dev\` 为引用路径来源
  - 若为 false, 则使用 `$(appdata)\XIVLauncher\addon\Hooks\dev\` 为引用路径来源
