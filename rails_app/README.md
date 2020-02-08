# このrailsアプリの概要

下記のコマンドで作成したRailsアプリです。

```shell
$ rails new rails_app --database=postgresql --skip-action-mailer --skip-action-text --skip-active-storage --skip-action-cable --skip-javascript --skip-turbolinks --skip-test
```

[config/database.yml](https://github.com/ikedakohei/v_docker_tutorial/commit/4d8a5dd790a267930d0a6290c783501c54a8a81d)をDocker環境で動くように編集しました。

[Dockerfile](./Dockerfile)と[docker-compose.yml](./docker-compose.yml)を追加しています。
