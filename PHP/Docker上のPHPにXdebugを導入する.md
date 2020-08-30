## Docker上のPHPにXdebugを導入する

DockerfileでXdebugをインストール
```
RUN pecl install xdebug && docker-php-ext-enable xdebug
```

php.iniの設定内容
```
xdebug.idekey="PHPSTORM"  // 識別しやすい値ならなんでもOK
xdebug.remote_enable = On
xdebug.remote_autostart = On
xdebug.remote_connect_back = Off
xdebug.remote_host = "host.docker.internal" //dockerコンテナから見たホスト(ローカル)マシン
xdebug.remote_port=9001  //9000はPHP-FPMのデフォルトとかぶる
```

## 参考
* [PhpStormとXdebugでステップ実行 ①ステップ実行するための設定 - Qiita](https://qiita.com/haruna-nagayoshi/items/99fa041e884c2c3975d2)
  * >Name, Host は識別のための名前なのでどんな名前でもOKです。
  * Hostは正しいホスト名でないと動かいと思われる  
* [[PHP] Xdebug のリモートデバッグ、理解していますか？ - Qiita](https://qiita.com/castaneai/items/d5fdf577a348012ed8af)