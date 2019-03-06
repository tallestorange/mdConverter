---
title: "ABC070-D Transit Tree Path"
date: 2018-2-22
competive_programming: true
score: 400
algorithms: ["DFS","木構造"]
order: "O(N)"
contest: "ABC"
difficulty: 3.5
importance: 4.0
---

## 問題

[ABC070-D Transit Tree Path](https://atcoder.jp/contests/abc070/tasks/abc070_d)

## 方針

- 木構造上での最短経路
  - LCAを求める系かなぁ
      - $K$が固定だからLCAを求める程でもない
  - $K$から各頂点への距離をDFSを使って求める
      - $K$からの各点の距離を$dist[i]$とする($1 \leq n \leq N-1$)
          - 各クエリの解は$dist[x_j]+dist[y_j]$になる

## 感想

- ~~DFSでバグらせた(初心者なので)~~
- Pythonだとsys.setrecursionlimit(1000000)しないとREになる([RE提出](https://atcoder.jp/contests/abc070/submissions/4343832))
  - それはそう

## Submission

[Python3](https://atcoder.jp/contests/abc070/submissions/4337500)