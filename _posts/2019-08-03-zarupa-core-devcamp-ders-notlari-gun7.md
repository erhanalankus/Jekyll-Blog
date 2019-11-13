---
title: "Zarupa Core Devcamp Ders Notları (7. Gün)"
---

## 7. Gün (40. ve 44. saatler arası)

Selam,

Bugün sanallaştırmaya giriş yaptık.

Sanallaştırma türlerine değindik. Bknz: [Gdg izmir kubernetes sunumu](https://www.slideshare.net/kunthar/gdg-izmir-kubernetes)

1. Full Virtualization: Yüklenecek işletim sistemine kendi istediği donanımı report ediyor. Yerleşik olanla göçebe olan arasında daima bir savaş hali var. Bknz: [Deleuze](https://dergipark.org.tr/download/article-file/213940)

2. Paravirtualization. Running a modified guest system(kernel). XEN, QEMU, KVM. Bu üçü için bir session yapacağız.

3. OS-Level Virtualization. Enables running an isolated process(tree). OpenVZ, LXC, BSD-jails, Linux-VServer, Solaris Zones.

4. Virtualized Containers. LXC, LXD, Docker.

lspci komutunu hatırladık. PCI device'ları listeliyor. Sanal makine oluştururken konuk işletim sistemini bu konuda kandırabiliyoruz.

Virtualbox bir hypervisor.

[Ingress, egress](https://www.techopedia.com/definition/2415/ingress-traffic); içe doğru, dışa doğru demek oluyor. Veri trafiği para demek, o yüzden veri miktarı azaltılmalı.

Docker, arka planda LXC container'ları kullanıyor.

Docker ile ilgili tanımlara baktık.

[Unikernel](https://en.wikipedia.org/wiki/Unikernel)'ın geleceğin teknolojisi olduğunu söyledik.

PETS anlayışından CATTLE anlayışına geçildi. Linux high availability artık eskisi kadar gündemde değil.

İki şey izole edilecek. Process ve disk erişimi. Cgroups diye bir şey var. Process'leri gruplayarak isolate ediyor, dışarıya vermiyor.

[Docker for beginners](https://docker-curriculum.com/) kaynakları inceledik.

chroot ile tebelleş olacağız.

[The twelve-factor app](https://12factor.net/) konusu önemli.

vagrant güzel bir şey. Bir development environment, kullanılmaya hazır bir halde paketleniyor. Açıp direk kullanıyorsun.

Hashicorp şirketine dikkat et.

[hub.docker.com](https://hub.docker.com)'da hesap açacağız.

Caddy web server'a göz attık.

dpkg -i hatırladık.

ENTRYPOINT ile bu container çalıştığında bu scripttekileri yap dedik.

export komutunu hatırladık.

ln -s ile symbolic link yapmayı hatırladık.

Eğitimin en lezzetli yerlerine geliyormuşuz gibi hissediyorum.

Sevgiler,

Erhan.