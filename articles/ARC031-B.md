---
title: "ARC031-B 埋め立て"
date: 2018-11-28T15:43:20+09:00
draft: false
---

## 問題

[ARC031-B 埋め立て](https://beta.atcoder.jp/contests/arc031/tasks/arc031_2)

## 方針
陸マスの数をtotalとする。任意の海マスを起点とした時に、探索できたマス数がtotal+1となるような海マスが存在する場合はYES、そうでない場合はNO。

盤面が$10 \times 10$と小さいため、連結判定はDFSでもBFSでもUnion-Findでも可。

## 感想

~~初めはUnion-Findで実装していたがバグって辛くなったのでDFSにしました~~

## Submission

[DFSを使った解法](https://beta.atcoder.jp/contests/arc031/submissions/3680075)
