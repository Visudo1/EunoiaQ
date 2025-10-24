# Eunoiaq - Lua App with Bottom Navbar (LOVE2D)

 Proyek contoh aplikasi sederhana menggunakan LOVE2D dengan bottom navigation bar berisi 5 tab:
 - Explorer
 - Shop
 - Home
 - Wallet
 - Profile

 Tujuan: memberikan pola struktur UI dasar, navigasi antar halaman, dan konten halaman Home yang khusus.

---

## Fitur utama

- Navbar bawah dengan 5 item: Explorer, Shop, Home, Wallet, Profile
- Konten halaman Home khusus (judul, subtitle, deskripsi, tombol aksi)
- Perilaku klik/touch mengganti halaman aktif
- Desain simpel untuk di-scale dengan ikon/gambar di kemudian hari

---

## Prasyarat

- Lua 5.3+ (opsional tergantung versi LOVE2D)
- LOVE2D (LOVE 11.x atau versi kompatibel)

---

## Instalasi

1. Install LOVE2D:
   - Windows: unduh dari https://love2d.org/
   - macOS: unduh dari https://love2d.org/ (gunakan Homebrew/masa instalasi)
   - Linux: via paket manajer distro Anda (contoh: sudo apt install love)

2. Buat folder proyek, simpan file utama:
   - main.lua (lihat contoh kode di bawah)

3. Jalankan:
   - love <path_ke_folder_proyek>

---

## Struktur Proyek


---

## Konsep Implementasi (Inti Kode)

- Struktur halaman dikelola melalui variabel `pages` dan `activePage`.
- Navbar bawah dibuat sebagai objek `navbar` dengan properti:
  - height, items, bgColor, itemColor, itemActiveColor, font
- Fungsi `love.draw()` menggambar konten halaman sesuai `activePage` dan menampilkan navbar.
- Ketika item navbar diklik, `activePage` diperbarui untuk menampilkan halaman yang dipilih.

Contoh inti kode (ringkas):

```lua
-- Contoh ringkas inti (main.lua)
function love.load()
  pages = { "Explorer", "Shop", "Home", "Wallet", "Profile" }
  activePage = "Home"
  -- inisialisasi navbar...
  -- inisialisasi konten Home
end

function love.draw()
  if activePage == "Home" then
    renderHome()
  else
    -- konten halaman lain (sementara)
  end

  -- gambar navbar
  -- highlight active tab
end

function love.mousepressed(mx, my, button)
  -- deteksi klik pada tombol navbar untuk mengganti activePage
end
