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
|--assets

  |--(folder img)
  
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
  • <div>: Elemen div adalah elemen blok yang digunakan sebagai kontainer untuk mengelompokkan elemen-elemen lain. Dalam hal ini, div dengan kelas gallery-grid berfungsi sebagai kontainer utama untuk elemen-elemen galeri.
  
  • class="gallery-grid": Kelas gallery-grid digunakan untuk menerapkan gaya CSS khusus yang mengatur tata letak elemen-elemen anak di dalamnya menggunakan flexbox. Ini membantu dalam membuat tampilan galeri yang responsif dan terstruktur.

- **Konten column**
  ```html
  <div class="gallery-column">
</div>
  ```
  • <div>: Elemen div ini berfungsi sebagai kolom dalam galeri. Elemen ini membantu mengelompokkan beberapa elemen figure menjadi satu kolom.
    
  • class="gallery-column": Kelas gallery-column digunakan untuk menerapkan gaya CSS yang mengatur lebar dan margin kolom, serta membuat kolom tersebut berperilaku responsif sesuai dengan ukuran layar.

-**figure**
  ```html
  <figure>
    <img src="assets/gambar_hutan.jpg" alt="Gambar Hutan">
    <figcaption>Gambar Hutan</figcaption>
</figure>
  ```
  • figure: Elemen figure digunakan untuk mengelompokkan konten media dengan deskripsi atau keterangan. Dalam hal ini, figure mengelompokkan gambar dengan keterangan gambar (figcaption).
  
  • img: Elemen img digunakan untuk menyematkan gambar. Atribut src menunjukkan path atau lokasi gambar, dan alt memberikan teks alternatif yang mendeskripsikan gambar jika gambar tidak bisa ditampilkan.
  
  • figcaption: Elemen figcaption menyediakan keterangan atau deskripsi untuk gambar. Dalam hal ini, teks "Gambar Hutan" menjelaskan gambar yang ditampilkan di atasnya.

- **Footer (Kaki Halaman)**:
  ```html
  <footer>
      <p>&copy; 2024 Galeri Foto</p>
  </footer>
  ```
  Bagian footer menampilkan pemberitahuan hak cipta.

### Penjelasan CSS:

