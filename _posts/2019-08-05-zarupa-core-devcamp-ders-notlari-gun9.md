---
title: "Zarupa Core Devcamp Ders Notları (9. Gün)"
---

## 9. Gün (52. ve 60. saatler arası)

Selam,

<br>

Bugün docker ve python ile uğraştık. Network problemleri yüzünden çok ilerleyemedik.

IP adresleri ile ilgili konuştuk, bazı şeyleri tekrarladık. Bu konu üzerine çok fazla geldik, bu konuyu iyi öğrenmek lazım belli ki.
[https://study-ccna.com/classes-of-ip-addresses/](https://study-ccna.com/classes-of-ip-addresses/)

ping komutunu gördük, ttl: time to leave. Ping atarken http, https yok. Sunucularımızı saldırgan botlardan bir nebze gizlemek için sunucumuzda ping'i disable edebiliriz.

[dig](https://linux.die.net/man/1/dig) komutunu gördük.

Bir sunucuda, birden fazla ağ cihazı olabilir, birden fazla IP adresi olabilir. 0.0.0.0('a **bind**irmek) demek, tüm IPlerden hizmet versin demek.

[iana](https://www.iana.org/)'yı öğren,
[ripe.net/](https://www.ripe.net/),
/etc/services, konuyla ilgili

traceroute komutunu hatırladık, bir IP adresine kaç HOP'da gidebildiğimizi tekrar gördük. Bununla ilgili OSP, Optimal Shortest Path çalışmaları var.

Google Cloud, AWS free tier hesaplarını hazır et.

docker inspect

OOM killer, out of memory killer

[vmstat](https://linux.die.net/man/8/vmstat)

[/proc/meminfo](https://www.thegeekdiary.com/understanding-proc-meminfo-file-analyzing-memory-utilization-in-linux/)

egrep, yani grep -E, yani regex kullanarak grep yapmaca

"new domain extensions" arattık, eğlendik :)

Python için virtual environment'ların önemini anladık. İşimiz bitince deactivate ediyoruz.

Virtual environment kurmadan python library kurmuyoruz. Anaconda gibi *** şeyler kullanmıyoruz :)

[gunicorn](https://gunicorn.org/)'a baktık. Python WSGI HTTP Server for UNIX.

mongodb'den uzak duruyoruz.

[slideshare.net/kunthar](https://www.slideshare.net/kunthar), nosql veritabanları sunumu.

neo4j, coğrafi veri için iyi.

pip install wheel, adettendir :)

chroot bilmek önemli

[tig](https://jonas.github.io/tig/), git için konsolda kullanabileceğimiz bir görsel arayüz.

<br>

Bir hafta bayram arası verdik. Şimdiye kadarki konuları sindirmek için güzel bir fırsat.

Sevgiler,