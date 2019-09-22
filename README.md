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
brew install brew-cask-completion
```

出现错误：

```
Error: Cask 'brew-cask' is unavailable: '/usr/local/Homebrew/Library/Taps/caskroom/homebrew-cask/Casks/brew-cask.rb' does not exist. 
```

再安装：
```
brew install caskroom/cask/brew-cask
```