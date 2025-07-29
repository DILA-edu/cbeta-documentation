# CBETA XML P5a

CBETA 公開提供 XML P5a 的網址：https://github.com/cbeta-git/xml-p5a

## Characters

* “□” (U+25A1) 表示此處應該有字，但編書的人也不知道是什麼字，就印出一個空白方塊「□」。
* XML `<unclear>` 元素 轉成各版用字會使用 “▆” (U+2586) 字元，這是 CBETA 認為書中文字難以辨識，例如影印古籍，但此處有污損或蟲蛀，所以使用「▆」表示。 

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
