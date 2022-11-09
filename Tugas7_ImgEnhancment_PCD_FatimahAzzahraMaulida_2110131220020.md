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

<p align=justify></p>

<p align=justify></p>
