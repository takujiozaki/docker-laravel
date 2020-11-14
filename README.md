# docker-laravel
## テスト用 Laravel6 コンテナ
##  構築&起動
```
$ git clone git@github.com:takujiozaki/docker-laravel.git
$ cd docker-laravel
$ docker-compose up -d --build
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