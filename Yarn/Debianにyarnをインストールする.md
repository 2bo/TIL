# Debianにyarnをインストールする

```bash
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
```
## 参考
[インストール | Yarn](https://classic.yarnpkg.com/ja/docs/install/#debian-stable)