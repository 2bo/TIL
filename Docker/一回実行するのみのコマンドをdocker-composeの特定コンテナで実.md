# 一回実行するのみのコマンドをdocker-composeの特定コンテナで実行する

`docker-compose run --rm -w /workdir container command`

* `--rm`は実行後にコンテナを削除する。コマンド実行後はコンテナは不要になるので削除する
* `-w`はワークディレクトリを指定する

## 例-DockerでLarvelを動かしている場合にmigrateコマンドを実行する

```bash
# phpコンテナ上でphp artisanコマンドを実行
$ docker-compose run --rm -w /var/www php php artisan migrate
```
* `docker-compose exec php bash`で一度コンテナのbashに入らずに直接ローカルからコマンドを実行できる。
* コマンドが長いのでShellScriptにすると便利(参考:[goodwork/install.sh at master · iluminar/goodwork](https://github.com/iluminar/goodwork/blob/master/install.sh))
