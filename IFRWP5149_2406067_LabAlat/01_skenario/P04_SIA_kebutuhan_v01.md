<!-- Tabel Kebutuhan -->

|    ID    |                                            Kebutuhan                                             |
|----------|--------------------------------------------------------------------------------------------------|
| SIA-R01  | Kebutuhan Pertemuan 2 (Lihat Jadwal Kuliah) tetap berlaku.                                       |
| SIA-R02  | Kebutuhan Pertemuan 2 (Kelola Jadwal Kuliah) tetap berlaku.                                      |
| SIA-R03  | Kebutuhan Pertemuan 3 (Ajukan & Validasi KRS) tetap berlaku.                                     |
| SIA-R04  | Kebutuhan Pertemuan 3 (Unduh Bukti KRS) tetap berlaku.                                           |
| SIA-R05  | Kebutuhan Pertemuan 3 (Proses Keputusan KRS) tetap berlaku.                                      |
| SIA-R06  | Kebutuhan Pertemuan 3 tetap berlaku.                                                             |
| SIA-R07  | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik.                 |
| SIA-R08  | Dosen dapat menginput nilai mata kuliah yang diampunya.                                          |
| SIA-R09  | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan.                   |
| SIA-R10  | Admin Akademik dapat mengelola data mahasiswa.                                                   |
| SIA-R11  | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data.       |
| SIA-R12  | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS.       |

<!-- Batas Sistem -->

- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
- Kalender akademik adalah agenda resmi institusi (awal semester, masa ujian, dll.).
- Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. KHS hanya menampilkan nilai publikasi.
- Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data akademik aktif.

<!-- Hasil Uji Konsistensi -->

- Situasi A: Mahasiswa melihat kalender akademik tanpa garis asosiasi langsung tetap sah karena mewarisi fungsi Civitas Akademika.
- Situasi B: Dosen non-pengampu menginput nilai ditolak oleh sistem dan pascakondisi gagal berlaku.
- Situasi C: Admin menghapus data mahasiswa aktif ditolak oleh sistem dan pascakondisi gagal berlaku.