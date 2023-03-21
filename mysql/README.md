# 構築時の環境

```
$ ruby -v
ruby 3.2.0 (2022-12-25 revision a528908271) [x86_64-darwin22]

$ docker -v
Docker version 20.10.21, build baeda1f
```

# 環境構築
`bin/` 配下に`env.sh`を配置することでそのスクリプトを先に実行してから
rakeタスクを実行するようにしています。
`env_sample.sh`を参考にして設定してください。

`MYSQL_ROOT_PASSWORD` は必須項目なので抜けているとコンテナのビルドで失敗します。

# 使いかた
mysqlコンテナはRakeタスクで起動できるようにしています。

rake タスクは一覧チェックで確認してください。
```
rake -T
```

コンテナが上がってなくても `db:cui` で立ち上げまで実行できます。
```
rake db:cui
```

# backup方法
TODO:

# restore方法
TODO:

# sample投入
