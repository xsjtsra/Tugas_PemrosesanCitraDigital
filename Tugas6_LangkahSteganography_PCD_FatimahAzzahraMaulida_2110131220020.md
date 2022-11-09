### Nama : Fatimah Azzahra Maulida

### NIM : 2110131220020

`Pemrosesan Citra Digital - Pendidikan Ilmu Komputer FKIP`

---

# <p align=center><b>STEGANOGRAPHY</b></p>

### <p align=justify>Pengertian</p>

<p align=justify>Kata steganografi berasal dari Bahasa Yunani, steganos yang artinya tersembunyi dan graphien yang artinya tulisan yang dapat diterjemahkan menjadi tulisan yang tersembunyi. Menurut Munir (2004) steganografi didefinisikan sebagai ilmu dan seni untuk menyembunyikan pesan rahasia (hiding message) sedemikian sehingga keberadaan pesan tidak terdeteksi oleh indera manusia. Media yang digunakan umumnya merupakan suatu media yang berbeda dengan media pembawa informasi rahasia, di sinilah fungsi dari teknik steganografi yaitu sebagai teknik penyamaran menggunakan media lain yang berbeda sehingga informasi rahasia dalam media awal tidak terlihat secara jelas.</p>

Dalam penyembunyian pesan ada beberapa kriteria yang perlu diperhatikan:

1. Imperceptibility. Keberadaan pesan rahasia tidak dapat dipersepsi oleh indra.
2. Fidelity. Mutu media penampung tidak berubah banyak akibat penyisipan.
3. Recovery. Pesan yang disembunyikan harus dapat diungkap kembali agar sewaktu – waktu pesan rahasia dapat diambil kembali untuk digunakan lebih lanjut.

<p align=justify>Satu hal esensial yang menjadi kelebihan steganografi adalah kemampuannya untuk menipu persepsi manusia, manusia tidak memiliki insting untuk mencurigai adanya arsiparsip yang memiliki informasi yang tersembunyi di dalamnya, terutama bila arsip tersebut tampak seperti arsip normal lainnya. Namun begitu terbentuk pula suatu teknik yang dikenal dengan steganalysis, yaitu suatu teknik yang digunakan untuk mendeteksi penggunaan steganografi pada suatu arsip. Seorang steganalyst tidak berusaha untuk melakukan dekripsi terhadap informasi yang tersembunyi dalam suatu arsip, yang dilakukan adalah berusaha untuk menemukannya. Terdapat beberapa cara yang dapat digunakan untuk mendeteksi steganografi seperti melakukan pengamatan terhadap suatu arsip dan membandingkannya dengan salinan arsip yang dianggap belum direkayasa, atau berusaha mendengarkan dan membandingkan perbedaannya dengan arsip lain bila arsip tersebut adalah dalam bentuk audio.</p>

### <p align=justify>Metode Steganografi pada Gambar menggunakan Least significant bit</p>

<p align=justify>LSB adalah teknik yang umum digunakan dalam enkripsi dan dekripsi informasi rahasia. Cara kerja metode LSB yaitu mengubah bit redundan cover image yang tidak berpengaruh signifikan dengan bit dari pesan rahasia. </p>

Encoding dilakukan dengan menggunakan langkah-langkah berikut:
 
1. Siapkan sebuah citra gambar.
2. Jika citra yang disiapkan masih dalam bentuk RGB (berwarna) maka ubah gambar menjadi skala abu-abu (grayscale).
3. Ambil ukuran dari citra (width dan height).
4. Siapkan pesan yang ingin disisipkan ke dalam citra.
5. Konversikan pesan ke format binernya.
6. Ambil nilai ASCII dari setiap huruf dari pesan yang akan disisipkan.
7. Ambil nilai biner dari pesan yang akan disisipkan.
8. Ubah biner dari pesan menjadi dalam bentuk satu baris ke samping dengan fungsi transpose dan ubah arraynya dari tipe string menjadi numerik. 
9. Inisialisasi gambar keluaran sama dengan gambar masukan.
10. Buat variabel counter yang memiliki 1 sebagai counter awal.
11. Telusuri setiap piksel gambar (menggunakan perulangan bersarang), selama counter masih kurang dari panjang pesan (length pesan) lakukan hal berikut:
    - Dapatkan LSB (Least Significant Bit) dari citra
    - Dapatkan bagian berikutnya dari pesan yang akan disematkan
    - Jika bit pesan dan LSB piksel sama, setel temp = 0
    - Jika bit pesan dan LSB piksel berbeda, setel temp = 1. Pengaturan temp ini dapat dilakukan dengan mengambil XOR bit pesan dan LSB piksel
    - Perbarui piksel gambar keluaran ke nilai piksel gambar masukan + temp
12. Terus perbarui gambar output hingga semua bit dalam pesan tertanam
13. Terakhir, tuliskan gambar input dan output ke sistem lokal
