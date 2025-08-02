# CBETA Documentation

這是一份供資訊技術人員使用的 CBETA 技術說明文件。

## What is CBETA

請參考 [CBETA 官網](http://www.cbeta.org/)

## CBETA 數位檔案 Big Picture
```mermaid
flowchart TD

  Start(["開始"])

  subgraph 基本資料
    BM:::green@{ shape: docs, label: "BM (簡單標記版)"}
    XMLP5a:::green@{ shape: docs, label: "XML P5a"}
    classDef green fill:#21804e, color:white
  end

  subgraph 資料庫
    Authority[("Authority 資料庫")]:::yellow
    Missing[("缺字資料庫")]:::yellow
    classDef yellow fill:#857c1b, color:white
  end

  Transform[["轉檔程式"]]:::red
  classDef red fill:#8b2c2c, color:white

  subgraph 公開資料
    Output@{ shape: docs, label: "HTML / EPUB / PDF / MOBI / Text / DocuXML / Docx"}
    XMLP5@{ shape: docs, label: "XML P5 (Github)"}
    XMLP5b@{ shape: docs, label: "XML P5b (CBReader)"}
  end

  subgraph 資料比對
    HTMLText@{ shape: docs, label: "HTML → TXT"}
    BMText@{ shape: docs, label: "BM → TXT"}
    P5Text@{ shape: docs, label: "P5 → TXT"}
    CBRText@{ shape: docs, label: "CBReader → TXT"}
    Compare{"比對OK？"}:::blue
    classDef blue fill:#3d49be, color:white
  end

  subgraph cbetaonline
    API[["API"]]:::red
    Online(["CBETAonline 網頁"])
  end

  END(["結束"])

  %% === 資料流程 ===
  Start --> BM --> XMLP5a

  XMLP5a --> Transform
  XMLP5a --> API
  Missing --> API
  Missing --> Transform
  Authority --> API

  Transform --> Output
  Transform --> XMLP5
  Transform --> XMLP5b

  Output --> API e1@==> Online
  e1@{ animate: true }
  
  BM --> BMText --> Compare
  XMLP5 --> P5Text --> Compare
  Output --> HTMLText --> Compare
  XMLP5b --> CBRText --> Compare
  
  Compare -- No --> BM
  Compare -- No --> XMLP5a
  Compare -- OK --> END
```

## XML

CBETA 文本採用的主要格式，說明詳見 [xml](xml) 資料夾。

## BM

CBETA Basic Markup 又稱「簡單標記版」，一冊一檔，純文字加上行首資訊、簡單標記。

[CBETA BM on Github](https://github.com/mahawu/BM_u8)

## 藏經代碼

CBETA 佛典集成收錄多套藏經，每套藏經給予一個唯一的 ID，列表請看 [這裡](http://www.cbeta.org/format/id.php)。

### 藏經排序

目錄排序（以下為各個藏經代碼）:  
T X A K S F C U P J L G M D N ZS I ZW B GA GB

全文檢索結果依據資料的參考價值按以下藏經代碼排序:  
T X A K S F C D U P J L G M N ZS I ZW B GA GB

上面兩種排序主要差別在 D 《國家圖書館善本佛典》。

## 卍續藏 三種版本

CBETA 網站對於 [卍續藏三種版本及其對照說明](http://www.cbeta.org/data-format/zrx.htm#zrx)

CBETA 在 Github 上的 [卍續藏X2R行號對照表](https://github.com/cbeta-git/cbwork-common-X2R)

## 典籍編號

請看 [work-id](work-id.md)

## 插圖

<https://github.com/cbeta-git/CBR2X-figures>

## 缺字圖檔

* 漢字 <https://github.com/cbeta-org/gaiji-CB>
* 悉曇字 <https://github.com/cbeta-org/sd-gif>
* 蘭札體 <https://github.com/cbeta-org/rj-gif>

## 電子書封面

<https://github.com/cbeta-org/ebook-covers>
