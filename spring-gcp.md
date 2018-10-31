#  SpringとGCPの素敵な関係

## メモ

### GCP
#### メリット
・スケール感
　・youtube とか動いている環境にサービスを持ち込める
・ネットワーク
　・ファイバーの投資に30%投資している。（インフラに投資）
・Googleの最新のサービスを利用できる
　・1billionユーザを扱うには、今までなかったものを自分たちで作って運用している。
　・ biodata, kubernetes orchestra

・GCP
　・Compute Engine(GCE)
　・Kubernetes Engin(GKE)  java関連あり
　・Cloud Functions(GCF)  java関連あり
　・AppEngin　java関連あり
　　・最初はpython   (C, C++, java , python, Go)
　　・2008年にリリース
　　・コードファースト
　　　　・システム構築、管理負荷を最小化する
　　・No-OPs
　　・

#### フレキシブルとスタンダードの違い
AppEngin

・フレキシブル
　・中身はVM
　・時間がかかる
　・制限はない
　・スケール対応が微妙

・スタンダード
　・使えるライブラリに制限あり
　・スタンダードを

・第２世代ランタイム
　・Javaであれば第２世代

・appEngineにJettyを使っているのでwarをdeployする必要がある
・GCP supportを入れるとGCPに簡単につながる


#### AppEngineの使い方
・AppEngineのプラグインを入れる(maven)
・appengine:deploy


・AppEngineのバージョン
　・トラフィックの割り当てを変えることができる
　　・バージョンのコントロールを簡単にできる
　　
・AppEngineはコンテナのようにプロセスが立ち上がるため、スケールアウトがすぐに行われる
・課金に対しても有効に使える（スケールアウトしてからスケールダウンした時のタイムラグはあるが使っていない）

#### Kubernetes Engine
　・コンテナオーケストレータ
　・デファクトスタンダード
　・どこでも動く

　・GCPの上で動いている
　・Zero-Ops


　・ワーカノード
　　・オプションあり
　　　・オートスケール
　　　・

### GAEとGKEどのように使うのか？
・GKE
　・内部でVMが動いている
　・kubernetesの環境を作るのが簡単
　・kubernetesはコンテナ化されているのが条件
　・コンテナはpodsの中に管理されている。
　・外部と繋げる時は、expose


### その他
GCPは３００ドル

AppEngine:28instance/h

Google Cloud platform

Cloud donair

