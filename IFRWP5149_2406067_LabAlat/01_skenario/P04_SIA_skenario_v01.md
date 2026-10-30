<!-- Deskripsi Skenario -->

Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin Akademik mengelola data mahasiswa: menambah data mahasiswa baru, mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh collaboration yang bersesuaian.

<!-- Tabel Identitas Aktor -->

|       Aktor        |                      Kedudukan                      |                           Tujuan terhadap sistem                           |
|--------------------|-----------------------------------------------------|----------------------------------------------------------------------------|
| Civitas Akademika  | Peran umum (general), baru pada Pertemuan 4         | Peran umum bagi peminjam/pengguna. Mewariskan fungsi ke Mahasiswa & Dosen. |
| Mahasiswa          | Khusus dari Civitas Akademika, tetap Pertemuan 3    | Mewarisi fungsi umum, ajukan KRS, unduh bukti KRS, dan lihat KHS.          |
| Dosen              | Khusus dari Civitas Akademika, baru Pertemuan 4     | Mewarisi fungsi umum dan menginput nilai mata kuliah.                      |
| Dosen Wali         | Tetap dari Pertemuan 3                              | Memvalidasi KRS mahasiswa bimbingan.                                       |
| Admin Akademik     | Tetap dari Pertemuan 2                              | Mengelola jadwal kuliah, keputusan KRS, dan mengelola data mahasiswa.      |

<!-- Tabel Katalog Use Case -->

|    ID    |      Nama use case       |                      Peran dalam model                      |  Sumber Kebutuhan  |
|----------|--------------------------|-------------------------------------------------------------|--------------------|
| SIA-UC01 | Lihat Jadwal Kuliah      | Tetap dari Pertemuan 2; fungsi Civitas Akademika/Mahasiswa  | SIA-R01            |
| SIA-UC02 | Kelola Jadwal Kuliah     | Tetap dari Pertemuan 2; fungsi Admin Akademik               | SIA-R02            |
| SIA-UC03 | Ajukan KRS               | Tetap dari Pertemuan 3; menyertakan SIA-UC04                | SIA-R03            |
| SIA-UC04 | Validasi KRS             | Tetap dari Pertemuan 3; perilaku yang disertakan SIA-UC03   | SIA-R03            |
| SIA-UC05 | Unduh Bukti KRS          | Tetap dari Pertemuan 3; tambahan bersyarat via «extend»     | SIA-R04            |
| SIA-UC06 | Proses Keputusan KRS     | Tetap dari Pertemuan 3; fungsi Admin Akademik               | SIA-R05            |
| SIA-UC07 | Lihat Kalender Akademik  | Baru Pertemuan 4; fungsi aktor umum Civitas Akademika       | SIA-R07            |
| SIA-UC08 | Input Nilai Mata Kuliah  | Baru Pertemuan 4; fungsi Dosen; direalisasikan SIA-CO01     | SIA-R08, SIA-R12   |
| SIA-UC09 | Lihat KHS                | Baru Pertemuan 4; fungsi Mahasiswa; direalisasikan SIA-CO02 | SIA-R09, SIA-R12   |
| SIA-UC10 | Kelola Data Mahasiswa    | Baru Pertemuan 4; use case UMUM bagi UC11, UC12, UC13       | SIA-R10, SIA-R11   |
| SIA-UC11 | Tambah Data Mahasiswa    | Baru Pertemuan 4; use case KHUSUS dari SIA-UC10             | SIA-R11            |
| SIA-UC12 | Ubah Data Mahasiswa      | Baru Pertemuan 4; use case KHUSUS dari SIA-UC10             | SIA-R11            |
| SIA-UC13 | Hapus Data Mahasiswa     | Baru Pertemuan 4; use case KHUSUS dari SIA-UC10             | SIA-R11            |

<!-- Use Case Description SIA-UC08 -->

Elemen SIA-UC08: Input Nilai Mata Kuliah
ID dan nama: SIA-UC08: Input Nilai Mata Kuliah
Sumber kebutuhan: SIA-R08 dan SIA-R12
Tujuan: Menyimpan data nilai mahasiswa untuk mata kuliah yang diampu dosen
Aktor utama: Dosen
Pemicu: Dosen memilih fungsi input nilai dan menentukan kelas yang diampu
Prasyarat: Dosen terautentikasi dan merupakan pengampu sah mata kuliah tersebut
Pascakondisi berhasil: Nilai mata kuliah tersimpan di sistem
Pascakondisi gagal: Nilai tidak tersimpan dan data nilai sebelumnya tidak berubah
Collaboration: SIA-CO01: Input Nilai Mata Kuliah

Alur Utama:
1. Memilih mata kuliah dan kelas -> Menampilkan daftar mahasiswa dan form nilai
2. Mengisikan nilai mahasiswa -> Menampung konfirmasi isian dosen
3. Menekan tombol simpan -> Memvalidasi hak pengampu dan rentang nilai
4. Tidak ada -> Menyimpan data nilai ke sistem
5. Melihat konfirmasi -> Menampilkan pesan sukses penyimpanan nilai

Alur Alternatif:
- A1: Dosen bukan pengampu (langkah 3): sistem menolak pencatatan dan menampilkan pesan akses ditolak. Pascakondisi gagal berlaku.
- A2: Nilai tidak sah (langkah 3): sistem meminta perbaikan input sebelum penyimpanan dilakukan.

<!-- Use Case Description SIA-UC09 -->

Elemen SIA-UC09: Lihat KHS
ID dan nama: SIA-UC09: Lihat KHS
Sumber kebutuhan: SIA-R09 dan SIA-R12
Tujuan: Menampilkan Kartu Hasil Studi (KHS) mahasiswa pada semester terpilih
Aktor utama: Mahasiswa
Pemicu: Mahasiswa memilih menu KHS dan menentukan semester
Prasyarat: Mahasiswa telah terautentikasi di dalam sistem
Pascakondisi berhasil: Sistem menampilkan lembar KHS yang hanya berisi nilai yang sudah dipublikasikan secara resmi
Pascakondisi gagal: KHS tidak menampilkan nilai atau memunculkan pesan nilai belum dipublikasikan
Collaboration: SIA-CO02: Lihat KHS