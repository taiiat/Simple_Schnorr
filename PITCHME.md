### Simple Schnorr Multi-Signatures with Applications to Bitcoin(Pre)

---

#### Abstract
1.新しいマルチシグなSchnorr署名の提案
  - より効率的かつシンプル
  - key aggregationの仕組みを追加（重要）

---
#### key words
- multi-signatures
- Schnorr signatures
- discrete logarithm problem（）
- forking lemma

---
#### multi-signatures
複数の署名を利用して、複数の合意が得られないと処理を進められないといった仕組み

(eg)

- メッセージｍに対してM人のうち、N人が秘密鍵で署名$\rho$	作成して合意
しかし、これでは署名者が増えるとサイズが大きくなってしまう

---
#### Schnorr signatures
- 複数の署名を一つにまとめることができる 
- 離散対数問題の困難生を利用
- *ランダムオラクルモデルにおいて選択メッセージ攻撃にたいして存在的偽造不可である

+++
- ランダムオラクルモデルとは
  - 理想的なハッシュ関

- 存在的偽造不可

どのような効率的なアルゴリズム F も、（署名鍵 sk を知らずに）検証鍵 pk だけを用いて、与えられたメッセージ m に対して妥当な署名σをつくることはできない


https://w.atwiki.jp/d1space/pages/20.html






