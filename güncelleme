# Sei network oylama sonrası güncelleme.

### sırayla komutları girelim ve loglar aksın.

```
cd $HOME

sudo rm sei-chain -rf

git clone https://github.com/sei-protocol/sei-chain.git

cd sei-chain

sudo systemctl stop seid

git checkout master && git pull

git checkout 1.0.6beta-val-count-fix

make install


sudo cp /root/go/bin/seid /usr/local/bin/seid

sudo systemctl restart seid

sudo journalctl -u seid -f -o cat
```
