## 概要

掲示板システムです。

機能：
- Post の CRUD
- コメントの CRUD
- 書くPostは複数のコメントが持ちます。

レッスンのリンク:

[Laravel 8入門 基本機能編](https://dotinstall.com/lessons/basic_laravel_v3)

[Laravel 8入門 データベース編](https://dotinstall.com/lessons/basic_laravel_v3)

[Laravel 8入門 CRUD処理編](https://dotinstall.com/lessons/basic_laravel_crud)

[Laravel 8入門 リレーション編](https://dotinstall.com/lessons/basic_laravel_relations)






## 環境設置

1. Dockerをインストールする

2. プロジェクトをクローンする

3. Sail 起動

    `$ cd MyBBS && ./vendor/bin/sail up -d`

4. key generate

    `$ ./vendor/bin/sail artisan key:generate`

5. DB migrate

    `$ ./vendor/bin/sail artisan migrate`

6. 確認

    `http://localhost:8573`で確認する

## エラー対策

- ./vendor/bin/sail: Permission denied

    `$ sudo chmod -R 775 ./vendor`

- Nothing to migrate.  

    ```
    $ ./vendor/bin/sail artisan migrate:reset
    $ ./vendor/bin/sail artisan migrate:
    ```