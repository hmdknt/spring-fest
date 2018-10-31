# Spring Data RestとSprint Cloud Contract

## メモ


###　背景
・FrontendとBackendでチームが分かれる
・リポジトリも違う
・CICDのサイクルも別
・別々のデプロイ環境

・FrontendとBackend側でのコミュニケーションが必要になった。

#### 解決策
・restの仕様は、Spring Data REST

・バージョンアップしても壊れない仕組みSpring Cloud Contract

###  Spring Data REST

・Entity-repository
　・Entryに対してのrestが作られる。（webのエンドポイント自動生成）

RESTスタイルな

・依存関係
　

・自動生成したものにリウエストを送ると、データ部とリンク部が返される

#### HATEOAS
・データ部の他にリンク情報が返却され、関連するリソースをたどることができる。
・
・

・リンクがあることで、フロントエンドのチームが仕様を知らなくてもエンドポイントのURIを叩くことができる
・次のアクションをリンクに追加することができる
・ビジネスロジックの流出を最低限にすることができる。（バックエンドで止めることができる）


ただし、
・CRUDのみしか生成されない


#### ビジネスロジックの実装パターン
・@ReposityryControllerはData Restの自動生成したものを Override


#### その他
・JSON SchemaからTypeScriptのコードを自動生成できる
・Hybernate Search


・ボイラープレートコード削除する
・RESTやHATEOASのr流行りの仕様を活用する
・FrontendとBackend側でやりとりが減った



### Spring Cloud Contract

・Test Pyramid(上に行くほどお金がかかかり、時間もかかる)
UI
Service
Unit

・モックに置き換える（どうやってチェックする、）
　・インターフェースは正しい
　・連携するサービスが変更されたら
　・誰がメンテナンスするか？

・microservieだとモックの数も増える

・

#### CDC(Consumer driven contract)
Contract
　・契約はインターフェース定義のようなもの
　　・API仕様書の内容
　・Provider

##### CDCステップ
Integration testの代わり

Consumer()
1. テストを書く
　　レスポンスを定義する
  2, Pact file(Contract)
  3. Pact Broker(contractを共有) に Pact fileをpublish (Groovy)
  　・pact Brokerはどのサービスと連携しているのかをビジュアルかできる

Provider(server side, api server)
  1. Pact Broker からContract(Pact file)を取得
  2. Testを自動生成（Spring Cloucd Contract）
  3. モックを自動生成（Spring Cloud Contract）


・Pact Brokerのステータスを見ればConsumer側のAPIが実装されたかわかる
・Consumer側の間違いが簡単にわかる
・PactfileからAPI仕様が見れる

#### Pact
Integration testを