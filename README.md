# Rust Hello World

## Contents

- [Rust Hello World](#rust-hello-world)
  - [Contents](#contents)
  - [Install](#install)
  - [Naming Rules](#naming-rules)
  - [Hello World!](#hello-world)
  - [How to use Cargo](#how-to-use-cargo)
  - [Different from other languages](#different-from-other-languages)
  - [Ownership](#ownership)
    - [領域](#領域)
    - [所有権規則](#所有権規則)

## Install

```bash
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

ターミナルを開き直して``rustc``コマンドが実行可能になった

## Naming Rules

- ファイル名: snake_case
- 関数名: snake_case
- 定数名: UPPER_SNAKE_CASE

## Hello World!

```bash
rustc main.rs
```

でコンパイルし実行ファイルが作成される

## How to use Cargo

``Cargo``は``Rust``のビルドシステム兼パッケージマネージャ

- ``cargo new <プロジェクト名>``でプロジェクト作成
- ``cargo build``でプロジェクトをビルド
  - ``./target/debug/hello_cargo``で実行
- ``cargo run``でプロジェクトのビルドと実行
- ``cargo check``でバイナリを生成せずにエラーがないかを確認できる
- ``cargo build --release``でリリースに向けたビルド

## Different from other languages

- 代入値を返さない
  - 例えば、Cなら``x = y = 6;``と書いて、``x``と``y``に``6``が代入される
  - 一方でRustでは``let x = (let y = 6);``であるとエラーになる
- if文で条件式に必ず論理値を与えないといけない

## Ownership

### 領域
- スタック
  - 固定サイズのデータを格納
- ヒープ
  - サイズ可変のデータを格納
  - 領域確保をallocateすると言う
- 比較
  - **アクセス速度**: スタック>ヒープ
- 関数が呼び出されたときに変数がスタック(or ヒープ)に格納される
- 関数の実行が終了すると覗かれる

### 所有権規則

- 各値は**所有者**(変数)と対応している
- 値に対し所有者は一つ
- 所有者がスコープから外れたら破棄

