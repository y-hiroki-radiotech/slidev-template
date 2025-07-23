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

# デフォルトテーマのレイアウト
[デフォルトテーマのレイアウト](https://zenn.dev/rinc5/articles/b7dc7a3b0bbd30)

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

# 横線
`***`

# hideInToc: true
Frontmatterに`hideInToc: true`を追加することで、目次に表示されなくなります。

# Material Icons
[Material Icons](https://icones.js.org/)

**`mdi:account-circle`** をSlidevで使うコンポーネント形式に変換するルールは以下の通りです。

1.  コロン（`:`）をハイフン（`-`）に変える。
2.  全体をコンポーネントのタグ（`<` と `/>`）で囲む。

---

### 具体的な変換手順

あなたの見つけたアイコン `mdi:account-circle` を例にすると、

1.  まず、コロン `:` をハイフン `-` に置き換えます。
    > `mdi:account-circle` → `mdi-account-circle`

2.  次に、その文字列をタグで囲みます。
    > `mdi-account-circle` → `<mdi-account-circle />`

これで完了です。
この `<mdi-account-circle />` をそのままSlidevのMarkdownファイルに貼り付ければ、画像と同じアイコンが表示されます。

### まとめ（ルール）

| 見つけた形式 | Slidevでの形式 |
| :--- | :--- |
| `[コレクション名]:[アイコン名]` | `<[コレクション名]-[アイコン名] />` |

**別の例:**
もし `carbon:settings` というアイコンを見つけたとします。
ルールに従うと、コロンをハイフンに変えてタグで囲むので `<carbon-settings />` となります。

このルールさえ覚えておけば、どのサイトで見つけたアイコンでも迷わず使えるようになります。


# 目次の表示
目次を表示するには、以下のように`<Toc />`コンポーネントを使用します。
```bash
<Toc maxDepth="2"/>
```
`maxDepth`は目次の深さを指定します。デフォルトは1です。
maxDepth属性の役割
maxDepth="2" 属性は、目次に表示する見出しレベルの最大深度を制御します。この設定により：

# 見出し1（レベル1）は目次に含まれます
## 見出し2（レベル2）は目次に含まれます
### 見出し3（レベル3以下）は目次に含まれません

