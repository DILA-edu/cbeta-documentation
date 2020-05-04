# CBETA Documentation

CBETA 技術說明文件。

# What is CBETA?

http://www.cbeta.org/

# Web Service

[CBETA 漢文大藏經網站網址規則](http://tripitaka.cbeta.org/url_rules) 2017-01-28

# XML

CBETA 文本採用的主要格式，說明詳見 [xml](xml) 資料夾。

# BM

CBETA Basic Markup 又稱「簡單標記版」，一冊一檔，純文字加上行首資訊、簡單標記。

[CBETA BM on Github](https://github.com/mahawu/BM_u8)

# 藏經代碼

CBETA 佛典集成收錄多套藏經，每套藏經給予一個唯一的 ID，列表請看 [這裡](http://www.cbeta.org/format/id.php)。

## 藏經排序

目錄排序（以下為各個藏經代碼）:  
T X A K S F C U P J L G M D N ZS I ZW B GA GB

全文檢索結果依據資料的參考價值按以下藏經代碼排序:  
T X A K S F C D U P J L G M N ZS I ZW B GA GB

上面兩種排序主要差別在 D 《國家圖書館善本佛典》。

# 卍續藏 三種版本

CBETA 網站對於 [卍續藏三種版本及其對照說明](http://www.cbeta.org/data-format/zrx.htm#zrx)

CBETA 在 Github 上的 [卍續藏X2R行號對照表](https://github.com/cbeta-git/cbwork-common-X2R)

# 典籍編號

## 四碼數字

經號通常為四碼數字，例如 T01n0001

## 四碼數字 + 英文字母

例如 T02n0128a.xml, T02n0128b.xml, 在主檔名最後多了小寫英文.  
這是大正藏只給了一個經號 128 《須摩提女經》, 但是在內文裡收了兩個異本.  
所以 CBETA 以不同的經號 128a, 128b 來區別.

又如 T02n0150A.xml, T02n0150B.xml, 在主檔名最後多了大寫英文  
這是大正藏只給一個經號 150, 但是有給了兩個編號 150A, 150B,  
CBETA 就根據這兩個編號為檔名.

以上檔名最後的大小寫英文分別表示不同的情況, 這是須留意的.  
大寫英文是大正藏給的, 小寫英文是 CBETA 給的.

## 英文字母 + 三碼數字

新文豐出版的嘉興藏分成正藏與續藏，其經號Ａ開頭為正藏，Ｂ開頭則為續藏，後接三位數。
例如 J01nA042.xml

# 插圖

https://github.com/cbeta-git/CBR2X-figures

# 缺字圖檔

* 漢字 https://github.com/cbeta-org/gaiji-CB
* 悉曇字 https://github.com/cbeta-org/sd-gif
* 蘭札體 https://github.com/cbeta-org/rj-gif

# 電子書封面

https://github.com/cbeta-org/ebook-covers
