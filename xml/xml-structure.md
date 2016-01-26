# CBETA XML 檔內容架構

## Overview

一個 CBETA XML 檔內部架構分為 Header 及 Text 兩部份：

```xml
<TEI>
  <teiHeader>........</teiHeader>
  <text>.....</text>
</TEI>
```

## TEI Header

teiHeader 分成 fileDesc, encodingDesc, profileDesc, revisionDesc 四大部份, 記錄本經相關資訊：

```xml
<teiHeader>
  <fileDesc>....</fileDesc>
  <encodingDesc>....</encodingDesc>
  <profileDesc>....</profileDesc>
  <revisionDesc>....</revisionDesc>
</teiHeader>
```

### File Description

```xml
<fileDesc><!-- File Description -->
  <titleStmt><!-- title statement -->
    <title>Taisho Tripitaka, Electronic version, No. 0001 長阿含經</title><!-- 經名 -->
    <author>後秦 佛陀耶舍共竺佛念譯</author><!-- 作者、譯者 -->
    <respStmt><!-- statement of responsibility -->
      <resp>Electronic Version by</resp>
      <name>CBETA</name>
    </respStmt>
  </titleStmt>
  <editionStmt>
    <edition>$Revision: 1.73 $<date>$Date: 2013/02/27 09:32:00 $</date>新式標點版</edition>
  </editionStmt>
  <extent>22卷</extent><!-- 卷數 -->
  <publicationStmt><!-- publication statement -->
    <distributor><!-- 發行者 -->
      <name>中華電子佛典協會 (CBETA)</name>
        <address><addrLine>cbeta@ccbs.ntu.edu.tw</addrLine></address>
    </distributor>
    <availability>
      <p>Available for non-commercial use when distributed with this header intact.</p>
    </availability>
    <date>$Date: 2009/01/07 01:35:12 $</date>
  </publicationStmt>
  <sourceDesc><!-- source description -->
    <bibl>Taisho Tripitaka Vol. 1, No. 001 &desc;</bibl>
  </sourceDesc>
</fileDesc>
```

### Encoding Description

```xml
<encodingDesc><!-- Encoding description -->
  <projectDesc><!-- 原始電子版提供者 -->
    <p lang="eng" type="ly">Text as provided by Mr. Hsiao Chen-Kuo, Text as provided by Mr. Chang Wen-Ming</p>
    <p lang="chi" type="ly">蕭鎮國大德提供，張文明大德提供</p>
  </projectDesc>
</encodingDesc>
```

### Profile Description

```xml
<profileDesc>
  <langUsage><!-- 本經所使用語言 -->
    <language id="pli">Pali</language>
    <language id="san">Sanskrit</language>
    <language id="eng">English</language>
    <language id="chi">Chinese</language>
  </langUsage>
</profileDesc>
```

### Revision Description 修訂記錄

```xml
<revisionDesc>
  <change>
    <date>19990810/22:31:27</date>
    <respStmt><name>CW</name><resp>ed.</resp></respStmt>
    <item>Created initial TEI XML version with BASICX.BAT (99/8/10)</item>
  </change>
  <!-- CVS 修訂記錄 -->
</revisionDesc>
```

## Text

本經內文

```xml
<text>
  <body>
  ........
  </body>
</text>
```

### 頁碼、行號

以 `<pb>` 記錄頁碼 (Page Break), `<lb>` 記錄行號 (Line Break)

```xml
<text>
  <body>
    <pb ed="T" id="T01.0001.0001a" n="0001a"/>
    <lb n="0001a01"/>
    <lb n="0001a02"/>
    <lb n="0001a03"/>
    ........
  </body>
</text>
```

其中 `<pb>` 的屬性 ed="T", 表示 Taisho edition, 大正藏一頁有三欄, n="0001a" 表示第一頁上欄.

### 分卷

分卷處加 `<milestone>` 標記.

```xml
<text>
  <body>
    <pb ed="T" id="T01.0001.0001a" n="0001a"/>
    <lb n="0001a01"/>
    <milestone unit="juan" n="1"/>
    <lb n="0001a02"/>
    <lb n="0001a03"/>
    ........
  </body>
</text>
```

大部份佛典都是從第一卷開始，但是有例外，例如：X03n0208 《華嚴經論〔卷十〕》是從第十卷開始，XML 檔裡的第一個 milestone 如下：

```xml
<milestone unit="juan" n="10"/>
```

大正藏的卷首資訊、卷末資訊, 格式不一, 時有時無, 以 CBETA 自訂標記 `<juan>` 記錄:

```xml
<text>
  <body>
    <juan fun="open" n="001"><!-- fun="open" 是卷首 -->
      <jhead><title>佛說長阿含經</title>卷第一</jhead>
    </juan>
    ..... <!-- 本卷內容 -->
    <juan fun="close" n="001"><!-- fun="close" 是卷末 -->
      <jhead><title>佛說長阿含經</title>卷第一
    </juan>
  </body>
</text>
```

### 章節架構

本文章節架構以 `<cb:div>` 標記, 章節標題以 `<head>` 標記.

```xml
<text>
  <body>
    <cb:div type="xu"><!-- type="xu" 表示這是一個序 -->
      ....
    </cb:div>
    <cb:div type="fen"><head>（一）第一分初</head><!-- type="fen" 表示本經第一層架構 "分" -->
      ........
    </cb:div>
  </body>
</text>
```

cb:div 與 TEI 的 div 意義相同，但是因為藏經文本結構多種，需要較寬鬆的規則，所以使用自訂的 cb:div 元素。

如果 div 之下還有第二層標題：

```xml
<cb:div type="fen"><head>（一）第一分初</head>
  <cb:div type="jing"><head>大本經第一</head><!-- type="jing" 表示本層架構是 "經" -->
    ........
  </cb:div>
  <cb:div type="jing"><head>遊行經第二</head>
    ....
  </cb:div>
</cb:div>
```

大正藏章節標題格式不一, 時有時無, CBETA 自訂 `<mulu>` 標記, 記錄全經目次架構：

T01n0001.xml

```xml
<cb:div type="xu">
  <mulu type="序" level="1" label="序"/>
  <head><title>長阿含經</title>序< /head>
</cb:div>
<cb:div>
  <mulu type="分" level="1" n="1" label="1 分"/><head>（一）第一分初</head>
  <cb:div type="jing">  
    <mulu type="經" level="2" n="1" label="1 大本經(一)"/><head>大本經第一</head>
  </cb:div>
  .....
</cb:div>
```
