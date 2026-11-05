# lb

換行 (line break)

## 同時記錄兩個版本的行號

例如 X01n0001.xml

```xml
<lb ed="X" n="0001a07"/><lb ed="R150" n="0705a04"/>卷一帖。一紙廿行。行十二字。經末有左藏庫西潘
```

ed="X" 是《卍新纂大日本續藏經》的行號，ed="R150" 是《卍續藏經-新文豐版》第150冊的行號。

## @n

行號的前四碼是頁碼，通常都是數字，但是也有例外，
例如 a001、b001、c001...，是「正文」之前的內容，如「序文」、「目錄」等等，因為這些「序文」、「目錄」也是各別從第1頁開始。
另外，可能也有 x001、y001、z001...，這是「正文」之後的內容，如「索引」等等。

例如 GA020n0017.xml：

```xml
<pb ed="GA" xml:id="GA020.0017.a003a" n="a003a"/>
<lb ed="GA" n="a003a01"/>
```
### 行號重複

行號通常不會重複，但也有例外，例如 X01n0010.xml：
```xml
<lb n="0353a02" ed="X"/><lb n="0682a01" ed="R001"/> 大明仁孝皇后夢感佛說第一希有
<lb n="0353a03" ed="X"/><lb n="0682a01" ed="R001"/>大功德經序</head>
```

## @type
### honorific

例如 J25nB154.xml, p. 35a26

```xml
<p xml:id="pJ25p0035a2601">
<note place="inline">吳江縣　佛弟子張維法名智嚴
<lb ed="J" n="0035a27" type="honorific"/>沈學閔法名淨英　董之垣法名明震捐資刻
<lb ed="J" n="0035a28" type="honorific"/>唯菴禪師語錄第一卷
<lb ed="J" n="0035a29" type="honorific"/>　吳門九章朱袞對稿　金陵潘　耕書
<lb ed="J" n="0035a30" type="honorific"/>　　　　　　　　　　自聞道人　蔣成榮刊
</note>
</p>
```

### old

例 Y25n0025.xml

```xml
<lb n="0170aa01" ed="Y" type="old"/>
```

### forced

強制換行。不帶 `@ed`、`@n`，不對應底本的行號，只表示呈現時要在此處換行。
用在表格儲存格 (`<cell>`) 等內容會連續排列的地方，需要保留斷行時使用。
轉為 HTML 時應輸出 `<br>`。

例一：底本儲存格內第二行縮排接續的英文書目，在新行號之後加上 `<lb type="forced"/>`，讓呈現時確實換行。

YP30n0031.xml, p. 13a01

```xml
<lb ed="YP" n="0013a01"/>Kathāvatthu, P. T. S. 2 volumes.
<lb ed="YP" n="0013a02"/><lb type="forced"/>　Points of Controversy, by Aung and Mrs. Rhys Davids (London 1915).</cell></row><row><cell cols="4" style="border-left:none;border-right:none">
```

例二：底本以大括號分支的樹狀圖改為平鋪重述，在同一行內插入強制換行，分開兩個分支。

YP30n0031.xml, p. 525a11

```xml
<lb ed="YP" n="0525a11"/><row><cell>28</cell><cell>有因業、有緣業｛</cell><cell>（有因＝有緣＝有緣轉業）。<lb type="forced"/>（有因＝有緣＝共業）。<note n="0525a1101" resp="CBETA.liyi" type="add" note_key="YP30.0525a11.09">CBETA 按：底本「有因＝有緣＝」下以大括號分立「有緣轉業」、「共業」二支。今為適應數位文本排版，將樹狀圖改採平鋪重述，作：（有因＝有緣＝有緣轉業）、（有因＝有緣＝共業）。</note></cell></row>
```
