# Ch. 2: CashBook - 線上記帳本
> 主題可以再討論

### 本章目標:

* 了解如何建立一個新的專案
* 了解如何使用Scaffold快速新增功能

> Rails是框架，Ruby是語言

> Rails的核心概念:
>> * Convention over configuration
>> * DRY (Don't repeat yourself)

## 把新網站設定起來

1. 建一個新的網站專案:

  ```
  rails new CashBook
  ```

  > * 指令 => rails
  > * 動作 => new
  > * 專案名稱 => _CashBook_

2. 切換到網站的目錄裡:

      cd CashBook

3. 建立資料庫:

      rake db:create

## Rails剛剛做了什麼事?
## TODO: 請幫忙補一下資料夾結構的說明

## 新增第一個功能

  1. Scaffold: 鷹架 - 快速建立功能的模版

    ```
    rails g scaffold record title:string amount:float date:date
    ```

  > * 指令 => rails
  > * 動作 => generate (g 是縮寫)
  > * 種類 => scaffold
  > * 名稱 => record
  > * 欄位:資料類型 => title:string

  其它資料類型: text, integer, boolean...

  1. 叫Rails幫我們設定資料庫

        rake db:migrate

  1. 試試看你的作品吧，這個指令會把server(伺服器)跑起來

        rails s

    用瀏覽器開啟[http://localhost:3000/records](http://localhost:3000/records)

> scaffold自動產生了以下幾樣東西:
>> * 一張叫records的資料表(複數喔)
>> * 一個叫record.rb的model, 在app/models/裡
>> * 一個叫records_controller的controller，在app/controllers/裡
>> * 一組顯示的頁面，在app/views/records/裡
>> * 一組網址(restful)
>> * 相關的javascript, css檔案(其實是coffeescript及scss)

## 把首頁設成`/records`

  1. 打開`config/routes.rb`，加入

    ```ruby
    root 'record#index'
    ```
