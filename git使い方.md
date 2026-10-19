git
ファイルの変更履歴を記録・管理するためのツール

github
https://github.com/
Gitで管理しているファイルや履歴をインターネット上に保存し、共有するためのサービス

gitのインストール
https://git-scm.com/install/windows

gitのインストール確認
git --version

#初期設定
「誰が変更を行ったかを記録する識別情報（名前・メールアドレス）」と
「WindowsとMac/Linux間の改行コードの差を自動調整するルール」の設定
git config --global user.name "KoukiTsuda"
git config --global user.email "tsuda.koki.kk@tut.jp"
git config --global core.autocrlf true

#設定変更の確認
git config --global --list



githubに自分のファイルをアップロードする方法

#初回

#ローカルパソコン上にGitリポジトリ(ローカルリポジトリ)を作成
→このコマンドが実行されたフォルダがリポジトリのルートになり、Gitの管理対象になる
git init

#GitHub上にGitリポジトリ(リモートリポジトリ)を作成
![左上の「New Rrepository」を選択](git使い方_photo\1.png)

![下の「Create Rrepository」を選択](git使い方_photo\2.png)

#ローカルリポジトリをリモートリポジトリにアップロードするための準備
git add .
git status

git add -- "git使い方.md" "git使い方_photo"
git commit -m "手順書とその画像を追加"