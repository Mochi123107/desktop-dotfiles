# Anime Frost Desktop

CachyOS / Hyprland 桌面配置快照，整理于 2026-10-24。

蓝色半透明主题，窗口透明度 0.67、圆角 14；包含 Waybar 音频频谱、亮度面板、应用启动器、桌面时钟、通知中心、Kitty、Fastfetch、GTK 主题和配套脚本。

## 环境与依赖

本机版本：Hyprland 0.56.2-4.1、Waybar 0.15.0-3.1、Hyprpaper 0.8.4-9.1、Kitty 0.49.2-1.1、Mako 1.11.0-1.1。
这是 Hyprland Lua 配置（hl.* API），需要兼容该 API 的版本；hyprland.conf 在原机为空。
Python 组件使用 python-gobject、python-cairo、gtk-layer-shell、GTK 3；其他功能使用 cava、playerctl、wireplumber/wpctl、brightnessctl、pavucontrol、nm-connection-editor、thunar、fcitx5、grim、slurp、wl-clipboard、libnotify。
字体为 Maple Mono NF CN。Zsh 配置引用 CachyOS 提供的 /usr/share/cachyos-zsh-config/cachyos-config.zsh；其他发行版请自行适配。

## 使用

这是配置快照，请先备份现有配置，再按目录选择复制到自己的主目录，不建议直接覆盖整个 .config。

1. 解压 desktop-dotfiles.tar.gz，在解压目录运行 python3 prepare.py，将 /home/USER 替换为你自己的主目录。此命令只处理解压目录，不安装或覆盖现有桌面配置。
2. 显示器使用自动选择和 preferred 模式，可按自己的硬件调整。
3. 时钟使用系统本地时区，桌面标识使用通用 FROST 字样。
4. 将需要的 .config 子目录、.local/bin 脚本及 .local/share 主题复制到相应位置。脚本需要可执行权限。
5. 壁纸在 Pictures/tamako2-enhanced.png；Fastfetch 图片在 .config/fastfetch 内。
6. 注销并在兼容的 Hyprland 会话中登录。启动入口为 .local/bin/mochi-desktop-start。

第三方程序和字体未打包，AnimeFrost 图标可能继承系统图标主题；没有重新分发 Bibata 光标包。部分可选启动项和应用需要自行安装。

## 常用快捷键

| 快捷键 | 功能 |
| --- | --- |
| Super + Q | Kitty |
| Super + E | Thunar |
| Super + R | 应用启动器 |
| Super + C | 关闭当前窗口 |
| Super + N | 通知中心 |
| Super + V | 浮动窗口 |
| Super + 数字 | 切换工作区 |
| Super + Shift + 数字 | 移动窗口到工作区 |
| Super + Delete | 关闭当前工作区所有窗口 |
| Print | 全屏截图 |
| Super + Shift + S | 区域截图 |

## 分享范围与验证

仅选择桌面配置、主题、图片及相关脚本。未包含浏览器资料、账号凭据、聊天数据、通知历史、缓存、日志或历史备份。没有采集实时桌面截图。
已检查打包 Python 文件语法和 Shell 脚本语法；未在新系统中安装验证，也未执行桌面重启。
SHA256SUMS 记录分享文件校验值。

壁纸、插图和第三方主题资源的权利归原作者所有；本仓库未为这些资源追加许可。

## 通用分享版

已移除手写 CPU 型号、固定用户名及主机显示名称、个人日期、原机显示器参数和固定时区。Fastfetch 自动读取运行者的用户名、主机名及 CPU；这些实际信息未写入包中。桌面外观与功能代码予以保留。
仅修改分享副本，不修改原机正在使用的配置。
