### Nama : Fatimah Azzahra Maulida

### NIM : 2110131220020

`Pemrosesan Citra Digital - Pendidikan Ilmu Komputer FKIP`

---

# <p align=center><b>IMAGE ENHANCEMENT</b></p>

<p align=justify>Image Enhancement disebut juga perbaikan citra. Perbaikan citra bertujuan untuk meningkatkan kualitas tampilan citra untuk pandangan manusia atau untuk mengkonversi suatu citra agar memiliki format yang lebih baik sehingga citra tersebut menjadi lebih mudah untuk diolah dengan mesin (komputer).</p>

<p align=justify>Yang dimaksud dengan perbaikan kualitas citra adalah proses memperjelas dan mempertajam ciri/fitur tertentu dari citra agar citra lebih mudah dipersepsi maupundianalisis secara lebih teliti. Secara matematis, image enhancement dapat diartikan sebagai proses mengubah citra f(x, y) menjadi f’(x,y), sehingga ciri-ciri yang dilihat pada f(x, y) lebih ditonjolkan. Image enhancement tidak meningkatkan kandungan informasi, malainkan jangkauan dinamis dari ciri agar bisa dideteksi lebih mudah dan tepat.</p>

Proses-proses yang termasuk ke dalam perbaikan kualitas citra :
1. Pengubahan kecerahan gambar (image brightness)

    Untuk membuat citra lebih terang atau lebih gelap, kita melakukan perubahan kecerahan gambar. Kecerahan gambar dapat diperbaiki dengan mnambahkan (atau mengurangi) sebuah konstanta kepada (atau dari) setiap pixel di dalam citra. Akibat dari operasi ini, histogram citra mengalami pergeseran. Secara matematis operasi ini ditulis f(x, y)' = f(x, y) + b Jika b positif, kecerahan gambar bertambah, sebaliknya jika b negatif kecerahan gambar berkurang.

2. Peregangan kontras (contrast stretching)

    Kontras menyatakan sebaran terang (lightness) dan gelap (darkness)di dalam sebuah gambar. Citra dapat dikelompokkan ke dalam tiga kategori kontras : citra kontras-rendah (low contrast), citra kontras-bagus (good contrast atau normal contrast), dan citra kontras-tinggi (high contrast). Ketiga kategori ini umumnya dibedakan secara intuitif.

    Citra kontras-rendah dicirikan dengan sebagian besar komposisi citranya adalah terang atau sebagian besar gelap.Dari histogramnya terlihat sebagian besar derajat keabuannya terkelompok (clustered) bersama atau hanya menempati sebagian kecil dari rentang nilai-nilai keabuan.
    
    Citra kontras-bagus memperlihatkan jangkauan nilai keabuan yang lebar tanpa ada suatu nilai yang mendominasi. Histogram citranya memperlihatkan sebaran nilai keabuan yang relatif seragam.
    
    Citra kontras-tinggi, memiliki jangkauan nilai keabuan yang lebar tetapi terdapat area yang lebar yang didominasi warna gelap dan area lebar yang didominasi oleh warna terang.

3. Pengubahan histogram citra.

    Untuk memperoleh histogram citra sesuai dengan keinginan, maka
penyebaran nilai - nilai intensitas pada citra harus dirubah. Terdapat dua
metode pengubahan citra berdasarkan histogram :

      a. Perataan histogram (histogram equalization)
        
        Nilai-nilai intensitas di dalam citra harus diubah sehingga penyebarannya seragam (uniform)
       
      b. Spesifikasi histogram (histogram specification)
        
        Nilai-nilai intensitas dalam citra diubah agar diperoleh histogram dengan bentuk yang dispesifikasikan oleh pengguna.

4. Pelembutan citra (image smoothing)

    Pelembutan citra bertujuan untuk menekan gangguan (noise) pada citra. Gangguan tersebut biasanya muncul sebagai akibat dari hasil penerokan yang tidak bagus (sensor nosie, photographic grain noise) atau akibat saluran transmisi (pada pengiriman data). Gangguan pada citra umumnya berupa variasi suatu pixel yang tidak berkolerasi dengan pixel- pixel tetangganya. Secara visual, gangguan mudah dilihat oleh mata karena tampak berbeda dengan pixel tetangganya.


5. Penajaman (sharpening) tepi (edge)

    Bertujuan untuk memperjelas tepi pada objek di dalam citra. Penajaman citra merupakan kebalikan dari operasi pelembutan citra karena operasi ini menghilangkan bagian citra yang lembut. Operasi penajaman dilakukan dengan melewatkan citra pada penapis lolos-tinggi (high-pass
filter). Penapis lolos-tinggi akan meloloskan (atau memperkuat) komponen yang berfrekuensi tinggi dan akan menurunkan komponen berfrekuensi rendah.

