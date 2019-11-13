---
title: "Zarupa Core Devcamp Ders Notları (Telafi 1)"
---

# Zarupa Core Devcamp Ders Notları
## Telafi 1 (İlk 10 saatin 4 saate sıkıştırılmış telafisi)
Bugün, müfredatın aşağıda listelediğim kısımları üzerinde durduk:

	0. Introduction
		0.1. Welcome!
		0.2. What is Free Software?
		0.3. Free Software philosophy
		0.4. A Brief history of GNU/Linux OS
		0.5. Software licenses
	1. GNU/Linux for Developers
		1.1. GNU/Linux OS distros
		1.2. What is an operating system?
		1.3. Components of GNU/Linux OS
		1.4. Boot sequence of Linux
		1.5. User and group management
		1.6. File system hierarchy

Neden Linux'u seçtiğimiz konusu ile başladık.
Üzerinde çalıştığımız işletim sisteminin çalışma mekaniğini anlamamız gerektiğine, anlamadığımız yerde durup o kısmı anladıktan sonra devam etmemiz gerektiğine değindik.
Üç ana işletim sistemi olduğunu söyledik: Linux, Unix ve Windows. Mainframe'lerde çalışan High Performance Computing(HPC) sistemlerinin alanımız dışında olduğunu söyledik, bunların yüzde sekseni Unix-Linux türevleri çalıştırıyormuş.

Windows'u pas geçiyoruz çünkü geliştirici dostu gibi görünen bir işletim sistemi. Prototipler üretmesi kolay, fakat kullanıcısına eziyet eden bir işletim sistemi. Pazarda geriye düştükleri için open source'a yöneldiler, fakat free software'in üstünlüğü devam ediyor.

Biz bütün dünyada çalışabilecek "Gerilla Geliştirici"ler olacağımızdan, daha evrensel olan Linux üzerinde çalışmayı seçiyoruz.

