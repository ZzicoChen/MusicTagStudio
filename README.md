# MusicTagStudio

Windows 音乐标签批量编辑器（PySide6 自研版，仿原版 MusicTag 重做）。**v1.0 正式版**，64 位。

## 下载

到 **[Releases](https://github.com/ZzicoChen/Music-Tag-Studio/releases/latest)** 里挑一个：

| 版本 | 文件 | 怎么用 |
|---|---|---|
| **Windows 安装版** | `MusicTagStudio-Win-64-Setup-v1.0.exe` | 双击 → 选安装目录 → 开始安装。自动创建桌面 / 开始菜单快捷方式，并注册到「应用和功能」里可卸载 |
| **Windows 便携版** | `MusicTagStudio-Win-64-Portable-v1.0.zip` | 解压到任意目录，双击里面的 `MusicTagStudio.exe` 即用；整个文件夹要保留（`_internal` 不能删） |

两个版本内容完全一样，只是分发形式不同。数据和缓存都在程序文件夹内的 `MusicTagStudio_Data`（`settings.json` / `defaults.json` / `undo` / `cache`），整个文件夹搬走就连设置一起走。

## 帮助页（关于 + 检测更新）

工具栏「帮助」按钮点一下即可，弹窗标题就是「帮助」，一页里同时是：

- 程序名 / 版本 v1.0 / 作者：Zzico / 数据目录与缓存目录
- 两张二维码：左 GitHub 首页、右 支持作者
- 检查更新：点「检测更新」后结果**直接显示在同一页**，不再另弹窗

更新地址三路镜像兜底，任意一路通就行：

1. `raw.githubusercontent.com` —— 主地址
2. `gh-proxy.com` —— 国内直连不畅时的代理镜像
3. `cdn.jsdelivr.net` —— jsDelivr CDN（走 GitHub 仓库缓存）

发现新版会显示版本 / 来源 / 更新说明，并给出「打开发布页下载」；也可以在设置里填自定义 `update_url` 覆盖默认地址。

## 说明

- 64 位（PE machine 0x8664，Python 3.13 AMD64）
- 依赖：PySide6 6.12 / mutagen / requests / zhconv，全部打包进目录，无需另外装 Python
- 支持格式：MP3 / FLAC / M4A / OGG / OPUS / WAV / WMA 等（按 mutagen 能力）
- 功能：批量标签编辑、封面搜索/替换、歌词搜索与编码修正、跨源匹配、撤销备份
