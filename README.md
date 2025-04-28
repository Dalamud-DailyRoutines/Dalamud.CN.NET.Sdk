# Dalamud.CN.NET.Sdk
Dalamud 插件开发专用 .NET SDK, 主要方便国服开发者

## 使用

将你的插件 `.csproj` 项目文件的开头由

```csharp
<Project Sdk="Microsoft.NET.Sdk">
```

替换为

```csharp
<Project Sdk="Dalamud.CN.NET.Sdk/11.3.0">
```

即可

注意 API 对应版本, 版本号首位为 11 则为 API 11 / .NET 8.0, 首位为 12 则为 API 12 / .NET 9.0

## 引用与配置

无特殊说明情况下, 下方配置项均默认启用

| 名称 | 可配置 | 配置项名称 |
| ---- | ---- | ---- |
| DalamudPackager | ✅ | `Use_DalamudPackager` |
| DotNet.ReproducibleBuilds | ❌  | - |
| Dalamud | ❌ | - |
| ImGui.NET | ❌ | - |
| ImGuiScene | ❌ | - |
| PInvoke.User32 | ❌ | - |
| PInvoke.Windows.Core | ❌ | - |
| FFXIVClientStructs | ✅ | `Use_Dalamud_FFXIVClientStructs` |
| InteropGenerator.Runtime | ✅ | `Use_Dalamud_FFXIVClientStructs` |
| Newtonsoft.Json | ✅ | `Use_Dalamud_Newtonsoft_Json` |
| Lumina | ✅ | `Use_Dalamud_Lumina` |
| Lumina.Excel | ✅ | `Use_Dalamud_Lumina_Excel` |
| Serilog | ✅ | `Use_Dalamud_Serilog` |

### 特殊

| 名称 | 可配置 | 配置项名称 | 备注 |
| ---- | ---- | ---- | ---- |
| DalamudHome | ✅ | `Use_Dalamud_CN` | true: `$(appdata)\XIVLauncherCN\addon\Hooks\dev`；false: `$(appdata)\XIVLauncher\addon\Hooks\dev\` |

### 示例

```csharp
<PropertyGroup>
    <Use_Dalamud_CN>false</TargetFramework>
</PropertyGroup>
```
