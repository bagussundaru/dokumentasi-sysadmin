# Maintenance Log File

Log File adalah file yang digunakan oleh sistem operasi atau aplikasi untuk mencatat aktivitas atau peristiwa yang terjadi di sistem. Berikut adalah beberapa perintah yang dapat digunakan untuk melakukan maintenance pada Log File di Centos 7:

* Untuk menampilkan daftar Log File yang tersedia di sistem, dapat menggunakan perintah berikut:

```bash
ls /var/log/
```

* Untuk melihat isi dari sebuah Log File, dapat menggunakan perintah berikut:

```bash
cat /var/log/nama_file.log
```

* Untuk menghapus isi dari sebuah Log File, dapat menggunakan perintah berikut:

```javascript
echo "" > /var/log/nama_file.log
```

* Untuk melakukan rotasi Log File, dapat menggunakan perintah berikut:

```bash
logrotate /etc/logrotate.conf
```
