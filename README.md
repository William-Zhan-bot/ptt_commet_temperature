# ptt_commet_temperature
以python爬蟲技術與情感分析，計算ptt文章的評論風向

爬蟲部分用request + bs4進行爬取和解碼，
情感分析採用 snowNLP 對所有評論的情感進行逐條分析與統計: 有特殊的格式設計，確保同一人的評論不會PTT發布的斷句受影響
詞頻計算採用 jieba 自訂的政治用詞字典(修改自台灣用語辭典)，進行tf/idf的計算

輸出的內容:
1. 長條圖 顯示文章評論的正/負面情感數量
2. 圓餅圖 顯示文章評論的正/負面情感數量比例
3. 詞頻圖 輸出文章中通用詞語的頻率
4. 前五大文章常出現的關鍵字

-------------------------------------
後續如果有需要可以透過迴圈一次打包大量ptt網址，直接進行多個文章的分析

字典參考自: https://github.com/APCLab/jieba-tw
作者在自行加上一些觀察到ptt政治版常用的詞彙
