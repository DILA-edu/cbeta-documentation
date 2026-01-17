# t

## @xml:lang
* pi
* sa
* sa-Sidd
* sa-x-rj
* san-tr
* x-unknown
* zh-Hant
* zh-x-yy

## @place

### place="foot"

ex: T08n0235.xml

```xml
<cb:tt n="0749002" type="app">
  <cb:t xml:lang="zh-Hant" resp="Taisho">樂阿蘭那行者</cb:t>
  <cb:t place="foot" resp="Taisho" xml:lang="sa">Araṇāvihārin.</cb:t>
</cb:tt>
```

### place="inline"

```xml
<cb:tt place="inline">
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-A5A9"/></cb:t>
  <cb:t xml:lang="zh-Hant">曩</cb:t>
</cb:tt>
```

## @style

ex: T54n2133A.xml, p. 1191b03

```xml
<cb:tt>
  <cb:t xml:lang="sa-Sidd" style="margin-left:0em">
    <g ref="#SD-CFCA"/><g ref="#SD-B6A4"/><g ref="#SD-E355"/>
  </cb:t>
  <cb:t style="margin-left:2em"/>
</cb:tt>
```

## t contain lg

ex: T01n0026_p0548c02

```xml
<cb:tt n="0548005" word-count="20" type="app">
  <cb:t resp="Taisho" xml:lang="zh-Hant">
    <lg type="regular" xml:id="lgT01p0548c0201">
      <l>「於有見恐怖，<caesura/>無有見不懼，</l><lb n="0548c03" ed="T"/>
      <l>是故莫樂有，<caesura/>有何不可斷。</l>
    </lg>
  </cb:t>
  <cb:t resp="Taisho" xml:lang="pi" place="foot">Bhave vāhaṃ bhayaṃ disvā bhavañ ca vibhavesinaṃ bhavaṃ nābhivadiṃ kañci nandiñ ca na upādiyin ti.</cb:t>
</cb:tt>
```
