# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 專案性質

這是 CBETA（中華電子佛典協會）數位檔案的**技術說明文件**，讀者是資訊技術人員。整個 repo 只有 Markdown 文件（與少量圖片），沒有程式碼、build、lint 或測試流程。文件直接在 GitHub 上瀏覽，因此相對連結、Mermaid 圖表（`README.md` 的資料流程圖）、錨點連結都以 GitHub 的渲染方式為準。

文件以繁體中文撰寫；XML 元素名、屬性名、檔名、行號等維持原文。

## 文件架構

- `README.md`：CBETA 數位檔案的整體流程（BM 簡單標記版 → XML P5a → 轉檔程式 → P5 / P5b / HTML 等輸出，以及各版轉 TXT 比對）。
- `xml/README.md`：XML 說明的入口。CBETA XML 依據 TEI，分兩種版本：
  - **P5a**：內部編輯用版本（公開於 https://github.com/cbeta-git/xml-p5a），本 repo 的元素說明主要針對它。
  - **P5**：由程式從 P5a 轉出、對外公開的版本。兩者差異（缺字 `<g>` 處理、校勘 `<app>` 放在 body 或 back）見 `xml/p5-p5a-diff.md`。
- `xml/file-structure.md`、`xml/work-multi-vol.md`：藏經代碼 / 冊號 / 經號（典籍編號）的命名規則，以及典籍跨冊時拆成多個 XML 檔的情形。
- `xml/xml-structure.md`：單一 XML 檔的 teiHeader / text 架構。
- `xml/global-attributes/`：所有元素共用的屬性（`xml:lang`、`rend`、`cb:behaviour`）。新增屬性文件時記得同步更新該資料夾的 `README.md` 索引。
- `xml/p5a/elements/`：每個 XML 元素一個檔，檔名即元素名（不含 `cb:` 前綴，例如 `mulu.md` 說明 `<cb:mulu>`）。此資料夾沒有索引檔，依賴 GitHub 的資料夾列表。
- `xml/p5a/attributes/`：僅限 P5a 的特定屬性用法（例如 `note` 的 `rend="hide"`、`wit`）；與 `xml/global-attributes/` 的通用屬性區分。

## 元素說明文件的寫法慣例

參考既有檔案（如 `xml/p5a/elements/rdg.md`、`div.md`、`lb.md`）：

- 標題 `# 元素名`；約一半的檔案接著一行「參考 [TEI xxx 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-xxx.html)」，其餘直接說明用途。
- 以 `## @屬性名` 或 `## type=="值" (中文說明)` 分節；屬性值清單用條列並附中文意義。
- 每個用法都附**真實出處**的範例：先寫檔名與位置（如 `T44n1840.xml, p. 137c27`、`Y03n0003_p0001a02` 或 `lb=0028a03`），再接 ```` ```xml ```` 程式碼區塊，內容取自實際 CBETA XML。不要自行杜撰範例或出處。
- 內容較長時，在開頭放錨點目錄（`* [標題](#錨點)`）。
