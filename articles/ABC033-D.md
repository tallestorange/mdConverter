---
title: "ABC033-D 三角形の分類"
date: 2018-12-03
competive_programming: true
score: 100
algorithms: ["二分探索"]
order: "O(N^2logN)"
contest: "ABC"
difficulty: 4.5
importance: 3.5
---

## 問題

[ABC033-D 三角形の分類](https://beta.atcoder.jp/contests/abc033/tasks/abc033_d)

## 方針

- 鈍角三角形の数 = 鈍角の数

## 解法

- 部分点解法(30点)
    - n個の点から3点を選んで三角形を作り、三角形の種別を調べる
    - 三角形の各辺の長さを$a,b,c\ (a \leq b < c)$とすると
        - $a^2+b^2=c^2$の時は直角三角形
        - $a^2+b^2<c^2$の時は鈍角三角形
        - $a^2+b^2>c^2$の時は鋭角三角形
    - 計算量は$O(n^3)$

- 満点解法(100点)
    - 三角形の内角の和は$180 ^\circ$であるから、鈍角の数=鈍角三角形の数となる
        - 鈍角の数と直角の数を求めれば良さそうなことがわかる
    - 点を1つ固定(Pとする)し、Pを中心とした時の偏角を求める。
    - 求めた偏角をソートする(**二分探索したいから**)
    - 点Q($P \neq Q$)をおく。この時$\angle QPR > 90 ^\circ$となるような点$R$の個数を求めたい(鈍角三角形の個数を求める場合)
        - **二分探索する**(Pythonならbisect.bisect_rightとか)
        - EPSが$1.0 \times 10^{-6}$のときにはWAになる(らしい)
            - 辛い
            - $1.0 \times 10^{-9}$だとAC
    - 計算量は$O(n^2logn)$

## 感想

- EPS考慮する問題はしんどい

## Submission

[満点解法](https://beta.atcoder.jp/contests/abc033/submissions/3603037)

[部分点解法](https://beta.atcoder.jp/contests/abc033/submissions/3607657)