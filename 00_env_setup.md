# Ch. 1: 環境設定指南

### 本章目標

* 了解如何設定環境。
* 之後在同一台電腦上開發自己的網站時，這一章的步驟不需要再重複。
* 建議學員打開檔案，用複製與貼上來進行操作。

>  *行前通知:*
>
>  * 請 Mac 使用者提前申請 [Apple developer](https://developer.apple.com/downloads/index.action)帳號，並下載命令行工具。
>  * 請所有人申請 [Heroku](https://www.heroku.com/) 帳號。
>  * 請 Windows 使用者下載 Virtual Box。

## 目錄

* [Mac](#mac)
* [Linux](#linux)
* [Windows](#windows)

## Mac

### 1. OSX 命令行工具

  [安裝檔下載](https://github.com/kennethreitz/osx-gcc-installer/downloads)

### 2. 安裝 [Homebrew](http://brew.sh/index_zh-tw.html)

    ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"

### 3. 安裝及設定 Git

    brew install git
    git config --global user.name "你的名字"
    git config --global user.email "你的 Email"

### 4. 安裝 RVM (Ruby 版本管理工具)

    curl -L https://get.rvm.io | bash -s stable

  記得重開終端機。

### 5. 安裝 Ruby

    rvm install 2.0.0
    rvm use 2.0.0 --default
    ruby -v

### 6. 安裝 Rails

    gem install rails
    rails -v

### 7. 美化終端機?

  [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) 或 [bash-it](https://github.com/revans/bash-it) （有人試過這個嗎?）

### 8. 安裝編輯器

  下載並安裝 [Sublime Text](http://www.sublimetext.com/)。

### 9. 安裝 Heroku 開發工具

  下載並安裝 [heroku toolbelt](https://toolbelt.heroku.com/)。

## Linux

### 1. 更新 `apt-get`，是 `yum` 的話請舉一反三

  （這步會有點久，不過會帶 Linux 來的想必是大大， 大大都會自己更新）

    sudo apt-get -y update
    sudo apt-get -y upgrade

### 2. 安裝 Git 及其它必要元件 (請協助除錯)

    sudo apt-get -y install git-core curl build-essential zlib1g-dev libssl-dev libreadline-dev libyaml-dev
    git config --global user.name "你的名字"
    git config --global user.email "你的Email"

### 3. 安裝RVM

    curl -L https://get.rvm.io | bash -s stable

  記得重開終端機。

### 4. 安裝 Ruby

    rvm install 2.0.0
    rvm use 2.0.0 --default
    ruby -v

### 5. 安裝 Rails

    gem install rails
    rails -v

### 6. 美化終端機？

  [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) or [bash-it](https://github.com/revans/bash-it) （有人試過這個嗎？）

### 7. 安裝編輯器

  下載並安裝 [Sublime Text](http://www.sublimetext.com/)。

### 8. 安裝 Heroku 開發工具

  下載並安裝 [heroku toolbelt](https://toolbelt.heroku.com/)。

## Windows

* [Rails Installer](http://railsinstaller.org/en)

* Virtual Box

* Native?

  其實不難裝

  優點：

  * 硬體要求沒有 VirtualBox 那麼高。

  缺點：

  * 命令提示字元很渣，用的指令要把 ls 改成 dir，然後斜線反向。
  * 要 Compile 的 gem 也許有一些雷（聽說 bootstrap 沒問題了？）
