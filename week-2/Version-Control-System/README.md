# 1. Penjelasan Penjelasan tentang Distributed Version Control

Distributed Version Control atau (DVC) adalah metode pengelolaan versi yang memungkinkan pengembang bekerja secara terdistribusi dengan repositori yang terdistribusi secara lokal. Setiap pengembang memiliki salinan penuh dari repositori dengan sejarah lengkap perubahan. DVC, seperti Git, memungkinkan kolaborasi, fleksibilitas, dan ketahanan terhadap gangguan. Developer dapat bekerja secara independen, membuat cabang, dan menyinkronkan perubahan dengan pengembang lain. Namun, penggunaan DVC memerlukan pemahaman yang lebih dalam dan disiplin dalam mengelola versi aplikasi/software.
<br/>

# 2. buat repository sample (diluar tugas) yang berisi 3 file dengan isi yang berbeda, Buat 2 branch
<br/>

1.  Masuk ke folder project lalu buat folder `mkdir sample-repo` lalu `cd sample-repo` dan ketikan `git init`, git init digunakan untuk membuat repositori Git baru di dalam direktori proyek. Repositori ini akan melacak perubahan yang terjadi pada proyek.
<br/>

![1](/week-2/Version-Control-System/img/1.png)
<br/>

2.  Anda dapat membuat repositori baru menggunakan Command-Line Interface GitHub, GitHub CLI atau disingkat sebagai gh, adalah alat baris perintah yang memungkinkan Anda berinteraksi dengan GitHub melalui terminal. `sudo apt update && sudo snap install gh --classic`, dengan gh ini nantinya kita bisa membuat repo github langsung dari terminal.
<br/>

![2](/week-2/Version-Control-System/img/2.png)
<br/>

3. Ketikan `gh repo create sample-repo --public`, Perintah gh repo create sample-repo --public digunakan untuk membuat repositori baru dengan nama "sample-repo" di GitHub melalui CLI (Command-Line Interface) GitHub (gh). Opsi --public menentukan bahwa repositori yang dibuat akan memiliki status publik, yang berarti dapat diakses dan dilihat oleh siapa saja. dan anda juga bisa melihat status atau alamat url repo yang tadi dibuat dengan perintah `gh repo view sample-repo`.
<br/>

![3](/week-2/Version-Control-System/img/3.png)
<br/>

4. Gunakan coma touch untuk menambah 3 file sekaligus 'touch file1 file2 file3`, setelah 3 file tadi dibuat lalu `git add . `, Perintah git add . digunakan untuk menambahkan semua perubahan dalam direktori proyek ke staging area sebelum melakukan commit. Dengan menjalankan perintah ini, Anda memberitahu Git agar melacak perubahan yang ada dalam file-file proyek. Setelah perubahan ditambahkan ke staging area, Anda dapat melakukan commit untuk menyimpan perubahan-perubahan tersebut ke dalam repositori Git. 'git commit -m "Create 3 file"`.
<br/>

![4](/week-2/Version-Control-System/img/4.png)
<br/>

5. Selanjutnya adalah menambahkan remote add dan set url ke dalam repositori github, setelah selesai lakukan push dengan `git push -u origin master`.
<br/>

![5](/week-2/Version-Control-System/img/5.png)
<br/>

6. Selanjutnya membuat dua branches yang berbeda `git branch staging` dan `git branch production`.
<br/>

![6](/week-2/Version-Control-System/img/6.png)
<br/>

7. Langkah terakhir untuk mempublish semua branch yang telah kita buat ke dalam platfrom github dengan cara, `git push origin staging` dan juga `git push origin production`.
<br/>

![7](/week-2/Version-Control-System/img/7.png)
<br/>

8. Dan berikut adalah hasil dari sample repo, 3 file, dan juga 2 branch baru yang telah kita buat.

![8](/week-2/Version-Control-System/img/8.png)

