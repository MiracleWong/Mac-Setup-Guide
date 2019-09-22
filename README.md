# DevOps 工程师的 macOS 搭建指南

Why：本项目的灵感来自于 [Phodal Huang](https://github.com/phodal)  的项目 [setup.guide](https://github.com/phodal/setup.guide) , 觉得这种总结的方式十分的好，方便以后从无到有地搭建一个合适宜用的macOS环境。加之我的RMBP因为苹果的电池🔋召回计划而返厂维修，自己把所有的数据清空了，刚好进行本项目的尝试。

What：这是一个几乎靠命令行安装 macOS 软件的仓库。
对于需要在网站下载dmg、pkg等软件、或者在Mac App Store下载的软件，请参照我的另一个仓库：


How：

1. Install Xcode
    PS：在Mac App Store 上安装

2. Install Xcode命令行工具

    ```
    xcode-select --install
    ```

3. Install Homebrew

    ```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

4. Install Homebrew Cask

    ```
    brew install caskroom/cask/brew-cask
    ```

    出现错误：

    ```
    Error: Cask 'brew-cask' is unavailable: '/usr/local/Homebrew/Library/Taps/caskroom/homebrew-cask/Casks/brew-cask.rb' does not exist. 
    ```

    再安装：
    ```
    brew install brew-cask-completion
    ```

    测试：
    ```
    brew search qq
    ```

5. JDK

    ```
    brew tap caskroom/versions
    brew cask install java8
    ```
6. Python

    ```
    ```

7. 日常使用工具

    ```
    brew cask install  google-chrome firefox（国外版）flux iina neteasemusic one-switch mweb thunder qq wechat virtualbox
    ```

8. 编程效率工具

    ```
    brew cask install iterm2 sourcetree alfred cheatsheet postman picgo 
    ```

9. 扩展预览程序<sup>[1]</sup>

    ```
    brew cask install qlcolorcode qlstephen qlmarkdown quicklook-json qlimagesize suspicious-package quicklookase qlvideo webpquicklook
    ```

10. 命令行工具

    ```
    brew install git wget curl mycil httpie lftp lrzsz jq xz coreutils autojump shellcheck htop axel cloc thefuck wtf fzf exa bat
    ```

11. 编辑器

    - Sublime Text 3

        ```
        brew cask install visual-studio-code
        ```

    - Visual Studio Code
    
        ```
        brew cask install visual-studio-code
        ```

    - Atom
    
        ```
        brew cask install atom
        ```

12. NVM

    ```
    curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
    ```

13. ZSH

    ```
    brew install zsh zsh-completions
    ```

12 已安装软件和工具说明
    TODO



[1]: https://github.com/sindresorhus/quick-look-plugins

