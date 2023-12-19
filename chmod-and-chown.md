# CHMOD & CHOWN

**CHMOD**

CHMOD (change mode) adalah perintah di sistem operasi Linux yang digunakan untuk mengubah hak akses file atau direktori. Hak akses ini menentukan siapa saja yang dapat membaca, menulis, atau mengeksekusi file atau direktori tersebut.

Perintah CHMOD menggunakan sintaks berikut:

```
chmod <mode> <file atau direktori>
```

Di mana:

* `<mode>` adalah hak akses yang baru.
* `<file atau direktori>` adalah file atau direktori yang hak aksesnya akan diubah.

Hak akses dapat ditentukan dengan menggunakan angka atau huruf. Berikut adalah tabel yang menunjukkan arti dari setiap angka dan huruf:

| Angka | Huruf | Keterangan                               |
| ----- | ----- | ---------------------------------------- |
| 0     | -     | Tidak ada hak akses                      |
| 1     | r     | Dapat membaca                            |
| 2     | w     | Dapat menulis                            |
| 3     | x     | Dapat mengeksekusi                       |
| 4     | s     | Dapat membaca dan menulis                |
| 5     | t     | Dapat membaca dan mengeksekusi           |
| 6     | u     | Dapat menulis dan mengeksekusi           |
| 7     | a     | Dapat membaca, menulis, dan mengeksekusi |

Untuk mengubah hak akses file atau direktori, Anda harus memiliki hak akses yang cukup. Jika Anda tidak memiliki hak akses yang cukup, perintah CHMOD akan gagal.

Berikut adalah beberapa contoh penggunaan perintah CHMOD:

* Untuk memberikan hak akses baca dan tulis kepada semua pengguna, gunakan perintah berikut:

```
chmod 666 <file atau direktori>
```

* Untuk memberikan hak akses eksekusi kepada semua pengguna, gunakan perintah berikut:

```
chmod 777 <file atau direktori>
```

* Untuk memberikan hak akses baca kepada pengguna saat ini, gunakan perintah berikut:

```
chmod u+r <file atau direktori>
```

* Untuk memberikan hak akses tulis kepada pengguna saat ini, gunakan perintah berikut:

```
chmod u+w <file atau direktori>
```

* Untuk memberikan hak akses eksekusi kepada pengguna saat ini, gunakan perintah berikut:

```
chmod u+x <file atau direktori>
```

**CHOWN**

CHOWN (change owner) adalah perintah di sistem operasi Linux yang digunakan untuk mengubah pemilik file atau direktori. Pemilik file atau direktori adalah pengguna yang memiliki hak akses penuh terhadap file atau direktori tersebut.

Perintah CHOWN menggunakan sintaks berikut:

```
chown <pemilik baru> <file atau direktori>
```

Di mana:

* `<pemilik baru>` adalah nama pengguna baru yang akan menjadi pemilik file atau direktori.
* `<file atau direktori>` adalah file atau direktori yang pemiliknya akan diubah.

Untuk mengubah pemilik file atau direktori, Anda harus memiliki hak akses yang cukup. Jika Anda tidak memiliki hak akses yang cukup, perintah CHOWN akan gagal.

Berikut adalah beberapa contoh penggunaan perintah CHOWN:

* Untuk mengubah pemilik file atau direktori menjadi pengguna saat ini, gunakan perintah berikut:

```
chown <file atau direktori>
```

* Untuk mengubah pemilik file atau direktori menjadi pengguna lain, gunakan perintah berikut:

```
chown <nama pengguna> <file atau direktori>
```

* Untuk mengubah pemilik file atau direktori menjadi grup lain, gunakan perintah berikut:

```
chown :<nama grup> <file atau direktori>
```
