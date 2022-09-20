### Nama = Fatimah Azzahra Maulida

### NIM = 2110131220020

---

## <p align=center><b>Layer Dalam Gambar Berwarna</b></p>

<p align=justify>Dalam merepresentasikan warna dalam suatu gambar digital, model-model warna digunakan untuk menggambarkan warna dalam bentuk angka. Pada umumnya, suatu warna direpresentasikan sebagai kombinasi dari beberapa warna primer yang memiliki intensitas yang beragam. Setiap model warna menggunakan cara yang berbeda dalam merepresentasikan warna. Selain itu, warna primer yang digunakan untuk merepresentasikan suatu warna jugalah berbeda sesuai dengan masing-masing model warna. Model-model warna yang umumya digunakan adalah model warna RGB, CMYK, HSB, dan CIE - XYZ.</p>

### <p align=center><b>Model Warna RGB (Red, Green, Blue)</b></p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/191282532-8d7a0736-f5a8-4f4b-b845-b25150b8a5e9.png" width=300 heigth=300></p>

<p align=justify>Dalam mata kuliah Pemrosesan Citra Digital ini, kita berfokus pada model warna RGB. Dalam model warna RGB, warna-warna primer yang digunakan adalah merah, hijau, dan biru. Warna merah yang bercampur dengan warna hijau akan menghasilkan warna kuning; hijau dan biru akan menghasilkan warna sian; sedangkan biru dan merah akan menghasilkan warna magenta. Gabungan antara warna biru, merah, dan hijau dalam intensitas penuh akan menghasilkan warna putih. Model ini sangat cocok dengan psikologi mata manusia yang memiliki reseptor terhadap tiga warna utama ini.</p>

<p align=justify>Jadi kesimpulannya adalah gambar berwarna memiliki 3 layer yaitu layer red(merah), layer green(hijau), dan layer blue(biru). Yangmana jika ketiga layer tersebut digabung, maka akan menghasilkan warna-warna lainnya. Setiap warna memiliki nilai dari 0-225.</p>

### <p align=center><b>Eksplorasi Layer Gambar Berwarna Menggunakan Octave</b></p>

**Keterangan:**
- foto = nama variabel dimana file Image itu disimpan
- imread = fungsi untuk membaca file image itu berada
- subplot = fungsi untuk memasukan objek kedalam 1 figure
- imshow =  fungsi untuk menampilkan objek gambar
- imhist  = Fungsi untuk menampilkan image dengan bentuk histogram
- Tanda : berarti semua nilai.

Berikut langkah-langkahnya:
1. Gunakan fungsi imread untuk bisa membaca citra sebuah gambar.

<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277201-6f753090-5e17-452f-b30b-95ad9a6737f6.png" width=900 heigth=100></p>

<p align=justify>Seperti yang terlihat pada gambar diatas, kita buat dulu sebuah variabel yang berisi fungsi imread disertai alamat/lokasi dari gambar yang akan dieksplor. Sudah dijelaskan secara singkat pada keterangan apa fungsi dari imread, jadi disini kita gunakan fungsi tersebut agar citra dari gambar bisa diketahui keberadaannya. Kemudian pada baris ke-2 ada fungsi imshow, sudah dijelaskan juga secara singkat pada keterangan apa fungsi dari imshow, ketikkan imshow(nama variabel yang sebelumnya dibuat);, maka saat dirun akan muncul gambar yang sudah dimasukkan alamatnya ke variabel pada baris sebelumnya.</p>

2. Gunakan cara mengakses elemen matriks untuk mengambil image citra RGB

<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277198-6aa838bd-ab18-4ab8-b2c9-8b4788428786.png" width=400 heigth=150></p>

<p align=justify>Seperti yang terlihat pada gambar diatas, kita buat dulu 3 variabel yang melambangkan RGB yang berisi nama gambar, lalu (:,:,1) berarti mengambil baris satu semua kolom, begitu juga dengan baris dua dan tiga. Jadi layer 1 adalah red, layer 2 adalah green, dan layer 3 adalah blue.</p>

3. Mengatur letak RGB

<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277192-2cb91f67-8c2c-4b8d-bb28-9b6c53f3355e.png" width=400 heigth=150></p>

<p align=justify>Seperti yang terlihat pada gambar diatas, kita buat dulu 3 variabel yang berisi fungsi cat. Fungsi cat adalah untuk nantinya bisa menampilkan gambar pada layer-layer tertentu. 3 adalah jumlah dari layer. Misal kita menginginkankan citra gambar merah, maka kalikan variabel hijau dan biru yang sebelumnya dibuat dengan 0, sehingga hanya tersisa layer merah.</p>
<p align=justify>Sedangkan pada baris 11 adalah untuk menentukan ukuran baris dan kolom.</p>

4. Menampilkan citra gambar asli

<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277189-4e855726-56b4-4a06-8244-629ee25c0c21.png" width=400 heigth=150></p>

<p align=justify>figure(1) adalah tampilan saat dirun nanti, jadi disini nantinya ada dua output yaitu figure(1) dan figure(2). Subplot sebelumnya sudah dijelaskan secara singkat di keterangan, jadi nantinya citra gambar asli akan terletak di figure pertama. Untuk fungsi imshow sudah dijelaskan pada langkah ke-1. Fungsi title adalah untuk memberikan nama/judul pada gambar yang ditampilkan dengan fungsi imshow sebelumnya.</p>

<p align=justify>Fungsi imhist adalah untuk menampilkan histogram dari gambar, histogram merupakan representasi grafik yang menunjukkan impresi visual dari distribusi sekelompok data.Histogram disini adalah representasi greyscale dari sebuah gambar.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277187-d1c87cfb-02d6-4826-af86-cebe9eb0c961.png" width=400 heigth=150></p>
<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277186-79990bb8-5c07-4f4e-8a33-a8b6724e3619.png" width=400 heigth=150></p>
<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277179-3144bf1f-74d3-42c3-a5cb-28a97d12b65c.png" width=400 heigth=150></p>

**Berikut kode lengkap dalam octave dan outputnya:**

<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277173-416a64aa-8446-4050-ab57-0c7be16e3120.png" width=400 heigth=150></p>

<p align=justify>Figure(1) berisi citra gambar asli beserta histogramnya dan citra gambar merah beserta histogramnya:</p>
<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277163-1f3ab9b3-67f5-480e-882c-64b9a5c3ff5b.png" width=400 heigth=150></p>

<p align=justify>Figure(2) berisi citra gambar hijau beserta histogramnya dan citra gambar biru beserta histogramnya:</p>
<p align=center><img src="https://user-images.githubusercontent.com/112606990/191277154-b8cc9695-6e24-4993-8ee2-1952ea0a45a9.png" width=400 heigth=150></p>