6. Penawaran semu (pseudocoloring)

    Pewarnaan semu adalah proses memberi warna tertentu pada nilai- nilai pixel suatu citra skala abu-abu pada suatu citra berdasarkan kriteria tertentu, misalnya suatu warna tertentu untuk suatu interval derajat keabuan tertentu. Hal ini dilakukan karena manusia mudah membedakan banyak jenis warna.

7. Pengubahan geometrik

    Koreksi geometrik dilakukan pada citra yang memiliki gangguan yang terjadi pada waktu proses perekaman citra, misalnya pergeseran koordinat citra (translasi), perubahan ukuran citra, dan perubahan orientassi koordinat citra (skew). Proses koreksi geometri untuk meningkatkan kualitas citra tersebut disebut juha koreksi geometri. Koreksi geometri yang sederhana adalah dengan operasi geometri sederhana seperti rotasi, translasi, dan, penskalaan citra.

Image enhancement memiliki dua pendekatan metode:

### Spatial Domain Method

<p align=justify>Nilai piksel dengan koordinat (x,y) pada citra F yang disempurnakan adalah
hasil dari melakukan beberapa operasi pada piksel di sekitar
(X, y) pada gambar masukan, F. Lingkungan dapat berbentuk apa saja, tetapi biasanya
mereka persegi panjang.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/200951618-82e5abb2-6f9b-499a-bc85-166c2bd8f7fb.png"></p>

<p align=justify>Pengolahan Citra dalam domain spasial dapat dinyatakan dengan: g (m, n) -T (f
(M N)). Dimana f (m, n) adalah gambar input, g (m, n) adalah Gambar yang diproses
dan T adalah operator yang mendefinisikan proses modifikasi. Operator -T, adalah
biasanya fungsi bernilai tunggal dan monoton yang dapat beroperasi pada
piksel individu atau pada nilai selektif dari input Gambar digunakan untuk
menghitung nilai piksel yang datang untuk Gambar keluaran. Dalam
gambar input digunakan untuk menghitung gambar yang dimodifikasi pada titik tertentu.
Seseorang dapat mempertimbangkan pemrosesan titik sebagai kasus khusus pemrosesan wilayah
di mana wilayah terdiri dari satu piksel. Pemrosesan poin
operator juga dapat dinyatakan dengan: S-T(r), Dimana r dan s adalah variabel
menyatakan tingkat intensitas flm, n) dan g(m ,n) pada sembarang titik (m ,n). Itu
bagian berikut menjelaskan beberapa gambar berbasis titik dan wilayah
teknik peningkatan. Artikel kedua juga akan membahas spasial
smoothing, yang merupakan contoh lain dari pemrosesan gambar berbasis wilayah,
dan bandingkan kelebihan dan kekurangannya dengan domain transformasi
metode. Lingkungan terkecil yang mungkin berukuran 1 X 1. Dalam hal ini g
hanya bergantung pada nilai lemak satu titik (x,y) dan T.</p>

#### Basic Spatial Filtering

<p align=justify>Proses penyaringan spasial terdiri dari hanya memindahkan topeng filter dari
titik ke titik dalam gambar. Di setiap titik, respons filter dihitung
menggunakan hubungan yang telah ditentukan. Di sini dua filter spasial menghaluskan -
mean dan median dibahas. Tujuan dari pemfilteran gambar adalah untuk mengurangi derau impuls atau derau Gaussian
menggunakan Filter Median dan Mean. Operasi pemfilteran median 2-D adalah
dilakukan dengan menggeser jendela P x P ke seluruh gambar dan mengganti
piksel tengah dengan median piksel di jendela itu.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/200951944-7827b036-31b6-4520-afa0-f40f11f10e86.png"></p>

<p align=justify>Dimana: y(m,n), v(n,m) adalah gambar input dan gambar output W adalah</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/200952009-211e109b-be83-4e9b-9646-69d937772149.png"></p>

<p align=justify>Jelas, P harus bilangan bulat ganjil untuk menentukan piksel pusat. Itu
nilai piksel berlapis disimpan dalam matriks lain, yang membentuk
gambar yang diproses. Filter rata-rata bekerja dengan cara yang sama seperti di atas kecuali itu
versi piksel tengah yang difilter adalah rata-rata jendela. Berarti dan
filter median efektif untuk mengurangi berbagai jenis kebisingan.
Eksperimen dengan detektor tepi Roberts dan Sobel menunjukkan bahwa kita
perlu menggabungkan penyaringan lolos rendah (atau pemulusan) dengan turunan
operator jika kita ingin menghasilkan peta tepi yang tidak mengandung noise
tepi palsu. Efek dari penyaringan lolos rendah dalam domain spasial adalah untuk
mengaburkan tepi tajam, dan karenanya meningkatkan ketidakpastian tentang
lokasi tepi. Faktanya, ingatlah bahwa kami menggunakan penyaringan lolos tinggi
technigue (unsharp masking) untuk meningkatkan kontras tepi. Dengan adanya
Seringkali dalam desain filter yang optimal, deteksi tepi melibatkan dua hal:
tujuan yang saling bertentangan: pembatalan kebisingan dan minimalisasi spasial
menghaluskan.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/200952094-8209ecac-33ea-4710-a1f4-804c05ddc40b.png"></p>

