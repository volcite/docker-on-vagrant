# docker-on-vagrant

環境構築用ファイル群です

以下の順番でコマンド入力いただけると完了いたします

- gitからvagrant環境構築用のファイル取得

`git clone https://github.com/volcite/docker-on-vagrant.git`

`cd docker-on-vagrant`

`mkdir Docks`

- vagrant起動

`vagrant up`

- 仮想マシンに入る

`vagrant ssh`

`sudo groupadd docker`

`sudo gpasswd -a $USER docker`

`sudo systemctl restart docker`

`exit`

これで仮想マシンの構築は完了
