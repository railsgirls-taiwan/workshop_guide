# Ch. 3: 一分鐘讓網站變漂亮

###本章目標:

* 了解編輯器的基本操作
* 了解如何使用Ruby gem來套用別人寫好的功能
* 介紹一些有名的gems跟如何找到適合自己的gem

## 在專案中加入twitter-bootstrap-rails gem

> 雖然bootstrap-sass比較好，但是這個有generator

  1. 打開Sublime Text，開啟CashBook目錄

  1. 按ctrl + p，輸入Gemfile，按下Enter開啟檔案

  1. 在檔案最底下加入
        gem 'therubyracer'
        gem 'less-rails'
        gem 'twitter-bootstrap-rails'

  1. 按ctrl + s 存檔

## 下載gem並安裝

  1. 回到Terminal，按下 ctrl + c 停止server，再輸入
        bundle

> 記得這個時候要能連到網路

## 把twitter bootstrap套用到網站上

  1. 自動產生基礎css檔案

        rails g bootstrap:install

  1. 覆寫剛剛Scaffold的樣式

        rails g bootstrap:themed Records

    出現Overwrite提示時，輸入a按下Enter

## 重新啟動Server
  1. 用什麼指令把server跑起來?

        rails s

    重新整理瀏覽器

> 介紹底下這些網站跟devise, omniauth, kaminari...

> * [RubyGems.org](https://rubygems.org/)
> * [Rubytoolbox](https://www.ruby-toolbox.com/)
> * [RailsCasts](http://railscasts.com/)
> 
