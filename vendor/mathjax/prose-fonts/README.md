# prose-fonts — 地の文の欧文用フォント（MathJax_Main のコピー）

`micro-notes.html` の `@font-face 'MJXText'` が読む woff。中身は
`../output/chtml/fonts/woff-v2/` にある同名ファイルとまったく同じもの。

**なぜコピーが必要か**：同じ URL を MathJax の `MJXTEX` と自前の `MJXText` の
2つの `@font-face` から参照すると、**Chrome の PDF 書き出しでフォントが1つしか
埋め込まれず、MathJax 側が Times にフォールバックする**（数式の数字・記号・
立体の英字だけ別フォントになる）。画面表示では起こらず PDF だけで出る。
URL を分ければ両方とも埋め込まれる。

MathJax を更新したら、この3ファイルも同じ版で置き直すこと。
