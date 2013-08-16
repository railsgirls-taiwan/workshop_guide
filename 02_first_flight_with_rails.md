# Ch. 2: CashBook - 線上記帳本
> 主題可以再討論

### 本章目標:

* 了解如何建立一個新的專案
* 了解如何使用Scaffold快速新增功能

## 把新網站設定起來

  1. 建一個新的網站專案:
        rails new CashBook

    * 指令: rails 
    * 動作: new 
    * 專案名稱: _CashBook_ (自行設定)

  1. 切換到網站的目錄裡:
        cd CashBook

  1. 初始化資料庫:
        rake db:migrate


## 新增第一個功能

  1. Scaffold: 鷹架 - 快速建立功能的模版
        rails g scaffold record title:string amount:float date:date

    * 指令: rails 
    * 動作: generate (g 是縮寫)
    * 種類: scaffole
    * 名稱
    * 欄位:資料類型

    其它資料類型: text, integer, boolean...

  1. 叫Rails幫我們設定資料庫
        rake db:migrate

  1. 試試看你的作品吧，這個指令會把server(伺服器)跑起來
        rails s

    用瀏覽器開啟http://localhost:3000/records

> 解釋一下剛剛自動產生了什麼東西, 特別是資料庫的部份
