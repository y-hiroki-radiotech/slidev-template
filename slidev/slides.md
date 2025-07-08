---
theme: seriph
aspectRatio: '16/9'
title: Welcome to Slidev
background: /images/sample.jpg
transition: slide-left
---

# Slide 1

Content of my slide

<!--
This is a note for my slide and I am typing here
-->

---
layout: center
background: /images/sample.jpg
class: text-white
transition: slide-left
---
# Slide 2
A page with the layout `center` and a background image

---

# Slide 2

Content of the second slide

```python {all|1|3-11|3}
import time

def long_process_task():
  """
  内部で8秒間待機することで、処理に時間がかかるように見せる関数。
  """
  print("▶️ 処理を開始します。")
  # この行で8秒間、処理を停止します
  time.sleep(8)
  print("✅ 処理が完了しました！")
# 関数の実行
long_process_task()
```

<style>
h1 {
  color: white
}
</style>
---

# Slide 3

Third sllide

<asterisks>
asterisks
</asterisks>

*asterisks*

**asterisks**

**asterisks and _underscores_**

~~Serect this~~


---

# Slide 4

1. First ordered list item
2. Another Item
   * Unordered sub-list.

* Unordered list can use asterisks
- or minues
+ or pluses

[私のGitHubのslideページ](https://github.com/y-hiroki-radiotech/slides/tree/main)

You can use numbers for reference-style link difinitions [^1]

![Markdown Here extension icon](https://raw.githubusercontent.com/adam-p/markdown-here/master/src/common/images/icon48.png)

[^1]: https://github.com/y-hiroki-radiotech/slides/tree/main

---

# Slide Image

![alt text](https://www.edelweiss.co.jp/wpedel/wp-content/uploads/2024/07/magazine_10_mv.jpg)

<style>
  img {
    margin: auto;
    width: 70%
  }
</style>

---

| Tables | Are | Cool |
|---|:---:|---:|
| col 3 is | right-aligned | $1600 |
| col 2 is | centered | $12 |
| zebra stripes | are neat | $1 |

<br>

> Black quote

---
layout: two-cols
---

## Left

This show on the left side

::right::

## Right

This shows on the right

---

# LaTeX

In line $\sqrt{3x-1} + (1 + x)^2$ and $a=2$

$$b=2$$

$$ \begin{array}{c}

\nabla \times \vec{\mathbf{B}} -, \frac1c, \frac{\partial\vec{\mathbf{E}}}{\partial t} & = \frac{4\pi}{c}\vec{\mathbf{j}} \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\

\nabla \times \vec{\mathbf{E}}, +, \frac1c, \frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\

\nabla \cdot \vec{\mathbf{B}} & = 0

\end{array} $$

---
layout: center
---

```mermaid {theme: 'neutral', scale: 0.8}
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop HealthCheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

---
src: ./pages/flowchart.md
---


---

# アニメーション

<v-click>Hello World!</v-click>
<br>
<br>
<v-click>こんにちは、世界！</v-click>
<br>
<div v-click class="text-x1"> Hey! </div>
<br>
<br>
<div v-click> Hello </div>
<div v-after> World! </div>

---

# クリック後に非表示にする

<div v-click>今日は</div>
<div v-click.hide>いい</div>
<div v-after.hide>天気</div>

---

# クリックをまとめて適応

<v-clicks>

- 今日は
- いい
- 天気
- だよね
</v-clicks>

<v-clicks depth="2">

- Item 1
  - Item 1.1
  - Item 1.2
- Item 2
  - Item 2.1
  - Item 2.2
  -
</v-clicks>

---

<div class="slidev-vclick-target slidev-vclick-hidden">Text</div>
