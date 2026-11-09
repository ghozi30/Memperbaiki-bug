Jurnal Perbaikan Bug & Setup Web "Rental Gear"

Berikut adalah dokumentasi langkah-langkah setup dan perbaikan bug (error) yang dilakukan pada proyek web hari ini:

🛠️ Log Perbaikan (Changelog)

1. Menginstal Dependensi (Folder Vendor)

Masalah: Folder vendor tidak ditemukan di dalam direktori proyek.

Solusi: Menginstal dependensi PHP yang dibutuhkan dengan menjalankan perintah berikut di terminal:

composer install


2. Mengatur File Environment (.env)

Masalah: File konfigurasi .env belum ada.

Solusi: Membuat file konfigurasi baru dengan cara menyalin data dari file .env.example ke dalam file baru bernama .env.

3. Membuat Application Key

Masalah: Aplikasi belum memiliki App Key untuk keamanan (encryption).

Solusi: Membuat kunci aplikasi (App Key) dengan menjalankan perintah berikut di terminal:

php artisan key:generate


4. Memperbaiki Tampilan Error (Routing)

Masalah: Tampilan halaman web tidak muncul atau terjadi error.

Solusi: Mengidentifikasi dan memperbaiki kesalahan penulisan route pada file routes/web.php. Setelah diperbaiki, tampilan web berhasil muncul.

5. Memperbaiki Gambar yang Hilang (Database Seeder)

Masalah: Ada beberapa gambar yang belum muncul di halaman web.

Solusi: Memperbaiki data link/gambar pada bagian seeder. Karena seeder baru saja diubah, database diperbarui secara menyeluruh menggunakan perintah:

php artisan migrate:fresh --seed


6. Mengubah Judul Website (Sesuai Arahan Asdos)

Tugas: Menyesuaikan judul web menjadi "rental gear".

Solusi: Membuka file .env dan mengubah variabel APP_NAME menjadi:

APP_NAME="rental gear"


Catatan dibuat pada: November 2026
