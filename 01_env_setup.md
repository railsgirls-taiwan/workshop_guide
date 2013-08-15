# Day 1: 環境設定指南

## Mac

  *行前通知:* 請Mac user在前一天申請[Apple developer site](https://developer.apple.com/downloads/index.action)帳號

  1. ###OSX Command Line Tools
    (如果有XCode，從XCode介面來裝), 沒有的話到上面的網址下載

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
        ruby -v

  1. ###安裝Rails
        gem install rails
        rails -v

  1. ###Prettify terminal?

    [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) or [bash-it](https://github.com/revans/bash-it)(有人試過這個嗎?)
  
  1. ###安裝編輯器
     下載[Sublime Text](http://www.sublimetext.com/)然後安裝

## Linux

## Windows

* Virtual Box

* Native? 

    其實不難裝
    
    Pros: 
    
    * 硬體要求沒有VirtualBox那麼高。
    
    Cons: 

    * 命令提示字元很渣，用的指令要把ls改成dir，然後斜線反向。
    * 要Comple的gem也許有一些雷(聽說bootstrap沒問題了?)
