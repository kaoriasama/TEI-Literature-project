# Granularity Taxonomy for TEI Texts

このフォルダには、TEIテキストで使用する共通の **空間粒度分類（granularity taxonomy）** を格納しています。  
ファイル名: `granularity-taxonomy.xml`

---

## 使い方

### 1. TEIファイルのヘッダでtaxonomyを参照する
各作品のTEIファイルでは、`<encodingDesc>` 内に以下のように記述してください。  

```xml
  <profileDesc>
　　 <textClass>
　　　 <catRef target="gran-scale"/>
　　 </textClass>
  </profileDesc>
  <encodingDesc>
     <classDecl>
　 　　<taxonomy xml:id="gran-ref"
                source="https://kaoriasama.github.io/TEI-Literature-project/taxonomies/granularity-taxonomy.xml">
　　 　　<desc>Shared granularity taxonomy (external reference)</desc>
　　　 </taxonomy>
     </classDecl>
  </encodingDesc>
```
### 2. 本文中で粒度を指定する

本文の <seg> や <place> 要素に、@ana 属性で taxonomy のカテゴリを参照します。
```
例：
<!-- 観念的空間 (gran-0) -->
<seg corresp="#夢の世界" ana="#gran-0">夢の世界</seg>

<!-- 素粒子スケール (gran-1.1) -->
<seg corresp="#電子" ana="#gran-1.1">電子</seg>

<!-- 人物・身体・服飾スケール (gran-5) -->
<seg corresp="#僕の服" ana="#gran-5">僕の服</seg>

<!-- 都市スケール (gran-7) -->
<seg corresp="#ロオマ" ana="#gran-7">ロオマ</seg>
```
## 目的

このtaxonomyは複数作品で 共通の粒度スケール を利用することを目的としています。
これにより、文学作品を横断的に比較したり、Viewerで一貫した可視化を行うことが可能になります。
