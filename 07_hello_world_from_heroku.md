# Ch. 7: Hello world from heroku

###本章目標:
* 了解必要的git指令
* 了解如何用Heroku發佈網站

## 配合heroku的修改 
1. 打開Gemfile，找到`gem 'sqlite3'`這行，改成
    ```ruby
    group :production do
      gem 'pg'
      gem 'rails_12factor'
    end

    group :development, :test do
      gem 'sqlite3'
    end
    ```

1. 打開`config/database.yml`，找到`production`，將底下那行改成
    ```ruby
    adapter: postgresql
    ```

## 初始化Git，並加入所有的檔案
> Git是非常有用的版本控制系統，對Ruby/Rail programmer來說更是不可或缺的工具。
> 這次由於時間的關係無法講太多，只用基本的指令來進行deploy，但是請務必找時間學好喔。

1. 在終端機輸入以下指令
    ```shell
    git init
    git add --all
    git commit -m 'first deploy'
    ```

## 登入heroku，並進行佈署
  1. 在終端機輸入`heroku login`，並輸入申請好的email及密碼。

  1. 輸入以下指令
    ```shell
    heroku create
    git push heroku master
    heroku run rake db:migrate
    ```

  1. 上一步跑完之後，會在倒數第三行印出一段網址，用瀏覽器打開看看吧。

## 成果範例

  [http://railsgirls-cashbook.herokuapp.com/](http://railsgirls-cashbook.herokuapp.com/)
