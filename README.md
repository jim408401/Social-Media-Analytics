# Social-Media-Analytics

## 專案說明：對 ptt 股市版面關鍵字為「台積電」的文章進行文本分析、情緒分析
## 套件說明：
- jieba : 中文斷詞套件
- wordcloud : 文字雲繪圖工具
- CKIP : 全名為 Chinese Knowledge and Information Processing，中研院開發的中文自然語言處理工具。
- SnowNLP : SnowNLP是一個可以方便的處理中文文本內容的python類庫，主要功能包括斷詞、詞性標註、情緒分析、漢字轉拼音、繁體轉簡體、關鍵詞提取以及文本摘要等等。
- NLTK: 全名為Natural Language Tool Kit，自然語言處理工具。
- CountVectorizer, TfidfTransformer: sklearn中計算詞頻與tf-idf的套件。

## 文字處理基本流程
+ **資料初步清理：** <br>
將文字內容轉為正規的語句，例如：去除特定標籤、符號、統一標點符號的使用等等。<br><br>
+ **斷句斷詞：** <br>
使用工具區隔文章中不同的句子、詞彙 <br><br>
+ **去除停用字：** <br>
停用字就是與分析無關的詞彙，甚至這些詞彙可能會影響分析的結果。   
因此我們必須在資料處理的過程中將其排除。例如：語助詞 <br><br>
+ **產生結構化資料：** <br>
根據需求產生不同結構化資料(Tidy Data)，以供後續分析使用。 <br><br>
+ **應用更多分析：** <br>
進行不同的分析，例如：詞頻分析、情緒分析、文辭和文件分析、文件分類、社會網路分析等等。

## 情緒分析
+ **Lexicon-based 情緒分析：** <br>
進行基於情緒字典的情緒分析，首先需要準備情緒字典後再將字典與斷詞後的文章進行合併<br><br>
+ **SnowNLP Courpus-base 情緒分析：** <br>
SnowNLP是Courpus-base的情緒分析，不是使用情緒字典，而是使用預訓練的情緒分析模型或演算法，給與整個文章一個情緒分數。<br><br>
