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
- *ランダムオラクルモデルにおいて選択平文攻撃にたいして存在的偽造不可

+++
- ランダムオラクルモデルとは
  - 完全なハッシュ関数

- 存在的偽造不可
  - どのような効率的なアルゴリズムも検証鍵 pk だけを用いて与えられたメッセージ m に対して妥当な署名σをつくることは不可


---
##### Scheme of Schnorr
 a cyclic group $G$ of prime order $p$, 
 
 a generator $g$ of G,and a hash function $H$
 
 
 
 







