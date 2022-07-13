<h1 align="center">Sei Network I atlantic-1 </h1>

![image](https://user-images.githubusercontent.com/101149671/178675500-886f53a3-45b7-48aa-ade4-2fb01d26d3ee.png)

<h1 align="center"> Selamlar herkese, sistem gereksinimleri hakkında olsun, ücretsiz sunucu olsun, Sei'nin geleceği olsun biraz uzun bir açıklamada bulunacağım herkesin faydası için, dikkatli okumanızı öneriyorum. </h1>

## Bahsi geçecek olan ücretsiz sunucu: [Flood Linki](https://forum.rues.info/index.php?threads/kamatera-uecretsiz-hesap-olusturma-ve-sei-icin-sunucu-kiralama.2139/)

Öncelikle, Sei için 1 ay boyunca sistem gereksinimlerini karşılayacak bir sunucu ayarladık 1 ay boyunca burada Sei network'ü kurup rahatlıkla çalıştırabilirsiniz.

Sei Network 9 hafta sürecek, 1 aylık sunucu bu.. diye sorabilirsiniz, şöyle;

- Sizler sei network için gerekli işlemleri, görevler, güncellemeler vs. yaptıktan sonra testnetin geri kalanında "yüksek ihtimalle" validator çalıştırmanın anlamı kalmayacak. Hatta ekibin söylediğine göre 5 günlük aktif set süresinde gerekli bir çok işlemi yapabilcek durumda olacağız.

Tamam rues hocam iyi hoşta Ahmet Sei bugün kurdu, sunucusunun 2. haftasında, testnetinde 2. haftasın gerekli işlemlerini yaptı ve Sei ile işi bitti. Peki ya Mehmet'in sırası 4 haftalık sunucu çalıştırma süresi içersinde gelmezse?

- Normal şartlarda bir çok kişi yüksek sunucu ücretleri verip bu testnete dahil olacaktı, çok çok sunucu biterse daha sonra taşıma işlemi ile devam edebilir, burada seçenek yine sizlere kalmış, zaten elinde sunucusu olan benim dediğim olayı umursamasına gerek yok, paylaşacağım sunucuyu başka testnetlerde kullanır. Örnek quai.

Burada tercih size kalmış, ben bireysel değil toplu olarak düşünmek zorundayım, beni bekleyin acele etmeyin derkende bunlardan bahsediyordum, bir çok kişi ücretsiz kullanıcak. 

Ee hocam ben sei için 3 aylık almıştım contabo 400 gb en küçük paketi o olur mu?

- Yukarıda bahsettiğim şartlar altında olur, yani bizim 4-5 günlük işimiz sürer ve daha sonra validatoru kapatırsak (öyle duruyor) yeterli olur kısmen. çok ucu ucuna arada derede bir konu :) 8 ram / 16 ram sıkıntısını sei-chain-2'de yaşamıştık burada sunucu yükseltip yükseltmemek size kalmış.

Veya o sunucuyu başka testnette kullanıp Kamatera 1 aylık ücretsize sei kurabilirsiniz.. Bunların hepsi tercih.

# Minimum gereksinimler ekibin söylediği ve tavsiye ettiği
```
4 CPU
16 RAM
500 SSD NVMe
```

# Benim tavsiyem yok, yukarıda senaryoları anlattım farklı bi durum yaşanırsa belirtirim, bu şartlar ve sunucular  yeterli olur diye düşünüyorum, sorun olursa:

Sei Network Türkiye Grubu: https://t.me/SeiNetworkTurkish

Sei Network Discord: https://discord.gg/gxBxGGcv

# Kurulum:
```
wget -q -O sei.sh https://api.rues.info/sei.sh && chmod +x sei.sh && sudo /bin/bash sei.sh
```

# Cüzdan oluşturmak için. walletName kısmına kendi cüzdan isminizi yazın:
```
seid keys add walletName
```

# Eskiden katıldıysanız (gentx'de cüzdan oluşturmuştuk) recover:
```
seid keys add walletName --recover
```
# Cüzdanımızı oluşturduktan sonra faucet'ı kullanalım: 

!faucet + adres komutu ile

![image](https://user-images.githubusercontent.com/101149671/178693732-5cd4d18f-1336-4c90-9f86-54df603f4e4d.png)

# Token alırken nodumuz eşleşiyordu, kontrol için:
```
seid status 2>&1 | jq .SyncInfo
```

# Böyle bir false çıktısı aldıysanız validator oluşturalım:

![image](https://user-images.githubusercontent.com/101149671/178694049-1023fb98-92d7-4a42-a202-5abcd121756e.png)

# Validator oluşturma, Moniker ve From gibi kısımları kendinize göre uyarlayın:
```
seid tx staking create-validator \
--moniker="RuesValidator" \
--details="https://linktr.ee/ruesandora0" \
--website="https://forum.rues.info/index.php" \
--amount=950000usei \
--pubkey=$(seid tendermint show-validator) \
--chain-id=atlantic-1 \
--commission-max-change-rate=0.01 \
--commission-max-rate=0.20 \
--commission-rate=0.10 \
--min-self-delegation=1 \
--from=rues \
--yes
```

# Validator oluşturma komutunu girdikten sonra en altta tx'i alıp kontrol edelim buradan: https://sei.explorers.guru/

![image](https://user-images.githubusercontent.com/101149671/178698389-2bb7e595-57b3-4b5a-b76c-33e65f0895fb.png)

# Succes yazarsa işlem tamam, geriye kaldı  benım duyurularımı beklemek :)

![image](https://user-images.githubusercontent.com/101149671/178698491-739de8e4-4d5c-43b6-afbb-cd10fc921149.png)


# Peer listesi ve peer paylaşımı:

[peers](https://forum.rues.info/index.php?threads/sei-network-atlantic-1-peer-listesi-olusturuyoruz-sizde-destek-olabilirsiniz.2144/)


# Hesaplar:

[<img src="https://cdn-icons-png.flaticon.com/512/733/733579.png" width="16px"> Twitter   ](https://twitter.com/Ruesandora0) 

[<img src="https://cdn-icons-png.flaticon.com/512/1336/1336494.png" width="16px"> Forum   ](https://forum.rues.info/index.php)

[<img src="https://cdn-icons-png.flaticon.com/512/2111/2111646.png" width="16px"> Telegram Announcement   ](https://t.me/RuesAnnouncement)

[<img src="https://cdn-icons-png.flaticon.com/512/2111/2111646.png" width="16px"> Telegram Chat   ](https://t.me/RuesChat)

[Discord](https://discord.gg/ruescommunity)







