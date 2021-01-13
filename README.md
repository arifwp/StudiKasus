# Arif Wahyu Prasetyo 19.11.2734

# StudiKasus

Diberi nama promos karena aplikasi ini merupakan pengembangan dari aplikasi sebelumnya dengan menambahkan beberapa fitur baru dan membuat code lebih rapi

# Kegunaan
- User dapat melihat daftar makanan yang ditawarkan
- User dapat memasukkan atau menghapus makanan pilihan ke dalam keranjang
- User dapat melihat subtotal makanan yang terdapat pada keranjang
- User dapat melihat daftar voucher yang ditawarkan
- User dapat menggunakan salah satu voucher
- User dapat melihat harga total termasuk potongannya

# Alur Program
 Saat aplikasi ini dibuka, user akan disuguhkan oleh tampilan dari MainWindow atau tampilan utama dari aplikasi ini yang berisikan keranjang, subtotal, total harga, dan voucher.
 User bisa memilih item yang telah tersedia dengan mengklik Pilih Item lalu memilih item. User juga bisa menggunakan voucher yang akan langsung mengurangi total harga sesuai dengan
 voucher.
 
 User pertama kali akan ditampilkan halaman mainwindow yang berisikan keranjang, serta subtotal dan total harga. Serta opsi untuk memilih voucher yang tersedia.
 kemudian user akan memilih item pada halaman penawaran yang kemudian item tersebut akan masuk ke dalam keranjang (user dapat menghapus item jika ada kesalahan)
 Lanjut dengan pemilihan voucher sebagai akhir dari alur aplikasi serta penggunaannya untuk pemotongan harga pada total.
 
 Berikut adalah potongan codingan untuk menampilkan voucher.


        private void generateListVoucher()
        {
            Model.Voucher awalTahun = new Model.Voucher(title: "Promo Awal Tahun Diskon 25%", discInPercent: 25);
            Model.Voucher tebusMurah = new Model.Voucher(title: "Promo Tebus Murah Diskon 30% atau max. 30.000", discInPercent: 30);
            Model.Voucher promoNatal = new Model.Voucher(title: "Promo Natal Potongan 10000", disc: 10000);

            voucherController.addItem(awalTahun);
            voucherController.addItem(tebusMurah);
            voucherController.addItem(promoNatal);

            DaftarVoucher.Items.Refresh();
        }



