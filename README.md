# docker-on-vagrant

## Windowsの場合VirtualBoxインストール後下記の対応が必要
1. "ネットワークと共有センター" を開く
2. "アダプターの設定の変更" を開く
3. "VirtualBox Host-Only Network #N" のプロパティを開く
4. "VirtualBox NDIS6 Bridged Networking Driver" にチェックを入れる
5. "インターネットプロトコル バージョン6(TCP/IPv6)" のチェックを外す
6. [OK] を押し、プロパティウィンドウを閉じる
7. "VirtualBox Host-Only Network #N" の右クリックメニューで「無効」にする
8. 再度、「有効」にし直す

## 以下の順番でコマンド入力いただけると完了いたします

### gitからvagrant環境構築用のファイル取得

```
git clone https://github.com/volcite/docker-on-vagrant.git
cd docker-on-vagrant
mkdir Docks
```
### vagrant起動

```
vagrant up
```

### 仮想マシンに入る

```
vagrant ssh
sudo groupadd docker
sudo gpasswd -a $USER docker
sudo systemctl restart docker
exit
```

### これで仮想マシンの構築は完了
