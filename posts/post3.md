# 静的サイトでのブログ記事管理

静的サイトでブログ記事を管理する方法について説明します。今回使用した技術とツールについて詳しく見ていきましょう。

## 使用した技術

- **HTML**: 基本的なページ構造を作成します。
- **CSS**: ページのスタイルを設定し、デザインを整えます。
- **JavaScript**: 記事の読み込みと表示を制御します。
- **jQuery**: DOM操作を簡単にするために使用します。
- **Marked.js**: MarkdownをHTMLに変換するためのライブラリです。

## 実装のポイント

1. **Markdownファイルの管理**:
   - 記事をMarkdownファイルとして保存し、簡単に編集できるようにします。
   ```markdown
   # サンプル記事
   これはサンプル記事です。Markdown形式で記述されています。
   ```
2. JavaScriptでの読み込み:
jQueryとMarked.jsを使用して、Markdownファイルを読み込み、HTMLに変換して表示します。

```javascript
$(document).ready(function() {
    $.get('post.md', function(data) {
        const htmlContent = marked.parse(data);
        $('#content').html(htmlContent);
    });
});
```

3. デザインの統一:
```css
CSSを使用して、全体のデザインを統一します。特に、フォントや色の設定に注意します。
css
コードをコピーする
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
結論
静的サイトでブログ記事を管理する方法は、簡単かつ効率的です。Markdownファイルを使用することで、記事の編集や管理が容易になり、JavaScriptを使用して動的に記事を表示することができます。