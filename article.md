# ハンズオンを通してWebVRの動向を知る

## これは何

この記事は[DMMグループ Advent Calendar 2020](https://qiita.com/advent-calendar/2020/dmm)の14日目の投稿です。

業務でWebVRに触る機会があり、面白いと思ったので布教の意味も込めてハンズオンを作成しました！記事を読み終えた後にはWebVRの基本を分かったような気になれるはずです。。！

本ハンズオンでは、three.jsとA-Frameというライブラリを使います。
執筆時点でのそれぞれの最新バージョンは以下です。

- [three.js](https://threejs.org/) r123
- [A-Frame](https://aframe.io/) v1.0.4

## まえがき

2020年10月13日、日本でもOculus Quest2が発売されました！前世代のQuestからハードウェアスペックや画質などが向上したにも関わらず、より低価格化したことによりVRの普及に向けた意気込みを感じます。

弊社でもOculus向けに動画アプリを出しており、たくさんのユーザの皆さんにご利用いただいております。ところが動画の購入前に視聴できる無料サンプルに関してはVRモードで見ることができず、ヤキモキした気持ちになった方もいらっしゃるのではないでしょうか。

そこで新卒として配属された私に、サンプル動画のWebVR対応という任務が命じられました。

## WebVR業界の動向

### WebVRからWebXRの時代へ
ここまでずっとWebVRという言葉を使っていましたが、実は最近WebVR APIは、WebARを取り込む形で[WebXR Device API](https://developer.mozilla.org/ja/docs/Web/API/WebXR_Device_API)へと統合されました。

Deviceとあるのは、基本的にはこのAPIはQuestなどのヘッドマウントデバイスをjavascriptから操作できるようにするためのハードウェアの抽象化APIで、実際のレンダリングはWebGLなどのレンダリングAPIを使うからです。

図　webxr webglの簡単な説明

　・webGL webXR three.js aframeの関係 https://tarepan.hatenablog.com/entry/2017/11/22/webVR%E3%81%A8Three.js%E3%81%A8A-frame%E3%81%AE%E9%96%A2%E4%BF%82
  ・ちなみにReact360

ところがこれらのAPIを直接描こうと思うと、行列計算などの割と高度な数学や物理の知識を要求されるため、さらに上の抽象レイヤーとして `three.js` というOSSのライブラリが作られています。three.jsを使えば数十〜数百行のコードでWebの3D表現が作れます。

さらにもっと手軽に3Dを扱えるように、`three.js`のラッパーライブラリとして`A-Frame`が誕生しました。`A-Frame`は、標準化技術としてのWebVRを提案し現在WebXRの策定を推し進めている`Mozilla`を中心として開発が進められています。

ちなみに少し前にWebVRに触ったことのある人は`React360`というライブラリを使ったことがあるかもしれません。`React360`は執筆時点ではWebXRに対応しておらず、開発もほとんど停滞しているようです。（おそらく滅びたようです）

この記事はWebGLなどの低レイヤーには触れずに、`three.js`と`A-Frame`でお手軽に入門することが目的です。

## ハンズオン1: three.js

### 3Dで必須の用語理解 
https://tympanus.net/codrops/2016/04/26/the-aviator-animating-basic-3d-scene-threejs/

### threejsにおけるvr対応 
https://ics.media/entry/18793/

## ハンズオン2: A-Frame
### aframeで同じことをやる
### コンポーネント実装

## まとめ

## 参考サイト
https://note.com/misaki_mofu/n/n21dccbabae20
https://tympanus.net/codrops/2016/04/26/the-aviator-animating-basic-3d-scene-threejs/
https://thebookofshaders.com/02/?lan=jp
https://www.clicktorelease.com/blog/vertex-displacement-noise-3d-webgl-glsl-three-js/