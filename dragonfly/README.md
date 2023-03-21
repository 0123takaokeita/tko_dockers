# USAGE
dragonflyのコンテナでbash起動
```
rake redis:bash
```

dragonflyのコンテナでcli起動
```
rake redis:bash
```

redis-cliで入ればキャッシュの状態もチェックできます。
```
docker exec -it dragonfly redis-cli
127.0.0.1:6379> set hello world
OK
127.0.0.1:6379> keys *
1) "hello"
127.0.0.1:6379> get hello
"world"
127.0.0.1:6379>
```

# NOTE
- `docker-compose.yml` で設定しているため port 番号など編集する場合は構成に合わせて修正してください。

