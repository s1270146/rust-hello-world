# Rust Hello World

## Contents

- [Rust Hello World](#rust-hello-world)
  - [Contents](#contents)
  - [Install](#install)
  - [Naming Rules](#naming-rules)
  - [Hello World!](#hello-world)
  - [How to use Cargo](#how-to-use-cargo)
  - [Different from other languages](#different-from-other-languages)

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