<!-- Deskripsi Skenario -->

Selain mahasiswa, dosen juga meminjam peralatan laboratorium untuk kegiatan praktikum dan penelitian. Mahasiswa dan dosen sama-sama dapat melihat ketersediaan peralatan dan mengajukan peminjaman. Petugas laboratorium mengelola data peralatan: menambah peralatan baru, mengubah data peralatan, dan menghapus data peralatan yang tidak lagi dipakai. Setelah peminjaman disetujui dan alat diambil, petugas mencatat pengembalian peralatan. Pada saat mencatat pengembalian, petugas memeriksa dan mencatat kondisi peralatan. Dua use case utama pada potongan model ini, Ajukan Peminjaman dan Catat Pengembalian Peralatan, ditunjukkan realisasinya oleh collaboration yang bersesuaian.

<!-- Tabel Identitas Aktor -->

|        Aktor         |                      Kedudukan                      |                           Tujuan terhadap sistem                           |
|----------------------|-----------------------------------------------------|----------------------------------------------------------------------------|
| Peminjam             | Peran umum (general), baru pada Pertemuan 4         | Peran umum bagi peminjam peralatan. Mewariskan fungsi ke Mahasiswa & Dosen.|
| Mahasiswa            | Khusus dari Peminjam, tetap dari Pertemuan 3        | Melihat ketersediaan, mengajukan peminjaman, dan cetak bukti pengajuan.    |
| Dosen                | Khusus dari Peminjam, baru pada Pertemuan 4         | Melihat ketersediaan peralatan dan mengajukan peminjaman.                  |
| Petugas Laboratorium | Tetap dari Pertemuan 3                              | Mengelola data peralatan, memproses keputusan, dan catat pengembalian.     |
| Kepala Laboratorium  | Tetap dari Pertemuan 3                              | Melihat laporan peminjaman peralatan.                                      |

<!-- Tabel Katalog Use Case -->

|    ID    |      Nama use case       |                      Peran dalam model                      |  Sumber Kebutuhan  |
|----------|--------------------------|-------------------------------------------------------------|--------------------|
| LAB-UC01 | Lihat Ketersediaan       | Tetap dari Pertemuan 3; fungsi aktor umum Peminjam          | LAB-R01, LAB-R07   |
| LAB-UC02 | Kelola Data Peralatan    | Tetap dari Pertemuan 3; use case UMUM bagi UC08, UC09, UC10 | LAB-R02, LAB-R08   |
| LAB-UC03 | Ajukan Peminjaman        | Tetap dari Pertemuan 3; fungsi Peminjam; direalisasikan CO01| LAB-R03, LAB-R07   |
| LAB-UC04 | Periksa Ketersediaan     | Tetap dari Pertemuan 3; perilaku yang disertakan LAB-UC03   | LAB-R03            |
| LAB-UC05 | Cetak Bukti Pengajuan    | Tetap dari Pertemuan 3; tambahan bersyarat via «extend»     | LAB-R04            |
| LAB-UC06 | Proses Keputusan         | Tetap dari Pertemuan 3; fungsi utama Petugas Laboratorium   | LAB-R05            |
| LAB-UC07 | Lihat Laporan Peminjaman | Tetap dari Pertemuan 3; fungsi utama Kepala Laboratorium    | LAB-R06            |
| LAB-UC08 | Tambah Data Peralatan    | Baru Pertemuan 4; use case KHUSUS dari LAB-UC02             | LAB-R08            |
| LAB-UC09 | Ubah Data Peralatan      | Baru Pertemuan 4; use case KHUSUS dari LAB-UC02             | LAB-R08            |
| LAB-UC10 | Hapus Data Peralatan     | Baru Pertemuan 4; use case KHUSUS dari LAB-UC02             | LAB-R08            |
| LAB-UC11 | Catat Pengembalian       | Baru Pertemuan 4; fungsi Petugas; direalisasikan LAB-CO02   | LAB-R09            |
| LAB-UC12 | Periksa Kondisi Peralatan| Baru Pertemuan 4; perilaku yang disertakan LAB-UC11         | LAB-R10            |

<!-- Decision Generalization & Collaboration -->

- Generalization Aktor: Mahasiswa dan Dosen mewarisi fungsi Peminjam. Asosiasi ke LAB-UC01 dan LAB-UC03 digambar 1 kali dari Peminjam. Asosiasi khusus Mahasiswa ke LAB-UC05 tetap digambar dari Mahasiswa.
- Generalization Use Case: LAB-UC08 (Tambah), LAB-UC09 (Ubah), dan LAB-UC10 (Hapus) adalah bentuk khusus dari LAB-UC02 Kelola Data Peralatan.
- Collaboration: LAB-CO01 (Ajukan Peminjaman) mewujudkan LAB-UC03, dan LAB-CO02 (Catat Pengembalian Peralatan) mewujudkan LAB-UC11.

<!-- Use Case Description LAB-UC11 -->

Elemen LAB-UC11: Catat Pengembalian Peralatan
ID dan nama: LAB-UC11: Catat Pengembalian Peralatan
Sumber kebutuhan: LAB-R09 dan LAB-R10
Tujuan: Pengembalian tercatat dan status peminjaman serta kondisi peralatan terbarui
Aktor utama: Petugas Laboratorium
Pemicu: Petugas memilih fungsi pencatatan pengembalian dan menentukan peminjaman
Prasyarat: Petugas telah terautentikasi; peminjaman terpilih berstatus Dipinjam
Pascakondisi berhasil: Pengembalian tercatat dengan tanggal kembali dan kondisi peralatan; status peminjaman menjadi Selesai
Pascakondisi gagal: Tidak ada pengembalian baru yang tercatat; status peminjaman tidak berubah
Include: LAB-UC12: Periksa Kondisi Peralatan
Collaboration: LAB-CO02: Catat Pengembalian Peralatan

Alur Utama:
1. Memilih peminjaman yang akan dikembalikan -> Menampilkan data peminjaman terpilih dan statusnya
2. Mengonfirmasi alat yang kembali dan jumlahnya -> Menampung konfirmasi petugas
3. Tidak ada -> Memeriksa status peminjaman harus Dipinjam
4. Tidak ada -> Menjalankan LAB-UC12: memeriksa dan mencatat kondisi peralatan
5. Menyimpan pencatatan pengembalian -> Menyimpan tanggal kembali dan kondisi; mengubah status menjadi Selesai
6. Melihat konfirmasi -> Menampilkan ringkasan pengembalian

Alur Alternatif:
- A1: Status bukan Dipinjam (langkah 3): sistem menolak pencatatan dan menampilkan status peminjaman saat ini. Pascakondisi gagal berlaku.
- A2: Kondisi Rusak Ringan atau Rusak Berat (langkah 4): sistem tetap menyimpan pencatatan, menandai kondisi tersebut pada data peralatan, dan pengembalian tetap tercatat.
- A3: Jumlah alat yang kembali tidak sesuai (langkah 2): sistem meminta petugas memeriksa kembali isian sebelum penyimpanan.