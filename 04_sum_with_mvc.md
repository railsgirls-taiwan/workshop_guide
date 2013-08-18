# Ch. 4: 顯示金額加總

###本章目標:
* 了解如何在Model增加Business logic
* 了解如何Controll中取值
* 了解如何在View上顯示取出來的值

# 真正計算總金額的地方
1. 找到`app/models/record.rb`，加入這幾行

```ruby
def self.sum
  all.sum(&:amount)
end
```
# 每次進入列表頁面時，進行計算
1. 找到`app/controllers/records_controller.rb`，在`def index`裡加入這幾行:

```ruby
@sum = Record.sum
```

# 顯示在畫面上
1. 找到`app/views/records/index.html.erb`，在`</table>`的下方加入這幾行

```html
<hr />
<p>
Total: <%= @sum %>
</p>
```
> 然後就跟學員說這個叫MVC架構
