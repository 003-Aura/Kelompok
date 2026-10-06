# Tugas Kelompok 3 — Dokumentasi Kebutuhan

## 1. Kebutuhan Fungsional

| **ID** | **Kebutuhan** | **Jenis** | **Prioritas** | **User Story / UC** |
| :----- | :------------ | :------- | :------------ | :------------------ |
| K-1 | Sistem dapat melakukan registrasi user. | F | Must | US-01 |
| K-2 | User (mahasiswa) dapat melakukan login menggunakan NIM. | F | Must | US-02 |
| K-3 | User dapat melihat daftar buku. | F | Must | US-03 |
| K-4 | User dapat mencari buku. | F | Must | US-04 |
| K-5 | User dapat melihat detail buku. | F | Should | US-05 |
| K-6 | User dapat melakukan peminjaman buku. | F | Must | US-06 |
| K-7 | User dapat melakukan pengembalian buku. | F | Must | US-07 |
| K-8 | User dapat melihat riwayat peminjaman. | F | Should | US-08 |
| K-9 | Admin dapat mengelola data buku. | F | Must | US-09 |
| K-10 | Admin dapat mengelola data user. | F | Should | US-10 |
| K-11 | Petugas dapat mengelola data peminjaman. | F | Must | US-11 |
| K-12 | Petugas dapat mengelola proses pengembalian buku. | F | Must | US-12 |

## 2. Kebutuhan Non-Fungsional

| **ID** | **Kebutuhan** | **Jenis** | **Prioritas** |
| :----- | :------------ | :------- | :------------ |
| K-13 | Sistem menggunakan autentikasi login untuk membatasi akses pengguna sesuai role. | NF | Must |
| K-14 | Sistem dapat digunakan pada perangkat laptop dan smartphone. | NF | Should |
| K-15 | Halaman sistem dapat digunakan dengan waktu respons yang cepat. | NF | Should |
| K-16 | Data pengguna dan data peminjaman disimpan secara terstruktur di database. | NF | Must |

## 3. User Story

| **ID** | **User Story** | **Prioritas** |
| :----- | :------------- | :------------ |
| US-01 | Sebagai mahasiswa, saya ingin melakukan registrasi agar dapat memiliki akun pada sistem E-Library. | Must |
| US-02 | Sebagai mahasiswa, saya ingin login menggunakan NIM agar dapat mengakses sistem E-Library. | Must |
| US-03 | Sebagai mahasiswa, saya ingin melihat daftar buku agar dapat mengetahui buku yang tersedia. | Must |
| US-04 | Sebagai mahasiswa, saya ingin mencari buku agar dapat menemukan buku yang saya butuhkan dengan mudah. | Must |
| US-05 | Sebagai mahasiswa, saya ingin melihat detail buku agar dapat mengetahui informasi buku sebelum meminjam. | Should |
| US-06 | Sebagai mahasiswa, saya ingin meminjam buku agar dapat menggunakan buku yang tersedia. | Must |
| US-07 | Sebagai mahasiswa, saya ingin mengembalikan buku agar status peminjaman saya dapat diperbarui. | Must |
| US-08 | Sebagai mahasiswa, saya ingin melihat riwayat peminjaman agar dapat mengetahui buku yang pernah saya pinjam. | Should |

## 4. Aktor

1. **Admin**
2. **Petugas**
3. **User / Mahasiswa**

## 5. Daftar Use Case

| **ID** | **Use Case** | **Aktor** |
| :----- | :----------- | :-------- |
| UC-01 | Login menggunakan NIM | User / Mahasiswa |
| UC-02 | Login | Admin, Petugas |
| UC-03 | Kelola Buku | Admin |
| UC-04 | Kelola User | Admin |
| UC-05 | Kelola Peminjaman | Petugas |
| UC-06 | Peminjaman Buku | User, Petugas |
| UC-07 | Pengembalian Buku | User, Petugas |
| UC-08 | Cari Buku | User |
| UC-09 | Lihat Riwayat Peminjaman | User, Petugas |

## 6. Skenario Use Case Detail — Peminjaman Buku

**Aktor:** User / Mahasiswa

**Tujuan:** User dapat melakukan peminjaman buku yang tersedia.

### Alur Utama

1. User memasukkan NIM dan melakukan login.
2. Sistem memvalidasi NIM dan menampilkan dashboard.
3. User memilih daftar buku.
4. User mencari atau memilih buku.
5. Sistem menampilkan detail buku.
6. User memilih peminjaman.
7. Sistem memproses peminjaman.
8. Sistem menyimpan data peminjaman.
9. Sistem menampilkan status peminjaman.

## 7. Activity Diagram

```mermaid
flowchart TD
    A([Mulai]) --> B[Masukkan NIM]
    B --> C[Login]
    C --> D{NIM valid?}
    D -- Tidak --> B
    D -- Ya --> E[Dashboard]
    E --> F[Pilih Daftar Buku]
    F --> G[Cari Buku]
    G --> H[Lihat Detail Buku]
    H --> I{Buku tersedia?}
    I -- Tidak --> G
    I -- Ya --> J[Peminjaman Buku]
    J --> K[Simpan Data Peminjaman]
    K --> L[Tampilkan Status Peminjaman]
    L --> M([Selesai])

## 8. Product Backlog Awal

| **No** | **Backlog** | **User Story** | **Estimasi Point** | **Prioritas** |
| -----: | :---------- | :------------- | -----------------: | :------------ |
| 1 | Registrasi user | US-01 | 3 | Must |
| 2 | Login menggunakan NIM | US-02 | 5 | Must |
| 3 | Melihat daftar buku | US-03 | 3 | Must |
| 4 | Mencari buku | US-04 | 3 | Must |
| 5 | Melihat detail buku | US-05 | 2 | Should |
| 6 | Peminjaman buku | US-06 | 5 | Must |
| 7 | Pengembalian buku | US-07 | 5 | Must |
| 8 | Melihat riwayat peminjaman | US-08 | 3 | Should |
