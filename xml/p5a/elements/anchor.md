# anchor

參考 [TEI anchor 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-anchor.html)

## id 以 fx 開頭

T01n0001, 42c08  
內文：見其村人[20]隊隊相隨  
校勘：隊隊＝隤隤【聖】＊

T01n0001, 42c10  
內文：彼人何故群＊隊相隨？​

XML:

```xml
彼人何故群<anchor xml:id="fxT01p0042c03"/>隊相隨？​
```

## type="circle"

T01n0008, p. 211a21, XML:

```xml
即時<anchor type="circle"/>合掌頂禮說伽陀曰：
```

原書內文作：

	即時◎[02]合掌頂禮說伽陀曰：