### Frequency Domain Method

<p align=justify>Teknik domain frekuensi didasarkan pada manipulasi
transformasi ortogonal gambar daripada gambar itu sendiri. Freguency
teknik domain cocok untuk memproses gambar sesuai dengan
konten frekuensi. Prinsip di balik metode domain frekuensi
peningkatan gambar terdiri dari komputasi transformasi kesatuan diskrit 2-D
gambar, misalnya DFT 2-D, memanipulasi transformasi
koefisien oleh operator M, dan kemudian melakukan transformasi terbalik.
Transformasi ortogonal dari gambar memiliki dua komponen besar dan
fase. Besarnya terdiri dari konten frekuensi gambar. Itu
Fase ini digunakan untuk mengembalikan citra kembali ke domain spasial. Biasa
transformasi ortogonal adalah transformasi kosinus diskrit, Fourier diskrit
transform, Hartley Transform, dll. Domain transformasi memungkinkan operasi
pada konten frekuensi gambar, dan oleh karena itu frekuensi tinggi
konten seperti tepi dan informasi halus lainnya dapat dengan mudah ditingkatkan.</p>

<p align=justify>Konsep penyaringan lebih mudah divisualisasikan dalam domain frekuensi.
Oleh karena itu, peningkatan flx gambar, y) dapat dilakukan dalam frekuensi
domain berbasis DFT. Hal ini sangat berguna dalam konvolusi jika
luas spasial dari titik sebaran seguence h(x,y) besar maka konvolusi
teori.</p>

G(x,y) = h(x,y)*f(x,y)

Where g(x, y) is enhanced image.

There are three basic steps to freguency domain filtering:

1. The image must be transformed from the spatial domain into the
freguency domain using the Fast Fourier transform.

2. The resulting complex image must be multiplied by a filter (that usually
has only real values).

3. The filtered image must be transformed back to the spatial domain.

#### Jenis filter domain frekuensi

1) Low Pass Filter

Filter lolos rendah ada dalam berbagai bentuk, termasuk sirkuit elektronik
(seperti filter desis yang digunakan dalam audio), filter anti-aliasing untuk pengkondisian
sinyal sebelum konversi analog-ke-digital, filter digital untuk menghaluskan
kumpulan data, penghalang akustik, pengaburan gambar, dan sebagainya. bergerak
operasi rata-rata yang digunakan di bidang-bidang seperti keuangan adalah jenis
lulus filter, dan dapat dianalisis dengan teknik pemrosesan sinyal yang sama
seperti yang digunakan untuk filter low-pass lainnya. Filter low-pass memberikan hasil yang lebih halus
bentuk sinyal, menghilangkan fluktuasi jangka pendek, dan meninggalkan
tren jangka panjang. 

<p align=center><img src="https://user-images.githubusercontent.com/112606990/200950822-b81e8a18-fcb6-4f71-94ce-fea6b968d1ab.png"></p>

Di mana D0 adalah kuantitas non-negatif yang ditentukan, dan D (u,v) adalah jarak
dari titik ke pusat persegi panjang frekuensi.

<p align=center><img src="https://user-images.githubusercontent.com/112606990/200951017-9541109a-494e-4bda-b2df-5e4825f0abec.png"></p>

2) High Pass Filter

Pemfilteran lolos tinggi berarti kita menyaring frekuensi rendah dari
sesuatu, dan biarkan pita frekuensi tinggi lewat. Dalam istilah gambar, ini
berarti detail gambar disimpan, sedangkan gradien skala yang lebih besar
dihapus. Untungnya, itu tidak serumit kedengarannya. Lulus tinggi yang ideal
filter HPF didefinisikan sebagai:

<p align=center><img src="https://user-images.githubusercontent.com/112606990/200951078-11eb991b-c9df-4b8e-8b6a-7aac5018cb8f.png"></p>

Dimana D0 jarak potong diukur dari jarak dari titik asal
dari persegi panjang frekuensi, dan D (u,v) adalah jarak dari titik asal
Transformasi Fourier, u & v adalah variabel frekuensi dari transformasi Fourier.
Filter ini adalah kebalikan dari filter lolos rendah Ideal yang memusatkan semua perhatian
frekuensi di dalam lingkaran berjari-jari D, saat melewati tanpa redaman
setiap freguency di luar lingkaran.

<p align=center><img src="https://user-images.githubusercontent.com/112606990/200951123-f4341dc6-7d8b-4a97-8aec-5bc8c8562e53.png"></p>

<p align=justify></p>

<p align=justify></p>

<p align=justify></p>

<p align=justify></p>
