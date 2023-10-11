### 1. hubコマンド
- 概要
  githubのコマンドを拡張させたもの

- セットアップ
  - インストール
    * Homebrew
      ```
      $ brew install hub
      ```
    * MacPorts
      ```
      $ sudo port install hub
      ```
    * その他
      ```
      $ curl http://hub.github.com/standalone -sLo ~/bin/hub
      $ chmod +x ~/bin/hub
      $ echo 'export PATH="~/bin:$PATH"' >> ~/.bash_profils
      ```
  - 動作を確認する
    ```
    $ hub --version
    ```
  - エイリアスを設定する
    .bash_profileなどのシェル設定ファイルに以下を追加
    ```
    eval "$(hub alias -s)"
    ```

- コマンド
  - クローン
    ```
    $ hub clone リポジトリ名
    ```
    ```
    $ git clone git@github.com:ユーザー名/リポジトリ名.git
    ```
  - リモートリポジトリと連携
    ```
    $ hub remote add リポジトリ名
    ```
    ```
    $ git remote add リポジトリ名 git@github.com:ユーザー名/リポジトリ名.git
    ```
  - 最新のデータを取得
    ```
    $ hub fetch
    ```
    ```
    $ git fetch リポジトリ名
    ```
  - 差分のコミットを取得して取り込む
    ```
    $ hub cherry-pick URL
    ```
    ```
    $ git remote add -f リポジトリ名 git@github.com:ユーザー名/リポジトリ名.git
    $ git cherry-pick ハッシュ
    ```
  - Fork
    他のユーザのリポジトリをcloneした後、自分のリポジトリにForkしたい時に以下のコマンドを利用
    ```
    $ hub fork
    ```
    ```
    $ git remote add -f ユーザ名 git@github.com:ユーザー名/リポジトリ名.git
    ```
  - Pull Requestを作成
    ```
    $ hub pull-request -b リポジトリ名:ブランチ名 -h リポジトリ名:ブランチ名
    ```
    Issueも同時にPull Request
    ```
    $ hub pull-request -i Issue番号 -b リポジトリ名:ブランチ名 -h リポジトリ名:ブランチ名
    ```
  - Pull Requestが送られた時に手元で確認する
    ```
    $ hub checkout URL
    ```
    ```
    $ git remote add -f -t ブランチ名 SSH
    $ git chekout --track -B ユーザ名-ブランチ名 ユーザー名/ブランチ名
    ```
  - 手元のリポジトリをGitHubにも作成 ※公開リポジトリ
    ```
    $ hub create
    ```
    ```
    (GitHubでリポジトリを作成)
    $ git remote add origin git@github.com:ユーザー名/リポジトリ名.git
    ```
  - 複数のリモートリポジトリへの同時push
    ```
    $ hub push リポジトリ名,リポジトリ名,リポジトリ名 ブランチ名
    ```
  - 現在操作しているリポジトリのブラウザ表示
    ```
    $ hub browse
    ```
    ```
    $ open URL
    ```
  - トピックブランチとmasterブランチの差分を表示する
    ```
    $ hub compare
    ```
    ```
    $ open https://github.com/ユーザ名/リポジトリ名/compare/ブランチ名
    ```
  - help
    ```
    $ hub help
    ```

- GitHub Enterprize
  ```
  $ git config --global --add hub.host my.example.org
  ```
  ※ my.example.orgをGitHub Enterpriseのホスト名に置き換える
