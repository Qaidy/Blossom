<div align="center">

# 🌸 Blossom

**Premium Fashion**

*Menggabungkan estetika editorial majalah fesyen dengan fungsionalitas aplikasi web full-stack real-time*

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_v3-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

</div>

---

## Tentang Proyek

**Blossom** adalah platform e-commerce storefront premium dengan tema editorial minimalis modern. Terinspirasi dari estetika butik mewah internasional seperti Zara, Mango, dan Vogue — Blossom mengutamakan *generous whitespace*, tipografi kontras tinggi antara Serif editorial dan Sans-serif geometris, serta tampilan flat yang bersih tanpa drop-shadow berlebihan.

Backend-nya ditenagai oleh **Supabase** sebagai sistem database dan autentikasi real-time, menjadikan setiap perubahan data langsung terefleksi di seluruh antarmuka tanpa perlu reload halaman.

---

## ✨ Fitur Utama

### 🛒 Customer Portal (Sisi Pembeli)

- **Single-Page Hash Routing** — Navigasi instan tanpa refresh halaman (`#/`, `#/shop`, `#/product/:id`, `#/wishlist`, `#/cart`, `#/profile`)
- **Halaman Detail Produk (PDP)** — Layout split-screen asimetris dengan galeri visual besar, deskripsi bahan, panduan perawatan, dan pemilihan ukuran
- **Keranjang Belanja Dinamis** — Manajemen kuantitas real-time, kalkulasi otomatis kupon, dan gratis ongkir untuk pembelian di atas $75
- **Wishlist Persisten** — Tersimpan langsung ke database, tidak hilang meski browser ditutup
- **Edit Profil Mandiri** — Perbarui nama, email, dan kata sandi langsung dari dasbor profil

### 🛡️ Admin Dashboard (Sisi Pengelola)

- **Manajemen Produk (CRUD)** — Tambah koleksi baru lengkap dengan gambar, harga, diskon, kategori, dan penanda *Best Seller*
- **Live Updates Real-Time** — Setiap perubahan di halaman admin (`#/admin`) langsung tercermin di katalog pembeli secara instan
- **Custom Confirmation Modal** — Dialog konfirmasi elegan bertema Blossom, menggantikan dialog bawaan browser

---

## 🛠️ Tech Stack

| Layer | Teknologi |
|---|---|
| **Frontend** | HTML5, JavaScript (ES6 Vanilla), Tailwind CSS v3 |
| **Database** | Supabase (PostgreSQL) |
| **Auth & Security** | Supabase Auth + Row Level Security (RLS) |
| **Tipografi** | Google Fonts — Playfair Display & Inter |

---

## 🗄️ Skema Database

Blossom mengaktifkan **Row Level Security** di setiap tabel untuk melindungi data pengguna di sisi server.

| Tabel | Kolom Utama | Aturan RLS |
|---|---|---|
| `profiles` | `id`, `full_name`, `is_admin` | Pengguna hanya bisa baca & ubah profil milik sendiri |
| `products` | `id`, `name`, `price`, `discount_percent` | Read: publik — Write: khusus admin |
| `wishlists` | `id`, `user_id`, `product_id` | Hanya pemilik yang bisa akses |
| `carts` | `id`, `user_id`, `product_id`, `quantity` | Hanya pemilik yang bisa akses |

---

## 🔒 Lisensi

Didistribusikan di bawah **Lisensi MIT**. Lihat berkas `LICENSE` untuk detail penggunaan komersial dan distribusi kode.

---

<div align="center">

Dikembangkan dengan penuh dedikasi untuk menyajikan kemewahan visual mode dan keandalan sistem full-stack real-time. 🌸

</div>
