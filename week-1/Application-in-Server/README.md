# Application in Server
<br/>

## 1. Berikut adalah beberapa perbedaan antara Monolith dan Microservices
<br/>

### 1. dalam Arsitekturnya:
<br/>

**Monolith:** Monolith adalah pendekatan di mana seluruh aplikasi dikembangkan sebagai satu unit yang besar. Semua komponen, fungsi, dan layanan tergabung menjadi satu kesatuan.
Microservices: Arsitektur microservices memecah aplikasi menjadi bagian-bagian yang lebih kecil yang disebut layanan independen. Setiap layanan memiliki tanggung jawab spesifik dan berkomunikasi melalui antarmuka yang didefinisikan dengan baik.
<br/>

**Microservices:** Arsitektur microservices memecah aplikasi menjadi bagian-bagian yang lebih kecil yang disebut layanan independen. Setiap layanan memiliki tanggung jawab spesifik dan berkomunikasi melalui antarmuka yang didefinisikan dengan baik.
<br/>
<br/>

### 2. Skalabilitas:
<br/>

**Monolith:** Skalabilitas monolith biasanya vertikal, yang berarti Anda harus meningkatkan sumber daya server (CPU, RAM) secara keseluruhan untuk meningkatkan kapasitas aplikasi.
<br/>

**Microservices:** Dalam arsitektur microservices, Anda dapat melakukan skalabilitas secara horizontal dengan menambah atau mengurangi instance dari layanan tertentu sesuai kebutuhan.
<br/>
<br/>

### 3. Fleksibilitas:
<br/>

**Monolith:** Dalam monolith, perubahan pada salah satu komponen dapat mempengaruhi seluruh aplikasi. Perubahan dalam satu fitur mungkin memerlukan pengujian dan pengiriman kembali keseluruhan aplikasi.
<br/>

**Microservices:** Dalam microservices, setiap layanan independen dapat diperbarui dan dideploy secara terpisah. Ini memberikan fleksibilitas dalam mengubah, memperbarui, dan mengganti layanan tanpa mempengaruhi aplikasi secara keseluruhan.
<br/>

<br/>

## 2. Deploy Aplikasi wayshub-frontend dengan menggunakan NodeJS

1. Pertama-tama kita bisa membuat folder project terlebih dahulu dengan menggunakan comand `mkdir`.

![1](/week-1/Application-in-Server/img/1.png)

2. setelah membuat folder project kita lalu meng clone website wayshub dengan mengambilnya langsung dari repositori github dengan perintah `git clone https://github.com/dumbwaysdev/wayshub-frontend`.

![2](/week-1/Application-in-Server/img/2.png)

3. Setelah selesai meng-clone lalu kita masuk ke folder wayshub dengan comand `cd` lalu di dalam folder kita harus menginstall semua dependensi dan package yang di perlukan, kita bisa melakukannya dengan cukup mengetikan `npm install`

![3](/week-1/Application-in-Server/img/3.png)

4. Kita juga bisa memperbaiki keamanan dengan `npm audit fix`.

![4](/week-1/Application-in-Server/img/4.png)

5. Selanjutnya kita bisa membangun website kita dengan comand `npm run build`.

![5](/week-1/Application-in-Server/img/5.png)

6. Lalu kita akan mengetikan comand `npm install -g serve` Perintah npm install -g serve digunakan untuk menginstal global package "serve" dalam lingkungan Node.js menggunakan NPM (Node Package Manager).

![6](/week-1/Application-in-Server/img/6.png)

7. Selanjutnya ketikan `serve -s build` Perintah serve -s build digunakan untuk menjalankan server lokal menggunakan paket "serve" dan menyajikan berkas-berkas yang ada dalam direktori build.

![7](/week-1/Application-in-Server/img/7.png)

8. Setelah itu kita bisa langsung mengecek menggunakan local host atau alamat ip computer kita di browser dan ini adalah website wayshub yang telah kita berhasil deploy.

![8](/week-1/Application-in-Server/img/8.png)
<br/>

<br/>

## 3. Deploy Golang dengan menampilkan nama kita

1. Pertama kita harus menginstall bahasa pemograman golang terlebih dahulu di os ubuntu kita, sebelumnya kita akan meng update repositori ubuntu dengan comand `sudo apt update && sudo apt upgrade -y`.

![9](/week-1/Application-in-Server/img/9.png)

2. Setelah selesai mengupdate repo ubuntu kita akan membuat folder baru yang akan kita berinama golang di dalam folder project yang telah kita buat.

![10](/week-1/Application-in-Server/img/10.png)

3. Selanjutnya kita bisa menginstall golang resmi dari repositori ubuntu dengan simpelnya mengetikan comand `sudo apt install golang` lalu kita tunggu sampai proses installasi selesai.

![11](/week-1/Application-in-Server/img/11.png)

4. Selanjutnya kita akan membuat file baru dengan nama `print-name.go` go sendiri adalah ekstensi dari golong ketikan comand berikut: `nano print name.go`
dan ketikan kode yang ada dibawah gambar ini.

![12](/week-1/Application-in-Server/img/12.png)

5. Setelah selesai kita bisa keluar dari nano dengan menekan tombol ctrl+x yang ada di keyboard, dan ketikan comand `go build print-name.go` untuk membangun aplikasi golang yang telah kita buat.

![13](/week-1/Application-in-Server/img/13.png)

6. Setelah selesai membangun file tadi kita akan notice bahwa ada file baru di folder kita dengan nama print-name, kita bisa langsung menjalankan file tersebut dengan mengetikan `./print-name` di terminal dan kode tersebut akan berjalan dan menampilkan nama kita.

![14](/week-1/Application-in-Server/img/14.png)
<br/>

<br/>

## 4. Deploy Python dengan menampilkan nama kita

1. Untuk langkah pertama sama seperti project golang, kita bisa membuat folder terlebih dahulu di dalam project kita bernama python, karna python sudah hampir terinstall semua secara bawaan di hampir semua distro linux jadi kita hanya akan menginstall pip dengan comand `sudo apt install pip`.

![15](/week-1/Application-in-Server/img/15.png)

2. Setelah pip terinstall, kita akan membuat file baru dengan ekstensi .py dengan nama print-name.py dan kita juga akan menginstall flask untuk menyajikan code kita yang akan di tampilkan didalam web browser, kita bisa menginstall flask dengan comand `pip install flask`.

![16](/week-1/Application-in-Server/img/16.png)

3.  Tuliskan code seperti di bawah ini, lalu setelah selesai kita akan keluar dari nano dengan menekan tombol ctrl+x.

![17](/week-1/Application-in-Server/img/17.png)

4. Setelah selesai kita bisa menjalankan script tersebut dengan perintah `python3 print-name.py` disana flask akan memberi tahu bahwa script kita telah running di local host maupun jaringan local kita.

![18](/week-1/Application-in-Server/img/18.png)

5. Terakhir kita bisa mengecek di browser dengan mengetikan alamat ip addres computer kita dan disana akan muncul nama kita.

![19](/week-1/Application-in-Server/img/19.png)
