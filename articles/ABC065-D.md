---
title: "ABC065-D Built?"
date: 2019-02-21T12:54:10+09:00
draft: false
toc: true
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