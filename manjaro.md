### 源
* 生成可用中国镜像站列表：`sudo pacman-mirrors -i -c China -m rank`
* 添加 archlinuxcn 源，编辑 /etc/pacman.config ，在末尾添加：
```
[archlinuxcn]
Server = http://repo.archlinuxcn.org/$arch
```
* 导入 GPG key：`sudo pacman -S archlinuxcn-keyring`
* 刷新缓存：`sudo pacman -Syy`

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
