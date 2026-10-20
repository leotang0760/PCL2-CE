# PCL2:CE By ZYT

PCL 2.99.0.0 二次修改版 · 下载恢复版
原作 © 龙腾猫跃 / 成都瓜皮龙科技有限公司 · 本修改仅用于学习研究

## 这是什么

PCL（Plain Craft Launcher）是 Windows 上最流行的 Minecraft 第三方启动器。
官方在 2026 年 10 月合规调整中，于开源版加入了 RestrictMcDownload = True 开关，
在 UI 层掐断了 MC 版本在线下载与整合包安装功能。

本仓库在官方开源版 2.99.0.0 基础上，仅做了一行修改恢复上述功能：

    ' Plain Craft Launcher 2\Modules\ModSecret.vb 第 18 行
    - Public Const RestrictMcDownload As Boolean = True
    + Public Const RestrictMcDownload As Boolean = False

原代码本就是 If/Else 双路径写好的，翻开关后所有拦截分支自动走回正常逻辑。

## 二次修改信息

| 项目 | 内容 |
|---|---|
| 修改作者 | Zhiyuant (QQ 2264958692) |
| 修改基线 | PCL 官方开源版 Release 2.99.0.0 |
| 修改内容 | 恢复 MC 版本下载、整合包在线安装；关于页追加二次修改说明卡片 |
| 编译环境 | Visual Studio 2022 + .NET Framework 4.8 |

## 下载预编译版

前往 [Releases](https://github.com/leotang0760/PCL2-CE/releases) 下载
PCL2-2.99-Download-Restored-win-x64.zip，解压后运行 Plain Craft Launcher 2.exe。

## 免责声明

- 本项目为学习研究用途的二次修改，不代表官方立场
- 请勿用于商业用途
- 本修改版不包含官方闭源模块（CDN 鉴权、赞助系统、正版登录 ClientId 等仍需自行配置）