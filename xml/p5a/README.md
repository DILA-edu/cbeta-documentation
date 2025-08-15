# CBETA XML P5a

CBETA 公開提供 XML P5a 的網址：https://github.com/cbeta-git/xml-p5a

## 字元 (Characters)

* “□” (U+25A1) 表示此處應該有字，但編書的人也不知道是什麼字，就印出一個空白方塊「□」。
* XML `<unclear>` 元素 轉成各版用字會使用 “▆” (U+2586) 字元，這是 CBETA 認為書中文字難以辨識，例如影印古籍，但此處有污損或蟲蛀，所以使用「▆」表示。
* 早期是 Big5 以外的字元做缺字處理，後來是 Unicode 3.0 以外的字會做缺字處理，以 `<g>` 元素標記。
  * 考慮到手機等行動裝置未能正確顯示全部 Unicode，因此將門檻定在 Unicode 3.0.
* 但有一些字元會以 通用字 做 正規化處理，詳見： CBETA 官方文件 [通用變異字形](https://cbeta.org/files/char_regular.zip)。
* CBETA 進行《嘉興藏》數位化時，有擴大「通用字 正規化」的範圍。
  * 嘉興藏 是繼 大正藏、卍續藏 之後的重頭戲，也是 CBETA 繼鉛版印刷（大正藏、卍續藏）之後所面對的木刻印刷作品。
  * 鉛版印刷 的 異體字 較少，木刻印刷 的 異體字 暴增。
  * CBETA 嘉興藏 的錄入時期約在 2008-2009 年，當時 Unicode 收錄漢字沒有如今那麼多。
  * CBETA 根據 教育部《異體字字典》，如果查到「異體字」有對應的「正字」，會直接採用「正字」。
  * CBETA 《嘉興藏》裡面有哪些字詞 採用了 通用字、通用詞，沒有列表記錄。

## Elements

各個元素的說明詳見 [elements](elements) 資料夾。

## XML Comments

### CBETA todo type: a

未以 app 標記不同版本間的差異，例 T30n1581.xml

```xml
<lb n="0909b04" ed="T"/>施與，
<note resp="Taisho" n="0909035" place="foot text" type="orig">〔若他…薩〕二十字－【三】【宮】</note>
<note resp="CBETA" n="0909035" type="mod">
  <!--CBETA todo type: a-->（若他…薩）二十字【大】，〔－〕【宋】【元】【明】【宮】
</note>
若他所須，是名略說菩薩四種一切門
```
