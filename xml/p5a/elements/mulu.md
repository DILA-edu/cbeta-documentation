# mulu

CBETA 自訂的目次節點 (TEI 無此元素)

## type="卷"

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

## 卷以外的空元素

某些地方會有空的 mulu 標記 (除了卷之外)，例如：B25n0145.xml, lb=0702a10

```xml
<cb:mulu type="附文" level="1"/><head>校訛</head>
```

據 CBETA 所說，這表示在目次裡不要呈現這個節點。
CBETA 會「儘量」清除這類標記，但處理程式應該忽略這種標記。
