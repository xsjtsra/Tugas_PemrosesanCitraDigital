### Nama : Fatimah Azzahra Maulida

### NIM : 2110131220020

`Pemrosesan Citra Digital - Pendidikan Ilmu Komputer FKIP`

---

`Tugas ini diberikan oleh Pa Harja saat praktikum PCD`

# <p align=center><b>IMPLEMENTASI KODE SENDIRI (HISTOGRAM DAN HISTOGRAM EQUALIZATION)</b></p>

## Histogram

<p align=justify>Histogram citra adalah grafik yang menggambarkan penyebaran nilai-nilai intensitas piksel dari suatu citra atau bagian tertentu di dalam citra. Dari histogram akan didapatkan frekuensi kemunculan nisbi (relative) dari intensitas pada citra tersebut. Selain itu, histogram juga menunjukkan kecerahan (brightness) dan kontras (contrast) dari sebuah citra. Oleh karena itu, histogram dapat digunakan sebagai salah satu metode pengolahan citra yang bekerja secara kualitatif dan kuantitatif (Putra, 2010). Pada citra digital yang memiliki L derajat keabuan yaitu dari 0 sampai L-1, histogram citra secara matematis dapat dihitung dengan rumus berikut:
</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202190128-87eca417-89b6-4798-befd-1d12c20bef39.png"></p>

<p align=justify>dengan niadalah jumlah pixel yang memiliki derajat keabuan i, n adalah jumlah seluruh piksel di dalam citra.</p>

<p align=justify>Histogram citra merupakan diagram yang menggambarkan distribusi frekuensi nilai intensitas piksel dalam suatu citra. Sumbu horizontal merupakan nilai intensitas piksel sedangkan sumbu vertikal merupakan frekuensi/jumlah piksel.</p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202190638-8d6fb062-bd15-48bf-920f-dc62f8e6bb5d.png"></p>

## Implementasi kode manual (Histogram)

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202204695-8ed19caf-ea4b-48db-9fe8-3c1993c9b4af.png"></p>

Output:

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202204830-7094d8ed-21d0-470a-93cc-44e937dd98f9.png"></p>

## Histogram Equalization

<p align=justify>Histogram Equalization adalah suatu proses perataan histogram, dimana distribusi nilai derajat keabuan pada suatu citra dibuat rata. Untuk dapat melakukan histogram
equalization ini diperlukan suatu fungsi distribusi kumulatif yang merupakan kumulatif dari histogram. </p>

Contoh:

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202192565-95a314f5-9e57-41f0-9db8-ec2b6765c814.png"></p>

## Implementasi Kode Manual (Histogram Equalization)

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202194546-eb19b842-9e19-4886-898a-acb95d3e919b.png"></p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202194619-f8b639f4-a70d-4c6e-89d3-4edb8a213397.png"></p>

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202195557-5539f2c7-4828-4193-b910-6b28e8d52344.png"></p>

Output:

<p align=center><img src="https://user-images.githubusercontent.com/112606990/202195775-7268ee3d-034f-49a9-bd9d-70139ee4649a.png"></p> 
