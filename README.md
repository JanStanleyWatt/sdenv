# sdenv

sdenvは、ウェブアプリケーションではないウェブサイトを開発するためのベストプラクティスに基づいて構成されたフロントエンド開発環境です。やりすぎないちょうどいい使い勝手の実現を念頭に置いて設計されている、より多くのウェブサイト開発者のためのツールキットです。

次のツールを採用しています:

- [Astro](https://astro.build/): ウェブサイト構築のためのフレームワーク
- [Tailwind CSS](https://tailwindcss.com/): ユーティリティファーストCSSフレームワーク
- [Alpine.js](https://alpinejs.dev/): HTML上に直接振る舞いを記述できるJavaScriptフレームワーク

sdenvを利用するに当たっては、これらのツールの使い方を理解している必要があります。理解が不十分な点があれば、それぞれの公式ドキュメントなどを参照してください。

そして、これらのツールを快適に使用できるように、[ESLint](https://eslint.org/)、[Prettier](https://prettier.io/)、[VSCode](https://code.visualstudio.com/)の設定が組み込まれています。

## 開発用コマンド

依存パッケージのインストール:

```bash
npm ci
```

ローカルサーバーの起動:

```bash
npm run dev
```

本番用ビルド:

```bash
npm run build
```

自動テスト:

```bash
npm test
```

ソースコードの静的検証:

```bash
npm run lint
```

ソースコードの静的検証および自動修正:

```bash
npm run lint:fix
```

## ディレクトリ構成

```
.
├── @types/             # 依存パッケージ用の型定義
├── public/             # ビルドによって加工されないアセット
├── src/                # メインのソースコード
│   ├── client/         # クライアントサイドで利用されるソースコード
│   │   ├── components/ # Alpine.jsのコンポーネント
│   │   └── stores/     # Alpine.jsのストア
│   ├── components/     # Astroコンポーネント
│   ├── content/        # Astroのコンテンツコレクション
│   ├── layouts/        # ページの構造を規定するAstroコンポーネント
│   ├── pages/          # ページと対応するAstroコンポーネント
│   └── styles/         # Tailwind CSSで読み込まれるCSSファイル
├── astro.config.ts     # Astroの設定
├── package.json        # 依存パッケージを管理するための設定
├── tailwind.config.cjs # Tailwind CSSの設定
├── tsconfig.json       # TypeScriptの設定
└── vitest.config.ts    # Vitestの設定
```

詳しくは、Astro公式ドキュメントの「[Project Structure](https://docs.astro.build/en/core-concepts/project-structure/)」も参照してください。
