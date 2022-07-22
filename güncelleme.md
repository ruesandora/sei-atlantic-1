
# 836963. blok ulaşanlar 1.07beta-postfix güncellemesi yapsın !
```
cd $HOME
rm $HOME/sei-chain -rf
git clone https://github.com/sei-protocol/sei-chain.git
cd $HOME/sei-chain
git checkout 1.0.7beta-postfix
make install
mv ~/go/bin/seid /usr/local/bin/seid
systemctl restart seid && journalctl -fu seid -o cat
```



# Sei network oylama sonrası güncelleme. (eski)

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


```
wget -O go1.18.2.linux-amd64.tar.gz https://golang.org/dl/go1.18.2.linux-amd64.tar.gz
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.18.2.linux-amd64.tar.gz && rm go1.18.2.linux-amd64.tar.gz
echo 'export GOROOT=/usr/local/go' >> $HOME/.bash_profile
echo 'export GOPATH=$HOME/go' >> $HOME/.bash_profile
echo 'export GO111MODULE=on' >> $HOME/.bash_profile
echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin' >> $HOME/.bash_profile && . $HOME/.bash_profile
go version



cd
rm $HOME/sei -rf
git clone https://github.com/sei-protocol/sei-chain.git && cd $HOME/sei-chain
git checkout master && git pull
git checkout 1.0.6beta-val-count-fix
make install


go build -o build/seid ./cmd/seid
chmod +x ./build/seid && sudo mv ./build/seid /usr/local/bin/seid
mv ~/go/bin/seid /usr/local/bin/seid
mv $HOME/sei-chain $HOME/sei
systemctl restart seid
journalctl -fu seid -o cat
```
