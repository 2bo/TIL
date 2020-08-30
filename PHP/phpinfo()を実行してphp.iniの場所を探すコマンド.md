# phpinfo()を実行してphp.iniの場所を探すコマンド

```php
php -r "echo phpinfo();" | grep "php.ini"
```

`-r`オプションで`<?php ?>`なしでphpが実行できる

## 参考
[もういい加減覚えよう。php.iniはどこにあるのか - Qiita](https://qiita.com/ritukiii/items/624eb475b85e28613a70)

xdebug.idekey=PHPSTORM
xdebug.remote_enable = On
xdebug.remote_autostart = On
xdebug.remote_connect_back = Off
xdebug.remote_host = host.docker.internal
xdebug.remote_port=9001
xdebug.profilier_enable=1
xdebug.remote_log=/var/log/xdebug_remote.log