[Linux Kernel](https://youtu.be/mycVSMyShk8) etrafında oluşturulmuş farklı dağıtımlar var. Hepsi Linux Kernel kullanır. Dağıtımlar hakkındaki bilgileri [distrowatch.com](https://distrowatch.com/) sitesinden takip edebiliriz.

Asıl mesele Kernel, fakat Kernel, işletim sistemi için yeterli değil. [GNU](https://en.wikipedia.org/wiki/GNU) ile [kullanıcı ve bilgisayar arasındaki ilişki yönetiliyor](https://youtu.be/RNeKYjWx-s4). GNU, bunun için tek seçenek değil. GNU, bir geliştirme ve yaşam felsefesi. Başında Richard Stallman var.

Linux, tüm dünyada kullanılıyor. Linux ile uğraşan bir çok topluluk var. Dağıtımlardaki minik parçaların geliştirmelerini, bakımlarını yapıyorlar. Debian ve RedHat iki ana akım, diğer dağıtımlar bunlar üzerine inşa edilir. Ubuntu, Debian'dan türemiştir. Redhat, CentOS; RedHat'ten türemiştir. Linux dağıtımlarının sistem gereksinimleri genellikle düşüktür. Linux, uyumluluk için tasarlanmıştır, çalışma ekosistemleri için yaratılmıştır. Linux işletim sistemlerinin her parçasını kafamıza göre değiştirebiliriz.

[Free Software ve Open Source farklı şeyler](https://youtu.be/lrcdhzr2qnk). Free Software terimindeki "free" kelimesini "free speech"teki gibi anlamalıyız. Open Source hareketi, bu kısma yeterince önem vermiyor. Free Software topluluğu, aktif yardımlaşma içinde bir topluluk, fakat soru sorarken [kuralına göre]([http://www.catb.org/~esr/faqs/smart-questions.html](http://www.catb.org/~esr/faqs/smart-questions.html)) sormak gerekiyor.

Linux'u anlamak için Unix'i anlamak gerekiyor. Bell laboratuvarlarında [Multics](https://en.wikipedia.org/wiki/Multics) projesi olarak başlıyor. Çok kullanıcılı bir işletim sistemi projesi olarak başlıyor fakat bir noktada bu proje duruyor. Daha sonra 72-73 yıllarında projeye portability kazandırmak için C ile devam ediyorlar. [POSIX](https://en.wikipedia.org/wiki/POSIX) standardını geliştiriyorlar. Proje portability sayesinde, her işlemcide çalışarak hayatta kalıyor. Sun Microsystems, ilk ticari Unix vendörü olarak işe dalıyor. Berkeley'de BSD Unix yapıyorlar ve bundan esinlenen bir sürü işletim sistemi yapılıyor. [NeXTSTEP](https://en.wikipedia.org/wiki/NeXTSTEP), Apple'ın işletim sistemine dönüşüyor. [MINIX](https://en.wikipedia.org/wiki/MINIX), Linus Torvalds sayesinde Linux oluyor.

Unix'in bakış açıları:

 - Clarity: Kısıtlı ve iyi belirlenmiş bir yol haritası.
 - Portability: C'de yazılmış olması sayesinde her yerde çalışabilmesi.
 - Simultaneity: Birden fazla kullanıcının özgürce yapacağı işlemleri kaldırabilmesi.

GNU'yu Richard Stallman başlatıyor. GNU, Free Software Foundation'ın odağı haline geliyor. GNU Projesinin Unix'in yerine kullanmak üzere geliştirmeye başladığı [GNU Hurd](https://www.gnu.org/software/hurd/) projesi 1985'ten beri meyve verememiş.

Linus Torvalds, 1991'de MINIX kullanan bir işletim sistemi yapıyor, ve bu işletim sistemi popüler oluyor. 1994'te 1.0 versiyonu yayınlanıyor. GNU ve Kernel'ı birlikte kullanma kararı alıyor, ve böylece diğer dağıtımlar da bunu kullanır oluyor.

Free Software topluluğu GNU tarafında duruyor. Linux tarafı Unix'ten çok şey aldı. Bir çok kaynaktan bir şeyler kullanarak bir işletim sistemi çıkarıyor.

Yazılım lisanslarına kısaca değindik. [ozgurlisanslar.org.tr](http://ozgurlisanslar.org.tr/) sitesinden yazılım lisanslarını öğrenebiliriz. GPL lisansı güzel, fakat kodu açık tutma zorunluluğu getirmesi yüzünden kapitalistler tarafından sevilmiyor. [BSD lisanslarının](https://en.wikipedia.org/wiki/BSD_licenses) iyi olmadığına değindik.

Linux, preemptive, gerçek zamanlı olarak donanım detaylarıyla baş edebiliyor.

	uname -a

Komutunun çıktısında;

	Linux vm-us 4.18.0-1023-azure #24~18.04.1-Ubuntu SMP Tue Jun 25 15:14:42 UTC 2019 x86_64 x86_64 x86_64 GNU/Linux

"GNU/Linux" u gördük, Richard Stallman'ın kazandığını belirttik.

Projelerde asıl meselenin minimum kaynak kullanma olduğuna değindik.

Debian ve RedHat iki ana linux dağıtımı, paket yönetim sistemleri farklı. Bunların bir çok türevleri var. RedHat tarafında Fedora(şirket içi), RedHat(ticari) ve CentOS(ücretsiz). CentOS ücretsiz olarak kullanılabiliyor. Bakım, SLA, destek isteyenler RedHat satın alıyor.

[BSD](https://www.bsd.org/)'nin önemli olduğunu söyledik ama ne olduğu üzerinde durmadık. OpenBSD projesinde dokuz yılda bir adet bug bulunduğunu söyledik. [Apache Foundation](https://www.apache.org/foundation/)'ı andık ama üzerine konuşmadık.

Bizim işimiz etrafında çok fazla bilgi olduğundan bahsettik. O anda yaptığımız iş ile ilgili detaylara odaklanalım, diğer unsurları o konudan ayrı tutalım dedik. Neyi nasıl hatırlayacağımızı öğrendiğimizden, herşeyi hatırlamaya çalışmayacağımızdan bahsettik.

Hardware<Kernel<Shell<X and Window Manager<User şeklinde bir şemayı inceledik. İşletim sistemi ve bilgisayar ile ilgili çeşitli şemalar inceledik.

	lspci, lsusb, lsdev, lsmod, modinfo, w, whoami, last, uptime 
komutlarını inceledik.

Ip adreslerinin A class, B class gibi sınıfları olduğuna değindik. [Detayına](https://study-ccna.com/classes-of-ip-addresses/) girmedik.

SCI, PM, VFS, MM, Network Stack, Arch, Device Drivers içeren bir şema inceledik. Bunun ne olduğunu unuttum.

Storage türlerinden bahsettik. DAS, direct attached storage, bilgisayarımıza doğrudan bağlı storage. Uzaktan bağlanan storage'lardan NAS ve SAN'a değindik.

	netstat, sudo netstat -nlp, netstat -s
komutlarını inceledik.
Farenin orta tuşuna basarak seçili metni copy&paste yapabileceğimizi gördük.

Boot Sequence'a değindik. Şöyle bir sıradan bahsettik:

 1. BIOS: Basic Input Output System. Bağlı donanımları biliyor.
 2. MBR: Master Boot Record. GRUB'u çalıştırır. Windows'ta sıfırıncı sektörde olmak zorunda.
 3. GRUB: Grand Unified Bootloader. Kernel'i çalıştırır
 4. Kernel: /sbin/init 'i çalıştırır
 5. Init: Runlevel programlarını çalıştırır.

Systemd'nin SystemV'nin yerine geldiğini söyledik.

[Runlevel](https://en.wikipedia.org/wiki/Runlevel) 'lardan bahsettik. Çok kullanıcılı bir işletim sisteminde bakım yapacağımız zaman runlevel set ederek, işletim sistemini tek kullanıcılı bir işletim sistemi haline getirip bakım yapabileceğimizi söyledik. runlevel komutu ile sistemin o an hangi runlevel'da olduğunu görebileceğimizi gördük. Runlevel'ı sıfıra set ederek makinayı programatik olarak kapatabileceğimize değindik.

Linux'un, tam programlanabilir bir ortam olduğunu söyledik.

Windows'ta file system hierarchy olmadığını, Windows'un çok kullanıcılı bir işletim sistemi olarak tasarlanmadığını söyledik.

[Linux Filesystem Hierarchy](https://www.tldp.org/LDP/Linux-Filesystem-Hierarchy/html/index.html)'ye geçtik. Bunun bilinmesinin gerekliliğine vurgu yaptık. "/" sembolünün herhangi bir diski değil, işletim sisteminin kökünü temsil ettiğini söyledik.

dmesg komutuna göz attık. dbus'ı atladığımızı fark ettik.

netcat'i anlamanın çok önemli olduğunu, netcat'in hacker'ların isviçre çakısı olduğuna değindik.

/etc/bash_completion'a göz attık.

Bizim işimizde hiç bir şeyin otomatik olmayacağını, her işimizi manuel yapacağımızı söyledik.

ps komutu ile, o anda çalışmakta olan [process](https://www.tecmint.com/linux-process-management/)'leri listeleyebileceğimizi gördük. ps -aux &#124; grep bash komutu ile bash ile ilgili process'leri gördük.

Tehlikeli olabileceğini düşündüğümüz komutlar hakkında man ve info komutlarını kullanarak bilgi alabileceğimizi gördük. apropos komutu ile benzer komutları listelettik.

Binary File'ın derlenmiş ve çalıştırılabilir dosya demek olduğunu söyledik. file komutu ile dosya türünü görebileceğimizi gördük.

Ctrl+A ve Ctrl+E ile yazmakta olduğumuz satırın başına veya sonuna atlayabileceğimizi gördük.

[/proc](https://www.tldp.org/LDP/Linux-Filesystem-Hierarchy/html/proc.html) klasörüne göz attık.

tecmint.com'un iyi bir kaynak olduğunu söyledik. Gnome'un bir window manager olduğunu söyledik.
"Hard Link" ve "Soft Link" kavramlarını bir sınıf arkadaşımızdan öğreneceğimizin haberini aldık :)
SID ve GID nedir? Araştırma ödevi verildi.
">"(redirection) ve ">>"(concatenation) komutlarını inceledik. touch komutuyla oynadık.

Umarım önemli bir şey atlamamışımdır.

Sevgiler,
Erhan