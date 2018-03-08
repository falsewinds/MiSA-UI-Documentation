# ListView

表格視圖(View)，用來顯示對多欄位資料的總覽。

## 欄位標題相關屬性

 - headers

headers 必須是一個 Array，其中每個項目都應該是 properties 的其中一個 key，不屬於 properties 的項目會被忽略。
被列在 headers 中的 key 表示會在 ListView 中顯示的欄位，並依照在 headers 中的出現順序，由左到右顯示。
headers 擁有在欄位順序上最高的優先級。

 - order

order 必須是一個 Array，其中每個項目都應該是 properties 的其中一個 key，不屬於 properties 的項目會被忽略。
被列在 order 中的 key 表示在 ListView 中由左到右的出現順序。
order 在 headers 未被設定時才會起作用，並會跟下方提到的 role 以及 optional 搭配產生效果。

 - optional

optional 必須是一個 Array，其中每個項目都應該是 properties 的其中一個 key，不屬於 properties 的項目會被忽略。
被列在 optional 中的 key 表示不會出現在 ListView 欄位。

 - properties/role: header

當沒有 headers 時，被設定具有 header 的 property 將視同被列在 headers 中。
如果 order 沒有被設定，其顯示順序與在 properties 中出現順序一致。

 - properties/role: optional

當沒有 optional 時，被設定具有 optional 的 property 將視同被列在 optional 中。
如果 order 沒有被設定，其顯示順序與在 properties 中出現順序一致。

### 優先級
 1. headers
 2. role:header + order
 3. optional + order
 4. role:optional + order
