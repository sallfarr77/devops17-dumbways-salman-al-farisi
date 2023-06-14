# 1.Penjelasan text manipulation beserta step by step
<br/>

## 1.Penjelasan apa itu text manipulation
Text manipulation adalah proses mengubah teks untuk mencapai tujuan tertentu. Ini melibatkan operasi seperti mencari, mengganti, memisahkan, menggabungkan, dan memformat teks. Contoh penggunaan text manipulation termasuk mengganti kata, memotong teks menjadi bagian-bagian, dan menghitung jumlah kata.

## 2.Contoh text manipulation beserta langkah-langkahnya
<br/>

### 1.Menggunakan perintah sed untuk mengganti teks dalam file
1.Buat sebuah nama file `nano sed.txt`, dan tuliskan nama macan didalamnya.

![1](/week-2/Manage-Terminal/img/1.png)

2.Selanjutnya tuliskan comand `sed -i 's/macan/singa/g' sed.txt` ini akan mengubah semua tulisan macan menjadi singa.

![2](/week-2/Manage-Terminal/img/2.png)

3.Lalu kita coba buka file tersebut, dan disini kata macan telah berubah menjadi singa.

![3](/week-2/Manage-Terminal/img/3.png)
<br/>

### 2.Menggunakan perintah grep untuk mencari kata didalam file
1.Buat sebuah file baru `nano grep.txt` disini saya mengutip sebuah kalimat dari ebook dumbways tentang text manipulation.

![4](/week-2/Manage-Terminal/img/4.png)

3.Disini saya ingin mencari kata nano dari file tersebut dan untuk mencarinya saya menggunakan `grep "nano" grep.txt`, Bisa dilihat disana saya telah menemukan kata yang di cari dan diberi warna merah pada warna tersebut.

![5](/week-2/Manage-Terminal/img/5.png)
<br/>

## 3.Menggunakan perintah awk untuk memanipulasi kolom dalam file
1.Buat file baru `nano awk.txt` dan masukan contoh data sebagai berikut.

![6](/week-2/Manage-Terminal/img/6.png)

2.Didalam data tersebut saya ingin mencari tabel usia, jadi saya bisa menggunakan comand `awk '{print $2}' awk.txt`, perinta tersebut akan menulis kolom kedua yang mana adalah usia dari orang orang yang ada di dalam data tersebut.

![7](/week-2/Manage-Terminal/img/7.png)
<br/>

# 2.Penjelasan tentang htop serta fitur-fiturnya

## 1.Penjelasan tentang Htop:
Htop adalah sebuah utilitas pengawasan sistem interaktif berbasis teks yang digunakan untuk memonitor dan mengelola kinerja sistem di lingkungan Linux. Ini adalah alternatif yang lebih kuat dan serbaguna dibandingkan dengan utilitas top bawaan di Linux. Htop menyediakan antarmuka yang lebih mudah digunakan dan menampilkan informasi yang lebih terperinci tentang penggunaan CPU, memori, dan sumber daya sistem lainnya.
<br/>

## 2. fitur utama Htop:
⚫Htop menyediakan tampilan interaktif yang dapat diperbarui secara real-time. Anda dapat melihat informasi yang diperbarui secara langsung tentang penggunaan sumber daya dan status proses.
<br/>

⚫Htop menampilkan informasi yang lebih terperinci tentang penggunaan CPU, memori, swap, penggunaan jaringan, dan statistik proses. Informasi ini ditampilkan dalam tampilan yang mudah dibaca dan dapat diurutkan berdasarkan kolom tertentu.

⚫Htop Dapat mengurutkan proses berdasarkan berbagai kriteria seperti penggunaan CPU, memori, waktu, dan lain-lain. Anda juga dapat menggunakan filter untuk membatasi tampilan hanya pada proses yang sesuai dengan kriteria tertentu.

⚫dapat menghentikan atau menghentikan proses yang sedang berjalan langsung dari antarmuka Htop. Ini memungkinkan Anda untuk memantau dan mengelola proses dengan cepat dan efisien.

⚫Htop menyediakan tampilan grafis yang dapat digunakan untuk memantau penggunaan sumber daya secara visual. Grafik ini mencakup penggunaan CPU dan memori dalam bentuk histogram.

