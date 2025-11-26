# 🚀 my_flutter_skeleton

Flutter × Clean Architecture の “超”使いやすいスターターテンプレート

Flutter アプリの毎回の土台作りをなくしたい人のための  
**Mason brick ベースのスケルトンテンプレート** です。

「アプリ作りたい！でもフォルダ構成どうしよ…」  
「毎回同じディレクトリ作るの面倒…」  
→ **これ一発で解決！**

---

## 🎯 Features（このテンプレ作ると何が嬉しい？）

- 📦 **feature-first 構成で迷わない**
- 🧱 `data / domain / presentation` によるクリーンアーキ風のレイヤ分割
- 🔄 **UI・ロジック・データを完全に分離**
- 🌱 最初は空フォルダ（`.gitkeep`）だから好きに育てていける
- 🧩 共通処理は `core` や `services` に集約して再利用しやすい
- 🛠 他の Flutter プロジェクトにも簡単に流用可能

---

## 🗂 ディレクトリ構成（テンプレ展開後の `lib/`）

```text
__brick__/
  lib/
    app/            ← アプリのエントリポイント（MaterialApp・DI など）
    config/         ← API URL・Flavor 設定など
    core/           ← 共通処理（constants, utils, widgets, themes）
    features/
      auth/
        data/       ← API / Repository 実装・DTO など
        domain/     ← Entity・UseCase（ビジネスロジック）
        presentation/ ← UI（Widget / ViewModel）
        .gitkeep
      home/
        data/
        domain/
        presentation/
        .gitkeep
      profile/
        data/
        domain/
        presentation/
        .gitkeep
      services/     ← Firebase / LocalDB / Auth など横断的なサービス
        .gitkeep
  HELLO.md
  brick.yaml
  CHANGELOG.md
  LICENSE
  README.md
```


📌 **feature-first のメリット**

- 大規模アプリでも「画面ごと」で整理される
- 新しい画面を追加するときに迷わない
- 各機能の独立性が高く、テストしやすい

---

## 🛠 インストール & 使い方

### 1. Mason CLI をインストール（未インストールの場合）

```sh
dart pub global activate mason_cli
```

### 2. この brick を追加（ローカルパスから追加する例）

```sh
mason add my_flutter_skeleton --path ./my_flutter_skeleton
```

### 3. Flutter プロジェクトでスケルトンを展開

```sh
mason make my_flutter_skeleton
```

プロンプト例：

```
? app_name (MyApp) → ここにアプリの名前を入力！✨
```

---

## 🎨 カスタマイズのヒント

- ✨ **新しい機能を追加したい場合**

  - `features/` に `settings/` や `todo/` をコピペで増やすだけ

- 🧪 **テストしたい場合**

  - domain（UseCase）にロジック集めるとテストしやすい

- 🧩 **サービスを追加したい場合**

  - Firebase Auth / Firestore / Drift などは `services/` にまとめると Good

---

## 🧪 開発中に brick をプレビューしたいとき

```sh
mason make my_flutter_skeleton -o ./_example
```

→ `_example/` に展開されるので、
生成結果を見ながらテンプレートを調整できます。

---

## ❤️ このテンプレートが向いている人

- Flutter の構成を毎回考えたくない人
- アプリを量産したい人
- チームで統一された構成を使いたい人
- クリーンアーキテクチャを軽く採用したい人
- 共通ロジックを Core にまとめたい人

---

## 📜 ライセンス

本リポジトリのライセンスは `LICENSE` を参照してください。

---

## ✨ Author

このテンプレートは Flutter を快適に開発するために作られました。
改善案やアップデート案があれば issue / PR 大歓迎！

