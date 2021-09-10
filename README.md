# docker-laravel
## ローカル開発用 Laravel6 コンテナ
##  構築&起動
```
$ git clone git@github.com:takujiozaki/docker-laravel.git project_name
$ cd project_name
$ docker-compose up -d --build
```
コンテナに入り、composerをインストール
```
$ docker-compose exec app bash
# cd laravel/
# composer install
```
.envを編集  
データベース関連を修正

```
# php artisan key:generate
```

## 動作 アドレス
http://127.0.0.1:8080/

## コンテナの状況を確認
```
$ docker-compose ps
```
## 停止
```
$ docker-compose down
```
## 削除
```
$ docker-compose down --rmi all --volumes --remove-orphans
```

## validation 日本語化
```
# php -r "copy('https://readouble.com/laravel/6.x/ja/install-ja-lang-files.php', 'install-ja-lang.php');"
# php -f install-ja-lang.php
# php -r "unlink('install-ja-lang.php');"
```

## 認証
```
# composer require laravel/ui 1.*
# php artisan ui vue --auth
//必要ならnpmをインストール
# apt update
# apt install nodejs
# npm install
# npm run dev


## 参考にした記事
https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4  
https://qiita.com/ucan-lab/items/bd0d6f6449602072cb87
