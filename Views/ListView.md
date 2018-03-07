# ListView

## MiSA Event

### insertRow(data[,replace])

在 ListView 新增一列資料。
如果有傳入 replace，則取代 replace 的位置。

### clear()

清空 ListView。

### loaded(datas)

當 UI.Data 讀取結束或是 createPage 時讀取到 "data" 關鍵字時，會透過這個事件將資料傳進來。
將資料存進 _dataList 後，呼叫 paginate 事件重新調整 Pagination 元件。
Pagination 元件會在調整分頁後呼叫 move 事件，並重新導向第一頁。

### move(page)

顯示 page 頁數的資料內容。
呼叫 clear 事件清空 ListView，然後透過 insertRow 事件將資料增加進入表格。

### create(data)
