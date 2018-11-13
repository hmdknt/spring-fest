# Augularを用いたデザインスプリント開発と設計手法

## メモ

### Web Application Design

- Webサイトとの違い  
  - 入力のしやすさなどを求める（Webデザイナー）


- Atomic Design
  - 細かい部品を作成する。（全体から細かい部品へ、その後細かい部品から全体に戻る）
  - 再利用性を意識する。
  - サイトをコンポーネントとして捉える
　
### Design Sprint

#### デザインカンプ
- 画面設計書のこと
- システムテストやシナリオテストもデザイナーが行なっている。（デザイナーが確認しないのはおかしいため）
- 成果物
  - 要件定義書
  - シナリオテスト仕様書
  - 機能テスト仕様書
- ヒアリング → ワイヤーフレーム

### Web Components
- Custom Elements ピースに名前をつける
- HTML Templates　ピースに模様をつける
- HTML Imports　ピースをパズルに取り込む
- Shadow DOM　ピースの独立性を保つ

#### Cuntom Elements
- 意味のあるものを自分で定義する。（x-をつける）

#### HTML Imports

#### Shadow DOM
- タグの中で使用するCSSを分けることができる。

### Scoped CSS

### JavaScript Framework
- Angularはscopedcssを持っていて、CSSに対して独立性を持たせることができる。
- Vue.js はScopedCSSは持っているが、Shadow DOMは持っていない？
- WebApplicationFrameworkはAngularとVue
- ReactはどちらかというとJavaScriptFramework

### DevOps for Front-end

### Wb Applicaiton Implementation

### A Comparsion 
