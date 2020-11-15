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
http://127.0.0.1:10080/

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

## 参考にした記事
https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4