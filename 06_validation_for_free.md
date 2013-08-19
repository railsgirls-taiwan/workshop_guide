# Ch. 6: 避免壞東西寫進系統裡…

###本章目標:
* 了解為什麼要有validation
* 了解如何使用validation

> 雖然其實蠻短的，教練判定時間不夠的話就跳過這章吧，deploy比較重要。
> 先請學員輸入一筆名稱空白的資料看結果。

## 確定使用者有輸入Title, Amount及Date
1. 開啟`app/models/record.rb`，在`belongs_to`的下一行加入:

    ```ruby
    validates :title, :amount, :date, presence: true
    ```

1. 重新整理瀏覽器，試著新增空白的資料。

## 確定使用者輸入的amount是數字
1. 在同一個檔案中，加入:

    ```ruby
    validates :amount, numericality: true
    ```

1. 重新整理瀏覽器，試著新增非數字的資料。
