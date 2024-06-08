# Galeri Foto

Ini adalah proyek website galeri foto sederhana yang dibuat menggunakan HTML dan CSS. Website ini dirancang untuk menampilkan berbagai gambar dalam tata letak grid.

## Fitur

- Menampilkan galeri foto dengan banyak gambar.
- Tata letak responsif yang menyesuaikan dengan ukuran layar perangkat.
- Menggunakan grid CSS untuk mengatur tata letak gambar.

## Cara Menggunakan

1. Clone repositori ini atau unduh file ZIP.
2. Ekstrak file ZIP jika Anda mengunduhnya.
3. Buka file `index.html` di browser pilihan Anda.

## Struktur Proyek
|-- index.html
|-- README.md


- `index.html`: File HTML utama yang berisi struktur dan konten website.
- `README.md`: File ini, yang berisi informasi tentang proyek.

## Kustomisasi

Anda dapat menyesuaikan galeri dengan mengubah atau menambahkan gambar pada div dengan kelas `gallery-grid` di dalam file `index.html`. Gunakan elemen `figure` untuk menambah gambar baru. Contoh:

### Penjelasan HTML:

- **Header (Kepala)**:
  ```html
  <header>
      <h1>Galeri Foto</h1>
  </header>
  ```
  Bagian ini berisi judul halaman, yaitu "Galeri Foto".

- **Konten Utama**:
  ```html
  <main>
      <div class="gallery-grid">
          <!-- Beberapa elemen figure yang masing-masing berisi gambar dan caption -->
      </div>
  </main>
  ```
  Area konten utama mencakup sebuah `div` dengan kelas `gallery-grid` yang berisi beberapa elemen `figure`. Setiap `figure` berisi elemen `img` dan `figcaption`.

- **Footer (Kaki Halaman)**:
  ```html
  <footer>
      <p>&copy; 2024 Galeri Foto</p>
  </footer>
  ```
  Bagian footer menampilkan pemberitahuan hak cipta.

### Penjelasan CSS:

- **Gaya Umum**:
  ```css
  body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f5f5f5;
      color: #333;
  }
  ```
  Mengatur font keseluruhan, margin, padding, warna latar belakang, dan warna teks untuk badan (body) halaman.

- **Gaya Header**:
  ```css
  header {
      background-color: #333;
      color: #fff;
      padding: 15px 0;
      text-align: center;
  }
  header h1 {
      margin: 0;
      font-size: 24px;
  }
  ```
  Mengatur gaya header dengan latar belakang gelap, teks putih, dan menyelaraskan judul di tengah.

- **Gaya Konten Utama**:
  ```css
  main {
      padding: 20px;
  }
  ```
  Menambahkan padding di sekitar area konten utama.

- **Galeri Grid**:
  ```css
  .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 20px;
  }
  ```
  Menggunakan CSS Grid untuk membuat tata letak yang fleksibel dan responsif untuk gambar-gambar. Grid menyesuaikan jumlah kolom berdasarkan ruang yang tersedia, memastikan setiap kolom setidaknya selebar 150px.

*Penjelasan*
 `gallery-grid`. Berikut adalah penjelasan dari setiap baris kode:

- **`display: grid;`**:
  Ini mengubah elemen `div` dengan kelas `gallery-grid` menjadi kontainer grid. CSS Grid Layout adalah teknik tata letak dua dimensi yang memungkinkan Anda mengatur elemen dalam baris dan kolom.

- **`grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));`**:
  Properti ini menentukan berapa banyak kolom yang akan ada dalam grid dan bagaimana lebarnya. 
  - `repeat(auto-fit, minmax(150px, 1fr))` adalah fungsi yang mengulangi kolom berdasarkan beberapa kondisi:
    - `auto-fit` membuat kolom sebanyak mungkin yang muat dalam kontainer, menyesuaikan ukuran kolom secara otomatis agar sesuai dengan lebar kontainer.
    - `minmax(150px, 1fr)` menentukan bahwa setiap kolom harus memiliki lebar minimum 150px dan dapat tumbuh hingga satu fraksi (1fr) dari ruang yang tersedia. Ini memastikan bahwa kolom tidak akan lebih sempit dari 150px tetapi akan membesar jika ada ruang yang cukup.

- **`gap: 20px;`**:
  Properti ini menambahkan jarak (gap) sebesar 20px antara setiap kolom dan baris dalam grid. Ini membuat elemen-elemen di dalam grid tidak terlalu berdekatan, memberikan ruang yang cukup untuk tampilan yang lebih rapi.

- **Gaya Figure**:
  ```css
  .gallery-grid figure {
      margin: 0;
  }
  .gallery-grid img {
      width: 100%;
      height: auto;
      border-radius: 10px;
  }
  .gallery-grid figcaption {
      font-size: 14px;
      color: #777;
      text-align: center;
      margin-top: 10px;
  }
  ```
  Memastikan elemen `figure` tidak memiliki margin, gambar mengambil lebar penuh dari wadahnya, responsif, dan memiliki sudut yang melengkung. Caption diberi gaya dengan ukuran font yang lebih kecil dan warna yang lebih terang, diselaraskan di tengah di bawah gambar.

- **Gaya Footer**:
  ```css
  footer {
      background-color: #333;
      color: #fff;
      text-align: center;
      padding: 10px 0;
      position: fixed;
      bottom: 0;
      width: 100%;
  }
  ```
  Mengatur gaya footer agar tetap berada di bagian bawah halaman dengan latar belakang gelap, teks putih, dan konten yang diselaraskan di tengah.
