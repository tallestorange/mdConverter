---
title: "ABC064-D Insertion"
date: 2019-02-20T23:48:00+09:00
draft: false
---

## 問題

[ABC064-D Insertion](https://atcoder.jp/contests/abc064/tasks/abc064_d)

## 方針

- 元々ある文字列で正しい括弧列ができるか考える
  - stackなりどんな方法でもいいので括弧列の判定をしましょう
- 正しい括弧列にできなかった括弧を数えます
  - 左括弧が$a$個余っているなら元の文字列の後ろに右括弧を$a$個追加
  - 右括弧が$b$個余っているなら元の文字列の前に左括弧を$b$個追加
- この方法だと計算量は$O(|S|)$になります

## 感想

- Nが小さいとどうしても色々と深読みしてしまい、愚直に解くことが出来ない

## Submission

[Python3(256B)](https://atcoder.jp/contests/abc064/submissions/4332894)