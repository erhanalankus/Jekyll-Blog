---
title: "Zarupa Core Devcamp Ders Notları (Telafi 2)"
---

# Zarupa Core Devcamp Ders Notları
## Telafi 2 (İkinci 10 saatin 4 saate sıkıştırılmış telafisi)
Bugün, müfredatın aşağıda listelediğim kısımları üzerinde durmamız gerekiyordu, fakat zaman yetişmedi, eksik kalan kısımların telafisini zamana yaymaya karar verdik.

	1.7. Symbolic and hard links
	1.8. Compression and archiving
	1.9. Search and find
	1.10. Package management
	1.11. Process management
	1.12. Update, upgrade, backup
	1.13. Scheduled tasks

dmesg komutunu inceledik, bilgisayar açıldığından beri olan her şeyin oraya not düşülmüş olduğunu gördük. Daha sonra bilgisayara bir flash disk bağladığımızda onunla ilgili yapılmış işlemlerin oraya eklendiğini gördük.

[ACPI](https://en.wikipedia.org/wiki/Advanced_Configuration_and_Power_Interface) ve [AHCI](https://en.wikipedia.org/wiki/Advanced_Host_Controller_Interface)'den çok kısa bahsettik.

/etc/systemd/system/sysinit.target.wants 'a göz attık.

AHCI'nin buglarıyla community'yi hep üzdüğüne değindik.

whois komutuyla aldığımız bilgideki adresin, geolocation'a dair bir ipucu vermediğini belirttik.

/dev/ klasörünü inceledik. Oradaki device'ları gördük.

df -kh komutu ile makinamızdaki tüm partition'ları gördük.

man komutuyla manual'ı çağırdığımızda gelen sayfaları less ile görüntülüyoruz gibi bir şey söyledik.

D-Bus'ın interprocess communication(IPC) ile ilgili bir şey olduğunu söyledik. Şu linki incele: [https://dbus.freedesktop.org/doc/dbus-tutorial.html](https://dbus.freedesktop.org/doc/dbus-tutorial.html).

Disklere [UUID](https://en.wikipedia.org/wiki/Universally_unique_identifier) atandığını ve disklerin o UUID'ler ile tanındığını söyledik.

Her dosyanın SUID'si, SGID'si var gibi bir şeyler söyledik, tamamlamadık. Bu konu bana ödev verildi.

Konsolda iyi, ne yaptığını bilen kişiler olmamız gerektiğini konuştuk.

file /dev/sda komutu ile bunun bir block special (8/0) olduğunu gördük. Disk'e block device dendiğini söyledik.

ls /proc/ ile process'leri gördük.

Ctrl+K kısayolu ile cursor'ın sağını uçurabileceğimizi gördük.

cat /proc/partitions ile partition'lara göz attık.

sda, sdb şeklinde disk identifer'lar var. Bunlar eskiden hd ile başlıyormuş, şimdi sd ile başlıyor. sr0 ile cdrom sürücü veya benzeri drive işaret ediliyor. 

home klasörümüzü ayrı bir partition'a koyarsak işletim sistemine yapacağımız büyük değişikler, dosyalarımızı etkilemez.

RAM bitince diskteki SWAP alanı kullanılır. Bu alanda özel bir dosya sistemi kullanıldığı için hızlı çalışır.

Disk, aniden ulaşılamaz hale gelirse "kernel panic" durumu yaşanır.

[Loop Device](https://en.wikipedia.org/wiki/Loop_device) : is a pseudo-device that makes a file accessible as a block device.

Ctrl+W ile bir kelime silebiliriz.

mount komutu ile mount edilmiş her şeyi görürüz. Diskler için sda ve sdb'leri ara.

htop, çalışan processleri izlemek için güzel bir alternatif, yükledik.

mkdir ve touch ile bol bol oynadık, basit bir for döngüzü yazdık.

		for i in {01..20}; do touch file-$i; done;

Dosya isimlerinde boşluk, türkçe harf, '-' harici özel karakter kullanmıyoruz.

Klasörlerdeki parent-child ilişkilerini konuştuk. Bol bol cp yaptık. mv'nin recursion'a takılmadığını, -r eklemek gerekmediğini gördük.

Bash'te yazmakta olduğumuz satırda, bulunduğumuz klasörü gösteren kısmın solundaki kısma(bende erhan@erhan-Lenovo-Z50-70: olarak geçiyor) ps1 diyormuşuz.

Absolute ve relative path'ler üzerinde durduk.

tar kullandık. Arşivledik, açtık. tar'ın sıkıştırma yapmadığını, sıkıştırma yapmak için farklı sıkıştırma algoritmaları kullanabileceğimizi gördük. Bash'teki autocomplete'in bu kullanılmış algoritmaları hesaba katarak autocomplete yaptığını gördük.

Asla rm -rf yapmamamız gerektiğini söyledik. Linux'ta kullanıcı hareketleri regüle edilmez, bu güzel bir şeydir, ama dikkatli olmazsak makinamızı bozabiliriz.

ln 'ye bir göz attık. Symbolic link yaptık. Kaynak dosyayı silince, symbolic link'in broken state'e geçtiğini gördük.

history komutu ile Linux'u yüklediğimizden beri girmiş olduğumuz tüm komutları gördük. .bashrc'de HISTSIZE ve HISTFILESIZE'a üç sıfır ekledik.

[Command-line fuzzy finder](https://github.com/junegunn/fzf) yükledik. Ctrl+R ile eski girilmiş komutları arama kısmı çok daha lezzetli oldu.

env komutu ile environment variable'ları gördük.

Umarım önemli bir şey atlamamışımdır.


Sevgiler,

Erhan