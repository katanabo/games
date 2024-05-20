# iframeを使用したブログ記事の表示

今回は、iframeを使用してブログ記事を表示する方法について説明します。iframeを使用することで、記事を別ページに読み込み、簡単に管理することができます。

## iframeの利点

- 記事の独立性: 各記事を別のHTMLファイルとして管理できるため、更新や修正が容易です。
- デザインの統一: メインページと記事ページでデザインを統一することができます。

## 実装手順

1. **iframeの設定**:
   - HTML内にiframeを配置し、記事のURLを指定します。

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
       <main>
           <iframe src="post.html" width="100%" height="600px"></iframe>
       </main>
       <script src="script.js"></script>
   </body>
   </html>
```

2. **JavaScriptでの制御:**

```javascript
jQueryを使用して、クリックイベントでiframeに記事を読み込みます。
javascript
コードをコピーする
$(document).ready(function() {
    $('button').click(function() {
        $('iframe').attr('src', 'post.html');
    });
});
```
3. CSSでのデザイン:
```css
iframe内のコンテンツが見やすくなるようにスタイルを設定します。
css
コードをコピーする
iframe {
    border: none;
}
```
結論
iframeを使用することで、ブログ記事の表示が簡単に管理でき、デザインの統一性も保つことができます。