# TODO アプリ
使われている技術
- [ransack](https://github.com/activerecord-hackery/ransack)
  - 参考サイト：https://qiita.com/nysalor/items/9a95d91f2b97a08b96b0
- Docker Rails
  - https://matsuand.github.io/docs.docker.jp.onthefly/samples/rails/

```
docker compose run web rails ---
```

# Docker
```
# オーナー変更
sudo chown -R 999:999 ./tmp/db
# パーミッション変更
sudo chmod 700 ./tmp/db
# 起動
docker compose up
```

# DB接続
```
docker compose run web db

=====================================

todo_development=# \dt
                   List of relations
 Schema |            Name            | Type  |  Owner   
--------+----------------------------+-------+----------
 public | active_storage_attachments | table | postgres
 public | active_storage_blobs       | table | postgres
 public | ar_internal_metadata       | table | postgres
 public | departments                | table | postgres
 public | schema_migrations          | table | postgres
 public | sections                   | table | postgres
 public | task_types                 | table | postgres
 public | tasks                      | table | postgres
 public | users                      | table | postgres
(9 rows)

todo_development=# \dt users;
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | users | table | postgres
(1 row)
```
