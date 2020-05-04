# Ubuntu by Docker for mac
Docker for Macで作成したUbuntu環境です。

# セットアップ手順
1. `cp docker/.env.example docker/.env`
1. Dockerコンテナ内に対しての環境変数を設定する
1. `cd docker && ./script setup`
1. `docker/ssh/config`, `docker/ssh/id_rsa`に必要な情報を設定する
