# 職務経歴書

## Fastly 2019-09 ~ current - Senior Software Engineer

### リバースプロキシの開発・運用

CDNで使われるリバースプロキシ（HTTP server, ベースはOSSのh2o ）の開発・保守・運用をしています。私は主に保守・運用よりです。このリバースプロキシはC言語で書かれており、周辺ツールがGo, Python, Perl, Ruby, shell scriptなどで作られています。

FastlyのCDNでは、このリバースプロキシがユーザーの すべてのリクエスト を HTTP/1, HTTP/2, HTTP/3 (+TLS) で受け、バックエンドのキャッシュサーバやエッジコンピューティングサーバへプロキシします。リバースプロキシに問題があるとあらゆるユーザーに影響が出ます。このため、よい意味で緊張感のあるプロダクト開発を行えていると思います。

実際に日々行っているのは次のようなことです。おもに生産性の向上でチームに貢献しています。

* CI/CDの整備・自動化
  * GitHub ActionsによるCIの構築・保守・改善
* リリースエンジニアリングの自動化・ツールの整備
  * 安定してリリースできるようリリースエンジニアリングの詳細に関する議論、パッケージング時の検証の強化など
* パフォーマンス分析基盤の開発（未完）
  * h2oのログ基盤の開発
  * QUIC用のパフォーマンス分析フレームワークQLogによる分析基盤の開発
* 障害対応・障害時の問題切り分け
  * 日々起きる障害の一時対応
* Linterの整備・改善
  * Linterのメンテナンス
  * 新しいルールに関してチームの合意形成・設定
* Observabilityの保守
  * Prometheusによるdashboardの改善
  * ロギングまわりのリファクタなど
* セキュリティ
  * h2oに組み込まれたLinux seccompロジックの保守
  * 依存関係の継続的なアップデート
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

### レシピサービスのWeb版の開発

使用技術: Ruby on Rails, MySQL, AWS

### レシピサービスのAndroid版の開発

使用技術: Java, Android SDK, SQLite

## ConnectLink, Inc. (2013-03 ~ 2013-07) - Software Engineer

### Androidアプリの開発

使用技術: Android SDK

## DeNA Co., Ltd. (2011-04 ~ 2013-02) - Software Engineer

### スマートフォン用ゲームエンジンの開発

使用技術: JavaScript, Java, Objective-C, C++

### コミュニケーションアプリの開発

使用技術: Objective-C, Perl
