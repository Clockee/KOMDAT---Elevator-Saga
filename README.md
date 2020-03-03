<p align="center">
  <img  width="200%" height="200%" src="https://github.com/Clockee/KOMDAT---Elevator-Saga/blob/master/etc/gambar.PNG">
</p>

# Daftar Isi
- [`Deskripsi`](#deskripsi)
- [`Instalasi`](#instalasi)
  - [`Instalasi Web Server Virtual`](#instalasi-web-server-virtual)
  - [`Instalasi Elevator Saga`](#instalasi-elevator-saga)
- [`Cara Bermain`](#cara-bermain)
- [`Pembahasan`](#pembahasan)
  - [`Kelebihan`](#kelebihan)
  - [`Kekurangan`](#kekurangan)
- [`Referensi`](#referensi)


# Deskripsi

Elevator saga adalah sebuah permainan berbasis web yang menggunakan algoritma/programing untuk menyelesaikan permainannya. Pemain diminta untuk membantu memecahkan permasalahan elevator dengan membuat program pada _JavaScript_ yang digunakan oleh pemain untuk memprogram pergerakan elevator. Tujuan permainan ini adalah untuk memindahkan orang dengan elevator se-optimal mungkin.

# Instalasi

Requirement yang dibutuhkan:
* HTML
* CSS
* JavaScript
* Apache
* MySQL
* PHP

## Instalasi Web Server Virtual


1. Membuat VM Ubuntu Server Membuat VM baru pada VirtualBox dengan tipe "Ubuntu 64-bit", menggunakan virtual disk Ubuntu Server 18.04.
2. Setting Port-Forwarding VM Tujuannya adalah agar VM bisa diakses dari luar melalui alamat IP host (localhost). Masuk ke 'Settings -> Network -> Advanced -> Port Forwarding' lalu ditambahkan dua aturan berikut.

: Aturan *port forwarding*

Name   | Protocol   | Host IP    | Host Port  | Guest IP   | Guest Port
----   | --------   | -------    | ---------  | --------   | ----------
http   | TCP        |            | 8888       |            | 80
ssh    | TCP        |            | 3000       |            | 22

<p align="center">
  <img src="https://raw.githubusercontent.com/Clockee/KOMDAT---Elevator-Saga/master/etc/port_forwarding.png">
</p>

3. Instalasi LAMP (Linux Apache MySQL PHP)
```bash
# akses vm dari host
ssh student@localhost -p 3000

# set repo
sudo tee /etc/apt/sources.list << !
deb http://repo.apps.cs.ipb.ac.id/ubuntu bionic          main restricted universe multiverse
deb http://repo.apps.cs.ipb.ac.id/ubuntu bionic-updates  main restricted universe multiverse
deb http://repo.apps.cs.ipb.ac.id/ubuntu bionic-security main restricted universe multiverse
!

# instal apache, mysql, php
sudo apt update
sudo apt upgrade
sudo apt install apache2 php mysql-server
sudo apt install php-mysql php-gd php-mbstring php-xml php-curl
sudo service apache2 restart

```

## Instalasi Elevator Saga
1. Clone Elevator Saga dari [repositori githubnya](https://github.com/magwo/elevatorsaga)
2. Copy folder yang sudah di clone ke folder  */var/www/html*

```bash

# clone source code
git clone https://github.com/magwo/elevatorsaga.git

# pindah folder
sudo cp -r elevatorsaga /var/www/html

```

# Cara Bermain
* Masukkan kode program dalam input window yang berada di dalam laman permainan, kemudian tekan tombol _Apply_ untuk memulai permainan
* Pemain dapat mengatuk kecepatan permainan dengan menekan tombol + dan -
* Jika terdapat error dalam kode, bisa menggunakan developer tools di browser untuk mencoba dan men-debug terlebih dahulu
* Jika ingin mengulang semua kodenya, tekan tombol reset
* Pemain bisa menggunakan text editor favorit, setelah itu menyalinnya ke editor di dalam permainan
* Kode yang sudah dibuat akan secara otomatis tersimpan di penyimpanan lokal sehingga tidak perlu takut jika tidak sengaja menutup browser

Lebih lengkapnya, cara bermain bisa dilihat [di sini](https://play.elevatorsaga.com/documentation.html)

# Pembahasan
### Kelebihan
- Melatih kemampuan membuat kode program dalam JavaScript dengan menyenangkan

### Kekurangan
- Tampilan kurang menarik

# Referensi
https://github.com/magwo/elevatorsaga

https://github.com/auriza/komdat-lab/blob/master/p01.md

https://play.elevatorsaga.com/documentation.html




