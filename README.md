# Evaluasi Akhir Semester - Pemrograman Integratif 2020
Repository sebagai dokumentasi Final Project dan Evaluasi Akhir Semester Pemrograman Integratif 2020 \
Disusun oleh : 
```
Nama        :   I Gde Made Bhaskara Jala Dhananjaya 
NRP         :   05311840000007 
Departemen  :   Teknologi Informasi
```
## Overview Aplikasi
Project kali ini, penulis ditugaskan untuk membuat website sederhana berbasis MVC sebagai tempat untuk donasi bagi bencana pandemik Covid-19. Website ini akan memudahkan donatur untuk mengisi donasi yang diinginkan melalui form yang disediakan. Selain itu donatur juga dapat melihat rekapan dari donasi yang telah diinput.

## Setup
- Database dapat diakses pada file berikut : [Database](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/donasi.sql)
- Konfigurasi untuk koneksi ke database dapat diakses pada file berikut : [Constant]()

## Controllers
Pada project ini penulis, menggunakan tiga controller yakni [Home](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/donasi/app/controllers/Home.php), [Jenis](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/donasi/app/controllers/Jenis.php), dan [Sumbangan](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/donasi/app/controllers/Sumbangan.php) . Method yang digunakan dalam controller tersebut antara lain :
- `index()`, method ini berfungsi untuk mengatur $_SESSION yang akan digunakan dan mengarahkan view yang digunakan ke Landing Page, dimana pada landing page nanti akan terdapat dua pilihan yakni form dan rekap.
- `filter()`, method ini berfungsi untuk melakukan filter pada view rekapan donasi.
- `inputdata()`, method ini berfungsi untuk menginput data pada $_SESSION ke dalam database.

## Models
Pada project ini, penulis menggunakan satu models untuk masing-masing tabel yakni [Sumbang](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/donasi/app/models/Sumbang.php) . \
Struktur tabel sumbangan adalah sebagai berikut :
- `s_id`, kolom ini akan berisi data mengenai id dari donasi yang dilakukan/diinput.
- `p_id`, kolom ini akan berisi data mengenai id dari donatur.
- `j_id`, kolom ini akan berisi data mengenai id dari jenis/kategori donasi. 

Struktur tabel penyumbang adalah sebagai berikut :
- `id`, kolom ini akan berisi data mengenai id donatur.
- `name`, kolom ini akan berisi data mengenai nama donatur.
- `gender`, kolom ini akan berisi data mengenai gender donatur.

Struktur tabel jenis_sumbangan adalah sebagai berikut :
- `id`, kolom ini akan berisi data mengenai id jenis/kategori donasi.
- `barang`, kolom ini akan berisi data mengenai jenis donasi yang didonasikan.

Pada model [Sumbangan]() , method yang digunakan adalah sebagai berikut :
- `getName()`, method ini berfungsi untuk mendapatkan kategori donasi yang diinputkan.
- `setUser()`, method ini berfungsi untuk menginput semua data yang berhubungan dengan donatur yakni nama, gender, dan id).
- `isThere()`, method ini berfungsi untuk mencari id berdasarkan jenis/kategori donasi.
- `setJS()`, method ini berfungsi untuk memasukan/menginput data jenis/kategori donasi ke database.
- `setSumbangan()`, method ini berfungsi untuk menginput semua data yang berhubungan dengan donasi yakni nama, gender, id, jumlah, jenis, dan lainnya.
- `getSumbangan()`, method ini berfungsi untuk mencari dan mendapatkan semua data yang berhubungan dengan donasi.
- `getFilterSumbangan()`, method ini berfungsi untuk mencari dan mendapatkan semua data donasi berdasarkan donaturnya.

## Views
Pada project ini, penulis menggunakan beberapa views yang digunakan sebagai tampilan fungsional dari web. View yang penulis gunakan antara lain :
- ***Home***, view ini digunakan sebagai halaman awal (landing page). Dalam halaman ini terdapat dua button. Pertama ada button ***Form Donasi*** yang akan mengarah ke view form untuk menginput data donasi. Yang kedua adalah button ***Rekap Donasi*** yang mengarah pada view rekapan data donasi. Berikut adalah merupakan tangkapan layar dari view ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Landing%20Page.PNG)

- ***Sumbangan***, view ini digunakan sebagai halaman pengisian form donasi. Pada halaman ini, kita dapat menginput data mengenai donasi yang terdiri dari nama, gender, jenis/kategori donasi, dan jumlah donasi. Berikut adalah merupakan tangkapan layar dari view ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Form%20Input.PNG)
- Kita dapat mengisi data kategori donasi dengan kuantitas lebih dari satu kategori.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Pengisian%20Form%20Input.PNG)
- Dan jika data telah masuk ke database, akan muncul pemberitahuan atau pop up seperti di bawah ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Donasi%20Berhasil.PNG)

- ***Jenis***, view ini digunakan sebagai halaman untuk menampilkan rekapan donasi pada database. Tampilan tabel adalah seperti di bawah ini. \
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Rekapan%20Donasi.PNG)
- Pada halaman ini kita dapat melakukan filter menggunakan ***nama donatur*** seperti di bawah ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Filer%20Nama%20Donarut.PNG)
- Pada halaman ini juga kita dapat melakukan filter berdasarkan ***kategori donasi*** untuk mendapatkan id dan nama donatur.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Filter%20Kategori%20Donasi.PNG)

## Error
- Jika donatur belum menginputkan namanya, maka data tidak dapat dimasukkan ke database dan akan muncul pop up seperti di bawah ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Eror1.PNG)
- Pada halaman rekapan donasi, jika data tidak ada, maka tabel akan kosong seperti di bawah ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Eror2.PNG)

## Kendala yang Dialami Penulis
***1.*** Beberapa kali source code gagal untuk connect ke database. \
***2.*** Penulis perlu mencari berbagai sumber untuk dapat menangani kondisi seperti kuantitas donasi yang dapat lebih dari satu jenis/kategori. \
***3.*** Beberapa kali terjadi kendala saat sinkronisasi program.
