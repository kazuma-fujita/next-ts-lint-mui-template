# About Next.js/TypeScript/ESLint/Prettier/Material-UI/styled-components Template.

Next.js/TypeScript/ESLint/Prettier/Material-UI/styled-components の自作テンプレートを作りました。

テンプレートは以下のコマンドでどなたでもご利用可能です。

```
yarn create next-app --example "https://github.com/kazuma-fujita/next-ts-lint-mui-template" sample-app
```

テンプレートには以下 package が含まれます。

- Next
- React
- TypeScript
- EsLint
- Prettier
- Material-UI
- styled-components

TypeScript/ESLint/Prettier を個別に設定されたい方は以下ファイルをそれぞれ調整してください。

- TypeScript
  - `tsconfig.json`
- Prettier
  - `.prettierrc.json`
- ESlint
  - `.eslintrc.json`

また、テンプレートに含まれるサンプルのソースコードはデフォルトで `src` ディレクトリ配下にあります。

ソースコードの import 文は `src` ディレクトリからの絶対パスで記述出来るように設定していますので、詳細はこちらの記事を参照ください。

[React の import 文を絶対パスで設定する(TypeScript 版) ](https://zuma-lab.com/posts/typescript-import-absolute-path-settings)

## 自作テンプレート作成手順

ここからは自作テンプレートを作成した時の作業手順です。

備忘録として残しておきます。

### 環境

- macOS Catalina 10.15.5(19F101)
- VSCode 1.52.1
- Next 10.0.5
- React 16.14.0
- TypeScript 4.0.5
- yarn 1.22.4

## テンプレートを作成する

`yarn create next-app` で今回公開する `next-ts-lint-mui-template` という名前の雛形を作成します。

今回はあらかじめ TypeScript が設定された `with-typescript` テンプレートを流用します。

```
yarn create next-app --example with-typescript next-ts-lint-mui-template
```

雛形が作成されたら、 `yarn dev` でアプリケーションを起動し、 [http://localhost:3000](http://localhost:3000) を開いて Next の初期画面が表示されることを確認します。

## src ディレクトリの作成

`create next-app` した初期状態では `src` ディレクトリがありません。

`src` ディレクトリを作成して他の階層を `src` ディレクトリに移動します。

この作業は好みですが、CRA で開発をする時は基本プロダクトソースコードを `src` ディレクトリ配下に置くので、慣例として実行します。

```
cd next-ts-lint-mui-template && mkdir src && mv components interfaces pages utils src/.
```

## import 文を src ディレクトリからの絶対パスに設定する

こちらに詳しい設定方法の記事を書きましたので参照ください。

[React の import 文を絶対パスで設定する(TypeScript 版)](https://zuma-lab.com/posts/typescript-import-absolute-path-settings)

## ESLint/Prettier を設定をする

こちらに詳しい設定方法の記事を書きましたので参照ください。

[TypeScript のプロジェクトに ESLint と Prettier を併用して VSCode の保存時に自動フォーマットをする](https://zuma-lab.com/posts/eslint-prettier-settings)

## Material-UI/styled-components を設定する

こちらに詳しい設定方法の記事を書きましたので参照ください。

[Next.js/TypeScript プロジェクトに Material-UI/styled-components を対応させる](https://zuma-lab.com/posts/next-material-ui-styled-components-settings)

## Github に作成したテンプレートを push する

Github に public repository を作成します。

今回は `next-ts-lint-mui-template` という名前にしました。

ローカルリポジトリに リモートリポジトリを追加します。

```
git remote add origin git@github.com.zuma:kazuma-fujita/next-ts-lint-mui-template.git
```

通常は `git flow init` などで develop ブランチを作成し、main ブランチ read-only にしますが、今回は割愛して直接 main に push します。

```
git push origin main
```

Github の public repository に置くだけでテンプレートの公開は完了です。
