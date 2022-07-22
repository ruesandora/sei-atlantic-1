 <h1 align="center">Sei Network ACT 1 görevleri</h1>

## Selamlar arkadaşlar bugün Sei network, atlantic-1 testnetinin, ACT1 görevlerini yapacağız, aşığaya yapacağımız görevler ve puanlarını sıralıyorum:

EN ÖNEMLİSİ BUNLARI YAPMAK İÇİN AKTİF SETE GİRMENİZ GEREKMİYOR, GİRDİĞİNİZ ZAMAN UPTİME VE JAİLE DİKKAT EDERSİNİZ.

* Redelege görevi - Uptime'ı minimum %75'ün üstünde olan, örnek ben %95'im, redelege yapmak: (5 PUAN)
* IBC Transfer, herhangi bir Cosmos ağına IBC transfer yapılacak. (30 PUAN)
* Validatör çalıştırmak - AKTİF SET ŞART DEĞİL (40 PUAN)
* Oylamaya katılmak (5 PUAN)
* Hata bildirme (20 PUAN)
* Katkıda bulunmak (PUAN BELLİ DEĞİL)
* Jail olmamak, uptime %0'a düşerse jail olursunuz (Uptime Ağdan kopmak) (20 PUAN)
* Slah olmayın, (Slah, ağdan atılmak, kimse atılmaz zaten) (5 PUAN)
* Uptime belli bir yüzdenin altına düşmemek, o yüzde (%) testnet sonunda belli olacak ağın durumundan dolayı. (50 PUAN)

Not: Şimdi görevlerimize başlayalım, hala kurmadıysanız Sei Node kurabilirsiniz, telegram: https://t.me/SeiNetworkTurkish

# Redelege görevi:

Bu redelegeyi kendi validatorünüzden başka bir validatöre redelege ediceksiniz. (tırnak işaretlerini kaldırın)

```
seid tx staking redelegate <KENDİvalidatörADRESİN> seivaloper1654kj35pszp4t49wcglwcg0cwlxg5vvwevaltm 5000usei --from=<CüzdanAdın> --chain-id=atlantic-1
```

# IBC Transfer:

Not: Burada istediğiniz cosmos ağına gönderebilirsiniz: Örnek cüzdan, osmosisxxx.. kujiraxxx, secretxxx, stafixxx.

```
seid tx ibc-transfer -y transfer transfer channel-77 <diğer ağ adresi> 20usei --chain-id atlantic-1 --from <cüzdan_adı>
```

# Oylama görevi:
```
seid tx gov vote 3 yes --from rues --chain-id atlantic-1
```

# CW20 IBC TRANSFER GÖREVİ:

* https://junomint.com/ üzerinden keplra juno ağı ekliyoruz
* https://faucet.roguenet.io/ üzerinden token alıyoruz.
* Keplr ayarlar kısmından IBC transferi aktif ediyoruz. 
* select chainden - New IBC transfer channel diyelim
* Sei testneti seçelim
* channel id kısmında channel-32 yazalım
* sei testnet cüzdanımızı kopyalayıp yapıştırıyoruz transfere
* Kısaca juno'dan IBC transfer ile junox gönderımı yapıyoruz ve böyle bir görsel çıkıyor:
* Gönderim yaparken sembolik bir küsüratlı sayı gönderin, terminalde belli olsun.
* okla işaretlediğim şu an yaptığımız token
* okla işaretlediğim tokenin üstünde ki token dün ki flood yapmayan varsa: https://github.com/ruesandora/CW20-ICS20-Smart-Contract/blob/main/README.md

