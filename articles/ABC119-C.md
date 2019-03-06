---
title: "ABC119-C Synthetic Kadomatsu"
date: 2019-02-24
competive_programming: true
score: 300
algorithms: ["全探索"]
order: "O(4^N)"
contest: "ABC"
difficulty: 3.5
importance: 2.5
---

## 問題

[ABC119-C Synthetic Kadomatsu](https://atcoder.jp/contests/abc119/tasks/abc119_c)

## 方針

$N$本の竹は、それぞれ最終的に

- 長さが$A$の竹を作るために使われる(Group Aとします)
- 長さが$B$の竹を作るために使われる(Group Bとします)
- 長さが$C$の竹を作るために使われる(Group Cとします)
- 使われない

のいずれかの状態をとる。

どうやらこの問題は$O(4^N)$で解けそうです。

Pythonの場合だと、itertools.product(range(4),N)を使ってそれぞれの場合について考えればよいです。このとき、Group A,B,Cそれぞれに1本以上の竹を割り振る必要があります。

Group A,B,Cに竹が$N_A,N_B,N_C$本入っているとし、長さの総和が$L_A,L_B,L_C$だったとします。

このとき延長・短縮魔法をかける必要のある回数はそれぞれ

$abs(A-L_A),abs(B-L_B),abs(C-L_C)$となります。

また、合成魔法をかける必要のある回数はそれぞれ

$N_A-1,N_B-1,N_C-1$となるため、

この場合必要なMPは

$abs(A-L_A)+abs(B-L_B)+abs(C-L_C)+10(N_A+N_B+N_C-3)$

となります。これのminが答えです

## 感想

- 350点位の重さがありますね

## Submission

[Python3](https://atcoder.jp/contests/abc119/submissions/4376271)
