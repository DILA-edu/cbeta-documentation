# figure

插圖。

參考：[TEI figure 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-figure.html)

例 T16n0719, p. 845c19

```xml
<figure><graphic url="../figures/T/T16p0845_01.gif"/></figure>
```

目前不管是行中小圖或是區塊插圖，CBETA 都是使用 figure 包 graphic，  
如果是區塊插圖，另外在 figure 外面包 p，  
所以在將 XML 轉為各種版本時，是忽略 figure 標記。
