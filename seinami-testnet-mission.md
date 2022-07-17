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
seid tx staking redelegate "KENDİvalidatörADRESİN" seivaloper1654kj35pszp4t49wcglwcg0cwlxg5vvwevaltm 5000usei --from="CüzdanAdın" --chain-id=atlantic-1
```

# IBC Transfer:

Not: Burada istediğiniz cosmos ağına gönderebilirsiniz: Örnek cüzdan, osmosisxxx.. kujiraxxx, secretxxx, stafixxx.

```
seid tx ibc-transfer -y transfer transfer channel-77 "göndereceğiniz ağ adresi" 20usei --chain-id atlantic-1 --from "rues"
```

<h1 align="center">Diğer görevler başladıkça ve güncelleme geldikçe eklenecektir, contabo sıkıntısı çıkmasa 1 görev daha ekleyecektim, sıkıntı yok 22 Temmuz son gün, 5 günümüz var.</h1>

Devamı..
