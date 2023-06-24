# 🗄️ ディレクトリ構造

本PJでは`src`ディレクトリ配下において、以下のようなディレクトリ構造となります。（随時更新予定）

```sh
src
│
├── components/
│   ├── ui-elements/　※Atomicデザインでいうところのatoms（機能横断的な最小単位ui）
│   │   └── Button/
│   ├── ui-parts/ ※Atomicデザインでいうところのmolecules（機能横断的な最小単位uiの集合体）
│   │   └── FieldCheckbox/
│   ├── functional/ ※featuresに属せないものがあれば作成
│   └── layouts/
│       └── Header/
│
├── consts/ 機能横断的な定数を定義
│
├── features 機能毎にディレクトリを作成
│   ├── todos/
│   │   ├── components/
│   │   │   ├── TodoItem/
│   │   │   └── TodoList/
│   │   ├── hooks/
│   │   ├── functions/
│   │   ├── api/
│   │   ├── test/
│   │   ├── pages/
│   │   └── recoil/
│   └── projects/
│
├── hooks/ 機能横断的なhooksを定義
│
├── libs/ 各種ライブラリの設定ファイルを定義する
│
│── pages/　※ルーティングのみが責務
│   ├── index.tsx
│   └── login.tsx
│
├── styles/ create-next-appで作成されたディレクトリ（現在は使用していない）

```

## Key Points

- 運用ルール策定における重要な視点は以下3点
    - 新メンバーでも直感的にすぐ理解できる
        - 新しくcomponentを作るとき、どこに分類させるかで迷わない
    - テストやリファクタしやすいシンプルな構成
        - 運用中、作成済みのComponentの分類先の移動がなるべく発生しない
        - フォルダ間の依存関係を定義することで、複雑な依存を発生させづらくする
    - 開発の快適さを保てるレベルの運用ルールにする
- 機能変更や追加、削除時に関連する`components`や`functions`を直感的に理解できるように`src/features`を1stカット（区分）に採用
- 機能横断的なコンポーネント（最小単位〜モジール）やレイアウト、ページ`src/components`に格納
- `src/pages`ディレクトリが必要なのはNext.jsの仕様であり、今後Nest.jsがどうなるかわからないため、`src/pages`ディレクトリの責務はルーティングのみにし、`src/features/projects/pages`ディレクトリにページの実態はもたせる