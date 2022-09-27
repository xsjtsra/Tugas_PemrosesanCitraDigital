### Nama : Fatimah Azzahra Maulida

### NIM : 2110131220020

`Pemrosesan Citra Digital - Pendidikan Ilmu Komputer FKIP`

---

# <p align=center><b>ULASAN HALFTONING</b></p>

<p align=justify>Halftoning adalah teknik reprografis yang mensimulasikan continuous-tone melalui penggunaan titik-titik, bervariasi baik dalam ukuran atau dalam jarak, sehingga menghasilkan efek seperti gradien.</p>

<p align=justify>Jika continuous-tone berisi rentang warna atau abu-abu yang tak terbatas, proses halftoning mengurangi reproduksi visual menjadi gambar yang dicetak hanya dengan satu warna tinta, dalam titik dengan ukuran berbeda (modulasi lebar pulsa) atau spasi (modulasi frekuensi) atau keduanya. Reproduksi ini bergantung pada ilusi optik dasar: ketika titik halftone kecil, mata manusia menafsirkan area berpola seolah-olah itu adalah nada halus. Pada tingkat mikroskopis, film fotografi hitam-putih yang dikembangkan juga hanya terdiri dari dua warna, dan bukan rentang nada kontinu yang tak terbatas.</p>

<p align=justify>Menurut saya, halftoning itu adalah suatu teknik untuk mengubah gambar menggunakan titik-titik yang bentuknya bervariasi dan jaraknya juga bervariasi, teknik ini hanya menggunakan satu warna yaitu hitam. Namun karena bentuk dan jaraknya bervariasi, hal ini membuat mata manusia melihat gambar tersebut menjadi seperti memiliki beberapa warna yang berbeda-beda.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192519922-08bb0891-bc49-40cc-9f2d-792dd20f574b.png"></p>

Ada 2 teknik yang bisa digunakan untuk melakukan halftoning:

## **1. Patterning**

<p align=justify>Patterning (pola) adalah teknik yang paling sederhana untuk menghasilkan gambar halftoning digital. Teknik ini menghasilkan gambar yang memiliki resolusi spasial lebih tinggi daripada gambar sumber. Jumlah sel halftone citra keluaran sama dengan jumlah piksel citra sumber. Namun, setiap sel halftone dibagi lagi menjadi kotak 4x4. Setiap nilai piksel input diwakili oleh jumlah kotak terisi yang berbeda dalam sel halftone. Karena kisi 4x4 hanya dapat mewakili 17 tingkat intensitas yang berbeda, gambar sumber harus dikuantisasi.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192524874-b9986475-1b77-4bfa-9ccf-70ebfd517524.png"></p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192525016-746be637-7713-4165-bc9d-15510eefbd3e.png"></p>

## **1. Dithering**

<p align=justify>Teknik lain yang digunakan untuk menghasilkan gambar halftoning digital adalah dithering. Tidak seperti patterning, dithering membuat gambar keluaran dengan jumlah titik yang sama dengan jumlah piksel pada gambar sumber. Dithering dapat dianggap sebagai thresholding gambar sumber dengan matriks dither. Matriks diletakkan berulang kali di atas gambar sumber. Dimanapun nilai piksel gambar lebih besar dari nilai dalam matriks, titik pada gambar output diisi. Masalah dithering yang terkenal adalah menghasilkan artefak pola yang diperkenalkan oleh matriks ambang batas tetap.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192526398-1a8e99d3-d808-44e6-9e98-17490de485fc.png"></p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192526429-db2bca66-f830-43d1-bccb-6a3aec429225.png"></p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192526483-9dd99da4-0512-4269-aaeb-a072e1bf2f8e.png"></p>

Contoh implementasi dari pattering dan dithering pada gambar yang sama:

##### <p align=center>Gambar asli</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192531686-aa5b8c7a-466e-49f9-b23a-96085e0aa31a.png"></p>

##### <p align=center>Pattering</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192532072-43ea8325-93c9-4ae0-b16f-19aa73b13448.png" height=200 width=200></p>

##### <p align=center>Dithering</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192532185-7a30a1fd-65b7-49d7-a0f5-35c45fe1b5a5.png"></p>

<p align=justify>Menurut saya, setelah melihat dari perbedaan gambar diatas, teknik dithering lebih bagus hasil dibandingkan dengan teknik pattering. Karena teknik dithering membuat gambar dengan jumlah titik yang sama dengan jumlah piksel pada gambar aslinya. Sehingga gambar yang dihasilkan akan sama bentuknya walaupun setelah di halftoning. Sedangkan teknik pattering setiap sel halftone dibagi lagi menjadi kotak 4x4, jadi setiap nilai piksel input diwakili oleh jumlah kotak terisi yang berbeda dalam sel halftone. Karena kisi 4x4 hanya dapat mewakili 17 tingkat intensitas yang berbeda. Sehingga nantinya output dari teknik pattering akan lebih besar (zoom in) di bandingkan dengan gambar aslinya.</p>
