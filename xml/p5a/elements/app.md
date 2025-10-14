# app

不同版本的不同用字

例如：T01, No. 1, p. 1，大正藏原文：

	T01n0001_p0001a14║言法歸。法歸者。蓋是萬善之淵府。總持之林
	T01n0001_p0001a15║苑。其為典也。淵博弘富。[05]韞而彌廣。明宣禍

校勘條目

	[05] 韞＝溫【宋】【元】

表示此處大正藏作「韞」字，而宋本、元本作「溫」字。

XML

```xml
<lb n="0001a15"/>苑。其為典也。淵博弘富。
<note n="0001005" resp="Taisho" type="orig" place="foot text">韞＝溫【宋】【元】</note>
<app n="0001005">
    <lem>韞</lem><!-- 大正藏用字 -->
    <rdg wit="【宋】【元】" resp="Taisho">溫</rdg><!-- 其他版用字 -->
</app>而彌廣。明宣禍
```

上面 rdg 元素的 wit 屬性請參考 [../attributes/wit.md](../attributes/wit.md)

## @type

### star

大正藏將重複的校勘以星號＊表示同上，
CBETA 使用 `<app type="star">` 標示。
	
ex: T11n0310.xml

```xml
<note n="0020009" resp="Taisho" type="orig" place="foot text">惟＝唯【宮】＊</note>
<note n="0020009" resp="CBETA" type="mod">惟【大】＊，唯【宮】＊</note>
<app n="0020009">
  <lem wit="【大】">惟</lem>
  <rdg resp="Taisho" wit="【宮】">唯</rdg>
</app>願開示如是法門
...(中略)...
<app type="star" corresp="#0020009">
  <lem wit="【大】">惟</lem>
  <rdg resp="Taisho" wit="【宮】">唯</rdg>
</app>願大慈威加守護
```

### star_removed

type="star_removed" 表示底本有個星號「＊」校勘，CBETA 修訂拿掉這個「＊」校勘。
因為 CBETA 在這裡選擇跟底本不同的用字，已經不適用「下同」。

此類標記在呈現底本時顯示星號「＊」，呈現 CBETA 版本時則不顯示星號「＊」。

例如 T01n0023.xml, p. 303c29

```xml
<lb n="0303a10" ed="T"/>...<app n="0303004">...</app>
... (中略) ...
<lb n="0303c29" ed="T"/>...
<note n="0303c2901" resp="CBETA" type="add">越【CB】【磧-CB】，趣【大】，越【宋】【元】【明】</note>
<app type="star_removed" corresp="#0303004">
  <lem wit="【CB】【磧-CB】" resp="CBETA.maha">越<note type="cf1">Q18_p0745a18</note><note type="cf2">T01n0023_p0277b11</note></lem>
  <rdg wit="【大】">趣</rdg>
  <rdg resp="Taisho" wit="【宋】【元】【明】">越</rdg>
</app>
```

## @rend

例 Y34n0032.xml 不呈現的校勘：

```xml
<app n="0324a0101" rend="hide">...</app>
```

## @note_key

對應 [CBETA 校訂考證資料庫](https://revisiondb.cbeta.org) 裡的「校注 ID」。

例 T01n0001_p0001a29

```xml
<note n="0001a2901" resp="CBETA.shin" cb:provider="來函：DL (2022-03-16)" type="add" note_key="T01.0001a29.07">
  CBETA 按：「一分四十五卷」，
  《磧砂》乙本（QC053n0665_p0635b11）、《洪武南藏》（U089n0585_p0406a05）、《永樂北藏》（P059n0541_p0572a06-07）、《嘉興藏》（日本東京大學綜合圖書館藏正編第78帙第5冊第6圖左欄第3行）作「一分四十五卷」，
  《福州藏》（日本宮內庁書陵部藏大藏經第2765帖第3圖第23至24行）作「二分四十品」。
</note>
```

上面 note_key 屬性值 "T01.0001a29.07" 可用於連結到 CBETA 校訂考證資料庫： https://revisiondb.cbeta.org/?notekey=T01.0001a29.07
