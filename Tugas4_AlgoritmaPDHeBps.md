### Nama : Fatimah Azzahra Maulida

### NIM : 2110131220020

`Pemrosesan Citra Digital - Pendidikan Ilmu Komputer FKIP`

---

# <p align=center><b>ALGORITMA PATTERNING</b></p>

Algoritma:
1. Pertama, intensitas setiap piksel dihitung pada skala 0 hingga 9. (0 menjadi intensitas terendah)
2. Kemudian setiap piksel menurut intensitasnya dipetakan ke dalam blok 3*3 .

     --- --- --- -X- -XX -XX -XX -XX XXX XXX
     
     --- -X- -XX -XX -XX -XX XXX XXX XXX XXX
     
     --- --- --- --- --- -X- -X- XX- XX- XXX
     
     9  8 7 6 5 4 3 2 1 0 (0 menjadi titik paling hitam).

    Kemudian pemetaan ke blok 3*3 berfungsi jika gambar raster yaitu saat kita membuat raster halftone dari gambar raster, tetapi untuk membuat halftone SVG kita harus     memetakan tingkat intensitas ke beberapa angka matematis.Jadi yang kami lakukan adalah, kami memetakan tingkat intensitas kami ke sebuah. Lingkaran
    b. Segi tiga
    c. Segi enam.
    0 dipetakan ke area maksimum Lingkaran/Segitiga/Segi Enam.
    
 3. Kemudian menggunakan python library svgwrite kami membuat halftone SVG.

# <p align=center><b>ALGORITMA DITHERING</b></p>

1. memuat paket yang diperlukan dan membaca dalam gambar. Perhatikan bahwa gambar berukuran 670x946 piksel, sehingga direpresentasikan sebagai larik dengan tiga          matriks (satu untuk merah, hijau, dan biru) yang 'ditumpuk di atas satu sama lain'.

2. Langkah selanjutnya adalah memprogram fungsi yang menciptakan palet warna yang lebih kecil. Saya senang bisa membuat palet warna dengan ukuran berbeda, seperti        delapan warna (3-bit), 512 warna (9-bit) atau bahkan 32.768 warna (15-bit). Oleh karena itu, fungsinya tergantung pada K, yang merupakan jumlah warna yang ingin        kita miliki di palet kita, atau ukuran bit.

3. Langkah terakhir adalah menulis fungsi yang menemukan untuk setiap piksel warna 'terdekat' dalam palet yang lebih kecil. Dimana cₖ = {Merahₖ, Hijauₖ, Biruₖ} untuk k {1,…, K} adalah warna tertentu dari palet warna tereduksi dan xᵢⱼ adalah vektor dengan intensitas untuk piksel yang kita pertimbangkan. Dalam istilah yang kurang teknis: warna terdekat adalah warna dengan jarak Euclidean kuadrat terkecil.

# <p align=center><b>ALGORITMA HISTOGRAM EQUALIZATION</b></p>

Langkah-langkah :

- Dapatkan gambar masukan
- Hasilkan histogram untuk gambar
- Temukan minimum lokal dari gambar
- Bagilah histogram berdasarkan minimal lokal
- Miliki tingkat abu-abu spesifik untuk setiap partisi histogram
- Terapkan pemerataan histogram pada setiap partisi

Algoritma :
- Hitung histogram nilai piksel dari gambar input. Histogram menempatkan nilai setiap piksel [𝑥,𝑦] ke dalam salah satu dari L ember dengan spasi seragam ℎ[𝑖]
  Dimana =2^8 dan dimensi bayangan adalah ×𝑁
- Hitung fungsi distribusi kumulatif.
- Skala gambar input menggunakan fungsi distribusi kumulatif untuk menghasilkan gambar output.

# <p align=center><b>ALGORITMA BIT PLANE SLICING</b></p>

1. Mengubah citra tingkat keabuan menjadi citra biner.
2. Mewakili gambar dengan bit yang lebih sedikit dan menyesuaikan gambar dengan ukuran yang lebih kecil
3. Meningkatkan gambar dengan memfokuskan.
