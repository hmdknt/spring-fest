# 基礎からのOauth2.0とSpring Security5.1による実装

## メモ

### Oauth2,0
#### Oauth2.0基本用語
・認可の流れを規定したプロトコル
・認証プロトコロルOpenIDConnct

・アクセストークン（ヘッダー）
・スコープ
・パスワードだと全ての権限を扱える
・アクセスとーくんんだと

#### 登場人物
・ リソースオーナー
　　情報の持ち主
・リソースサーバ
　　情報を保持するサーバ
・クライアント

・認可サーバ

####  アクセストークンの取得方法
・認可コード
　認可サーバから認可コードをもらいクライアントは再度認可サーバに再度送る

・インプリシット

・リソースオーナーパスワードクレデンシャル

##### 認可コードの必要性
・アクセストークンがブラウザに渡らない
　クライアントと認可サーバとのやりとりしかない

・認可部分は開発者が作る部分（決まりはない）
・

#### アクセストークンを利用したリソースアクセス

リソースオーナ->  クライアント




・アクセストークンを送る部分の決まりごとはない
　リクエストヘッダにアクセストークンを入れることぐらいしか決まりがない

#### アクセストークンやスコープの検証方法
・
・
・

#### JWT(JSON Web Token)
・アクセストークンの形式の一種
・アクセストークン自身にユーザ情報やスコープ


##### 構造
・ヘッダー
・ペイロード
・電子署名（認可サーバの秘密鍵で暗号化されている）


#### JWK(JSON Web Key)
・認可サーバの公開鍵の元となる情報が含まれる
・認可サーバからJWKSet形式(JWKの配列)で取得する

#### JWTの弱点と対策
弱点
　・アクセストークンの剥奪が不可能

対策
　・有効期限を短くする

### 認可サーバ(5.2以降)
・4.x 以前は姉妹
　新規機能の追加はなし

・5.0
　Oauth2.0の機能を新規機能として追加

 ### 対応情報
・クライアント ：


### 認可サーバを作る
・Spring Security

・keycloakを使う


#### keycloak



### Spring Security5.1


ログイン画面
/oauth/authorization//<provider >


#### ログアウト



####　リソースサーバ
Oauth2-resoutce-

hasAuthority(“SCOPE_read”)








