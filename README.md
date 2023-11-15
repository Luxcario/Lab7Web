# Lab7Web
# PHP Dasar 
**Laporan Praktikum**
1. Buatlah repository baru dengan nama Lab7Web.
2. Kerjakan semua latihan yang diberikan sesuai urutannya.
3. Screenshot setiap perubahannya.
4. Buatlah file README.md dan tuliskan penjelasan dari setiap langkah praktikum 
beserta screenshotnya.
5. Commit hasilnya pada repository masing-masing.
6. Kirim URL repository pada e-learning ecampus.

**Pertanyaan dan Tugas**
Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan 
nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung 
umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang 
berbeda-beda sesuai pilihan pekerjaan.

<hr>

1. Buatlah repository baru dengan nama Lab7Web.
2. Kerjakan semua latihan yang diberikan sesuai urutannya.

# Latihan 
**Menginstal XAMPP**
![image](https://github.com/Luxcario/Lab7Web/assets/116184002/02892102-2b97-4ef0-9b37-b93c1882874d)

**Konfigurasi Web Server**
**Konfigurasi Apache**
Untuk konfigurasi HTTP server, seperti port yang digunakan akses HTTP, modul yang diaktifkan, lokasi document root, dll. Lokasi file: \xampp\apache\conf\httpd.conf
**Konfigrasi PHP**
Untuk konfigurasi perilaku engine PHP yang berefek pada keamanan dan performa.
Seperti batas maksimal waktu eksekusi script, batas file yang dapat diupload, error 
reporting, dll.
Lokasi file: \xampp\php\php.ini
**Konfigrasi MySql**
Konfigurasi server MySQL, seperti administrator user, port, timezone, dll.
Lokasi file: \xampp\mysql\bin\my.ini

**Menjalankan Web Server**
Untuk menjalankan web server dari menu XAMPP Control, click tombol start pada Apache

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/80e9c1a1-05d5-4412-8675-0867d3048adb)

• Uji coba apakah server sudah berkerja dengan baik
http://127.0.0.1 atau http://localhost

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/fab40ef2-d4da-4365-b581-c3a0102a09cb)


Tampil halaman utama XAMPP jika server sudah berkerja dengan baik.

• Dokumen Website
Semua file website tempatkan di direktori: \xampp\htdocs\

• Database MySQL
Direktori: \xampp\mysql\

Manajemen database: http://localhost/phpmyadmin

**Memulai PHP**
Buat Folder **lab7_php_dasar** pada root directory web server c:\xampp\htdocs

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/11198822-91e8-4633-b1c3-4fac3bb85d51)

Kemudian untuk mengakses direktory tersebut pada web server dengan mengakses URL:

http://localhost/lab7_php_dasar/

! sesuaikan dengan nama folder yang di buat

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/5c45946c-d8d4-4835-9157-164b10a53488)

**PHP Dasar**
Buka Text Editor, contoh VSCode, pilih menu file lalu openfolder, buka folder **lab7_php_dasar** yang tadi sudah dibuat pada root htdocs. setelah buat file baru dengan nama **php_dasar.php** pada directory tersebut. Kemudian buat kode seperti berikut.

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/045a4a43-748b-450b-ba24-c6f15740c43a)

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>PHP Dasar</title>
</head>
<body>
  <h1>Belajar PHP Dasar</h1>
  <?php
  echo "Hello World";
  ?>
</body>
</html>
```

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/decfa359-1bf2-4731-892e-e0581391b388)

save file, kemudian untuk mengakses hasilnya melalui URL : http://localhost/lab7_php_dasar/php_dasar.php 

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/9f4097a2-cceb-400d-ae0c-4e106bdbbef5)

**Variable PHP**
Menambahkan variable pada program
```
<?php
$nim = "0411500400"; //(deklarasi) variable, $ adalah key untuk php
$nama = 'Abdullah';
echo "NIM : " . $nim . "<br>"; //echo untuk menampilkan hasil output
echo "Nama : $nama";
?>
```

Setiap Perubahan wajib disave, kemudian refresh pada browser.

Hasilnya 

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/8f0dfb6f-567e-4d66-aa63-cb20ad7dc2d0)

**Predefine variable $_GET**
```
<?php
echo 'Selamat Datang ' . $_GET['nama'];  //($_GET[]) untuk memanggil string pada variable
?>
```

untuk mengakses hasilnya agar tidak adanya tampilan Warning tambahkan ```?```nama=JinxPro //(variable+ = + value)
![image](https://github.com/Luxcario/Lab7Web/assets/116184002/77c5e7d0-aaff-4861-92ba-91b9355f441a)

code dan hasil

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/e516871e-43a1-4ef1-a6a7-c1a598dbb59d)

