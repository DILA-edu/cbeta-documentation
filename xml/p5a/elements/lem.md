# lem

lem 元素內容為底本用字，或 CBETA 依據各種版本選用最適當的用字。

例 T01n0001_p0001a15

```xml
<app n="0001005">
  <lem wit="【大】">韞</lem>
  <rdg resp="Taisho" wit="【宋】【元】">溫</rdg>
</app>
```

lem 的 wit 屬性值為【大】，表示《大正藏》使用「韞」字，而【宋】【元】二本使用「溫」字。

又如 T01n0001_p0002b13

```xml
<app n="0002016">
  <lem resp="CBETA.maha" wit="【CB】">牟</lem>
  <rdg wit="【大】">無</rdg>
  <rdg resp="Taisho" wit="【宋】【元】【明】">牟</rdg>
</app>尼
```

第一個 rdg 的 wit 屬性值為【大】，表示《大正藏》作「無」字；  
第二個 rdg 的屬性值為【宋】【元】【明】，表示此三本作「牟」字；  
而 lem 的 wit 屬性值為【CB】，表示 CBETA 採用「牟」字。

## 校勘範圍跨行

校勘範圍可能跨行，為了在切換「底本」及「CBETA版本」時都可以正常顯示行號，需同時在 lem（CB本）或 rdg（底本）裡面插入同樣的 lb。

例 T32n1644.xml, p. 189a21

```xml
<app n="0189001">
  <lem resp="CBETA.maha" wit="【CB】【磧-CB】">忉<lb n="0189a22" ed="T"/>利天<note type="cf1">Q27_p0016b17</note></lem>
  <rdg resp="Taisho" wit="【宋】【元】【明】">忉利天</rdg>
  <rdg wit="【大】">忉<lb n="0189a22" ed="T"/>利</rdg>
</app>
```

## lem contain div

ex: T16n0665_p0403a03

```xml
<app n="0403a0301">
  <lem wit="【CB】" resp="CBETA.ting" cb:provider="來函：萧苏晏 (2022-06-16)">
    <cb:div type="xu">
      <cb:mulu level="1" type="序">大唐龍興三藏聖教序</cb:mulu>
      <head>大唐龍興三藏聖教序</head>
      <byline cb:type="author">中宗孝皇帝製</byline>
      <p xml:id="T16p0403a030016" cb:place="inline">蓋聞蒼蒼者天⋯⋯又若斯焉。</p>
      ....
    </cb:div>
  </lem>
  <rdg wit="【大】"><space quantity="0"/></rdg>
</app>
```

## lem 包多個 p

ex: T03n0159_p0331c11

```xml
<lem wit="【CB】" resp="CBETA.ting" cb:provider="來函：李周淵 (2020-07-07)">
  <p xml:id="pT03p0331c1112" cb:place="inline">元和五年七月三日，內出梵夾，其月廿七日奉　詔於長安醴泉寺，至六年三月八日翻譯進上。</p>
  <p xml:id="pT03p0331c1148" cb:place="inline">罽賓國三藏賜紫沙門般若宣梵文</p><p xml:id="pT03p0331c1162" cb:place="inline">醴泉寺日本國沙門靈仙筆受并譯語</p>
  <p xml:id="pT03p0331c1177" cb:place="inline">經行寺沙門令謩潤文</p>
  <p xml:id="pT03p0331c1186" cb:place="inline">醴泉寺沙門少諲迴文</p>
  <p xml:id="pT03p0331c1195" cb:place="inline">濟法寺沙門藏英潤文</p>
  <p xml:id="pT03p0331c11104" cb:place="inline">福壽寺沙門恆濟迴文</p>
  <p xml:id="pT03p0331c11113" cb:place="inline">惣持寺沙門大辨證義右街都勾當大德莊嚴寺沙門一微詳定</p>
  <p xml:id="pT03p0331c11138" cb:place="inline">都勾當譯經押衙散兵馬使兼正將朝議郎前行隴州司功參軍上柱國賜緋魚袋臣李霸、給事郎守右補闕雲騎尉襲徐國公臣簫俛奉　勑詳定</p>
  <p xml:id="pT03p0331c11194" cb:place="inline">銀青光祿大夫行尚書工部侍郎　充皇太子及諸王侍讀上柱國長州縣開國男臣歸登奉　勑詳定</p>
  <p xml:id="pT03p0331c11232" cb:place="inline">朝請太夫守給事中充集賢殿　御書院學士判院事臣劉伯蒭奉　勑詳定</p>
  <p xml:id="pT03p0331c11260" cb:place="inline">朝議郎守諫議大夫知匭使上柱國賜緋魚袋臣孟簡奉　勑詳定</p>
  <p xml:id="pT03p0331c11285" cb:place="inline">右神策軍護軍中尉兼右街功德使扈從特進行右武衛大將軍知內侍省上柱國剡國公食邑三千雇第五從直</p>
  <note type="cf1">大屋德城《石山写経選》（日本國會圖書館藏第19-20圖）</note><note type="cf2">池田温《中国古代写本識語集録》收於《東洋文化研究所叢刊》11（1990）第335頁</note>
</lem>
```