- **Gaya Konten Utama**:
  ```css
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #121212;
    color: #fff;
  }
  ```
  • font-family: Menentukan jenis font yang digunakan di seluruh halaman web. Pada contoh ini, font yang digunakan adalah Arial, atau jika tidak tersedia, font sans-serif.
  
  • margin: Mengatur margin seluruh halaman menjadi nol, menghapus ruang default di sekitar tepi halaman.
  
  • padding: Mengatur padding seluruh halaman menjadi nol, menghapus ruang default di dalam elemen body.
  
  • background-color: Mengatur warna latar belakang halaman menjadi warna abu-abu gelap (#121212).
  
  • color: Mengatur warna teks menjadi putih (#fff), sehingga kontras dengan latar belakang gelap.

- **Header**:
  ```css
  header {
    background-color: #333;
    color: #fff;
    padding: 15px 0;
    text-align: center;
}

  ```
  • background-color: Mengatur warna latar belakang header menjadi abu-abu gelap (#333).

  • color: Mengatur warna teks dalam header menjadi putih (#fff) untuk kontras yang baik dengan latar belakang.

  • padding: Menambahkan ruang vertikal (padding) sebesar 15px di atas dan di bawah konten dalam header, membuatnya lebih terlihat dan terbaca.

  •text-align: Mengatur teks dalam header agar rata tengah (centered), memberikan tampilan yang simetris dan terpusat.

**`main`*:
  ```css
  main {
    padding: 20px;
    max-width: 1200px;
    margin: auto;
}

  ```
  • padding: Menambahkan ruang di dalam elemen main sebesar 20px, memberikan ruang antara konten dan tepi elemen.
  
  • max-width: Mengatur lebar maksimum elemen main menjadi 1200px, memastikan elemen tidak menjadi terlalu lebar pada layar yang besar.
  
  • margin: Mengatur margin otomatis (auto) untuk elemen main, sehingga elemen ini terpusat secara horizontal di dalam elemen induknya.

**`gallery-grid`**:
  ```css
  .gallery-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

  ```
  • .gallery-grid { ... }: Ini mengatur gaya untuk elemen dengan kelas gallery-grid.
  
  • display: flex;: Mengatur elemen ini untuk menggunakan model tata letak fleksibel. Dengan kata lain, elemen ini dan anak-anaknya akan diatur menggunakan aturan tata letak flexbox, yang memudahkan pengaturan elemen dalam baris atau kolom.
  
  • flex-wrap: wrap;: Memungkinkan elemen anak di dalam gallery-grid untuk membungkus ke baris baru jika mereka tidak muat dalam satu baris. Tanpa properti ini, elemen anak akan tetap dalam satu baris, bahkan jika mereka melampaui lebar elemen induk.
  
  • justify-content: space-between;: Mengatur jarak antara elemen anak dalam elemen gallery-grid. Properti ini memastikan bahwa elemen anak didistribusikan secara merata dengan ruang yang sama di antara mereka. Ruang ekstra akan dibagi secara merata antara elemen anak, sehingga elemen pertama berada di awal dan elemen terakhir berada di akhir baris.

- **galery column**:
  ```css
  .gallery-column {
    flex: 0 0 48%;
    margin: 1%;
}

  ```
  • flex: Menentukan ukuran elemen flex anak. Dalam hal ini, elemen mengambil 48% dari lebar container, dengan pertumbuhan dan penyusutan yang tidak diizinkan (0 0).

  • margin: Menambahkan margin sebesar 1% di sekitar elemen, memberikan ruang antara kolom galeri.

**galery column figure**
  ```css
  .gallery-column figure {
    margin: 0 0 20px 0;
    background: #333;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s;
}

  .gallery-column figure:hover {
    transform: scale(1.05);
}

  ```
  • .gallery-column figure { ... }: Ini mengatur gaya untuk elemen figure yang berada di dalam elemen dengan kelas gallery-column.
  
  • margin: 0 0 20px 0;: Mengatur margin (jarak luar) untuk elemen figure. Margin atas adalah 0, margin kanan adalah 0, margin bawah adalah 20 piksel, dan margin kiri adalah 0. Ini berarti elemen figure akan memiliki jarak 20 piksel dari elemen di bawahnya.
  
  • background: #333;: Mengatur latar belakang elemen figure dengan warna abu-abu gelap (#333).
  
  • border-radius: 10px;: Mengatur sudut elemen figure menjadi melengkung dengan radius 10 piksel, memberikan efek sudut yang lebih halus.
  
  • overflow: hidden;: Menyembunyikan bagian konten yang melampaui batas elemen figure. Ini berguna untuk memastikan bahwa gambar atau konten lain di dalam figure tidak keluar dari batas elemen tersebut.
  
  • box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);: Menambahkan bayangan pada elemen figure. Bayangan ini memiliki offset vertikal 4 piksel, offset horizontal 0 piksel, blur radius 8 piksel, dan warna bayangan hitam dengan opasitas 10%. Ini memberikan efek bayangan halus di bawah elemen, membuatnya terlihat lebih tiga dimensi.
  
  • transition: transform 0.2s;: Mengatur efek transisi pada properti transform selama 0.2 detik. Ini berarti jika elemen figure berubah posisi atau skala (misalnya saat di-hover), perubahan tersebut akan terjadi secara halus selama 0.2 detik.
  
  • transform: Mengatur transformasi elemen figure ketika di-hover, memperbesar ukuran elemen sebesar 5% untuk memberikan efek zoom.

- **gaya gallery-column bagian img**:
  ```css
  .gallery-column img {
    width: 100%;
    height: auto;
    display: block;
}

  ```
  • .gallery-column img { ... }: Ini mengatur gaya untuk elemen img (gambar) yang berada di dalam elemen dengan kelas gallery-column.

  • width: 100%;: Mengatur lebar gambar agar selalu 100% dari lebar elemen induknya. Ini berarti gambar akan secara otomatis menyesuaikan lebarnya agar sesuai dengan lebar elemen tempatnya berada, memastikan tidak ada bagian gambar yang terpotong atau melampaui batas.

  • height: auto;: Mengatur tinggi gambar agar otomatis menyesuaikan berdasarkan aspek rasio aslinya. Ini memastikan gambar tidak akan terlihat terdistorsi atau terjepit meskipun lebar gambar berubah.

  • display: block;: Mengubah cara gambar ditampilkan dari tampilan default inline menjadi block. Ini berarti gambar akan mengisi seluruh lebar elemen induknya dan tidak ada elemen lain yang bisa berada di sampingnya. Juga, ini menghilangkan celah kecil yang biasanya muncul di bawah gambar jika tetap sebagai inline.

**figcaption**:
  ```css
  .gallery-column figcaption {
    padding: 10px;
    font-size: 14px;
    color: #ccc;
    text-align: center;
}

  ```
  • padding: Menambahkan ruang di dalam elemen figcaption sebesar 10px untuk memberikan ruang antara teks dan tepi elemen.
  
  • font-size: Mengatur ukuran font teks dalam figcaption menjadi 14px.
  
  • color: Mengatur warna teks dalam figcaption menjadi abu-abu terang (#ccc) untuk kontras yang lembut dengan latar belakang.
  
  • text-align: Mengatur teks dalam figcaption agar rata tengah.
  
**footer**
  ```css
  footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    margin-top: 20px;
}

  ```
  • background-color: Mengatur warna latar belakang footer menjadi abu-abu gelap (#333).
  
  • color: Mengatur warna teks dalam footer menjadi putih (#fff) untuk kontras yang baik dengan latar belakang.
  
  • text-align: Mengatur teks dalam footer agar rata tengah.
  
  • padding: Menambahkan ruang vertikal (padding) sebesar 10px di atas dan di bawah konten dalam footer, membuatnya lebih terlihat dan terbaca.
  
  • margin-top: Menambahkan ruang (margin) sebesar 20px di atas footer untuk memberikan jarak antara elemen sebelumnya dan footer.
  
**mengatur tampilan smartphone**
  ```css
  @media (max-width: 768px) {
    .gallery-column {
        flex: 100%;
        margin: 10px 0;
    }
}

  ```
  • @media (max-width: 768px): Ini adalah media query yang menargetkan perangkat dengan lebar layar maksimum 768 piksel. Media query ini membantu membuat desain yang responsif dengan mengubah tata letak dan gaya elemen berdasarkan ukuran layar perangkat.

  • .gallery-column { ... }: Gaya yang diterapkan pada elemen dengan kelas gallery-column ketika kondisi media query terpenuhi.

  • flex: 100%;: Mengatur elemen gallery-column untuk mengambil lebar 100% dari kontainer induknya. Ini berarti kolom-kolom galeri akan ditampilkan dalam satu baris vertikal, mengisi seluruh lebar layar, yang lebih cocok untuk tampilan pada layar kecil seperti smartphone.

  • margin: 10px 0;: Mengatur margin di sekitar elemen gallery-column. Margin atas dan bawah diatur sebesar 10px, sementara margin kiri dan kanan diatur menjadi 0. Ini membantu memberikan sedikit ruang di antara kolom-kolom galeri saat ditampilkan secara vertikal.
  
**Mengatur tampilan desktop**
  ```css
  @media (min-width: 1200px) {
    .gallery-column {
        flex: 0 0 32%;
        margin: 1%;
    }
}

  ```
  • @media (min-width: 1200px): Ini adalah media query yang menargetkan perangkat dengan lebar layar minimum 1200 piksel. Media query ini membantu membuat desain yang responsif dengan mengubah tata letak dan gaya elemen berdasarkan ukuran layar perangkat. Jadi, aturan di dalamnya akan berlaku hanya pada layar yang lebarnya 1200 piksel atau lebih besar.

  • .gallery-column { ... }: Gaya yang diterapkan pada elemen dengan kelas gallery-column ketika kondisi media query terpenuhi.

  • flex: 0 0 32%;: Mengatur elemen gallery-column untuk mengambil 32% dari lebar kontainer induknya. Ini berarti setiap kolom galeri akan memiliki lebar 32% dari kontainer induknya, memungkinkan hingga tiga kolom untuk ditampilkan dalam satu baris secara berdampingan, dengan ruang kecil di antara mereka.

  • margin: 1%;: Mengatur margin di sekitar elemen gallery-column. Margin ini memberikan ruang sebesar 1% di semua sisi kolom, yang membantu memberikan jarak antara kolom-kolom galeri.
  
  
