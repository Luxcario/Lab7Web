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

<hr>

**Memulai PHP**
Buat Folder **lab7_php_dasar** pada root directory web server c:\xampp\htdocs

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/11198822-91e8-4633-b1c3-4fac3bb85d51)

Kemudian untuk mengakses direktory tersebut pada web server dengan mengakses URL:

http://localhost/lab7_php_dasar/

! sesuaikan dengan nama folder yang di buat

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/5c45946c-d8d4-4835-9157-164b10a53488)

<hr>

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

<hr>

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

<hr>

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

<hr>

**Membuat Form Input**

untuk membuat form, gunakan ```$_POST[]```.

```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <title>PHP Dasar</title>
</head>
<body>
<h2>Form Input</h2>
<form method="post">
 <label>Nama: </label>
 <input type="text" name="nama">
 <input type="submit" value="Kirim">
</form>
<?php
echo 'Selamat Datang ' . $_POST['nama'];
?>
</body>
</html>
```

Untuk melihat hasil gunakan URL http://localhost/lab7_php_dasar/form_input.php?nama . maka hasilnya

![Screenshot 2023-11-18 185554](https://github.com/Luxcario/Lab7Web/assets/116184002/58315b68-fb97-4ea3-aae4-f970f206653b)

Kemudian Masukkan nama, Misal JinxPro, kemudian kirim. maka hasilnya

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/90e3a31a-70e5-470f-9162-24d38e9c3d35)

<hr>

**Operator**

```
<?php
$gaji = 1000000;
$pajak = 0.1;
$thp = $gaji - ($gaji*$pajak);
echo "Gaji sebelum pajak = Rp. $gaji <br>";
echo "Gaji yang dibawa pulang = Rp. $thp";
?>
```

Untuk melihat hasilnya gunakan URL, http://localhost/namaFolder/namaFile.

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/88502c1e-4236-4afe-ba62-03e68b3e457e)

<hr>

**Kondisi IF**

```
<?php
$nama_hari = date("l");
if ($nama_hari == "Sunday") {
 echo "Minggu";
} elseif ($nama_hari == "Monday") {
 echo "Senin";
} else {
 echo "Selasa";
}
?>
```

Untuk melihat hasilnya gunakan URL, http://localhost/namaFolder/namaFile.

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/1f11e778-b67b-4bd1-9ee4-c3ad5073ca11)

<hr>

**Kondisi Switch**
```
<?php
$nama_hari = date("l");
switch ($nama_hari) {
 case "Sunday":
   echo "Minggu";
   break;
 case "Monday":
   echo "Senin";
   break;
 case "Tuesday":
   echo "Selasa";
 break;
   default:
 echo "Sabtu";
 }
?>
```

Untuk melihat hasilnya gunakan URL, http://localhost/namaFolder/namaFile.

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/012e2457-4325-4cc2-9c86-a199919c7b50)

<hr>

**Perulangan FOR**

```
<?php
    echo "Perulangan 1 sampai 10 <br />";
    for ($i=1; $i<10; $i++){
        echo "Perulangan ke naik : $i <br />";
    }

    echo "Perulangan Menurun dari 10 ke 1 <br />";
    for ($i=10; $i>=1; $i--){
        echo "Perulangan menurun ke : $i  <br />";
    }
    ?>
```

Untuk melihat hasilnya gunakan URL, http://localhost/namaFolder/namaFile.

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/1a6fbadf-4dc2-44e7-b3aa-4572906942c7)

<hr>

**Perulangan While**
```
<?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    while($i<=10){
        echo "Perulangan ke : " .$i. '<br />';
        $i++;
    }
    ?>
```

Untuk melihat hasilnya gunakan URL, http://localhost/namaFolder/namaFile.

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/f470fe38-a078-42c6-980c-0990a17131a9)

<hr>

**Perulangan dowhile**
```
<?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    do{
        echo "Preulangan ke : ".$i.'<br />';
        $i++;
    }while ($i<10);
    ?>
```

Untuk melihat hasilnya gunakan URL, http://localhost/namaFolder/namaFile.

![image](https://github.com/Luxcario/Lab7Web/assets/116184002/a73022e5-b1ea-4b97-93da-91d734ae6459)

<hr>

**Pertanyaan dan Tugas**
Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan 
nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung 
umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang 
berbeda-beda sesuai pilihan pekerjaan


