# punctuation

標點類型，有三種可能：

* 新式標點
* 原書標點
* AI 標點

## @resp

### AI

resp = "AI" 表示使用「古籍酷 AI 自動標點引擎」製作的新式標點初稿，例如 X01n0008.xml:

```xml
<editorialDecl>
  <punctuation resp="AI"><p>AI 標點</p></punctuation>
</editorialDecl>
```

### orig

resp="orig" 表示是原書的標點，例 A091n1057.xml

```xml
<editorialDecl>
  <punctuation resp="orig"><p>原書標點</p></punctuation>
</editorialDecl>
```

以下表示標記表示原書就是新式標點，例 B07n0023.xml

```xml
<editorialDecl>
  <punctuation resp="orig"><p>新式標點</p></punctuation>
</editorialDecl>
```

### CBETA

resp="CBETA" 表示這是由 CBETA 製作的新式標點，例 B25n0144.xml

```xml
<editorialDecl>
  <punctuation resp="CBETA"><p>新式標點</p></punctuation>
</editorialDecl>
```

### DILA

resp="DILA" 表示這是由 法鼓文理學院 製作的新式標點，例 GA009n0008.xml

```xml
<editorialDecl>
  <punctuation resp="DILA"><p>新式標點</p></punctuation>
</editorialDecl>
```
