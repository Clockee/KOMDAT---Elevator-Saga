<p align="center">
  <img  width="200%" height="200%" src="https://github.com/Clockee/KOMDAT---Elevator-Saga/blob/master/gambar.PNG">
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
3. Instalasi LAMP (Linux Apache MySQL PHP)
```bash
# akses vm dari host
ssh student@localhost -p 2222

# instal apache, mysql, php
sudo apt update
sudo apt upgrade
sudo apt install apache2 php mysql-server
sudo apt install php-mysql php-gd php-mbstring php-xml php-curl
sudo service apache2 restart

```


