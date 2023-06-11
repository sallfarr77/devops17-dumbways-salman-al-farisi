# Application in Server
<br/>

## 1. Berikut adalah beberapa perbedaan antara Monolith dan Microservices
<br/>

### 1. Adalah di dalam Arsitekturnya:
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
