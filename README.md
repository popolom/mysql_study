## このリポジトリの役割

dockerを使用して、PostgreSQL、MySQLの環境構築を行う
<br><br>
## 事前にダウンロードが必要なソフトウェア
- [Docker](https://chigusa-web.com/blog/windows%E3%81%ABdocker%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%97%E3%81%A6python%E7%92%B0%E5%A2%83%E3%82%92%E6%A7%8B%E7%AF%89/)
コンテナ仮想化技術を提供するプラットフォーム

- [`A5:SQL Mk-2`](https://a5m2.mmatsubara.com/)
汎用SQL開発環境/ER図ツール
<br><br>


## MySQL 構築の流れ
**MySQL**　※CMDでも可能<br>
イメージの入手
```bash
docker image pull mysql:latest
```
ボリュームの作成
```bash
docker volume create test_mysql_valume
```
コンテナの作成
```bash
docker container run -p 3306:3306 --name test-mysql -v test_mysql_valume:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=hogehoge -d mysql:latest
```
bashで起動
```bash
docker exec -it test-mysql bash
```
