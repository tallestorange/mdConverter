---
title: "ABC015-D 高橋君の苦悩"
date: 2018-11-28
competive_programming: true
score: 400
algorithms: ["DP"]
order: "O(N^3)"
contest: "ABC"
difficulty: 4.0
importance: 4.5
---

## 問題
[ABC015-D](https://beta.atcoder.jp/contests/abc015/tasks/abc015_4)

$N(1 \leq N \leq 50)$枚のスクリーンショットから幅の総和が$W(1 \leq W \leq 100000)$を超えないように$K(1 \leq K \leq N)$枚以下のスクリーンショットを選んだ時の価値の最大値を求める。それぞれのスクリーンショットの幅、価値は$a[i]$,$b[i]$($0 \leq i < N$)として与えられている。

## 方針
個数制限付きナップザック問題。

DPテーブルを dp[i][j][k] := i番目までのスクリーンショットをj枚加えた時に幅k以下になった場合の価値の最大値とおき、値を更新する。

i番目のスクリーンショットを選ぶ場合($k-a[i-1] \geq 0$の場合のみ)

$$dp[i][j][k]=max(dp[i-1][j-1][k-a[i-1]]+b[i-1],dp[i][j][k])$$

i番目のスクリーンショットを選ばない場合

$$dp[i][j][k]=max(dp[i-1][j][k],dp[i][j][k])$$

最終的な答えは$dp[N][K][W]$となる。

この方針では$O(N^2W)$となる事から[Pythonでは計算量的に厳しく、TLE](https://beta.atcoder.jp/contests/abc015/submissions/3674985)となってしまった。~~Pythonで通している人もいるので実装がダメなだけだが~~

## 感想・反省点
今ABCで出たら300~400程度の問題だと思った。

計算量的にPythonでは厳しい問題はC++を積極的に用いてゆきたい。

## Submission
[ABC015-D (C++で提出)](https://beta.atcoder.jp/contests/abc015/submissions/3675019)