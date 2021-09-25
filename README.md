# Jarkom-Modul-1-A07-2021
Laporan resmi berisi dokumentasi soal Jarkom Modul 1.
---
Kelompok A-02:
- [Arkan Aulia Farhan](): 05111940000128
- [Muchamad Maroqi Abdul Jalil](https://github.com/maroqijalil): 05111940000143
- [Syamil Difaul Haq Sukur](https://github.com/Syamil28): 05111940000196
---

6.  Cari username dan password ketika melakukan login ke FTP Server!

Jawaban:

Display filter: **ftp.request.command == USER \|\| ftp.request.command
== PASS**

username : secretuser

password : aku.pengen.pw.aja

![](./images/image11.png)

7.  Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip,
    > 1.zip, 2.zip, \..., 499.zip. Simpan dan Buka file pdf tersebut.
    > (Hint = nama pdf-nya \"Real.pdf\")

Jawaban:

Display filter: **ftp-data contains Real.pdf**

![](./images/image9.png)

Pilih salah satu package yang terfilter, klik kanan dan klik Follow \>
TCP Stream, kemudian ganti show data as "Raw" dan Save as.

![](./images/image18.png)

Buka file "Real.pdf"

![](./images/image12.png)

8.  Cari paket yang menunjukan pengambilan file dari FTP tersebut!

Jawaban:

Display filter: **ftp.request.command == RETR**

![](./images/image6.png)

9.  Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan
    > beberapa file. Salah satunya adalah sebuah file berisi data
    > rahasia dengan nama \"secret.zip\". Simpan dan buka file tersebut!

Jawaban:

Display filter: **ftp-data**

![](./images/image23.png)

Pilih salah satu package yang ditemukan, klik kanan dan klik Follow \>
TCP Stream, kemduain ganti show data as "Raw" dan Save as.

![](./images/image8.png)

Berhasil save, lalu buka file tersebut.

![](./images/image3.png)

10. Selain itu terdapat \"history.txt\" yang kemungkinan berisi history
    > bash server tersebut! Gunakan isi dari \"history.txt\" untuk
    > menemukan password untuk membuka file rahasia yang ada di
    > \"secret.zip\"!

Jawaban:

Dsiplat filter: **ftp-data**

Find: **"history.txt"**

![](./images/image25.png)

Pilih salah satu package yang ditemukan, klik kanan dan klik Follow \>
TCP Stream.

![](./images/image24.png)

Display filter: **ftp-data**

Find: **"bukanapaapa.txt"**

![](./images/image26.png)

Pilih salah satu package yang ditemukan, klik kanan dan klik Follow \>
TCP Stream. Password file "Wanted.pdf" ditemukan, yaitu
"d1b1langbukanapaapajugagapercaya".

![](./images/image4.png)

Buka file "secret.zip"

![](./images/image22.png)

Buka file "Wanted.pdf" dengan memasukkan password tadi.

![](./images/image20.png)
