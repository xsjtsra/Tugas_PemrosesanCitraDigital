### Nama : Fatimah Azzahra Maulida

### NIM : 2110131220020

`Pemrosesan Citra Digital - Pendidikan Ilmu Komputer FKIP`

---

# <p align=center><b>NEIGHBOURHOOD OPERATING</b></p>

<p align=justify>Neighbourhood Processing merupakan perluasan dari point atau pixel processing, dimana a
fungsi diterapkan ke piksel yang tertarik dan tetangganya. Idenya adalah untuk
memindahkan mask yang biasanya berupa persegi panjang ganjil di atas gambar yang diberikan. Lihat gambar 3.1</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201910979-7bce9ef7-199d-4178-90f8-f33d7bc3f8c6.png"></p>

### Spatial Filtering Procedure

- Proyeksikan pusat mask di atas piksel sub-gambar
- Hitung hasil kali elemen mask dengan piksel dan tetangganya menggunakan operasi dot Product ( .* )
- Jumlahkan hasil kali untuk menemukan nilai piksel terfilter yang baru. Operasi ini (penjumlahan dari perkalian) disebut **konvolusi** citra.

## <p align=center><b>Konvolusi</b></p>

<p align=justify>Konvolusi menyediakan cara untuk menggabungkan dua array, biasanya untuk ukuran
array yang berbeda, tetapi untuk dimensi array yang sama, menghasilkan array ketiga yang
mempunyai dimensi yang sama. Konvolusi dapat digunakan dalam image processing untuk menerapkan operator yang mempunyai nilai output dari piksel yang berasal dari kombinasi linear nilai input piksel tertentu.</p>

<p align=justify>Konvolusi citra adalah tehnik untuk menghaluskan suatu citra atau memperjelas citra dengan menggantikan nilai piksel dengan sejumlah nilai piksel yang sesuai atau berdekatan dengan piksel aslinya. Tetapi dengan adanya konvolusi, ukuran dari citra tetap sama, tidak berubah.</p>

Operasi konvolusi dilakukan dengan menggeser konvolusi kernel piksel per piksel. Hasil konvolusi disimpan di dalam matriks baru.

Contoh 1. Misalkan citra f(x,y) yang berukuran 5x5 dan sebuah kernel atau mask yang berukuran 3x3 masing-masing adalah sebagai berikut: 

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201913289-ca862ed7-ff5f-4e17-97ad-7a86e5511e7b.png"></p>

Operasi konvolusi antara citra f(x,y) dengan kernel g(x,y), yaitu f(x,y) * g(x,y) dapat diilustrasikan sebagai berikut: 

<p align=justify>(1) Tempatkan kernel pada sudut kiri atas, kemudian hitung nilai piksel pada posisi (0,0) dari kernel.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201913516-384a2b0e-62a4-4e26-8286-9474a5c3ce9b.png"></p>

Hasil konvolusi = 3. Nilai ini dihitung dengan cara berikut:

(0x4) + (-1x4) + (0x3) + (-1x6) + (4x6) + (-1x5) + (0x5) + (-1x6) + (0x6) = 3 

<p align=justify>(2) Geser kernel satu piksel ke kanan, kemudian hitung nilai piksel pada posisi (0,0) dari kernel:</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201913790-05f0d3ee-5a32-472c-9819-c1d6319acf6f.png"></p>

Hasil konvolusi = 0. Nilai ini dihitung dengan cara berikut:

(0x4) + (-1x3) + (0x5) + (-1x6) + (4x5) + (-1x5) + (0x6) + (-1x6) + (0x6) = 0 

<p align=justify>(3) Geser kernel satu piksel ke kanan, kemudian hitung nilai piksel pada posisi (0,0) dari kernel: </p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201913916-440d2be8-1e33-415d-8f9a-12076276b4ac.png"></p>

Hasil konvolusi = 2. Nilai ini dihitung dengan cara berikut:

(0x3) + (-1x5) + (0x4) + (-1x5) + (4x5) + (-1x2) + (0x6) + (-1x6) + (0x2) = 2 

Dengan cara yang sama, piksel-piksel pada baris kedua dan ketiga di konvolusi sehingga menghasilkan:

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201914217-eb78e45f-cdde-4417-9b51-1161bfdb9189.png"></p>

<p align=justify>Jika hasil konvolusi menghasilkan nilai piksel negative, nilai tersebut dijadikan 0. Sebaliknya jika hasil konvolusi menghasilkan nilai piksel lebih besar dari nilai keabuan maksimum (255), nilai tersebut dijadikan ke nilai keabuan maksimum.</p>

Masalah timbul bila piksel yang dikonvolusi adalah piksel pinggir, karena beberapa koefisien konvolusi tidak dapat diposisikan pada piksel-piksel citra, seperti contoh di bawah ini:

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201914701-35bcbed2-1406-4b77-9dd4-dfceaf1998b4.png"></p>

Solusi untuk masalah ini adalah:

1. piksel-piksel pinggir diabaikan, tidak dikonvolusi, jadi nilai piksel pinggir sama dengan nilai pada citra semula.
2. Duplikasi elemen citra, misalnya elemen kolom pertama disalin ke kolom M+1, begitu juga sebaliknya, lalu konvolusi dapat dilakukan terhadap pixel-pixel pinggir tersebut.
3. Elemen yang ditandai dengan “?” diasumsikan bernilai 0 atau konstanta yang lain, sehingga  konvolusi pixel-pixel pinggir dapat dilakukan.

<p align=justify>Solusi dengan ketiga pendekatan di atas mengasumsikan bagian pinggir citra lebarnya sangat kecil (hanya satu pixel) relatif dibandingkan denagn ukuran citra, sehingga pixel-pixel pinggir tidak memperlihatkan efek yang kasat mata.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201915231-873aea2a-a7cd-4436-ba26-8029e5e3d4d9.png"></p>

<p align=justify>Dalam algoritma konvolusi citra N x M dengan mask atau kernel yang berukuran 3 x 3 piksel yang dikonvolusi adalah elemen (i,j). Delapan buah piksel yang bertetangga dengan piksel (i,j) diperlihatkan pada gambar dibawah:</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/201915571-9c57f83c-ac41-4209-a5e6-f89bd12acb26.png"></p>

## <p align=center><b>Penerapan Konvolusi Pada Octave</b></p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202181702-a390d4b6-1299-42dc-90fe-9e9c1998cafd.png"></p>
<p align=center><img src="https://user-images.githubusercontent.com/112606990/202181791-a47c0761-4478-4dc2-829a-dd738b47a89c.png"></p>
<p align=center><img src="https://user-images.githubusercontent.com/112606990/202181900-0ca79daf-9891-487a-9034-e352ce83d621.png"></p>

Output :

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202182162-a5a90f6e-6450-4d28-ad72-32f687049dc7.png"></p>
