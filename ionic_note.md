# [HTML5でアプリを作るIonic 2 + ミートアップ東京](https://ionic-jp.connpass.com/event/61051/)

## Webの未来を切り開くIonic Framework(仮):monkey:


- [ionic framework](https://ionicframework.com/)
  - angular が土台
  - クラスランナー、ライブリロードが自動化
  - bootstrapのようなUIコンポートを持ち
  - TechFeed, Hibee, McDonald's Turkiye

- 始める
  - `npm install -g ionic cordova`
  - `ionic start ProjectName`
  - `ionic serve`
  - usecaseから学ぶConponents demo:  [ionic-team.gitgub.com](https://github.com/ionic-team/ionic)

- ionic cordove build ios|android  iosかandroid化にwrappingすると、変更できる
- 2015年から、ionic 1；2017年からionic3
- googleが、[PWA](https://developers.google.com/web/progressive-web-apps/)でwebをアプリ化、つまりwebをアプリにする
  - オフラインでの表示：キャッシュから読み込み
  - 一番から入った時点で、offlineでもonlineでもアクセスできる
  - demo: [air2.areaia.jp](https://air2.areaia.jp)
  - Push通知

- 疑問
  - 起動遅いでしょう → ionic3から、moduleを分割して遅延ロード、遅くない
  - deeplinkがなくなった
  - 実は、[lighthouse](https://developers.google.com/web/tools/lighthouse/?hl=ja)の点数が高い；
  - [OGPタグ](https://ferret-plus.com/610)が動かないでしょう → [prewrender.io](https://prerender.io/)を使うことで対応可能

- safraiも来年にできる可能
- 簡単に始める,[ionic-WP.com](http://ionic-wp.com/)を試すアプリ:[wp pocket](https://ja.wordpress.org/plugins/pocket-wp/)
- 例：[俺の嫁が可愛い](https://itunes.apple.com/us/app/%E4%BF%BA%E3%81%AE%E5%AB%81%E3%81%8C%E5%8F%AF%E6%84%9B%E3%81%84/id1261036550?l=ja&ls=1&mt=8)、数時間でできる
- wordpressの代わりにできる、第2wordpressでできる
- webアプリ、iosアプリ、androidアプリ all in oneの単価は、かなり安くなる
- [slack](https:://www.ionic2.slack.com)で日本語情報共有

## Ionic（Angular）初心者によるテスト奮闘記:octopus:
- [k-kuwahra](https://speakerdeck.com/clown0082), roit
- テストの必要性
  - 動作検証、開くor閉じる
  - バグを見つける事ができる
  - コードの質を高めることに繋がる
  - 良いテストを自動化できる
- ionic appのテスト
  - ionic start hoge
  - test環境を自分を用意
    - angularのテスト環境を自作
    - ツール：[jasmine](https://jasmine.github.io/), [protractor](http://www.protractortest.org/#/), [arma](https://karma-runner.github.io/1.0/index.html),
    - policy: componenetごとに書く、ファイル名は*.spec.ts*
    - home.spec.tsに、describeから書くこと
    - serviceクラスがシンプルに、依存なし方が良い
    - TypeScript：型がある、Objectの中身
    - テスト環境：jasme, karam..angularと一緒
    - angular毎回読み込み、ionicはbeforeを用意する
    - ionic独自のモジュール
- Native機能、[ionic Native](https://ionicframework.com/docs/native/)
  - [usage native module](https://facebook.github.io/react-native/docs/native-modules-ios.html)
  - テストも同様
- sample application: k-kuwahra

- まとめ：
  - 書いたほうがよい
  - angularのテストを真似

## ionic + cordova アプリを自動運用するために:
- [slide](http://slides.com/karageageta/ionic-20170806#/)
- [Hibee](https://itunes.apple.com/us/app/hibee-%E3%83%8F%E3%82%A4%E3%83%93%E3%83%BC-%E6%97%A5%E8%A8%98%E3%82%A2%E3%83%AB%E3%83%90%E3%83%A0-%E5%A5%BD%E3%81%8D%E3%81%AA%E3%83%A2%E3%83%8E%E3%82%B9%E3%82%AF%E3%83%A9%E3%83%83%E3%83%97%E5%B8%B3/id1174172088?mt=8) 自動デプロイ
- Purpose
- How?
- [Crashlytics](https://try.crashlytics.com/) アプリのクラッシュ収集・解析
- Circle CI 複数のjobを定義できる circleの設定ファイル
- setup and install
- [Fastlane](https://github.com/fastlane/fastlane)
  - 各ツールactionをまとめる
  - Deploy iOS のcircle.yml
  - Fastfile ios
  - circle CIのMac OSs
  - build-extraをコピーする必要
- Hibeeを開発／運用
  - 一つのcodeで両方対応
  - 開発速度が早い
  - デザインの自動度が高い
  - プロ読書んビルド足質くはことも多い
  - ES2015多用時、端末依存のバグが
  - 実機デバッグがしづらい
  - 各OSの最新版を使えない

- Native or Hybrid?
  - OS固有の機能を使いたい　Native
  - サクッと両方OS作りたい Hybrid

## アンチパターン

- npm install -g sadf
- ionic
- cordova(https://cordova.apache.org/): モバイルOSで押すと、webviewを起動する
- npm run build --prod
 - オプションをつけたら、JItコンパイルが走って低速
 - 今晩環境でのbuildが行けない
- ionic cordova build --prod
  - ionicでAotコンパイルして、Cordovaでラッピングして、書き出す
  - アプリ配布作業は面倒なんですが、androidで、unsigned.apk
  - ionic 自社用など、レジのアプリなど
  - ionic services


## Ionicと[GraphQL](http://graphql.org/)とのお話

- demonstration
  - ionicの
- [GraphQL](http://qiita.com/bananaumai/items/3eb77a67102f53e8a1ad)
  - githubが標準4, 参照実装はJavascrip
  - single Endpoint
    - 独自のquey言語
    - webpocketが使う
  - demand driven architechture
    - 使う側が要求する(sqk, sparql)
  - mobile and DDA
    - mobile側で提供する
  - schema system
  - Caveat n + 1 問題、セキュリティ
  - フィールドを一つ一つ指定する分、フロントの実装負荷が高い

  - Pros: APIの性能とリソース設計の両面、周辺ツール作りやすい
- 統合
  - Facebook Relay
  - Apollo
  - backend as a service
    - firebase functionでGraphQL service
    - serveless =+ GraphQL
    - Aws上での
    - graphcool, ts-graph

- 概要、モバイルとの組み合わせに
  - Baasも登場
  - [Apollo](https://alligator.io/angular/getting-started-graphql-apollo/)の定義もできる

## [wpionic.tokyo](https://wpionic.tokyo/)
 - もくもく形式
 - wordpressの標準スキル
 - [wordcamp tokyo 2017](https://2017.tokyo.wordcamp.org/)

## ハマったところ
 - appをつくる
 - chat
 - modalController


## Q&A：
- IOSでDeployした時は、遅い
  - 感じない、イベントを何で読んでいる
- Conponentの探し方(例えば：calendar)
  - [webcomponents.org](https://www.webcomponents.org/)で探す
  - [native plugins](https://ionicframework.com/docs/native/browser.html)

- cordovaのプラグイン
  - [ionic3](http://blog.ionic.io/ionic-3-0-has-arrived/) をつかってください
  - angularの最新情報
  - angularのバージョンニング、半年1回バージョンアップ
  - native

- prototypeを作るなら,Hybridをつくるならionic
- 参考リソース：[joshmorony](https://www.joshmorony.com/)、[cordovaプラグイン](https://cordova.apache.org/docs/ja/latest/guide/hybrid/plugins/)

