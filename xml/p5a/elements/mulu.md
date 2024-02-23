# mulu

CBETA 自訂的目次節點 (TEI 無此元素)

例 T01n0001.xml

```xml
<cb:mulu level="1" type="序">序</cb:mulu>
```

## @type

type 屬性值有很多種，例如：卷、經、序、處、會、地、品、分、論、跋、科判、附文、其他。

其中「卷」目次自成一個體系，其他類型共構一個目次樹。

### type="卷"

例 T01n0001.xml, lb=0001b08

```xml
<cb:mulu type="卷" n="1"/>
```

上面的標記在 CBReader 的卷目次裡顯示「第一」。

T34n1718

```xml
<cb:mulu n="1a" type="卷">第一上</cb:mulu>
```

上面的標記在 CBReader 的卷目次裡顯示「第一上」。

## @n

n 屬性值有時會與內文不符，例 T02n0099.xml

```xml
<cb:mulu level="2" n="140" type="經">140-141</cb:mulu><head>（一四〇、一四一）</head>
<cb:mulu level="2" n="141" type="經">142</cb:mulu><head>（一四二）</head>
<cb:mulu level="2" n="142" type="經">143-144</cb:mulu><head>（一四三、一四四）</head>
<cb:mulu level="2" n="753" type="經">755-7</cb:mulu><head>（七五五～七）</head>
```

## 卷以外的空元素

某些地方會有空的 mulu 標記 (除了卷之外)，例如：B25n0145.xml, lb=0702a10

```xml
<cb:mulu type="附文" level="1"/><head>校訛</head>
```

據 CBETA 所說，這表示在目次裡不要呈現這個節點。
CBETA 會「儘量」清除這類標記，但處理程式應該忽略這種標記。
