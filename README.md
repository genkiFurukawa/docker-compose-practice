# docker-compose-practice
## はじめに
ローカル開発環境で細かい手順書を作るのがめんどくさい+手順書が腐る現実に対面したため、dockerで一発で動くようにしたい。
mysqlとnginxの設定をできるだけ簡略化することを目的とする。

## ファイル構成

```
├── docker
│   ├── mysql
│   │   ├── Dockerfile
│   │   ├── conf.d
│   │   │   └── my.cnf #追加設定したいconfig
│   │   ├── data #データ永続化のためのディレクトリ
│   │   ├── initdb.d
│   │   │   └── schema.sql #初回ビルド時に実行されるSQL
│   │   └── log #ログの出力先
│   └── nginx
│       ├── Dockerfile
│       ├── conf.d
│       │   └── default.conf #追加設定したいconfig
│       └── images # 画像保存先
├── docker-compose.yml
```
