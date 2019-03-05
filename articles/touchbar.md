---
title: "AtCoder TouchBar作った"
date: 2019-02-20T15:53:26+09:00
draft: false
---

## これって何

![screenshot](/static/touchbar/Screenshot_8.png)

AtCoderの精進に役立つ(かもしれない)TouchBarです。
  
~~詳しくは[README](https://github.com/tallestorange/ACTouchBar)を読んでください~~

## なんで作ったのか

理由は3つです

1. TouchBar付きのMacBookProを買った([**15インチモデルはTouchBar無しモデルがない**](https://www.apple.com/jp/shop/buy-mac/macbook-pro/15%E3%82%A4%E3%83%B3%E3%83%81))
2. シングルディスプレイ環境
3. **TouchBarがクソすぎる**

まず1.についてなのですが、私がMacBookProを買った当時(2018 / 6) 13インチモデルにクアッドコアモデルが無かったため15インチモデルを買う決断をしました。~~すごく高かった...~~

2.については現在お家に作業机がなく、サブモニタが置けないのです。辛い。

3.については話すとINF時間かかりそうですが、一番のクソポイントとしては

**ActiveなWindowに紐づけられたTouchBarのアイテムしか表示できない**

ということに尽きます。いくつか例を挙げると、

(Google Chrome)
![screenshot](/static/touchbar/Screenshot_9.png)

(iTunes)
![screenshot](/static/touchbar/Screenshot_10.png)

こんな感じで、ActiveなWindowに紐付けられたアイテムしか表示ができません。そしてこれらのアイテムは**そんなに便利な物でもない**為、TouchBarが活躍する機会はありませんでした・・・

## 時は流れ西暦2019年...

「そういえば、Swift少しできるんだったなぁ」

ふと192は思いました。

「折角TouchBar付きのMacBookを使っているのに、TouchBarを全く活用していないのは勿体無いなあ」

「AtCoderの精進状況をTouchBarに常時表示できないかなあ」

「MacOSのアプリなら、iOSアプリと同じ要領で作れるのでは？」

『善は急げ』という訳で(?)2019/2/6に開発をスタートしました。

目標としては、AtCoderのレートや提出状況の常時表示あたりができればいいなあくらいに考えました。

## 課題に直面

素直に実装したらWindowが非Activeの時にアイテムが隠れてしまったのです(それはそう)

しばらくインターネットの海を彷徨っていたところ、どうやら**AppleのプライベートAPIを使用するとTouchBarのアイテムの常時表示ができる**ことがわかりました。

しかし、プライベートAPIなので当然情報があまりなく、なんとかたどり着いた[これ](https://github.com/Toxblh/MTMR)や[これ](https://github.com/a2/touch-baer)を参考にしながら実装しました。

## 完成

2019/2/16になんとか[リリース](https://github.com/tallestorange/ACTouchBar/releases/tag/1.0.0-alpha)をすることができました。

少しずつ機能追加はしていますが、まだまだ発展途上な部分が多々あるので一緒に開発してくれる人がいれば嬉しいですね・・・

## おわりに

TouchBar最高！！！

(※ちなみにXcodeを入れるとTouchBarシミュレータがついてきます)

![screenshot](/static/touchbar/IMG_20190220_204946.jpg)