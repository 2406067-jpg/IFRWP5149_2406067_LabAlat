<!-- Tabel analisis model P04 LAB -->

|               Sumber               |  Hubungan   |              Tujuan               |
|------------------------------------|-------------|-----------------------------------|
| Peminjam                           | Asosiasi    | LAB-UC01 Lihat Ketersediaan       |
| Peminjam                           | Asosiasi    | LAB-UC03 Ajukan Peminjaman        |
| Mahasiswa                          | Asosiasi    | LAB-UC05 Cetak Bukti Pengajuan    |
| Mahasiswa                          | Generalisasi| Peminjam                          |
| Dosen                              | Generalisasi| Peminjam                          |
| Petugas Laboratorium               | Asosiasi    | LAB-UC02 Kelola Data Peralatan    |
| Petugas Laboratorium               | Asosiasi    | LAB-UC06 Proses Keputusan         |
| Petugas Laboratorium               | Asosiasi    | LAB-UC11 Catat Pengembalian       |
| Kepala Laboratorium                | Asosiasi    | LAB-UC07 Lihat Laporan Peminjaman |
| LAB-UC03 Ajukan Peminjaman         | «include»   | LAB-UC04 Periksa Ketersediaan     |
| LAB-UC05 Cetak Bukti Pengajuan     | «extend»    | LAB-UC03 Ajukan Peminjaman        |
| LAB-UC08 Tambah Data Peralatan     | Generalisasi| LAB-UC02 Kelola Data Peralatan    |
| LAB-UC09 Ubah Data Peralatan       | Generalisasi| LAB-UC02 Kelola Data Peralatan    |
| LAB-UC10 Hapus Data Peralatan      | Generalisasi| LAB-UC02 Kelola Data Peralatan    |
| LAB-UC11 Catat Pengembalian        | «include»   | LAB-UC12 Periksa Kondisi          |
| LAB-CO01 Ajukan Peminjaman         | Realisasi   | LAB-UC03 Ajukan Peminjaman        |
| LAB-CO02 Catat Pengembalian        | Realisasi   | LAB-UC11 Catat Pengembalian       |