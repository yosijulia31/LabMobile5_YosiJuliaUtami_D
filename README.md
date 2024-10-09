Nama: Yosi Julia Utami
NIM: H1D021022

1. Proses Login
   a. SS Form Regis
      SS Form Login
   b. SS PopUp (Berhasil/Tidak)
      SS PopUp Regis Berhasil Masuk
   ![Logo]([./images/logo.png](https://github.com/yosijulia31/LabMobile5_YosiJuliaUtami_D/blob/main/Dokumentasi/Screenshot%20(128).png)
   Gambar tersebut menunjukkan sebuah halaman registrasi aplikasi dengan tampilan sukses setelah pengguna berhasil mendaftarkan diri. Password dan Konfirmasi Password diisi tetapi dalam bentuk bintang (*), menunjukkan bahwa password telah disembunyikan untuk keamanan.
  ![Logo]([./images/logo.png](https://github.com/yosijulia31/LabMobile5_YosiJuliaUtami_D/blob/main/Dokumentasi/Screenshot%20(129).png)
   Gambar tersebut menunjukan registrasi gagal karena ada beberapa isi form yang tidak sesuai dengan kriteria.

3. Proses Tambah Data Produk
   a. Kode
       Kode yang menyatakan proses tambah data produk berada di dalam fungsi simpan(). Fungsi ini dipanggil ketika tombol "SIMPAN" ditekan dalam kondisi penambahan produk baru. Berikut adalah penjelasan rinci:
    Logika pengecekan tombol simpan/ubah:
      ![Logo]([./images/logo.png](https://github.com/yosijulia31/LabMobile5_YosiJuliaUtami_D/blob/main/Dokumentasi/Screenshot%20(133).png)
    Pada widget _buttonSubmit(), dilakukan pengecekan apakah produk yang ada adalah produk baru atau produk yang akan di-update.
    dart
    Copy code
    if (widget.produk != null) {
      // kondisi update produk
      ubah();
    } else {
      // kondisi tambah produk
      simpan();
    }
    Jika widget.produk bernilai null, artinya produk yang sedang dikerjakan adalah produk baru, sehingga akan memanggil fungsi simpan().

   Tampilan Tambah Produk Gagal
  ![Logo]([./images/logo.png](https://github.com/yosijulia31/LabMobile5_YosiJuliaUtami_D/blob/main/Dokumentasi/Screenshot%20(132).png)
4. Proses Tampil Data
   a. Kode
      Proses lihat data dalam kode yang kamu berikan ditangani di dalam kelas ProdukDetail. Kelas ini menampilkan detail data produk dan menyediakan opsi untuk mengedit atau menghapus produk tersebut. Berikut adalah penjelasan lebih detail mengenai proses lihat data:
  ![Logo]([./images/logo.png](https://github.com/yosijulia31/LabMobile5_YosiJuliaUtami_D/blob/main/Dokumentasi/Screenshot%20(117).png)
Menampilkan Detail Produk:

Pada method build(BuildContext context), detail dari produk yang dioper dari halaman sebelumnya (melalui parameter produk di ProdukDetail) ditampilkan dalam bentuk teks. Informasi yang ditampilkan adalah kode produk, nama produk, dan harga produk.
dart
Copy code
Text(
  "Kode : ${widget.produk!.kodeProduk}",
  style: const TextStyle(fontSize: 20.0),
),
Text(
  "Nama : ${widget.produk!.namaProduk}",
  style: const TextStyle(fontSize: 18.0),
),
Text(
  "Harga : Rp. ${widget.produk!.hargaProduk.toString()}",
  style: const TextStyle(fontSize: 18.0),
),
Tiga komponen Text di atas menampilkan data produk secara spesifik:

Kode Produk: ditampilkan dalam ukuran font 20.
Nama Produk: ditampilkan dalam ukuran font 18.
Harga Produk: harga produk juga ditampilkan dengan ukuran font 18.

Tampilan Edit dan Hapus Produk
  ![Logo]([./images/logo.png](https://github.com/yosijulia31/LabMobile5_YosiJuliaUtami_D/blob/main/Dokumentasi/Screenshot%20(119).png)
  Tampilan Ubah Produk
    ![Logo]([./images/logo.png](https://github.com/yosijulia31/LabMobile5_YosiJuliaUtami_D/blob/main/Dokumentasi/Screenshot%20(120).png)
    
5. Logout
   Gambar menunjukan halaman Logout yang langsung diarahkan ke halaman login

   
