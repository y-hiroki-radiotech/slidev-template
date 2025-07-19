---
theme: default
background: white
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## 医学系論文抄読会

  論文タイトル: {{論文のタイトル}}
  発表者: {{発表者名}}
  日付: {{日付}}
drawings:
  persist: false
transition: slide-left
title: {{論文のタイトル}}
---

# {{論文のタイトル}}

**{{著者名}}**

*{{雑誌名}}* {{巻}}, {{号}}, {{出版年}}

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    発表開始 <carbon:arrow-right class="inline"/>
  </span>
</div>

---
transition: fade-out
---

# 背景

<v-clicks>

- {{既存の知見1}}
- {{既存の知見2}}
- {{研究の重要性}}
- {{研究の関連性}}

</v-clicks>

---

# 背景（続き）

<v-clicks>

- {{未解決の問題点1}}
- {{未解決の問題点2}}
- {{研究のギャップ}}
- {{研究の目的（簡潔に）}}

</v-clicks>

---

# 背景（続き）

<v-clicks>

- {{研究の具体的な目的1}}
- {{研究の具体的な目的2}}
- {{期待される成果1}}
- {{期待される成果2}}

</v-clicks>

---
layout: two-cols
---

# 方法

## 研究デザイン

<v-clicks>

- {{研究デザインの詳細}}
- {{デザイン選択の理由}}
- {{デザインの長所}}
- {{デザインの制限事項}}

</v-clicks>

::right::

<div class="ml-4">
  <!-- 必要に応じて図表やイラストを追加 -->
</div>

---

# 方法（続き）

## 参加者選定

<v-clicks>

- {{適格基準1}}
- {{適格基準2}}
- {{除外基準1}}
- {{除外基準2}}
- {{サンプルサイズとその根拠}}

</v-clicks>

---

# 方法（続き）

## 評価項目と測定方法

<v-clicks>

- {{主要評価項目}}
- {{副次的評価項目}}
- {{測定方法1の詳細}}
- {{測定方法2の詳細}}
- {{データ収集の時期と頻度}}

</v-clicks>

---

# 方法（続き）

## 統計解析

<v-clicks>

- {{使用した統計手法1}}
- {{使用した統計手法2}}
- {{有意水準の設定}}
- {{欠損データの取り扱い}}
- {{使用した統計ソフトウェア}}

</v-clicks>

---
layout: center
class: text-center
---

# 結果

---

# 結果

<v-clicks>

- {{主要な結果1}}
- {{主要な結果2}}
- {{統計的有意性}}
- {{効果量}}
- {{信頼区間}}

</v-clicks>

---

# 結果（続き）

<v-clicks>

- {{副次的結果1}}
- {{副次的結果2}}
- {{サブグループ解析結果}}
- {{予定外の発見}}
- {{有害事象（該当する場合）}}

</v-clicks>

---

# 結果（続き）

<v-clicks>

- {{図表1の説明}}
- {{図表2の説明}}
- {{図表から読み取れる傾向}}
- {{結果の要約}}

</v-clicks>

---
layout: center
class: text-center
---

# 考察

---

# 考察

<v-clicks>

- {{主要な発見1とその意味}}
- {{主要な発見2とその意味}}
- {{既存の知見との整合性}}
- {{新たな知見の重要性}}
- {{臨床的または理論的意義}}

</v-clicks>

---

# 考察（続き）

<v-clicks>

- {{支持する先行研究1}}
- {{支持する先行研究2}}
- {{反論する先行研究1}}
- {{反論する先行研究2}}
- {{矛盾する結果の解釈}}

</v-clicks>

---

# 考察（続き）

<v-clicks>

- {{研究の強み1}}
- {{研究の強み2}}
- {{研究の限界1}}
- {{研究の限界2}}
- {{結果の一般化可能性}}

</v-clicks>

---

# 考察（続き）

<v-clicks>

- {{予期せぬ結果の解釈}}
- {{代替説明の検討}}
- {{結果の実践的応用}}
- {{今後の研究課題}}

</v-clicks>

---
layout: center
class: text-center
---

# 結論

<v-clicks>

- {{主要な知見の要約}}
- {{研究分野への貢献}}
- {{臨床実践への示唆}}
- {{将来の研究方向}}
- {{最終的なメッセージ}}

</v-clicks>

---
layout: center
class: text-center
---

# ご清聴ありがとうございました

質疑応答

<div class="pt-12">
  <span class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    <carbon:email class="inline"/> {{発表者の連絡先（任意）}}
  </span>
</div>
