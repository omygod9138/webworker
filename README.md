#Web Worker 介紹

Javacsript 是個單執行序的語言, 單執行序就是每個任務都必須有個執行結果才會進行到下一個任務執行.
單執行序最大的問題就是, 當你遇到需要較多時間來執行運算的時候, 所有的任務就會因等待而造成執行的時間變長.
這就是所謂的 blocking.在Client端若是因blocking造成等待時間過長, 會讓使用者繼續瀏覽的意願大大降低.
Web worker 提供了多執行序的功能, 能讓Javascript在等待時先執行其他的任務來降低等待的時間.

Web worker 雖然好用, 但有一些限制:

1. Same Origin Policy
	所有的script必須是在同一個domain才能執行. 這也包括了通訊協定, 例如, 一個在http:// 開啟的網頁是不能用https:// 來呼叫worker的script.
	
2. 存取的限制
	由於web worker 不是跟主應用程式同一個執行序, 所以它對於 DOM, document物件, window物件和parent物件是沒有存取權限的.
	
3. 只能通過http協定啟用
	如果是用 file:// 等方式是不能執行web worker的

