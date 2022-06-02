# pb (page break, 換頁)

ex: T01n0001.xml
```xml
<pb n="0001a" ed="T" xml:id="T01.0001.0001a"/>
```

n屬性值 0001a 表示 第1頁 a欄。

## 頁碼開頭不是數字

佛寺志的一冊裡有多部寺志，每部寺志的頁碼都從第一頁開始。  
為了解決一冊之中頁碼重複的問題，頁碼前面加上 a, b 等等。  
例如：GA020n0017.xml
```xml
<pb ed="GA" xml:id="GA020.0017.a001a" n="a001a"/>
```

n屬性值 a001a 表示頁碼 a001 的 a 欄。

其他例子：GA015, 20, 28, 30, 35, 39, 43, 48, 93 等冊,  
每一冊有二套頁碼, 分別為 axxx , bxxx,  
其中 GA043 有 a,b,c,d 四套。