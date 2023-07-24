# 1.Demokan penggunaan git restore
<br/>

1.Masuk kedalam folder repositori kita disini saya menggunakan sample-repo, lalu saya mengecek ada file apa saja didalamnya `ls` , selanjutnya saya akan membuat file baru `touch file4` setelah terbuat kita bisa add file tersebut dengan `git add file4` lalu commit file tersebut `git commit -m "create file4"`.

![1](/stage-1/week-2/git-restore/img/1.png)
<br/>

2.Selanjutnya kita akan menghapus file  tadi yang baru dibuat `rm file4` kita bisa melihat status file tersebut dengan `git status` disana kita mendapatkan info bahwa file4 telah dihapus.

![2](/stage-1/week-2/git-restore/img/2.png)
<br/>

3.Lalu kita bisa mengecek bahwa file4 sudah tidak ada di dalam folder kita `ls`, lalu seperti apa cara mengembalikannya? nah kita bisa menggunakan git restore untuk case ini saya mengetikan `git restore file4`, setelah selesai coba `ls` pasti disana kita akan melihat file4 sudah kembali lagi.

![3](/stage-1/week-2/git-restore/img/3.png)
<br/>

4.Langkah terakhir kita bisa add dan commit perubahan tersebut dengan, `git add .` dan juga `git commit -m "restore file4".

![4](/stage-1/week-2/git-restore/img/4.png)
<br/>

<br/>

## 2.hapus sebuah file di repository, dan kembalikan filenya dengan memeriksa versinya
<br/>

1.Kita bisa mengecek ada file apa saja didalam folder kita dengan `ls` nah disini saya ingin menghapus si file4 maka `rm file4` lalu kita bisa belihat statusnya bahwa telah terhapus `git status`.

![5](/stage-1/week-2/git-restore/img/5.png)
<br/>

2.Selnajutnya untuk melihat log atau versi dari si file4 ini kita bisa menggunakan `git log --- file4`, lalu bisa dilihat disana ada commit id dengan warna kuning yang nantinya kita akan merestore file tersebut dengan versi ini, untuk merestorenya kita bisa menggunakan git checkout di ikuti oleh versi atau commit id yang ada di dalam git log jadi seperti dibawah ini, disana kita bisa melihat bahwa file4 yang sudah kita hapus tadi sudah terestore.

![6](/stage-1/week-2/git-restore/img/6.png)
<br/>

3.Untuk langkah terakhirnya kita bisa add dan commit semua perubaha tersebut dengan perintah berikut `git add .` di ikuti dengan `git commit -m "restore file4 with version"`

![7](/stage-1/week-2/git-restore/img/7.png)
<br/>







