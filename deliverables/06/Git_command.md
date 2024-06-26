# Git command
更新日：2024-06-21

### 目的
Gitを利用した開発ができる。

### Gitとは？
Gitはバージョン管理システム(VCS:Version Control System)の1つです。

### Gitの基本用語
|用語|意味|
|:--|:--|
|リポジトリ<br>(repository)|ファイルやディレクトリの状態を記録する場所。ローカルリポジトリとリモートリポジトリがある。|
|ローカルリポジトリ<br>(local repository)|自分のPCにあるリポジトリ。|
|リモートリポジトリ<br>(remote repository)|サーバーにあるリポジトリ。ネットワーク上に存在し、複数人でも管理ができる。|
|クローン<br>(clone)|リモートリポジトリをローカルリポジトリにコピーして作成すること。|
|フォーク<br>(fork)|他の人のリモートリポジトリを自分のリモートリポジトリにコピーすること。|
|プル<br>(pull)|リモートリポジトリの変更をローカルリポジトリに反映させること。|
|ワークツリー<br>(work tree)|履歴管理をするファイルがある場所のこと。|
|インデックス<br>(index)|コミットしたいファイル又はファイルの一部を登録する場所のこと。|
|ステージ<br>(stage)|ワークツリーからコミットしたいファイル又はファイルの一部をインデックスに登録すること。|
|コミット<br>(commit)|インデックスに登録してある変更対象をローカルリポジトリに反映すること。|
|リセット<br>(reset)|コミット前の変更をローカルリポジトリの状態へ戻すこと。ローカルリポジトリに限る。|
|ヘッド<br>(head)|作業対象となっているブランチ、コミットのこと。|
|チェックアウト<br>(checkout)|ヘッドを切り替えること。過去のコミットを対象にチェックアウトした場合、それをもとにコミットすることはできない。|
|プッシュ<br>(push)|ローカルリポジトリの変更をリモートリポジトリに反映させること。|
|プル<br>(pull)|リモートリポジトリの変更をローカルリポジトリに反映させること。|
|プルリクエスト<br>(pull request)|フォークしたリポジトリでの変更を、フォーク元のリポジトリへ反映するよう依頼すること。|
|ブランチ<br>(branch)|履歴管理を枝分かれさせてたもの。ブランチを使うことにより、複数の履歴を並列に管理できる。|
|フェッチ<br>(fetch)|リモートリポジトリに変更がないか確認すること。コンフリクトを防ぐ。|
|マージ<br>(merge)|異なるブランチの変更を反映させること。お互いの変更履歴が残る。|
|リベース<br>(rebase)|異なるブランチの変更を反映させること。変更履歴が片方に集約される。|
|コンフリクト<br>(conflict)|マージ対象の２ファイルで同じ箇所が変更されており、自動でマージができないこと。|

参考URL   
[Git 基本の用語集](https://qiita.com/toshi_um/items/72c9d929a600323b2e77)   
[完全初心者向けGit用語集](https://qiita.com/shinshingodmt/items/637cf9e5c6660509c460)   
[【Git・GitHub】用語のまとめ](https://zenn.dev/miya_akari/articles/13c718afa783fe)   

### ローカルの基本操作
 #### 初期化
 - ```$ git init```
 新しいGitリポジトリを初期化する。

 #### 記録
 - ```$ git add <file name> ```
    指定したファイルを次のコミットのためにステージングエリアに追加する。```<file name>```を"."とすると全変更ファイルを指定できる。

 - ```$ git commit -m "commit message"```
変更を保存し、メッセージを付けて記録する。

 #### 状況確認
 - ```$ git diff```
 作業ディレクトリとインデックスの差分を表示する。

 - ```$ git diff --staged```
 インデックスと最後のコミットの差分を表示する。

 - ```$ git status```
 作業ディレクトリとインデックスの状態を表示する。

 #### 履歴の確認
 - ```$ git log```
 コミット履歴を表示する。

 #### 元に戻す
 - ```$ git restore <file name>```
 ファイルの変更を取り消し、最後のコミットに戻す。

 - ```$ git restore -staged <file name>```
 インデックスの変更を取り消し、ファイルをステージ解除する。