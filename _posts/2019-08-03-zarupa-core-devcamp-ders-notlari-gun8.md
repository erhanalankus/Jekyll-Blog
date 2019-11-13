---
title: "Zarupa Core Devcamp Ders Notları (8. Gün)"
---

## 8. Gün (44. ve 52. saatler arası)

Bugün docker ile haşır neşir olduk.

Kendi makinalarımızda mantıklı bir dosya hiyerarşisi, bir directory yaratma stratejisi oluşturmamız iyi olur.

~/development
~/work

mkdir komutu ile /x/y/z gibi bi klasör yaratacaksak, y klasörü yoksa onu da yaratsın diye -p kullanabiliriz.

$ ne demek idi? Shell prompt demek idi.

docker run -it hello-world komutunu girdik, açıklamalarını okuduk. -it demezsek daemon olarak çalışıyor, bir şey görmüyoruz.

docker images komutu ile görüyoruz, docker ps ile görmüyoruz, çünkü çalıştı kapandı. docker ps -a ile görebiliyoruz.

docker search redis deyince docker hub'da search ediyor.

Anlamadığımız imajı kullanmamamız gerekiyor.

docker run yaparken name'i ilk parametre olarak kullanmalıyız.

[bash-it](https://github.com/Bash-it/bash-it) yükledik. bash ile çalışmayı çok kolaylaştırıyor.

bash-it show aliases

bash-it enable alias docker

BASH_PREVIEW=true bash-it reload komutu ile bash-it theme'lerine göz attık.

[Brave web browser](https://brave.com/)'ı övdük.

[Daemon](https://en.wikipedia.org/wiki/Daemon_(computing))'un ne olduğunu hatırladık.

Bilgisayarda systemd ile çalışan servisler var. systemd, servisleri çalıştırıyor.

systemctl list-unit-files &#124; grep enabled

dbus, interprocess communication'ı sağlıyor.

VM'i pull ettim, build ettikten sonra yapmam gereken şeyler için ENTRYPOINT'i kullanıyoruz.

DNS, Language, Timezone variable'ları çok önemli!

ENTRYPOINT ile VM tamamen kurulduktan, build olduktan sonra yapılacak ayarlar ve kurulacak paketler işlenir.

LABEL önemli.

overlay2, filesystem'i yönetmek için.

Container'larla oynamak diski hemen doldurur, ayık ol.

json_pp

sudo visudo dedik, açılan dosyaya
erhan ALL=NOPASSWD: ALL
girdik, artık sudo x dedikten sonra şifre girmemize gerek yok.

Bir ebedi gökçe belik kitabını okuyacağız.

HOSTPORT:CONTAINERPORT. Soldaki host'a ait, sağdaki container'a ait.

portainer, bizim makinedeki containerlar, ıvır-zıvırlar için güzel bir kullanıcı arayüzü sunuyor.

https://raft.github.io/

Markdown'ı kullanacağız.

zR ile vim'de unfold all yaptık.

virbr0, virtual bridge 0 demek.

loopback:
hiçbiyere bağlı değil
devnull gibi bir şey
sadece kendisini referans gösteriyo
127.0.0.1
dışarıya açmak istemediğimiz hizmeti buna bindirecez

10, 172,192 ile başlayan ip adresleri subnet içlerinde

consul, consulate'ın kısaltılmışı, gözlemliyor, etcd kullanıyor, bilgilendiriyor.

DMZ. 80 ve 443 de-militarized zone

public-private network ayrımını unutma
ingress içeri, egress dışarı

http://jodies.de/ipcalc , subnet calculator.