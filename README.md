# Evaluasi Akhir Semester - Pemrograman Integratif 2020
Repository sebagai dokumentasi Final Project dan Evaluasi Akhir Semester Pemrograman Integratif 2020 \
Disusun oleh : 
```
Nama        :   I Gde Made Bhaskara Jala Dhananjaya 
NRP         :   05311840000007 
Departemen  :   Teknologi Informasi
```

## Setup
- Database dapat diakses pada file berikut : [Database](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/donasi.sql)
- Konfigurasi untuk koneksi ke database dapat diakses pada file berikut : [Constant]()

## Controllers
Pada project ini penulis, menggunakan tiga controller yakni [Home](), [Jenis](), dan [Sumbangan]() . Method yang digunakan dalam controller tersebut antara lain :
- ***index()***, method ini berfungsi untuk mengatur $_SESSION yang akan digunakan dan mengarahkan view yang digunakan ke Landing Page, dimana pada landing page nanti akan terdapat dua pilihan yakni form dan rekap.
- ***filter()***, method ini berfungsi untuk melakukan filter pada view rekapan donasi.
- ***inputdata()***, method ini berfungsi untuk menginput data pada $_SESSION ke dalam database.

## Models
Pada project ini, penulis menggunakan satu models untuk masing-masing tabel yakni [Sumbangan]() . \
Struktur tabel sumbangan adalah sebagai berikut :
- ***s_id***, kolom ini akan berisi data mengenai id dari donasi yang dilakukan/diinput.
- ***p_id***, kolom ini akan berisi data mengenai id dari donatur.
- ***j_id***, kolom ini akan berisi data mengenai id dari jenis/kategori donasi. \
Struktur tabel penyumbang adalah sebagai berikut :
- ***id***, kolom ini akan berisi data mengenai id donatur.
- ***name***, kolom ini akan berisi data mengenai nama donatur.
- ***gender***, kolom ini akan berisi data mengenai gender donatur.
Struktur tabel jenis_sumbangan adalah sebagai berikut :
- ***id***, kolom ini akan berisi data mengenai id jenis/kategori donasi.
- ***barang***, kolom ini akan berisi data mengenai jenis donasi yang didonasikan.

Pada model ... , method yang digunakan adalah sebagai berikut :
- ***getName()***, method ini berfungsi untuk mendapatkan kategori donasi yang diinputkan.
- ***setUser()***, method ini berfungsi untuk menginput semua data yang berhubungan dengan donatur yakni nama, gender, dan id).
- ***isThere()***, method ini berfungsi untuk mencari id berdasarkan jenis/kategori donasi.
- ***setJS()***, method ini berfungsi untuk memasukan/menginput data jenis/kategori donasi ke database.
- ***setSumbangan()***, method ini berfungsi untuk menginput semua data yang berhubungan dengan donasi yakni nama, gender, id, jumlah, jenis, dan lainnya.
- ***getSumbangan()***, method ini berfungsi untuk mencari dan mendapatkan semua data yang berhubungan dengan donasi.
- ***getFilterSumbangan()***, method ini berfungsi untuk mencari dan mendapatkan semua data donasi berdasarkan donaturnya.

## Views
Pada project ini, penulis menggunakan beberapa views yang digunakan sebagai tampilan fungsional dari web. View yang penulis gunakan antara lain :
- ***a***, view ini digunakan untuk \
Berikut adalah merupakan tangkapan layar dari view ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Landing%20Page.PNG)

- ***b***, view ini digunakan untuk \
Berikut adalah merupakan tangkapan layar dari view ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Form%20Input.PNG)
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Pengisian%20Form%20Input.PNG)
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Donasi%20Berhasil.PNG)

- ***c***, view ini digunakan untuk \
Berikut adalah merupakan tangkapan layar dari view ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Rekapan%20Donasi.PNG)
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Filer%20Nama%20Donarut.PNG)
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Filter%20Kategori%20Donasi.PNG)

- ***c***, view ini digunakan untuk \
Berikut adalah merupakan tangkapan layar dari view ini.
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Eror1.PNG)
![](https://github.com/Bhaskaraa/EAS_Pemrograman-Integratif_05311840000007/blob/master/Screenshot/Eror2.PNG)

## Kendala yang Dialami Penulis
***1.*** Beberapa kali source code gagal untuk connect ke database.
***2.***
***3.***
