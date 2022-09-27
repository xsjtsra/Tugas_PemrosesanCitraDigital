### Nama : Fatimah Azzahra Maulida

### NIM : 2110131220020

`Pemrosesan Citra Digital - Pendidikan Ilmu Komputer FKIP`

---

# **PENGAPLIKASIAN KETIGA RUMUS UNTUK MENGUBAH RGB MENJADI GREYSCALE**

## **Lightness Method**

##### <p align=center>Rumus lighness method</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192546284-03b3f8a3-c29e-4201-963b-3d9a4e903f16.png" width=600 heigth=80></p>

##### <p align=center>Output lightness method</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192545755-550d0db9-b9dc-4ef2-bb06-6d5071ddb66d.png"></p>

<p align=justify>Seperti yang terlihat pada gambar diatas, lightness method menghasilkan greyscale yang terlalu gelap karena rumus yang digunakan sangat sederhana. Karena sebenarnya setiap channel(R,G,B) memiliki berat yang berbeda satu sama lain.</p>

## **Lightness Method**

##### <p align=center>Rumus Average method</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192548601-eb6c0065-ccb8-4312-832e-0fdcee238894.png" width=600 heigth=80></p>

##### <p align=center>Output Average method</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192548819-ae5912a1-9097-4c45-a9f8-82063e72c3f1.png"></p>

<p align=justify>Seperti yang terlihat pada gambar diatas, average method menghasilkan greyscale yang lebih terang jika dibandingkan dengan lightness method, hal ini karena rumus yang digunakan sudah memuat berapa berat dari masing-masing channel(R,G,B), walaupun beratnya masih sama. Setiap channel memiliki berat yang berbeda karena mata manusia cenderung lebih sensitif ke warna hijau, lalu merah, kemudisn biru. Jadi diperlukan berat yang berbeda-beda pada setiap channel.</p>

## **Luminosity Method**

##### <p align=center>Rumus Luminosity method</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192549375-44b0d86b-878a-44a8-bf91-9bd6406a7c4b.png" width=600 heigth=80></p>

##### <p align=center>Output Luminosity method</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/192549460-36aa98e5-3d25-4549-845d-d6cb0e3aba13.png"></p>

<p align=justify>Seperti yang terlihat pada gambar diatas, luminosity method menghasilkan greyscale yang paling bagus jika dibandingkan dengan method-method yang lain, hal ini karena rumus yang digunakan sudah memuat berapa berat dari masing-masing channel(R,G,B) dengan berat yang berbeda-beda.</p>

##### <p align=center>Semua kode pada octave</p>
<p align=center><img src="https://user-images.githubusercontent.com/112606990/192546109-5ae59f51-0a51-488b-a2b2-72f92bc04f74.png" width=700 heigth=450></p>
