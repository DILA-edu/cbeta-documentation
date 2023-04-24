# rend attributes

## bold

粗體。例 Y03n0003_p0001a02

```xml
<byline rend="bold">——民國四十年夏在香港屯門淨業林講——</byline>
```

## border

外框。例 Y01n0001_p0001a03

```xml
<seg rend="border">懸論</seg>
```

## circle-above

上方加圈點。例 Y10n0010_p0184a13

```xml
「謂業為先，後<seg rend="circle-above">色心</seg>起中無間斷，名為相續。」
```

## del

刪除線。未使用。

## heiti

字型為「黑體」。目前未使用。

## hide

隱藏。例： TX01n0001_p0140a12

```xml
<note n="0140a1201" resp="CBETA" type="add" rend="hide" note_key="TX01.0140a12.33">斂【CB】，歛【太虛】</note>
```

## inline

例 T54n2132_p1186b04

```xml
<cb:tt rend="inline">
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-CFC5">􆿅</g></cb:t>
  <cb:t xml:lang="zh-x-yy"><cb:yin><cb:zi>阿</cb:zi><cb:sg>上聲短呼</cb:sg></cb:yin></cb:t>
</cb:tt>
```

## italic

斜體。例 Y41n0039_p0028a05

```xml
這是<title level="m">《<foreign rend="italic" xml:lang="en">Ancient India</foreign>》</title>的中文譯本
```

## kaiti

字型為「楷體」。例 Y06n0006_p0034a12

```xml
<p rend="kaiti">【附論】真諦的譯本裡，又把界字解釋作『解性』，說界是如來藏...</p>
```

## larger

較大字。未使用。

## mingti

字型為「明體」。例 Y25n0025_p0417a06

```xml
<lg rend="mingti">
  <l>身是菩提樹，　心如明鏡臺，　時時勤拂拭，　莫使有塵埃！</l>
</lg>
```

## no-border

表格不要框線。例：GA002n0005_p0007a02

```xml
<table cols="4" rend="no-border" style="margin-left:2em">
  <row>
    <cell>建初寺</cell>
    <cell>長干寺</cell>
    <cell>高座寺</cell>
    <cell>白馬寺</cell>
  </row>
  ...
</table>
```

## no-marker

list 不要項目符號。例如： B17n0092_p0630a13

```xml
<list rend="no-marker">
  <item><p>一、訪聞近日僧尼等...</p></item>
  ...
</list>
```

## no_nor: 不使用通用字

停用，改用 `cb:behaviour="no-norm"`

例如 T54n1896.xml, p. 863a05

```xml
二明稽首者古文為<term rend="no_nor"><g ref="#CB05129"/></term>
```

## over

上橫線。未使用。

## pl-1 .. pl-8

例如 ZW01na003_p0027a20

```xml
<cell rend="pl-2">附：文軌及其著作</cell>
```

pl-2 對應的 CSS 是 padding-left:2em, 依此類推。
目前 (2021-01-08) 只有出現 pl-2 和 pl-4 這二種，CBReader 支援 pl-1 至 pl-8 八種。

## small

小字。例 Y27n0027_p0042a12

```xml
<biblScope n="41" rend="small" type="卷">四一</biblScope>
```

## smaller

較小字。未使用。

## sub

下標字。例 B08n0026_p0164b26

```xml
酪酸（Butyric Acid <formula>CH<hi rend="sub">3</hi>(CH<hi rend="sub">2</hi>)<hi rend="sub">2</hi>COOH</formula>）
```

## sup

上標字。例 Y43n0041_p0116a03

```xml
<seg rend="sup">上</seg>印<seg rend="sup">下</seg>順導師
```

## text-center

置中。例 ZS01n0001_pa001a03

```xml
<head rend="text-center">《正史佛教資料類編》緣起</head>
```

## text-left

靠左。未使用。

## text-right

靠右。例 ZS01n0001_p0001a18

```xml
<p rend="text-right">（《後漢書》卷八十八《西域傳》2921）</p>
```

## under

下底線。未使用。
