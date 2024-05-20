# ブログページの作成方法

このブログページは、静的なHTML、CSS、JavaScriptを使用して作成されました。特に、ブログ記事をMarkdownファイルから読み込み、表示する方法について説明します。

## 必要なツールと技術

- HTML
- CSS
- JavaScript
- jQuery
- Marked.js (Markdownパーサー)

## 手順

**HTMLの構成**:
   - 基本的なHTML構造を作成し、スタイルを適用します。
   ```html
   <!DOCTYPE html>
   <html lang="ja">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>ブログページ</title>
       <link rel="stylesheet" href="style.css">
   </head>
   <body>
       <header>
           <h1>ブログページ</h1>
       </header>
       <main id="content"></main>
       <script src="script.js"></script>
   </body>
   </html>
```   
**CSSの設定**

全体のデザインを整えるためにCSSを使用します。特に、フォントや色の設定を行います。
```css

body {
    font-family: 'Roboto', sans-serif;
    background-color: #f0f0f0;
    color: #333;
    margin: 0;
    padding: 0;
}
header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}
main {
    padding: 20px;
    max-width: 800px;
    margin: 0 auto;
}
```
**JavaScriptの実装**
```javascript
jQueryとMarked.jsを使用して、Markdownファイルを読み込み、HTMLに変換して表示します。
javascript
コードをコピーする
$(document).ready(function() {
    $.get('post.md', function(data) {
        const htmlContent = marked.parse(data);
        $('#content').html(htmlContent);
    });
});
```
結論
この方法を使用することで、簡単にブログページを作成し、記事をMarkdownファイルとして管理できます。