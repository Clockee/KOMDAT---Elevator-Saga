<p align="center">
  <img  width="200%" height="200%" src="https://github.com/Clockee/KOMDAT---Elevator-Saga/master/etc/gambar.PNG">
</p>



# Sekilas Tentang

Elevator saga adalah web-based game yang ....... (jelasin)

# Instalasi

System Requirement:

* Unix, Linux atau Windows.
* Apache Web server 1.3+.
* PHP 5.2+.
* MySQL 5.0+.
* RAM minimal 64 Mb+

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
ssh student@localhost -p 2222

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



