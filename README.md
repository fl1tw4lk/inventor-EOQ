
# Sistem Informasi Manajemen Persediaan Oojhi Bakery

## Deskripsi

Sistem Informasi Manajemen Persediaan Oojhi Bakery adalah aplikasi web yang dirancang untuk membantu Oojhi Bakery dalam mengelola persediaan bahan baku mereka. Aplikasi ini menyediakan fungsionalitas untuk menghitung Economic Order Quantity (EOQ), mengelola data bahan baku, dan mencatat transaksi keluar masuk bahan baku.

## Fitur

*   **Manajemen Bahan Baku**: Menambah, melihat, memperbarui, dan menghapus data bahan baku.
*   **Penghitung EOQ**: Menghitung kuantitas pemesanan optimal untuk setiap bahan baku menggunakan metode EOQ.
*   **Manajemen Transaksi**: Mencatat setiap transaksi pembelian dan penggunaan bahan baku.
*   **Dasbor**: Menyediakan ringkasan informasi penting mengenai persediaan.

## Teknologi yang Digunakan

*   **Next.js**: Framework React untuk membangun antarmuka pengguna.
*   **Prisma**: ORM untuk berinteraksi dengan database.
*   **MySQL**: Sistem manajemen database relasional.
*   **Tailwind CSS**: Framework CSS untuk styling.
*   **TypeScript**: Superset JavaScript yang menambahkan tipe statis.

## Memulai

### Prasyarat

Pastikan Anda telah menginstal Node.js dan MySQL di sistem Anda.

### Instalasi

1.  **Buat database di MySQL:**
    ```sql
    CREATE DATABASE db_oojhi_bakery;
    ```

2.  **Clone repositori ini:**
    ```bash
    git clone <URL_REPOSITORI>
    cd <NAMA_DIREKTORI>
    ```

3.  **Instal dependensi:**
    ```bash
    npm i
    ```

4.  **Salin file `.env.example` menjadi `.env` dan konfigurasikan variabel lingkungan, terutama `DATABASE_URL`:**
    ```
    DATABASE_URL="mysql://<user>:<password>@<host>:<port>/db_oojhi_bakery"
    ```

5.  **Terapkan skema database:**
    ```bash
    npx prisma db push
    ```

6.  **Seed database dengan data awal:**
    ```bash
    npx prisma db seed
    ```

7.  **Hasilkan Prisma Client:**
    ```bash
    npx prisma generate
    ```

8.  **Jalankan server pengembangan:**
    ```bash
    npm run dev
    ```

Aplikasi sekarang akan berjalan di `http://localhost:3000`.

## Struktur Proyek

```
/
├── app/                # Halaman dan logika aplikasi
│   ├── actions/        # Server actions untuk interaksi backend
│   └── dashboard/      # Halaman-halaman dasbor
├── components/         # Komponen React yang dapat digunakan kembali
├── lib/                # Utilitas dan fungsi bantuan
├── prisma/             # Skema dan file seed database
└── public/             # Aset statis
```

## Lisensi

Proyek ini dilisensikan di bawah Lisensi MIT - lihat file [LICENSE](LICENSE) untuk detailnya.
