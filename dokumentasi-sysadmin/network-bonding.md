# Network Bonding

Anda perlu mengikuti langkah-langkah berikut:

1.  Pastikan CentOS 7 Anda sudah terinstal dengan paket ifenslave. Jika belum, Anda dapat menginstalnya dengan menjalankan perintah berikut:

    ```
    yum install -y ifenslave
    ```
2.  Buka file konfigurasi bonding menggunakan editor teks, seperti nano atau vi:

    ```bash
    nano /etc/sysconfig/network-scripts/ifcfg-bond0
    ```
3.  Dalam file tersebut, tambahkan konfigurasi bonding dengan menyesuaikannya dengan preferensi jaringan Anda. Berikut adalah contoh konfigurasi:

    ```makefile
    DEVICE=bond0
    BOOTPROTO=none
    ONBOOT=yes
    NETWORK=<network-address>
    NETMASK=<netmask>
    BONDING_OPTS="mode=<bonding-mode> miimon=100"
    ```

    * Gantilah `<network-address>` dengan alamat jaringan yang sesuai dengan konfigurasi Anda.
    * Gantilah `<netmask>` dengan subnet mask yang sesuai.
    * Gantilah `<bonding-mode>` dengan mode bonding yang diinginkan, seperti mode 0 (balance-rr), mode 1 (active-backup), mode 4 (802.3ad), dll. Sesuaikan dengan kebutuhan Anda.
4. Simpan dan tutup file konfigurasi.
5.  Buat file konfigurasi untuk setiap antarmuka jaringan yang akan diikatkan ke bonding. Misalnya, jika Anda ingin mengikatkan eth0 dan eth1, buat file konfigurasi berikut:

    ```bash
    sudo nano /etc/sysconfig/network-scripts/ifcfg-eth0
    ```

    Isi file dengan konfigurasi berikut:

    ```makefile
    DEVICE=eth0
    TYPE=Ethernet
    BOOTPROTO=none
    ONBOOT=yes
    MASTER=bond0
    SLAVE=yes
    ```

    Buat juga file konfigurasi untuk eth1:

    ```bash
    sudo nano /etc/sysconfig/network-scripts/ifcfg-eth1
    ```

    Isi file dengan konfigurasi berikut:

    ```makefile
    DEVICE=eth1
    TYPE=Ethernet
    BOOTPROTO=none
    ONBOOT=yes
    MASTER=bond0
    SLAVE=yes
    ```
6. Simpan dan tutup file konfigurasi.
7.  Restart layanan jaringan untuk menerapkan perubahan:

    ```
    systemctl restart network
    ```

Setelah langkah-langkah ini, Anda seharusnya memiliki network bonding yang aktif di CentOS 7. Pastikan untuk menyesuaikan konfigurasi sesuai dengan kebutuhan dan preferensi jaringan Anda.
