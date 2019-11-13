---
title: "Zarupa Core Devcamp Ders Notları (10. Gün)"
---

## 10. Gün

Selam,

Bugün büyük ödevlerimizin sunumlarını yaptık. Konular şöyle idi:

- Relative & Absolute Paths
- Wget & Curl
- Netcat
- Ansible
- Library Management in Programming Languages

<br>

Wget'te user agent bilgisini değiştirebileceğimizi, kendimizi herhangi bir browser'mış gibi tanıtabileceğimizi gördük.

http://www.networkinghowtos.com/howto/change-the-user-agent-in-wget/

https://www.whatsmyua.info/

Kullandığımız araçlar zeki olmayan, basit araçlar. Bu araçlara ihtiyaçlarımızı doğru söylememiz önemli.

Proxy'lerden bahsettik. Bunlar aralardaki vekiller. Bir kaynağa ulaşmak isterken uğradığımız bir vekil, bize istediğimiz bilgiyi dönebilir. İnternet, devasa bir proxy'ler cenneti. CDN'lerden bahsettik.

Netcat ile hangi port açık, hangi port kapalı incelemeleri yaptık. Portun açık-kapalı olmasının ne demek olduğunu sorguladım. O port üzerinden gelen isteği dinleyen bir uygulama var ise, o port açıktır gibi anladım ama bu tam doğru değilmiş. Öğrenilmeli.

FTP'den bahsettik. Debian'ın şu adresine `(ftp.tr.debian.org/debian)` hem FTP, hem HTTP ile ulaşabiliyoruz. HTTP ile ulaşırken port 80'de çalışmakta olan web sayfası ile muhattap oluyoruz. FTP ile ulaşırken bir arayüze ihtiyaç duymuyoruz.

`cat /etc/services | grep ftp` komutu ile FTP portunu gördük.

tcpdump'ı kurcaladık.

`tcpdump -D`

`sudo tcpdump -i wlp2s0`

komutları ile ağ trafiğini gözlemledik.

Promiscuous Mode'dan bahsettik. Biz bu moda geçirmediysek ve ağımızı bu durumda görürsek hacklenmişiz demektir.

`curl icanhazip.com` komutu ile IP adresimizi gördük. IP adresinden başka hiç bir şey dönmemesi güzel.

whoishostingthis.com sitesiyle oynadık.

`sudo tcpdump -n -c 50 -i wlp2s0 arp` komutu ile ARP oynamacaları yaptık. Bunu fazla yaparsak firewall bize karşı aksiyon alabilirmiş.

Programlama dilleri için ortak package manager olan asdf'ye göz attık.

Kısaca Vagrant'ı hatırladık.

PyCharm yükleme sorunlarıyla uğraştık.

Git üzerinde bolca çalıştık.

<br>
Sevgiler,