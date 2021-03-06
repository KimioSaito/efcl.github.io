---
title: ATNDをもっと便利にするGreasemonkey「Better ATND」
author: azu
layout: post
permalink: /2011/0306/res2353/
SBM_count:
  - '00005<>1355446965<>5<>0<>0<>0<>0'
dsq_thread_id:
  - 300851621
categories:
  - Greasemonkey
tags:
  - google
  - Greasemonkey
  - イベント
---
ATNDのイベントページに最寄り駅情報の表示やGoogleカレンダーの登録ボタンを追加などをするGreasemonkeyスクリプトを書いてみました。 元ネタは[ATND++][1]というものがあったのですが、メンテされてなかったので自分で修正([ATND++を適当に修正したもの — Gist][2])して使っていたのですが、そのままだとメンテしにくかったので最初から書き直してみました。

*   [Better ATND for Greasemonkey][3]

機能としては以下のような機能が付いています。(2011-03-06)

*   最寄り駅情報の表示
*   最寄り駅をまとめた地図画像の表示
*   Google Calendarへの登録ボタンの追加

Googleカレンダーへの登録時には、イベントページから場所や概要などの情報も自動で入力します(説明文は長すぎるとエラーになるので300文字ぐらいで切っています)

**画像でみる機能**<figure id="attachment_2357" style="width: 300px;" class="wp-caption aligncenter">

[<img class="size-medium wp-image-2357" title="ss-2011-03-06-1" src="https://efcl.info/wp-content/uploads/2011/03/ss-2011-03-06-1-300x288.png" alt="" width="300" height="288" />][4]<figcaption class="wp-caption-text">最寄り駅情報</figcaption></figure> <figure id="attachment_2356" style="width: 300px;" class="wp-caption aligncenter">[<img class="size-medium wp-image-2356" title="ss-2011-03-06-2" src="https://efcl.info/wp-content/uploads/2011/03/ss-2011-03-06-2-300x82.png" alt="" width="300" height="82" />][5]<figcaption class="wp-caption-text">Google Calendarの登録ボタン</figcaption></figure> <figure id="attachment_2355" style="width: 271px;" class="wp-caption aligncenter">[<img class="size-medium wp-image-2355" title="ss-2011-03-06-3" src="https://efcl.info/wp-content/uploads/2011/03/ss-2011-03-06-3-271x300.png" alt="" width="271" height="300" />][6]<figcaption class="wp-caption-text">Google Calendarの登録ページ</figcaption></figure> 
作った(使ってた)理由としては場所を言われてもピンとこない場合が多いのと、電車が主な移動手段であることが多いので、会場がどの駅に近いのかがわかると便利です。また参加してなくてもUstや後で資料を出してくれるイベントも多いので、忘れないように気になったイベントはGoogle Calendarに登録していました。最初はブックマークレット([ATNDのイベント画面にGoogleカレンダーへ予定を登録するボタンを追加するブックマークレット &#8211; 電脳戦士ハラキリ -SE道とは死ぬ事と見つけたり-][7])を使ってたのですが、少し面倒になったのでGreasemonkeyにその機能を入れました。  
ATNDのリニューアルでicsリンクがでて、Google Calendarで読み込む事ができるのですが、icsを読み込むと&#8221;他のカレンダー&#8221;が増えるのであんまり好みじゃないので今まで通り登録ボタンにしました。

APIは以下の2つを使っています

*   [ATND API リファレンス][8]
*   [SimpleAPI vol.2 &#8211; 最寄り駅Webサービス & 最寄り駅モバイル地図][9]

両方ともjsonなどいろいろな形式ではいたりしてくれるので、手軽に使えて便利です。

**Better ATND for Greasemonkey**
:   [http://userscripts.org/scripts/show/98456][3]

**better_atnd at master from azu/Greasemonkey &#8211; GitHub**
:   [https://github.com/azu/Greasemonkey/tree/master/better_atnd][10]

 [1]: http://www.kugimiyabyou.net/2009/10/23/atnd%E6%8B%A1%E5%BC%B5%E3%83%84%E3%83%BC%E3%83%ABatnd-ver-10%E3%82%92%E3%83%AA%E3%83%AA%E3%83%BC%E3%82%B9/ "ATND++"
 [2]: https://gist.github.com/784085 "ATND++を適当に修正したもの — Gist"
 [3]: http://userscripts.org/scripts/show/98456 "Better ATND for Greasemonkey"
 [4]: https://efcl.info/wp-content/uploads/2011/03/ss-2011-03-06-1.png
 [5]: https://efcl.info/wp-content/uploads/2011/03/ss-2011-03-06-2.png
 [6]: https://efcl.info/wp-content/uploads/2011/03/ss-2011-03-06-3.png
 [7]: http://d.hatena.ne.jp/hagino_3000/20091216/1260894102 "ATNDのイベント画面にGoogleカレンダーへ予定を登録するボタンを追加するブックマークレット - 電脳戦士ハラキリ -SE道とは死ぬ事と見つけたり-"
 [8]: http://api.atnd.org/ "ATND API リファレンス"
 [9]: http://map.simpleapi.net/ "SimpleAPI vol.2 - 最寄り駅Webサービス & 最寄り駅モバイル地図"
 [10]: https://github.com/azu/Greasemonkey/tree/master/better_atnd "better_atnd at master from azu/Greasemonkey - GitHub"
