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


#全てのファイルをリモートリポジトリにアップロードしたい場合
git add .
git status
git commit -m "～～～"

#個別にアップロードしたい場合
git add -- "git使い方.md" "git使い方_photo" ←アップロードしたいファイルを選択
git status                                 ←アップロード予定のファイルを表示
git commit -m "手順書とその画像を追加"       ←ローカルリポジトリに変更を記録、コメントも付けられる

git add -- hello_world.py
git status
git commit -m "hello_world.pyを追加"

#アップロード先のリモートリポジトリのリンクをoriginという名前で登録
git remote add origin https://github.com/KoukiTsuda/github_tutorial.git

#masterブランチにアップロード
→ -uをつけると次回以降　git push　で同じ操作可能
git push -u origin master


master何？

#ローカルにリポジトリをダウンロードする方法
 git clone した場合、コマンドを実行した場所の中に、リポジトリ名のフォルダが作られる
 そのフォルダがリポジトリのルートになる
git clone https://github.com/KoukiTsuda/github_tutorial.git