# 実行方法
- `npm run dev`
- `npm run dev -- ファイル名`
- `npm run dev -- ファイル名 --remote`

# codeプロック内の遷移
```python {all|1|3-9}
<Code></Code>
```

# Mermaid図のリンク
[Mermaid](https://mermaid.js.org/intro/)

# UnoCSSのリンク
[UnoCSS Interactive](https://unocss.dev/interactive/)

# ページ下部にページ数を埋め込む
```bash
<div class="absolute bottom-5 right-5">
  <span class="font-size-2">
    {{ $page }}<!-- 1 -->
  </span>
</div>
```

# おすすめフォント
```bash
---
fonts:
  # 標準テキスト用
  sans: Noto Sans JP
  # UnoCSS で `font-serif` クラスを指定したとき用
  serif: Noto Serif JP
  # コードブロック用
  mono: Fira Code
---
```

# Material Icons
[Material Icons](https://icones.js.org/)

# Export
- PDF
```bash
slidev export
```
- PPTX
```bash
slidev export --format pptx
```
PPTXファイル内のすべてのスライドは画像としてexportされるので注意。

- PNGs and Markdown
```bash
slidev export --format md
```
- 出力ファイル名をつけたい場合
```bash
slidev export --output <file-name>
```
- ダークモード
```bash
slidev export --dark
```

# Frontmatter
- title: Welcome to slidev

urlのタイトルとリンクを作成したときや、デフォルトでexportしたときのタイトルとして扱われる。

-
background: これは1枚目のFrontmatterに入れるべきものかな

# アニメーション
**Click**
  クリックはスライド内のアニメーションステップの単位。スライドには1回以上のクリックがあり、クリックごとに1つ以上のアニメーションがトリガーされる。

- `v-click`
<v-click>Hello world!</v-click>
クリック時に表示される。
<div v-click class="text-x1"> Hey! </div>

- `v-after`
`v-click`に連動して表示
<div v-click> Hello </div>
<div v-after> World </div>  <!-- or <v-after> World </v-after> -->

- クリック後に非表示にする
`.hide`クリック後に表示を消す
```bash
<div v-click> Visible after 1 click </div>
<div v-click.hide> Hidden after 2 clicks </div>
<div v-after.hide> Hidden after 2 clicks </div>
```

- `v-clicks`
まとめて適応させる
```bash
<v-clicks>

- 1
- 2
- 3
- 4
</v-clicks>
```
- ネストされたリストの場合
```bash
<v-clicks depth="2">
- Item 1
  - Item 1.1
  - Item 1.2
- Item 2
  - Item 2.1
  - Item 2.2
</v-clicks>
```

# スライドトランジション
Slidevは標準でスライドtransitionをサポートしています。transition frontmatterオプションを設定することで有効にできます。

```bash
---
transition: slide-left
---
```
- `fade` - Crossfade in/out
- `fade-out` - Fade out and then fade in
- `slide-left` - Slides to the left (slide to right when going backward)
- `slide-right` - Slides to the right (slide to left when going backward)
- `slide-up` - Slides to the top (slide to bottom when going backward)
- `slide-down` - Slides to the bottom (slide to top when going backward)
- `view-transition` - Via the view transitions API

# Theme
[テーマギャラリー](https://sli.dev/resources/theme-gallery)

# Layout
[レイアウトの設定](https://sli.dev/builtin/layouts)
