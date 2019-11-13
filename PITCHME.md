### Simple Schnorr Multi-Signatures with Applications to Bitcoin(1)

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
- rounge key attack

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
 
 a generator $g$ of $G$,and a hash function $H$
 
 private/public key=$(x,X)\in {{1,2\cdots,p}}\times G$
 
 $X=g^x$
 
 
+++
 #### sign a message and checking validity
 
 signer draws a random integer $r \in Z_p$ 
 
 computes $R = g^r,c=H(X,R,m) and then, s=r+cx$
 
 The signature=$(R,s)$
 
 ###### verifying
 $g^s=RX^c$
 
---
  ##### Schnorr multi-signature scheme
  
  a group of n signers want to cosign a message m
  
  multiset of all their public key
  
  - $L={X_1=g^x_1,X_2=g^x_2,\cdots,X_n=g^x_n}$
  
+++
  ##### Signatures
  each of them computes 
  
  $\displaystyle R =\prod_{i=0}^n R_i ,c = H(\tilde{X}, R, m) $
  
  $\displaystyle \tilde{X}= \prod_{i=0}^n X_i$
  
   a partial signature:$ s_i = r_i + cx_i$ 
 
 then,combined into a single signature $(R, s)$
 
 - where $\displaystyle s = \sum_{i=0}^n s_i \pmod{p}$
 
  

 
+++
 ##### The validity of a signature (R,s)
 
  $g_{s} = R \tilde{X}$
  
  - where $\tilde{X} =  \prod_{i=1}^n X_i and c = H(\tilde{X},R,m)$
  
  $\tilde{X}$:key aggregation
  
  
+++
 ##### vulnerable to a rogue-key attack
 
 a corrupted signer sets its public key to $X{1} = g^x_1 ( \prod_{i=1}^n X_{i})^{−1}
 
  
---
  
  
 
 


 
 
 
 
 
 
 
 
 
 







