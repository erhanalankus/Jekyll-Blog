---
title: "Zarupa Core Devcamp Ders Notları (4. Gün)"
---

## 4. Gün (20. ve 24. saatler arası)

Bugünün gündemi bash ve vim idi, fakat başlangıçta package management konusunun üzerinden geçtik.

Uygulama kurarken version, description, nereye kuruluyor, paket bağımlılıkları var mı, paket bazı şeyleri kırabilir mi?

.deb dosyaları arşiv dosyları. zip değil ar kullanıyor.

apt-cache policy [paket adı]

apt show

lib ile başlayanlar library demek, executable'ları yok, uygulamalar bu library'leri kullanıyor.

suggests kısmında belirtilenleri de kursak iyi olur.

dpkg -l, sistemde kurulu tüm paketleri gösterir.
dpkg -L, paketin bileşenlerinin yerlerini gösterir.

/var/cache/apt/archives/ klasöründe yüklenmiş deb dosyaları saklanıyor

sudo du -csh /var/cache/apt/archives/ ile bunların diskte kapladığı yeri gördük.

Çekeceğimiz her şeyde sürüm çok önemli.

cat /etc/lsb-release ile sistem bilgilerimizi gördük
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=18.04
DISTRIB_CODENAME=bionic
DISTRIB_DESCRIPTION="Ubuntu 18.04.2 LTS"

/etc/apt/sources.list'de paketler için kullanılan kaynakları gördük.

Paketleri güncellemek için:
sudo apt update
sudo apt upgrade

Sunucuda kafamıza göre güncelleme yapmıyoruz.

vim'e ctags ekledik, metot isimlerini listeliyor, vs.

apt remove la paket kaldırınca leftoverlar kalıyor
configleri değiştirdiysen onlara ellemiyor
apt purge, configleri falan da siliyor

nginx çok hızlı. hız, her zaman birinci öncelik değil.

[Debian Sources List Generator](https://debgen.simplylinux.ch/)

POSIX üzerine konuştuk. Herkesin hemfikir olduğu bir sistem, kimse ortamı domine edemesin. Signal'ların, process'lerin vs. standartlarını belirliyor.

Cron'dan ayrı olarak Kernel'in bir scheduler'ı var.

htop'da f7 ile process'leri nice etmece. Bi uygulamayı daha önemli olarak işaretlemece, kaynak kullanım önceliği.

traceroute ile bi URL'e kaç HOP'ta gittiğimize baktık.

shell, POSIX'in ifade ettiği bir şey.

Bash nedir'in üzerinde durduk.

Environmental variable'lar uppercase olur.

echo $HOME dediğimizde HOME diye bi makrom vardı, bunu expand etmiş oldum.

cp, mv, ls falan bunlar hep GNU utility.

Bi dosyaya bash script yazdık, sonra onu komut yaptık(shortdate)

Bash Reference Manual üzerinde uzunca durduk. Tanımlara baktık. Control operatörlerine baktık.

&, fg, bg kullandık. Ctrl+Z ile stop ettik. jobs komutu ile arkada bişey kaldı mı kontrol ettik.

environment variable'a backtick içinde bir komut ataması yaparken komutu çalıştırmaya çalışıyor, komut hata vermezse atama gerçekleşiyor

paketler kurulurken uzun bi liste görüren iyi oku, hayır de
gnome env'a bi kde paketi kurmaya çaışırsan bilimum kde paketleri de yanında gelir

openvim.com

Vim üzerinde uzunca çalıştık

y,p copy paste
v ile seçmeye başldık
0 ile satırbaşına döndü
seçerken $ ile sona kadar götürdük
:x ile xinci satıra gittik
:set nu

multiple line insert
ctrl+v
down arrow
shift+ı
type
esc

search and replace: :%s/test/dombak./g

.bashrc gibi .vimrc var, buradan tüm dosyalarda nu olsun yapabiliriz
oraya set nu yazdık, oldu
yanlış bişey yazarsak vim açılırken uyarır

/ ile search ettik. n, shift+n ile next/previous yaptık.

vim'in plugin yöneticileri olduğuna değindik.

Bu seferki notlar biraz özensiz oldu, kusra bakmayın.

Sevgiler,

Erhan