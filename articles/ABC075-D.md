---
title: "ABC075-D Axis-Parallel Rectangle"
date: 2019-02-23T08:22:39+09:00
draft: false
toc: true
---

## 問題

[ABC075-D Axis-Parallel Rectangle](https://atcoder.jp/contests/abc075/tasks/abc075_d)

## 方針

- $N \leq 50$なのでとりあえず全探索することを考える
- 長方形の高さを$H$,幅を$W$とする
  - このとき$H$は$_N C _2$通り
  - $W$も$_N C _2$通りある
- 各$(H,W)$に対して$N$個の点が長方形の内部にあるか確認すればよい
- 計算量は$O(N^5)$
  - Pythonではきつそう

## 感想

- やるだけだった

## Submission

[PyPy3](https://atcoder.jp/contests/abc075/submissions/4349695)