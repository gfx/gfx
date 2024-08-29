# 職務経歴書

## Fastly 2019-09 ~ current - Senior Software Engineer

### リバースプロキシの開発・運用

CDNで使われるリバースプロキシ（HTTP server, ベースはOSSのh2o ）の開発・保守・運用をしています。私は主に保守・運用よりです。このリバースプロキシはC言語で書かれており、周辺ツールがGo, Python, Perl, Ruby, shell scriptなどで作られています。

FastlyのCDNでは、このリバースプロキシがユーザーの すべてのリクエスト を HTTP/1, HTTP/2, HTTP/3 (+TLS) で受け、バックエンドのキャッシュサーバやエッジコンピューティングサーバへプロキシします。リバースプロキシに問題があるとあらゆるユーザーに影響が出ます。このため、よい意味で緊張感のあるプロダクト開発を行えていると思います。

実際に日々行っているのは次のようなことです。実際には「運用」でリソースのかなりの割合を使っています。

* **運用**: CI/CDの整備・自動化
  * CircleCIからGitHub Actionsへの移行
  * GitHub ActionsによるCIの構築・保守・改善
  * Code coverage計測システムの構築
* **運用**: リリースエンジニアリングの自動化・ツールの整備
  * changelogの自動生成
  * upstreamの取り込みの自動化
  * パッケージング時のパッケージ検証の強化
  * Canaryリリースの対象ノードをデプロイ前に確認できるツールの開発
  * 安定してリリースできるようリリースエンジニアリングの詳細に関する議論
* **運用**: 障害対応・障害時の問題切り分け
  * 日々起きる障害の一時対応
* **運用**: Linterの整備・改善
  * Linterのメンテナンス
  * 新しいルールに関してチームの合意形成・設定
* **運用**: Observabilityの保守
  * Prometheusによるdashboardの改善
  * ロギングまわりのリファクタなど
* **運用**: セキュリティ
  * h2oに組み込まれたLinux seccompロジックの保守
  * 依存関係の継続的なアップデート
* パフォーマンス分析基盤の開発（未完）
  * h2oのログ基盤の開発（h2olog）
  * QUIC用のパフォーマンス分析フレームワークQLogによる分析基盤の開発
* サービスの新機能の開発
  * h2oとC製ミドルウェア（Varnish）との通信を必要とする新機能
  * h2oとRust製ミドルウェア（Fastly Compute）との通信を必要とする新機能

使用技術: C, HTTP, Go, Python, Perl, Ruby, shell script, Rust, GitHub Actions, Prometheus, Linux, BigQuery

## Bit Journey, Inc. (2016-08 ~ 2019-09) - Software Engineer

### 社内情報共有サービスKibelaの開発・運用

社内情報共有ツール Kibela (https://kibe.la/) （2017年3月1日 正規リリース）の開発を行っていました。

サーバーサイドはRailsアプリケーションです。マルチテナント・ウェブアプリケーションとして、サブドメインごとにPostgreSQLのschemaによって名前空間を分けている構成です。マルチテナンシーのあたりはやや癖がありますが、それ以外はごく普通のRailsアプリケーションでした。

ウェブフロントエンドはReact + TypeScriptを採用しており、ビルドツールとしてはwebpackを使っていました。フロントエンドのビルドは私が入社した当初はbrowserifyだったのですが、このビルドが非常に遅く、webpackのほう開発用のビルドサーバで差分ビルドができて高速ということでwebpackに移行しました（2016年）。その後もwebpackビルドは安定して稼働しています。

Reactコンポーネントはサーバーサイドレンダリング（SSR）をしています。SSRは Hypernova (https://github.com/airbnb/hypernova ) によるレンダリングサーバ（NodeJS製）によるもので、UX向上のために導入しています。このあたりは私が進めたので、Rails + React + SSRについてはかなりノウハウがたまりました。

全文検索はElasticsearch 5.xです。導入は私ではありませんが、全体的なリファクタやインデックスの再設計、スコアリングの調整などは私が主導しました。このサービスではElasticsearchを全文検索だけでなくランキング（個人用のランキング、全体のランキングともに）にも使用しており、そのあたりの設計もやっています。ランキングは当初RedisとPostgreSQLによる実装でしたが、Elasticsearchのスコア関数による柔軟なスコアリングが魅力的で、しかもElasticsearchを使うほうがずっとシンプルに実装できるということで移行を決定しました。

内部APIとしてGraphQLの採用もしており（2017年）、ReactやTypeScriptと相性がよいこともありフロントエンドの開発環境としてはかなりやりやすい状態です。

またその他、細かい機能は自ら企画・実装・デプロイ・運用をしています。たとえば、PlantUMLをレンダリングする機能は、その企画から レンダリングサーバ ( https://github.com/bitjourney/plantuml-service Kotlin製 )の開発、インフラの整備などすべてやりました。MathJaxの導入やsyntax highlight engineの置き換え（pygments.rbからrougeへの置き換え）も行いました。

使用技術: Ruby on Rails, React, TypeScript, GraphQL, Elasticsearch, PostgreSQL, PlantUML, Redis, Docker, AWS

## Cookpad, Inc. (2013-08 ~ 2016-08) - Software Engineer

### レシピサービスのAndroid版の開発

使用技術: Java, Android SDK, SQLite

### レシピサービスのWeb版の開発

使用技術: Ruby on Rails, MySQL, AWS

## ConnectLink, Inc. (2013-03 ~ 2013-07) - Software Engineer

### Androidアプリの開発

使用技術: Android SDK

## DeNA Co., Ltd. (2011-04 ~ 2013-02) - Software Engineer

### スマートフォン用ゲームエンジンの開発

使用技術: JavaScript, Java, Objective-C, C++

### コミュニケーションアプリの開発

使用技術: Objective-C, Perl

## 趣味領域

### Perl用の高速なテンプレートエンジン Xslate (2011年頃)

https://github.com/xslate/p5-Text-Xslate

実質的にフルスクラッチで開発したプログラミング処理系です。XSというPerl用ネイティブ拡張用の言語（C + Perl API）で書かれています。速度にフォーカスしており、Perlのテンプレートエンジンの中でも当時最速といっていい水準でした。

### Android用のO/R mapper Orma (2016年頃)

https://github.com/maskarade/Android-Orma

Android向けのO/R mapperです。クエリビルダーAPIのコード生成や自動マイグレーションなどの機能を持ちます。趣味で開発したものながら当時の自社アプリに採用するなどしました。

### JavaScript向けのMessagePack library (2019年頃)

https://github.com/msgpack/msgpack-javascript

MessagePackのJavaScript/TypeScript実装です。このライブラリはMessagePackプロジェクトの公式実装となるべく、仕様に忠実でかつ高速な実装を目指しています。
