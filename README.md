# bookers2-4
## DMM WEBCAMP 2ヶ月目応用課題

### 課題5 検索機能を追加しましょう

#### ①Bookers2に検索機能を追加しましょう
ヘッダー下部に検索窓を設置し、入力と一致する名前のユーザー・投稿を検索しましょう
##### 実装する機能
* コントローラ
* searchコントローラ追加
* searchアクション追加 用途：検索を行う
* ビュー
* ログインしている場合に限り、ヘッダーに検索窓・検索ボタンを設置すること
* 検索結果表示画面を作成し、検索結果を表示すること
* 検索対象(ユーザーか投稿か)の選択かをプルダウンメニューで選択できること

#### ② ①に検索手法を追加しましょう
##### 実装する機能
* ビュー
* 完全一致, 前方一致, 後方一致, 部分一致の検索手法をプルダウンメニューで選択できること

## 使用言語
Ruby on Rails

## 使用方法
### テスト手順の自動化
gemを入れて、specファイルを移動して、テストを実行するコマンドを打つという手順をまとめたcheck.shというファイルを作成した
アプリケーションのルートディレクトリにおいて
bash check.sh
というコマンドを打つと最後まで自動で終了する
ディレクトリが野原のディレクトリにあっているため、自分で修正が必要

### 実行コマンド
bundle exec rspec spec/ --format documentation

### 注意
カラム名が違うとほとんどのテストに失敗してしまうが、このコマンドですべてのファイルの文字列を変更することができる
例はopinionというカラム名で作られていたため、それをすべてbodyというカラム名に変更した
find . -type f | xargs sed -i 's/opinion/body/g'

一回テストを試していると、テスト用のデータベースtest.sqlite3ができているため、カラム名を変更したのちに再びやる時は
rm db/test.sqlite3によって、ファイルを削除してから実行する


## 参照
[DMM WEBCAMP カリキュラム](https://web-camp.online/lesson/curriculums)

