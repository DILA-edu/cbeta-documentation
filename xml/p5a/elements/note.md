# note

參考：[TEI note 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-note.html)

## 大正藏校勘原文

大正藏校勘原文以 `<note type="orig">` 記錄

例：T01, No. 1, p. 1，大正藏原文：

	T01n0001_p0001a14║言法歸。法歸者。蓋是萬善之淵府。總持之林
	T01n0001_p0001a15║苑。其為典也。淵博弘富。[05]韞而彌廣。明宣禍

頁尾校勘條目：[05] 韞＝溫【宋】【元】

XML 標記:

```xml
<lb n="0001a15"/>苑。其為典也。淵博弘富。
<note n="0001005" resp="Taisho" type="orig" place="foot text">韞＝溫【宋】【元】</note>
而彌廣。明宣禍
```

n="0001005" 表示第1頁的第5個校勘

place="foot text" 表示在內文(text)中有校勘數字 [05], 在頁尾(foot)有校勘內容. 有少數例外情形, 內文中有校勘數字, 頁尾卻無對應校勘; 或者頁尾有校勘文字, 內文中卻無對應校勘數字.

大正藏校勘欄使用許多略符，請參考 CBETA 網站文件：

* [校異略符](http://www.cbeta.org/format/abbr_app.php)
* [對校略符](http://www.cbeta.org/format/abbr_dz.php)

## 經 CBETA 修訂的校勘文字標記

經 CBETA 修訂的校勘文字標記以 `<note type="mod">` 記錄. (mod means modified)

例如：T01, No. 1, p. 1，大正藏原文

	T01n0001_p0001b10║[12]後秦弘始年佛陀耶舍共竺佛念譯

頁尾校勘條目

	[12] 後秦弘始年＝姚秦三藏法師【三】

說明：【三】是指【宋】【元】【明】三本, 所以 CBETA 將 【三】直接修訂為【宋】【元】【明】

XML 標記

```xml
<lb n="0001b10"/><byline type="Translator">
<note n="0001012" resp="Taisho" type="orig" place="foot text">後秦弘始年＝姚秦三藏法師【三】</note>
<note n="0001012" resp="CBETA" type="mod">後秦弘始年＝姚秦三藏法師【宋】【元】【明】</note>
後秦弘始年姚秦三藏法師佛陀耶舍共竺佛念譯</byline>
```

resp="CBETA" 表示是由 CBETA 所作修訂. (resp means responsibility)

## place 屬性

### foot

通常底本頁尾註的標記是：

```xml
<note place="foot text" type="orig">⋯⋯</note>
```

如果底本有頁尾註，卻在內文缺了註標，那麼 place 屬性裡就會沒有 text，例 T05n0220_p0159c29​：

```xml
<note place="foot" type="orig">⋯⋯</note>
```

如果底本​內文有​註標，卻在​頁尾缺了​校註，那麼 place 屬性裡就會沒有 foot，例 T10n0291_p0607c12：

```xml
<note place="text" type="orig">⋯⋯</note>
```

### inline

行中夾註

T01n0001.xml, p. 30a17

```xml
<note place="inline">丹本注云問中應有何等時出家諸本並闕</note>
```

#### 雙行夾註 包 偈頌、段落

例 T53n2122_p0683a29

```xml
<note place="inline">故佛本行經云...說偈云。
  <lg>巧攝諸根識...此必釋種子</lg>
  <p>爾時舍利弗...即說偈報云。</p>
  <lg>如芥對須彌...與彼世尊威德別</lg>
  <p>於是舍利弗復聞說偈云。</p>
  <lg>諸法因緣生...常說如是法</lg>
  <p>舍利弗聞已...至於佛所得阿羅漢果</p>
</note>
```

#### 雙行夾註 包 雙行夾註

例 T20n1033_p0013b04

```xml
<note place="inline">即最初者是，
  <note n="0013038" resp="Taisho" type="orig" place="foot text">未＝末【宋】</note>
  <note n="0013038" resp="CBETA" type="mod">未【大】，末【宋】</note>
  <app n="0013038">
    <lem wit="【大】">未</lem>
    <rdg resp="Taisho" wit="【宋】">末</rdg>
  </app>加娑嚩
  <note n="0013039" resp="Taisho" type="orig" place="foot text">〔二合〕－【三】</note>
  <note n="0013039" resp="CBETA" type="mod">二合【大】，〔－〕【宋】【元】【明】</note>
  <app n="0013039">
    <lem wit="【大】"><note place="inline">二合</note></lem>
    <rdg resp="Taisho" wit="【宋】【元】【明】"><space quantity="0"/></rdg>
  </app>賀
</note>
```

### inline2

例 Y35n0033_p0374a12

```xml
1外道<note place="inline2">四月別住</note>
```

### interlinear

行間註解

例 X61n1165.xml, p. 793b24

```xml
如來我若欲見隨意即見<note place="interlinear">以下正明欲見即見之故</note>我能了知如來國土莊嚴
```

## type

type 屬性可能的值：add, authorial, cf1, cf2, cf3, equivalent, foot, inline, mod, orig, orig_biao, orig_ke, rest, star

### add

CBETA 新增的校註，例 T27n1545.xml, p. 3a19

```xml
<note n="0003a1901" resp="CBETA.maha" type="add">
  本頁校勘欄有校勘條目[02]，但內文出現兩處註標[02]，故此處內文註標改以[02A]表示。
</note>
```

n 屬性值是行號 `0003a19` 再加序號 `01`。

### authorial

例 Y36n0034.xml, p. 518a13

```xml
《俱舍論<note type="authorial">（光）</note>記》
```

### cf1, cf2, cf3

note 在 lem 裡面，例如 T02n0099.xml

```xml
<app n="0003b2901">
  <lem resp="CBETA.heaven" wit="【CB】【北藏-CB】">座<note type="cf1">P58_p0011b05</note></lem>
  <rdg wit="【大】">坐</rdg>
</app>
```

note 在 rdg 裡，例如：T24n1488.xml

```xml
<app n="1054c1301">
  <lem wit="【大】">坊</lem>
  <rdg wit="【磧-CB】" resp="CBETA.maha">坊<note type="cf1">Q14_p0038b18</note></rdg>
  <rdg resp="CBETA.maha" wit="【麗-CB】">房<note type="cf1"/>K14n0526_p0282a05<note></rdg>
</app>
```

`<note type="cf1">` 裡面不一定都是 K14n0526_p0282a05 這種格式，也有可能是各種文字敍述。

### equivalent

例 T01n0001.xml, p. 11a06

```xml
（二）第一分<note n="0011004" resp="Taisho" type="orig" place="foot text">遊行經～D. 10. Mahāparinibbānasuttanta.</note>
<note n="0011004" place="foot" type="equivalent">遊行經～D. 10. Mahāparinibbānasuttanta.</note>遊行經第二
```

上面的「D.」表示「長部」，請參考 CBETA [巴利語書名略號](http://www.cbeta.org/format/pali.php)。

### mod

經過 CBETA 修訂的校勘註

例 T01n0001.xml, p. 1b10

```xml
<byline cb:type="Translator">
  <note n="0001012" resp="Taisho" type="orig" place="foot text">後秦弘始年＝姚秦三藏法師【三】</note>
  <note n="0001012" resp="CBETA" type="mod">後秦弘始年＝姚秦三藏法師【宋】【元】【明】</note>
  <app n="0001012">
    <lem wit="【大】">後秦弘始年</lem>
    <rdg resp="Taisho" wit="【宋】【元】【明】">姚秦三藏法師</rdg>
  </app>佛陀耶舍共竺佛念譯
</byline>
```

### orig

底本校勘註

例 T01n0001.xml, p. 1a02

```xml
<note n="0001001" resp="Taisho" type="orig" place="foot text">此序依宋元明三本ニ依テ載ス</note><head><title>長阿含經</title>序</head>
```

### rest

校勘註不能轉為 app 標記的部份，以 &lt;note type="rest"> 記錄。

例 T01n0026.xml, p. 578a25

```xml
<note n="0578006" resp="Taisho" type="orig" place="foot text">品末題在卷末題前行【三】，〔中阿含〕－【明】</note>
<note n="0578006" resp="CBETA" type="mod">品末題在卷末題前行【宋】【元】【明】，〔中阿含〕－【明】</note>
<app n="0578006">
  <lem wit="【大】">中阿含</lem>
  <rdg resp="Taisho" wit="【明】"><space quantity="0"/></rdg>
</app>
<note n="0578006" place="foot" type="rest">品末題在卷末題前行【宋】【元】【明】</note>穢品第三竟
```

### star

例 N19n0007_p0211a04

```xml
於語行惡行<note n="0211020" resp="NanChuan" place="foot text" type="orig">
  底本將（行惡行已）之一句，以略符表示，卻不見其要，故今即不從此。以下附[＊]者亦然。
</note>已...(中略)...
於語行<note type="star" corresp="#0211020"/>惡行
```

## subtype

### biao 標

例 X10n0262

```xml
<note n="0600b01" resp="Xuzangjing" place="foot text" type="orig" subtype="biao">文殊問次</note>
```

### jie 解

例 X10n0252_p0180c11

```xml
<note n="0180j01" resp="Xuzangjing" place="foot text" type="orig" subtype="jie">四請修方便也</note>
```

### ke 科

例 X13n0287

```xml
<note n="0524k01" resp="Xuzangjing" place="foot text" type="orig" subtype="ke">第一序分初證信序</note>
```

### shift 位移

CBETA 校註說明這裡的修訂是文字的移動，例 X10n0262

```xml
<lb ed="X" n="0601c24"/>...
<note n="0601c2401" resp="CBETA" type="add" subtype="shift">一【CB】，［－］【卍續】</note>
<app n="0601c2401">
  <lem wit="【CB】" resp="CBETA.maha">一</lem>
  <rdg wit="【卍續】"><space quantity="0"/></rdg>
</app>
... ... ...
<lb ed="X" n="0603a01"/>...
<note n="0603a0101" resp="CBETA" type="add" subtype="shift">［－］【CB】，一【卍續】</note>
<app n="0603a0101">
  <lem wit="【CB】" resp="CBETA.maha"><space quantity="0"/></lem>
  <rdg wit="【卍續】">一</rdg>
</app>
```
	
### 規範字詞

CBETA 校註說明這裡的修訂是關於「文字正規化」，例如《印順法師佛學著作集》Y01n0001.xml

```xml
<lb n="0019a08" ed="Y"/>...
<note n="0019a0801" resp="CBETA" type="add" subtype="規範字詞">稟【CB】，禀【印順】</note>
<app n="0019a0801">
  <lem wit="【CB】" resp="CBETA">稟</lem>
  <rdg wit="【印順】">禀</rdg>
</app>受大乘佛法。什公一面翻譯，一面講學。所翻的大乘經論很多，
```

## 校勘編號 n

### 編號以頁為單位

例 T01n0001.xml

```xml
<note n="0001001" resp="Taisho" type="orig" place="foot text">此序依宋元明三本ニ依テ載ス</note>
```

上面 n 屬性值 0001001 前四碼 0001 是頁碼，後三碼 001 表示本頁第一個註。

如果是 CBETA 新增的校注，則由 CBETA 自行編號，例 T01n0001.xml

```xml
<note n="0001b0201" resp="CBETA" type="add">念【CB】【磧-CB】，忘【大】</note>
<app n="0001b0201">
  <lem wit="【CB】【磧-CB】" resp="CBETA">念<note type="cf1">Q17_p0302a30</note></lem>
	<rdg wit="【大】">忘</rdg>
</app>
```

流水號是 xml 編輯人員依據該行「行首資訊（0001b02）」，加上是在該行的第幾個「新增校註（參照）」，如這裡是第1個則作「0001b0201 」。

但，其實呈現在 CBReader 或 CBETA Online 的流水號則是由程式自動控制，以「卷」為單位來依序編號。這點，跟大正藏以「頁」為單位來編號不同。

### 一條校勘拆成兩個 note

一條校勘經 CBETA 修訂，可能拆成兩個，例 T85n2882, p. 1383c26:

```xml
<note n="1383062" resp="Taisho" type="orig" place="foot text">〔不得…枝〕二十四字－【甲】</note>
<note n="1383062a" resp="CBETA" type="mod">〔不得停止〕－【甲】</note>...
<note n="1383062b" resp="CBETA" type="mod">〔佛有…枝〕二十字－【甲】</note>
```

### 編號為 0

例：T32n1645, p. 238a29

```xml
<note resp="Taisho" n="0238000" place="foot" type="orig">
  (A) P.101 [08] 參照，(B) 乃至 (F) P. 102 [02][03][05][07][12] 參照</note>
<note resp="CBETA" n="0238000" type="mod">
  (A) P.101 [08] 參照，(B) 乃至 (F) P. 102 [02][03][05][07][12] 參照（CBETA 按：大正藏校勘欄有「(A) P.101 [08] 參照，(B) 乃至 (F) P. 102 [02][03][05][07][12] 參照」之校勘條目，但此頁內文及大正藏校勘欄無相對應之校勘符號，故將此頁校勘符號作[00]處理，並置於本頁內文最後。）</note>
```

### 編號以行為單位

例 Y01n0001.xml

```xml
<note n="0019a0801" resp="CBETA" type="add" subtype="規範字詞">稟【CB】，禀【印順】</note>
```

上面 n 屬性㥀 0019a0801 其中的 0019a08 為行號，最後兩碼 01 為流水號。

### 含小經編號

《大藏經補編》的註解放在小經結束的地方，在同一頁中可能出現兩個「註一」，因此必須加上小經編號避免重複。
例：B06n0003_p0030b03

```xml
<note n="0030001-n10" resp="BuBian" place="foot text" type="orig">
  原本之中為 āsavānaṁ khayā ñāṇāya（因漏之盡因智之故）．然在是處．意義欠妥．今從沙門果經之類文 āsavānaṁ khaya-ñāṇāya。
</note>
```

上例中的 note 編號 `0030001-n10`, 前四碼 `0030` 表示頁碼，接下來的 `001` 表示「註一」，`n10` 表示第十號小經「須婆經第十」。

## note 出現位置 特例

### note 夾在 l 之間

例 T18n0908, p. 920b08

```xml
...
<l>瀉杓長及圓</l>
<note n="0920048" resp="Taisho" place="foot text" type="orig">〔并及…相〕二偈－【甲】</note>
<note n="0920048" resp="CBETA" type="mod">〔并及刻鏤文皆如注杓相〕二偈－【甲】</note>
<l>并及刻鏤文</l>...
```

### list/note
note 夾在 item 之間

ex: T51n2087_p0939b12

```xml
<list>
  ...
  <item xml:id="itemT51p0939b1201">淫薄健國</item>
  <note n="0939005" resp="Taisho" type="orig" place="foot text">〔屈居…鎩國〕二十七字－【甲】</note>
  <note n="0939005" resp="CBETA" type="mod">（屈居…鎩國）二十七字【大】，〔－〕【甲】</note>
  ...
</list>
```

### body/note

note 直接出現在 body 下

例 T03n0159_p0291a03

```xml
<body>
  ...
  <lb n="0291a02" ed="T"/><cb:docNumber>No. 159</cb:docNumber>
  <lb n="0291a03" ed="T"/><note n="0291a0301" resp="CBETA" type="add" note_key="T03.0291a03.01">（大唐…年也）四百九十七字【CB】【麗-CB】，〔－〕【大】（CBETA 按：諫議大夫「孟蕑」之「蕑」字依宮本（日本宮內庁書陵部藏大藏經db2第5798帖第4圖第3行）及他校（T50n2061_p0722b02）修訂作「簡」。）</note>
  ...
</body>
```

### div/note

note 直接出現在 div 下

例 T02n0099_p0366b23

```xml
<cb:div>
  ...
  <note n="0366005" resp="Taisho" place="foot text" type="orig">〔娑多…法〕二十八字－【三】</note>
  <note n="0366005" resp="CBETA" type="mod">（娑多…法）二十八字【大】，〔－〕【宋】【元】【明】</note>
  <app cb:word-count="28" n="0366005">
    <lem wit="【大】">
      <p>娑多耆利說偈答言：</p>
      <lg type="regular" style="margin-left:1em;text-indent:-1em">
        <l>「牟尼善心具，<caesura/>及身口業跡，</l>
        <l>明行悉成就，<caesura/>讚歎於其法。」</l>
      </lg>
    </lem>
    <rdg resp="Taisho" wit="【宋】【元】【明】"><space quantity="0"/></rdg>
  </app>
  ...
</cb:div>
```

### div/note/p

夾注下包多個 p, ex: T21n1299_p0388a16

```xml
<cb:div>
  ...
  <note place="inline">
    <p xml:id="pT21p0388a1601">新演如左。...庶當代高才知此意也。</p>
    ...
    <lb n="0388b23" ed="T"/><p xml:id="pT21p0388b2301">　　三十日　危壁婁昴觜井柳張軫亢房尾</p>
  </note>
  ...
</cb:div>
```

## note_key

連結 CBETA 修訂考證資料庫，例 T01n0001.xml

```xml
<note n="0001a2901" resp="CBETA.shin" cb:provider="來函：DL (2022-03-16)" type="add" note_key="T01.0001a29.07">
  CBETA 按：「一分四十五卷」，《磧砂》乙本（QC053n0665_p0635b11）、《洪武南藏》（U089n0585_p0406a05）、《永樂北藏》（P059n0541_p0572a06-07）、《嘉興藏》（日本東京大學綜合圖書館藏正編第78帙第5冊第6圖左欄第3行）作「一分四十五卷」，《福州藏》（日本宮內庁書陵部藏大藏經第2765帖第3圖第23至24行）作「二分四十品」。
</note>
```

上例中 note_key 屬性值 `"T01.0001a29.07"` 可連結至 CBETA 修訂考證資料庫：
https://www.cbeta.org/revised_research.php?notekey=T01.0001a29.07
