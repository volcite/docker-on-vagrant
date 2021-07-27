# docker-on-vagrant

環境構築用ファイル群です

以下の順番でコマンド入力いただけると完了いたします

gitからvagrant環境構築用のファイル取得

`git clone https://github.com/volcite/docker-on-vagrant.git`

`cd docker-on-vagrant`

vagrant起動

`vagrant up`

docker環境構築用のファイル取得

`git clone https://github.com/volcite/docker-laravel.git`

仮想マシンに入る

`vagrant ssh`

`cd docks`

`cd docker-laravel`

`sudo groupadd docker`

`sudo gpasswd -a $USER docker`

`exit`

`sudo systemctl start docker`

`docker-compose build`

`docker-compose up -d`

`docker-compose exec resys_api_back bash`

`composer create-project --prefer-dist laravel/laravel lara-d "6.*"`

- docker-compose.yml変更

volumes:

./back-api

↓

volumes:

./back-api/lara-d

*front-apiも同様に



- apatch.confの変更

DocumentRoot ”var/www/html/”　→　DocumentRoot ”var/www/html/public”

数行下

Directory ”var/www/html/” →　Directory ”var/www/html/public”



`docker-compose down`

`docker-compose build`

`docker-compose up -d`

lara-dの.envを下記に変更

APP_URL=http://192.168.33.11

DB_HOST=mysql5.7

DB_PASSWORD=root

api-back
http://192.168.33.11

api-front
http://192.168.33.11:81

で立ち上がれば環境構築完了です
