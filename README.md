# Music Tag Studio

Windows 音乐标签批量编辑器（PySide6 自研版，仿原版 MusicTag 重做）。**v1.0 正式版**，64 位。

## 下载

到 **[Releases](https://github.com/ZzicoChen/Music-Tag-Studio/releases/latest)** 里挑一个：

| 版本 | 文件名 | 怎么用 |
|---|---|---|
| **Windows 安装版** | `Music Tag Studio v1.0 Windows 安装版.exe` | 双击 → 选安装目录 → 开始安装。会自动创建桌面 / 开始菜单快捷方式，并注册到「应用和功能」里可卸载 |
| **Windows 便携版** | `Music Tag Studio v1.0 Windows 便携版.zip` | 解压到任意目录，双击里面的 `Music Tag Studio.exe` 即用；整个文件夹要保留（`_internal` 不能删） |

两个版本内容完全一样，只是分发形式不同。数据目录（`settings.json` / `defaults.json` / 撤销备份）在软件文件夹上一级 `MusicTagStudio_Data`，便携版换机器直接搬文件夹即可。

## 检测更新

软件里 **帮助 → 关于 → 检测更新**（设置页里也有入口），会依次尝试三路镜像读取本仓库的 `version.json`，任意一路通就能比对版本：

1. `raw.githubusercontent.com` —— 主地址
2. `gh-proxy.com` —— 国内直连不畅时的代理镜像
3. `cdn.jsdelivr.net` —— jsDelivr CDN（走 GitHub 仓库缓存）

有新版会直接给出「打开发布页下载」，安装版 / 便携版都在发布页里。也可以在设置里填自定义 `update_url` 覆盖默认地址。

## 说明

- 64 位（PE machine 0x8664，Python 3.13 AMD64）
- 依赖：PySide6 6.12 / mutagen / requests / zhconv，全部打包进目录，无需另外装 Python
- 支持格式：MP3 / FLAC / M4A / OGG / OPUS / WAV / WMA 等（按 mutagen 能力）
- 功能：批量标签编辑、封面搜索/替换、歌词搜索与编码修正、跨源匹配、撤销备份
