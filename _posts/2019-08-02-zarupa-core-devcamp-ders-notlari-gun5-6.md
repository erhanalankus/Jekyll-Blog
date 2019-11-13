---
title: "Zarupa Core Devcamp Ders Notları (5. ve 6. Gün)"
---

## 5. ve 6. Gün (24. ve 40. saatler arası)

Selam,

HDD değişimleri, yeniden işletim sistemi yüklemeceler falan derken 6. günden aldığım notları yanlışlıkla sildiğimi farkettim.

Sistem yöneticileri boşuna maaş almıyor.

Beşinci ve altıncı gün, ["Bash Reference Manual"](https://www.gnu.org/s/bash/manual/bash.pdf) ve ["Vim User Manual"](https://www.vi-improved.org/vimusermanual.pdf) üzerinde bol bol çalıştık. Vim ile bash script'ler yazdık. [Güzel bir tutorial](https://linuxconfig.org/bash-scripting-tutorial-for-beginners) yaptık.

Beşinci günden almış olduğum notlar:

gvim(graphical vim) diye bir şey var, vim'de fare de kullandırır.

Bizim kullandığımızın gnome masaüstü olduğunu ~/.config klasöründeki dosyalara bakarak teyit ettik.

vim'de '0' ve '$' ile satır başına, satır sonuna zıplayabiliyoruz.

vim'e birtakım eklentiler kurduk, sonra .vimrc'yi boşaltınca vim eski haline döndü.

awk'yi ve sed'i inceledik. Bunlar "text manipulators". Bi komutun çıktısının n. sütununu almaca yaptık.

jobs komutunu gördük, arka plandaki process'i stopped olarak gösterdi.

"Signal" ları inceledik. SIGKILL ile process'i ani durdurabiliyoruz, bu ani durdurmanın yan etkileri olabiliyor. SIGTERM ile kibarca durdurabiliriz. Ctrl+C, SIGINT gönderir.

alias x=ls, dedik. x yazınca ls çalıştı. Shell'i kapatınca alias gidiyor. Atamayı .bashrc'ye koyarsak kalıcı oluyor.

Backtick'ler içine yazılanlar çalıştırılıyor, mesela mkdir \`pwd\`/folder

Tek tırnak literal demek oluyor. Çift tırnak içindeki $HOME, expand olur.

locale komutunu gördük. LC ile başlayanlar language variable, C derlerken bunların doğru olmaları önemli.

time komutu ile bi komutun gerçekleşme süresini ölçebiliyoruz.

Dosyaya girdiğimiz karaktere göre bash, dosya tipini otomatik ayarlıyor. Mesela sadece "g" varsa ASCII text, "ğ" eklersen UTF-8 Unicode text oluyor.

Komutların stdout'u var stderror'u var. Yazdığımız şey stdin, verdiği çıktı stdout, verdiği hata stderr.

Shell'de \ ile multiline yazabiliyoruz.

Shell scripti yazarken komutu direk kullanmıyoruz, full path'i ile kullanıyoruz.

Shell'de backtick ile gördüğümüz işi, script dosyası yazarken $() ile görüyoruz.(içtekinin çalıştırılması)

Backup tiplerini konuştuk.

rsync örnekleri yaptık.

/dev/null bir kara delik.

DRY. Aynı işi yapan kodu tekrar tekrar yazma.

find . type f &#124; wc -l
