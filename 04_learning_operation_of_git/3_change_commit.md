### 3. コミットを変更する操作
- 歴史を戻る
  ```
  $ git reset --hard ハッシュ
  ```
  - 作業のログを確認する
    ```
    $ git reflog
    ```
    logは過去のみだが、reflogはlogで表示されない部分も確認できる

- コンフリクト（競合）を解消
  - 表示される内容
    ```
    <<<<<<< HEAD
      現在のブランチのHEAD
    =======
      マージしようとしているブランチの内容
    >>>>>>> ブランチ名
    ```
    解消できたあとは、addとcommitを行う

- 直前のコミットメッセージを修正
  ```
  $ git commit --amend
  ```

- 歴史を押しつぶして改変
  ```
  $ git rebase -i HEAD~2
  ```
