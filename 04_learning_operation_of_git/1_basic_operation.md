### 1. 基本的な操作
- リポジトリを初期化
  ```
  $ git init
  ```

- リポジトリの状態を確認
  ```
  $ git status
  ```

- ステージ領域へファイルを追加
  ```
  $ git add ファイル名
  ```

- リポジトリの歴史を記録
  - 1行のコミットメッセージ
    ```
    $ git commit -m "コミットメッセージ"
    ```
  - 詳細なコミットメッセージ
    ```
    $ git commit
    ```
    * フォーマット
      1行目：コミットする変更内容の要約を1行で記述
      2行目：空行
      3行目以降：変更した理由や詳細を記述
  - コミットを中止する
    コミットメッセージをを書かずにエディタを終了させる
  - コミット後の状態を確認する
    ```
    $ git status
    ```

- コミットログを確認
  ```
  $ git log
  ```
  [![Image from Gyazo](https://i.gyazo.com/ccdf97da33b6386a185e40681bedbfbc.png)](https://gyazo.com/ccdf97da33b6386a185e40681bedbfbc)
  commit：コミットを指し示すハッシュ
  - コミットメッセージの1行目のみを表示する
    ```
    $ git log --pretty=short
    ```
    [![Image from Gyazo](https://i.gyazo.com/78485369e59a7c42659577ec0da48ebd.png)](https://gyazo.com/78485369e59a7c42659577ec0da48ebd)
  - 指定したディレクトリ、ファイルのみのログを表示する
    ```
    $ git log ファイル名
    ```
  - ファイルの差分を表示する
    ```
    $ git log -p
    $ git log -p ファイル名
    ```

- 変更差分を確認
  - ワークツリーとステージ領域の差分を確認する
    ```
    $ git diff
    ```
  - ワークツリーと最新コミットの差分を確認する
    ```
    $ git diff HEAD
    ```
    HEADは作業しているブランチの最新のコミットを参照するという意味
