<!-- Tabel Kebutuhan -->

|    ID    |                                            Kebutuhan                                             |
|----------|--------------------------------------------------------------------------------------------------|
| LAB-R01  | Kebutuhan Pertemuan 3 (Lihat Ketersediaan Peralatan) tetap berlaku.                              |
| LAB-R02  | Kebutuhan Pertemuan 3 (Kelola Data Peralatan) tetap berlaku.                                     |
| LAB-R03  | Kebutuhan Pertemuan 3 (Ajukan & Periksa Ketersediaan) tetap berlaku.                             |
| LAB-R04  | Kebutuhan Pertemuan 3 (Cetak Bukti Pengajuan) tetap berlaku.                                     |
| LAB-R05  | Kebutuhan Pertemuan 3 (Proses Keputusan Peminjaman) tetap berlaku.                               |
| LAB-R06  | Kebutuhan Pertemuan 3 (Lihat Laporan Peminjaman) tetap berlaku.                                  |
| LAB-R07  | Mahasiswa dan Dosen, sebagai Peminjam, dapat melihat ketersediaan dan mengajukan peminjaman.     |
| LAB-R08  | Petugas laboratorium mengelola data peralatan dalam tiga bentuk khusus: tambah, ubah, dan hapus. |
| LAB-R09  | Petugas laboratorium dapat mencatat pengembalian peralatan untuk peminjaman berstatus Dipinjam.  |
| LAB-R10  | Sistem memeriksa dan mencatat kondisi peralatan sebagai bagian dari pencatatan pengembalian.     |
| LAB-R11  | Model menunjukkan collaboration yang merealisasikan Ajukan Peminjaman dan Catat Pengembalian.    |

<!-- Batas Sistem dan Aturan -->

- Sistem mencatat dan menyediakan informasi; perpindahan fisik alat tidak terjadi di dalam perangkat lunak.
- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
- Pengembalian hanya dapat dicatat untuk peminjaman berstatus Dipinjam. Peminjaman yang masih Menunggu Keputusan atau Ditolak tidak dapat dicatat pengembaliannya.
- Kondisi peralatan pada pengembalian dicatat dengan salah satu nilai: Baik, Rusak Ringan, atau Rusak Berat.
- Hapus Data Peralatan hanya untuk peralatan yang tidak sedang dipinjam dan tidak memiliki pengajuan aktif.

<!-- Pertanyaan Terbuka -->

- Keterlambatan pengembalian dan perhitungan denda belum dimodelkan pada Pertemuan 4 ini (diusulkan untuk analisis tahap berikutnya).