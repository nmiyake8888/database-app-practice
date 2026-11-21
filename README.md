# database-app-practice

## 概要
COACHTECH 教材 Tutorial 9-3「データベース操作ハンズオン演習」で作成した成果物です。
Laravelを使用して商品管理システムのデータベースを構築し、商品名・価格・在庫数・カテゴリを一覧表示する機能を実装しました。

## 使用技術
- PHP 8.2
- Laravel 10.x
- MySQL
- Laravel Sail
- Docker
- Blade
- マイグレーション、シーダー、クエリビルダ


## 学んだこと
- マイグレーションを使用して、テーブルやカラムの構成を定義し、データベースを構築する方法
- シーダーを使用して、テストデータをまとめてデータベースに登録する方法
- クエリビルダを使用してデータを取得し、コントローラーからBladeに渡して画面に表示するまでの流れ

## 動作確認
1. Dockerを起動する。
2. プロジェクトのルートディレクトリで以下のコマンドを実行する。
    - ./vendor/bin/sail up -d
3. マイグレーションとシーダーを実行する。
    - ./vendor/bin/sail artisan migrate
    - ./vendor/bin/sail artisan db:seed --class=ProductSeeder
4. ブラウザで以下のURLにアクセスする。
    - http://localhost/products
5. 商品一覧ページに5件の商品が表示されることを確認する。
6. 確認後、Dockerコンテナを停止する。
    - ./vendor/bin/sail down