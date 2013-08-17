# Ch. 1: 環境設定指南

###本章目標:

* 了解如何設定環境
* 之後在同一台電腦上開發自己的網站時，這一章的步驟不需要再重複。
* 建議學員打開檔案，用copy & paste進行操作

>  *行前通知:*
>
>  * 請Mac user在提前申請[Apple developer](https://developer.apple.com/downloads/index.action)帳號，並下載Command Line Tools
>  * 請所有人申請[Heroku]()帳號
>  * 請Windows user下載Virtual Box

##Quick Links
* [Mac](https://github.com/railsgirls-taiwan/workshop_guide/blob/master/01_env_setup.md#mac)
* [Linux](https://github.com/railsgirls-taiwan/workshop_guide/blob/master/01_env_setup.md#linux)
* [Windows](https://github.com/railsgirls-taiwan/workshop_guide/blob/master/01_env_setup.md#windows)

## Mac

  1. ###OSX Command Line Tools
    (如果有XCode，從XCode介面來裝)，沒有的話到上面的網址下載

  1. ###安裝Homebrew
        ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)"

  1. ###安裝及設定Git
        brew install git
        git config --global user.name "你的名字"
        git config --global user.email "你的Email"

  1. ###安裝RVM
        \curl -L https://get.rvm.io | bash -s stable

    記得重開Terminal

  1. ###安裝Ruby
        rvm install 2.0.0
        rvm use 2.0.0 --default
        ruby -v

  1. ###安裝Rails
        gem install rails
        rails -v

  1. ###Prettify terminal?
    [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) or [bash-it](https://github.com/revans/bash-it)(有人試過這個嗎?)

  1. ###安裝編輯器
     下載[Sublime Text](http://www.sublimetext.com/)然後安裝

## Linux

  1. ### 更新apt-get，是yum的話請舉一反三
     (這步會有點久，不過會帶Linux來的想必是大大， 大大都會自己更新)

        sudo apt-get update
        sudo apt-get upgrade

  1. ### 安裝Git及其它必要元件 (請協助除錯)
        sudo apt-get install git curl build-essential zlib1g-dev libssl-dev libreadline-dev xlcip
        echo "alias clipboard='clip -sel clip'" >> ~/.bashrc
        git config --global user.name "你的名字"
        git config --global user.email "你的Email"

  1. ### 安裝RVM
        \curl -L https://get.rvm.io | bash -s stable

    記得重開Terminal

  1. ### 安裝Ruby
        rvm install 2.0.0
        rvm use 2.0.0 --default
        ruby -v

  1. ### 安裝Rails
        gem install rails
        rails -v

  1. ###Prettify terminal?
    [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) or [bash-it](https://github.com/revans/bash-it)(有人試過這個嗎?)

  1. ###安裝編輯器
     下載[Sublime Text](http://www.sublimetext.com/)然後安裝


## Windows

* Virtual Box

* Native?

    其實不難裝

    Pros:

    * 硬體要求沒有VirtualBox那麼高。

    Cons:

    * 命令提示字元很渣，用的指令要把ls改成dir，然後斜線反向。
    * 要Comple的gem也許有一些雷(聽說bootstrap沒問題了?)
