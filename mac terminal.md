
# 效果

![图](https://user-images.githubusercontent.com/10276208/36086434-5de52ace-0ff2-11e8-8299-c67f9ab4e9bd.gif)

# 下载并安装 iterm2

[Iterm2 官网](https://www.iterm2.com/)  

1. 下载后加入应用程序  

2. 给予 完全访问权限

# 切换 iterm2 的主题

[dracula theme](https://draculatheme.com/iterm/)
```
$ git clone https://github.com/dracula/iterm.git

1. iTerm2 > Preferences > Profiles > Colors Tab
2. Open the Color Presets... drop-down in the bottom right corner
3. Select Import... from the list
4. Select the Dracula.itermcolors file
5. Select the Dracula from Color Presets...
```

# 安装 oh-my-zsh



[oh-my-zsh github](https://github.com/robbyrussell/oh-my-zsh)  
```
# 安装在根目录
cd ~
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

# 安装 oh-my-zsh 主题

[spaceship-prompt](https://github.com/denysdovhan/spaceship-prompt)  
```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"

ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"

Set ZSH_THEME="spaceship" in your .zshrc
vim ~/.zshrc
```

# 安装 FiraCode 字体

[FiraCode github](https://github.com/tonsky/FiraCode)  

下载后拖到mac字体库  
iterm2 中设置字体

# 切换shell
```
chsh -s /bin/zsh
chsh -s /bin/bash
```

# 安装自动提示
[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)  
```
Clone this repository into $ZSH_CUSTOM/plugins (by default ~/.oh-my-zsh/custom/plugins)  

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions


Add the plugin to the list of plugins for Oh My Zsh to load (inside ~/.zshrc):  

plugins=(zsh-autosuggestions)  
```
# 安装语法高亮
[github](https://github.com/zsh-users/zsh-syntax-highlighting)  
plugin 目录 : ~/.oh-my-zsh/plugins
```
Clone this repository in oh-my-zsh's plugins directory:

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
Activate the plugin in ~/.zshrc:

plugins=( [plugins...] zsh-syntax-highlighting)
Restart zsh (such as by opening a new instance of your terminal emulator).
```

# 快捷键设置
```
PATH="/Library/Frameworks/Python.framework/Versions/3.6/bin:${PATH}"
export PATH
alias bianji="vim ~/.zshrc"
alias baocun="source ~/.zshrc && echo "已生效""
alias ip="curl cip.cc"
# 设置socket5代理
alias proxy='export all_proxy=socks5://127.0.0.1:1086'
alias unproxy='unset all_proxy'
alias gs="git status"
alias gm="git commit -m 'change'"
alias ga="git add -A"
alias gp="git push"
alias ll='ls -al'
```
# mac 环境变量
vim ~/.zshrc
export MAVEN_HOME=/usr/local/apache-maven-3.5.0  
export PATH=$PATH:xx:xx:xx:xx:$MAVEN_HOME/bin
source ~/.zshrc

# 利用bash_profile增加快捷键

```
#编辑
vim ~/.zshrc

#bash_profile的编辑,用&&执行两条命令,或;
alias fanqiang="ls && cd Desktop && echo "文字" "

#保存修改
source ~/.bash_profile
```
# mac terminal 使用代理

```
# proxy list
vim ~/.zshrc
alias proxy='export all_proxy=socks5://127.0.0.1:1080'
alias unproxy='unset all_proxy'
source ~/.zshrc
```

