# Granularity Taxonomy for TEI Texts

このフォルダには、TEIテキストで使用する共通の **空間粒度分類（granularity taxonomy）** を格納しています。  
ファイル名: `granularity-taxonomy.xml`

---

## 使い方

### 1. TEIファイルのヘッダでtaxonomyを参照する
各作品のTEIファイルでは、`<encodingDesc>` 内に以下のように記述してください。  

```xml
<encodingDesc>
  <taxonomy xml:id="gran-ref"
            source="https://username.github.io/tei-project/taxonomies/granularity-taxonomy.xml">
    <catRef target="gran-scale"/>
  </taxonomy>
</encodingDesc>
