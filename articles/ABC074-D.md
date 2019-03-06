---
title: "ABC074-D Restoring Road Network"
date: 2018-2-22
competive_programming: true
score: 500
algorithms: ["ワーシャルフロイド法"]
order: "O(N^3)"
contest: "ABC"
difficulty: 4.0
importance: 4.0
---

## 問題

[ABC074-D Restoring Road Network](https://atcoder.jp/contests/abc070/tasks/abc070_d)

## 方針

- $A[i][j]=A[i][k]+A[k][j]\,\,(i \neq k, k \neq j)$の時$i,j$を繋ぐ辺を張る必要がない
  - $i$から$k$を経由して$j$に至れば良く、$i$と$j$を直接繋ぐ必要がないため
- $A[i][j] > A[i][k]+A[k][j]$の時はそのような道路構造を構築できない
  - $A[i][j]$は$i$から$j$への最短距離であるという事実に矛盾するため
- 各$i,j$のペアに対して$k$を動かして考えれば良い
  - 上記$2$つの条件に該当しない辺を使う
- 計算量は$O(N^3)$

## 感想

- バグらせて死んだ
- $N \geq 200$の$O(N^3)$解法はPython3でとTLEになるリスクが高い([というかTLEになった](https://atcoder.jp/contests/abc074/submissions/4346206))

## Submission

[PyPy3](https://atcoder.jp/contests/abc074/submissions/4345608)