### 源
* 生成可用中国镜像站列表：`sudo pacman-mirrors -i -c China -m rank`
* 添加 archlinuxcn 源，编辑 /etc/pacman.config ，在末尾添加：
```
[archlinuxcn]
Server = http://repo.archlinuxcn.org/$arch
```
* 导入 GPG key：`sudo pacman -S archlinuxcn-keyring`
* 刷新缓存：`sudo pacman -Syy`

### pacman
* 让本地的包数据库和远程的软件仓库同步: `pacman -Syy`
* 同步非本地(local)软件仓库并升级系统的软件包: `pacman -Syu`
* 清理软件包缓存(/var/cache/pacman/pkg/): `pacman -Sc`
* 安装或者升级单个软件包: `pacman -S package_name1 package_name2`
* 删除单个软件包，保留其全部已经安装的依赖关系: `pacman -R package_name`
* 删除指定软件包，及其所有没有被其他已安装软件包使用的依赖关系: `pacman -Rs package_name`
* paccache 命令默认会删除近3个版本前的软件包：`paccache -r`
* 安装一个本地包(不从源里下载）:`pacman -U /path/to/package/package_name-version.pkg.tar.xz`

### 输入法
* 安装：`sudo pacman -S fcitx fcitx-im fcitx-configtool fcitx-sogoupinyin`
* 编辑 `~/.xprofile` 增加：
```
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS="@im=fcitx"
```
* 配置好后需要注销系统重新登录一次

### 字体
* source-code-pro

### 软件
* ccat/bat/wget/vim/nodejs/npm: 
`pacman -S ccat bat wget vim nodejs npm`

### oh-my-zsh
* 切换默认 shell 为 zsh：`chsh -s /bin/zsh`
* 安装 oh-my-zsh:
`sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"`
* plugins:
```
git
fasd
zsh-interactive-cd
zsh-autosuggestions
copydir
encode64
colored-man-pages
zsh-completions
zsh-syntax-highlighting
```

### 双击状态栏最大化
* settings -> window manager -> advanced -> double click action
* settings -> mouse and touchpad -> behavior -> double click -> time -> 571ms

### vim 粘贴进入 visual 模式
* .vimrc -> set mouse=
