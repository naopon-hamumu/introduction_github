### 2. ブランチの操作
- ブランチを一覧表示
  ```
  $ git branch
  ```

- ブランチの切り替え
  ```
  $ git checkout ブランチ名
  ```
  - ブランチに作成し、切り替える
    ```
    $ git checkout -b ブランチ名
    ```
  - 1つ前のブランチに切り替える
    ```
    $ git checkout -
    ```

- ブランチをマージ
  ```
  $ git merge ブランチ名
  ```
  - マージの歴史を残す
    ```
    $ git merge --no-ff ブランチ名
    ```

- ブランチを視覚的に確認する
  ```
  $ git log --graph
  ```
