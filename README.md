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

3. Composer install と 依存関係解決

   ```
   $ docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
   ``` 
   https://laravel.com/docs/9.x/sail#installing-composer-dependencies-for-existing-projects

3. Sail 起動

    `$ cd MyBBS && ./vendor/bin/sail up -d`

4. key generate

    `$ ./vendor/bin/sail artisan key:generate`

5. DB migrate (Freshデータ)

    `$ ./vendor/bin/sail artisan migrate:fresh`

6. 確認

    `http://localhost:8573`で確認する

## エラー対策

- ./vendor/bin/sail: Permission denied

    現在のUserは docker groupに入れる

    `$ sudo usermod -aG docker username`