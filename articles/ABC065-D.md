---
title: "ABC065-D Built?"
date: 2018-2-21
competive_programming: true
score: 400
algorithms: ["UnionFind","最小全域木","木構造"]
order: "O(NlogN)"
contest: "ABC"
difficulty: 3.0
importance: 4.0
---

## 問題

[ABC064-D Built?](https://atcoder.jp/contests/abc064/tasks/abc065_d)

## 方針

街を頂点、道を辺とみた時の**最小全域木**が欲しい

任意の2つの街を選んだ場合は$N(N-1)/2$通りある為、
$O(N^2)$となり間に合わない。

$x, y$それぞれでソートを行った時、両隣の要素がそれぞれの街における最短距離の街であるので、これらだけを追加する辺の候補とみなして良い。

街の連結判定はUnionFindを使えば良い(探すのに時間かかった)

計算量は$O(NlogN)$なのでPythonでも十分に間に合う。

## 感想

やるだけでした

## Submission

[Python3](https://atcoder.jp/contests/abc065/submissions/4335829)