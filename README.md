# Rust Hello World

## Contents

- [Rust Hello World](#rust-hello-world)
  - [Contents](#contents)
  - [Install](#install)
  - [Hello World!](#hello-world)
  - [How to use Cargo](#how-to-use-cargo)

## Install

```bash
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

ターミナルを開き直して``rustc``コマンドが実行可能になった

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
