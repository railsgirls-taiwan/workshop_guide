# Ch. 5: 所謂的關係嘛…

###本章目標:
* 了解Relationship是資料間的關聯
* 了解何時用:has_many, :belongs_to

## 加入'類別'功能
  1. 類別只需要'name'這個欄位，再用一次scaffold指令

        rails g scaffold category name:string

  1. 接著要讓record資料表上有`category_id`欄位

        rails g migration add_category_id_to_record category_id:integer

    > 這個指令會在`db/migrate`裡產生一個檔案，有空的話可以研究一下內容。

  1. 要記得更新資料庫

        rake db:migrate
  
## 一個類別會有多筆記錄 (has_many)

  1. 打開`app/models/category.rb`，在中間加入

    ```ruby
      has_many :records
    ```
    > records是複數

## 一筆記錄屬於一個類別 (belongs_to)
  1. 打開`app/models/record.rb`，在中間加入

    ```ruby
      belongs_to :category
    ```
    > catetory是單數

## 先新建幾筆資料，並且把舊的Record資料清空

  1. 用瀏覽器打開`http://localhost:30000/categories`，隨便新增幾筆資料。
  1. `http://localhost:30000/records`將所有資料刪除，如果太多筆或是很懶惰的話，請教練用特技(rails c)幫忙刪…

## 在新增記錄的表單裡，加入category下拉選單

  1. 打開`app/views/records/_form.html.erb`，在中間加入
    ```html
    <div class="control-group">
      <%= f.label :category_id, :class => 'control-label' %>
      <div class="controls">
        <%= f.collection_select :category_id, Category.all, :id, :name %>
      </div>
    </div>
    ```

  1. 打開`app/controllers/records_controller.rb`，把最後一段改成
    ```ruby
    def record_params
      params.require(:record).permit(:title, :amount, :category_id, :date)
    end
    ```
    > `app/views`的各個子資料夾裡，_form.html.erb負責新增及修改時的表單內容

## 在列表頁面上顯示每個record的Category資訊

  1. 打開`app/views/records/index.html.erb`，在一堆`<th>`裡加入
    ```html
    <th><%= model_class.human_attribute_name(:category) %></th>
    ```

    在一堆`<td>`底加入
    ```html
    <td><%= record.category.name %></td>
    ```

    記得`<th>`跟`<td>`各項的順序要對齊。

    > `app/views`的各個子資料夾裡，index.html.erb就是項目的清單頁面。

    > 這一步跟下一步就是抄一下附近的鄰居，再改成你要的內容

## 在單筆記錄頁面上顯示recored的Category資訊
  1. 打開`app/views/records/show.html.erb`，在`record.amount`的下一行加入
    ```html
    <dt><strong><%= model_class.human_attribute_name(:category) %>:</strong></dt>
    <dd><%= @record.category.name %></dd>
    ```

    > 每個view的子資料夾裡，show.html.erb就是單筆資料的顯示頁面。

## 再看看自己的成果吧

  * TIPS: 如果有錯誤的話，很可能是舊的資料沒有清空，讀不到category。用rails c或是delegate吧。

