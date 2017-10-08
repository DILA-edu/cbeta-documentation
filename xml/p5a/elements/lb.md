# lb

換行 (line break)

## 同時記錄兩個版本的行號

例如 X01n0001.xml

```xml
<lb ed="X" n="0001a07"/><lb ed="R150" n="0705a04"/>卷一帖。一紙廿行。行十二字。經末有左藏庫西潘
```

ed="X" 是《卍新纂大日本續藏經》的行號，ed="R150" 是《卍續藏經-新文豐版》第150冊的行號。

## type="honorific"

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

## @n

行號的前四碼通常都是數字，但是也有例外，例如 GA020n0017.xml：

```xml
<pb ed="GA" xml:id="GA020.0017.a003a" n="a003a"/>
<lb ed="GA" n="a003a01"/>
```
