### 1. 利用する前の準備
- SSH Keyの設定
  ```
  $ ssh-keygen -t rsa -C "your_email@example.com"
  ```
  - id_rsa：秘密鍵
  - id_rsa.pub：公開鍵
- 公開鍵の登録
  SSH KeysのAdd SSH keyに公開鍵をコピペする
  - id_rsa.pubは以下のコマンドで参照
    ```
    $ cat ~/.ssh/id_rsa.pub
    ssh-rsa 公開鍵の内容 your_email@example.com
    ```
