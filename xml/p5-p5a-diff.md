# CBETA XML P5 與 P5a 的差異

## 缺字

P5a 可以直接使用 unicode 字元或 `<g>` 標記。

P5a 轉成 P5 時，才把 unicode 2.0 以內的字元都用 unicode 表達，而 unicode 2.0 以外的用 `<g>` 標記，並將缺字資料記錄在檔頭。

理由是 XML 編輯者很難知道某個字元是否在 Unicode 2.0 以內，所以交給程式。
而 XML 編輯者直接看到 Unicode 字元，而不是 `<g>` 標記，也有助於閱讀、編輯。

## 校勘

p5a 直接將校勘放在 body 本文中：

```xml
<note n="0001002" resp="Taisho" type="orig" place="foot text">〔長安〕－【宋】</note>
<app n="0001002">
  <lem wit="【大】">長安</lem>
  <rdg resp="Taisho" wit="【宋】"><space quantity="0"/></rdg>
</app>
```

P5 在 body 本文中只放 anchor：

```xml
<anchor xml:id="nkr_note_orig_0001002" n="0001002"/>
<anchor xml:id="beg0001002" n="0001002"/>長安<anchor xml:id="end0001002"/>
```

`<app>` 標記則是放到 back 去：

```xml
<app from="#beg0001002" to="#end0001002">
  <lem wit="#wit1">長安</lem>
  <rdg resp="#resp1" wit="#wit2"><space quantity="0"/></rdg>
</app>
```

理由是 P5a 校勘和本文放在一起，有前後文才方便 XML 編輯者處理，而 P5 的格式有好幾個區塊，有note、app 會增加維護難度。

# 檔頭記錄

以上例來看, P5a 直接寫 `<lem wit="【大】">`

P5 則是 `<lem wit="#wit1">`

檔頭另外記錄 wit1 的意義：

```xml
<witness xml:id="wit1">【大】</witness>
```

這對維護者也不方便，要自行查版本，有新的還要自行加上新的編號。

## 流水號

上面的 wit1, wit2 就是流水號的一種，如果加了一版，就有新的編號。

又如這個修訂，P5a 直接寫:

```xml
<choice>
  <corr>念</corr>
  <sic>忘</sic>
</choice>
```

P5 就要一個流水號 

```xml
<choice cb:from="#beg_2" cb:to="#end_2">
  <corr>念</corr>
  <sic>忘</sic>
</choice>
```

如果修訂有增減，流水號要全面調整，也不是人力能處理的，所以 P5 是由程式從 P5a 轉出。
