# DevOps 工程师的 macOS 搭建指南

## Why

本项目的灵感来自于 [Phodal Huang](https://github.com/phodal)  的项目 [setup.guide](https://github.com/phodal/setup.guide) , 觉得这种总结的方式十分的好，方便以后从无到有地搭建一个合适宜用的macOS环境。~~加之我的RMBP因为苹果的电池🔋召回计划而返厂维修，自己把所有的数据清空了，刚好进行本项目的尝试。~~ 刚好趁着Apple暑期计划，购买了新的M1 Mac Mini，可以在一个新的 macOS 上实施这个项目

## What

这是一个绝大多数靠命令行（Homebrew），安装 macOS 软件的仓库。
对于需要在网站下载dmg、pkg等软件、或者在Mac App Store下载的软件，请参照我的另一个仓库：
[Mac-Software-In-Use](https://github.com/MiracleWong/Mac-Software-In-Use)

对于M1 Mac Mini等搭载苹果最新 M1 芯片的机器，需要软件额外的支持，具体查询网站如下：

- [Does it ARM](https://doesitarm.com/)
- [is apple silicon ready](https://isapplesiliconready.com/zh)

从软件收集数量来看，Does it ARM 更胜一筹；从提交情报方式来看，Does it ARM 采用开源平台、情报公示，而项目 is apple silicon ready 通过 Google 表单提交给主理人，Does it ARM 更胜一筹；从美观度和易用性来看，项目 is apple silicon ready 为每个软件设置了图标、做了分页处理、每行高度适中，完胜 Does it ARM。<sup>[1]</sup>

## How

1. Install Xcode
  
    备注：在Mac App Store 上安装

2. Install Xcode命令行工具

    ```
    xcode-select --install
    ```

3. Install Rosetta（罗塞塔）

    ![install-rosetta](http://blog.iotop.work/image/install-rosetta.png)

    备注：
    - 首次打开为基于 Intel 的 Mac 构建的 App 时，系统会要求您安装 Rosetta（罗塞塔）。
    - [如果您需要在 Mac 上安装 Rosetta - Apple 支持 (中国)](https://support.apple.com/zh-cn/HT211861)

4. Install Homebrew

    ```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

    官方地址：[Homebrew](https://brew.sh/index_zh-cn)

5. 更改Homebrew的配置

    [Homebrew 镜像使用帮助](https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/)

6. Python

    ```
    brew install python@3.10
    ```

7. 日常使用工具

    ```
    brew install --cask appcleaner google-chrome microsoft-edge flux iina one-switch mweb-pro qq wechat licecap tencent-lemon maczip hiddenbar obsidian itsycal hazeover eudic calibre
    ```
    
    备注：
    - 使用brew 下载的 firefox 是国外版本，其账号系统和国内的火狐是不通的
    - 迅雷（thunder），不再使用
    - [Usage](https://usage.pro/)（usage） 不再使用，改用腾讯出品的柠檬清理（tencent-lemon）
    - One Swithc（one-switch）、MWeb Pro（mweb-pro） 均需要付费，请谨慎选择
    - virtualbox 不再使用，原因：暂时没有建立虚拟机的需求，已经购买了云主机
    - 网易云音乐（neteasemusic）Homebrew 下载的经常有小问题，排查未果后，现通过[官方网站下载](https://music.163.com/#/download)


8. 编程效率工具

    ```
    brew install --cask iterm2 sourcetree alfred postman picgo upic switchhosts dash
    ```
    
    备注：cheatsheet 暂时不支持M1 系列芯片，等待支持后再加入
    

9. 扩展预览程序<sup>[2]</sup>

    ```
    brew install --cask qlcolorcode qlstephen qlmarkdown quicklook-json qlimagesize suspicious-package quicklookase qlvideo webpquicklook
    ```

10. 命令行工具

    ```
    brew install wget curl mycil httpie lftp lrzsz jq xz coreutils autojump shellcheck htop axel cloc thefuck wtf fzf exa bat tmux gh youtube-dl imagemagick restic
    ```
    
    备注：已买的M1 Mac Mini 自带了git，这里不再安装

11. 编辑器

    - Visual Studio Code
    
        ```
        brew install --cask visual-studio-code
        ```

12. Node

    ```
    brew install node
    ```

13. NVM

    ```
    curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
    ```
    
    备注：12 和 13 选择一种方式即可。

14. ZSH

    ```
    brew install zsh zsh-completions
    ```

15. JDK（存疑，待修订）

    ```
    brew tap caskroom/versions
    brew install --cask java8
    ```

### 已不再使用Atom 和 Sublime Text，这里仅仅给出安装方式，便于读者参考，如有问题请自行搜索
    
    - Atom
    
        ```
        brew install --cask atom
        ```
    - Sublime Text 3

        ```
        brew install --cask sublime-text
        ```


[1]: https://www.pokooo.com/6808.html
[2]: https://github.com/sindresorhus/quick-look-plugins