![image](https://user-images.githubusercontent.com/101149671/180287685-55212c12-0ac2-4702-950f-6000f6b9440b.png)

# Şimdi sei'ye geçmesi 5-10dk sürmüştür, sei'den geri juno'ya atalım.

* Komut alltta ki gibi ancak siz bu komutu göndermeyin çünkü bu benim cüzdanım, size komutun altında anlatacağım şimdi.

```
seid tx ibc-transfer -y transfer transfer channel-5 juno1654kj35pszp4t49wcglwcg0cwlxg5vvwua7utk 50000ibc/1F7826C2682AA476F4AB378D70B72D1272F30CEF6D0597F30CE6AAF3158170A1 --chain-id atlantic-1 --from rues
```

### Altta ki komutu girerek cüzdan da ki tokenleri görüntülüyoruz.
```
seid q bank balances seicüzdanadresi
```

# Bu komutu terminalde girdikten sonra altta ki görselde ki gibi çıktı alacaksınız.

* amount yazan kısım token adeti.
* denom yazan tokenin adı, örnek usei, uquick, upaloma yazmamız gibi.

![image](https://user-images.githubusercontent.com/101149671/180288487-2bea66c5-3aae-4273-9b8a-88962779a229.png)

## Şimdi size yukarıda verdiğim IBC transfer komutunu alın ve sırasıyla:

* 1 . kısım göndereceğiniz juno adresi veya testnet adresi.
* 2 . kısım 5000ibc/xxxx ile başlıyor fark ettiyseniz.
* 5000 yazan token adeti (usei veya junox yazmıyoruz zaten ibc ile başlayan token adı demiştim)
* token adetini belirleyip birleşik bir şekilde denom kısmında yazan 5000ibc/xxxxx adresini yazın, komutun sonunda from kısmını değişin sizin cüzdanınız olsun.

```
seid tx ibc-transfer -y transfer transfer channel-5 juno1654kj35pszp4t49wcglwcg0cwlxg5vvwua7utk 50000ibc/1F7826C2682AA476F4AB378D70B72D1272F30CEF6D0597F30CE6AAF3158170A1 --chain-id atlantic-1 --from rues
```

### görevleri teyit etmek için txhası sei explorerden aratın succes desin, juno içinde https://testnet.mintscan.io/juno-testnet burdan aratın en altta succes yazar.

# BU GÖREVLER TAMAM ŞİMDE AXELAR GÖREVLERİNE GEÇELİM.


* Axelar üzerine gidelim: https://testnet.satellite.money/ 
* Görselde ki gibi ethereum ağından sei'ye seçelim. (sei yeni eklendı yoksa bin takla atılmış  versiyonla flood yazmıştım boşa gitti .d)
* Seiye ethereum'dan wETH atalım. wETH'niz yok mu?
* https://app.uniswap.org/#/swap?chain=ropsten üzerinden eth'yi çevirin.
* ETH'niz yok mu?
* Hadi onuda ben yapim hadi, alın ropsten eth faucet: https://is.gd/ropsten :))
* Sei testnet cüzdana gönderelim. 

![image](https://user-images.githubusercontent.com/101149671/180289691-e86438d3-84c5-441c-bf54-fd51b11344b1.png)


* Gelmesi uzun sürebilir ama gelir:

![image](https://user-images.githubusercontent.com/101149671/180291700-25bdbab4-52c9-4b90-8ab1-9e06c924a941.png)


# Şimdi bu ethereumu yukarıda yaptğımız gibi farklı bir cosmos'A atalım, örnek juno osmo stafi vs.



# FORM konusuna dönelim:

* Form https://docs.google.com/forms/d/1qxpIL-ATe1HMX87w1P7BjMqpjXExlKyo1_btEJi00JM/viewform?edit_requested=true
* Burada doldurmanız gerekenler belli tx hasları not ettık IBC transferlere sırasıyla txhashları vs. yapıştırabilirsiniz.
* Completed mission: sorusuna yaptığınız görevlerden birisini ingilizce yazın.
* tx hash kısmına da yaptığınız ıbc transferlerden 1 tanesını eklesenız yeterli.
* son soru screenshot, orasıda size kalmıs yapmadıysanı ağ dışında bir işlem boş bırakın.



<h1 align="center">İŞLEMLER BU KADAR..</h1>

