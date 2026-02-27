# Minpro-1-PBW-

# 🌟 Portofolio Pribadi - Dimas Aji Mukti

Website portofolio pribadi yang menampilkan profil, pengalaman, skills, dan sertifikasi.

---

## 📸 Tampilan Setiap Section/Fitur

### 1. Section Home (Hero Section)
- **Tampilan:** Background dengan gambar, foto profil berbentuk lingkaran di tengah, dan judul perkenalan.
- **Fitur:** Tombol "Lihat Profil" yang menuju ke section About Me.

### 2. Section About Me
- **Tampilan:** Dua kolom (kiri: deskripsi & pengalaman, kanan: skills progress bar).
- **Fitur:**
  - Deskripsi singkat tentang diri
  - Daftar pengalaman organisasi & olahraga
  - Progress bar skills (Basketball Skills, Teamwork, Leadership, dll)

### 3. Section Certificates
- **Tampilan:** Grid layout dengan 3 kolom (Responsif: 1 kolom di HP).
- **Fitur:** Menampilkan kartu sertifikasi dengan gambar, judul, dan penerbit.

### 4. Navbar
- **Tampilan:** Navigation bar gelap di bagian atas (sticky).
- **Fitur:** Menu navigasi (Home, Tentang Saya, Sertifikat) yang smooth scroll ke section tujuan.

---
Penjelasan: Menggunakan Vue.js untuk menampilkan data secara dinamis. Semua teks seperti nama, skills, dan pengalaman diambil dari data() di Vue.

## 💻 Penjelasan Code Setiap Section/Fitur

### 1. Struktur HTML & Vue.js
```
- Section Home
```html
<!-- Vue App Mount Point -->
<div id="app">
    <!-- Semua konten ada di dalam div ini agar bisa diakses Vue -->
</div>
<section id="home" class="hero-section d-flex align-items-center text-center text-white">
    <img :src="profileImage" class="rounded-circle profile-img">
    <h1>Halo, Saya <span>{{ name }}</span></h1>
</section>

Penjelasan:

Menggunakan class Bootstrap d-flex dan align-items-center untuk menengahkan konten.
:src adalah shorthand Vue untuk binding attribute src.
{{ name }} adalah interpolation Vue untuk menampilkan nama dari data.

- Section About Me (Skills Progress Bar)

```html
<div class="progress" style="height: 10px;">
    <div class="progress-bar bg-warning" role="progressbar" 
         :style="{ width: skill.level + '%' }">
    </div>
</div>

Penjelasan:

Menggunakan komponen Bootstrap .progress dan .progress-bar.
Vue :style digunakan untuk mengatur lebar bar secara dinamis berdasarkan data skill.level.

- Section Certificates (Grid Card)

```html

<div class="row g-4">
    <div class="col-md-4" v-for="cert in certificates" :key="cert.id">
        <div class="card h-100 shadow-sm cert-card">
            <img :src="cert.image" class="card-img-top">
            <div class="card-body">
                <h5>{{ cert.title }}</h5>
            </div>
        </div>
    </div>
</div>

Penjelasan:

v-for="cert in certificates" adalah directives Vue untuk meloop data array sertifikat.
g-4 adalah class Bootstrap untuk jarak (gap) antar kartu.
col-md-4 berarti 3 kartu dalam satu baris di layar medium ke atas.

- Navbar

```html

<nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
    <div class="container">
        <a class="navbar-brand" href="#">{{ name }}</a>
    </div>
</nav>

Penjelasan:

fixed-top membuat navbar tetap di atas saat discroll.
navbar-expand-lg navbar akan menjadi hamburger menu di layar kecil.
```
# 🛠️ Teknologi yang Digunakan

## Teknologi | Fungsi

HTML5        | Struktur dasar halaman web

CSS3         | Styling tambahan dan kustomisasi tampilan

Bootstrap 5  | Layouting (Grid, Container), Komponen UI (Navbar, Card, Button, Progress Bar), Responsif

Vue.js 3     | Interaktivitas data statis (Interpolation, v-for, Binding)

Google Fonts | Font Poppins untuk tampilan modern

CDN          | Pemanggilan library Bootstrap dan Vue secara online

# Foto Tampilan Portofolio


<img width="1920" height="1080" alt="Screenshot 2026-02-28 044555" src="https://github.com/user-attachments/assets/5d9959be-1b4c-4b8c-a0c6-4f67ee5d06e5" />
<img width="1920" height="1080" alt="Screenshot 2026-02-28 044618" src="https://github.com/user-attachments/assets/21ff3966-8828-4392-a93e-faa4c946df01" />
<img width="1920" height="1080" alt="Screenshot 2026-02-28 044606" src="https://github.com/user-attachments/assets/2d849339-9db8-4e85-bc44-59101257c2de" />


