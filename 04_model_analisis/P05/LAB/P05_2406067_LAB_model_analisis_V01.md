<!-- Tabel analisis model P05 LAB -->

| ID Skenario | Nama Use Case                | Sumber / Aktor                 | Hubungan / Pemetaan | Tujuan / Use Case Target               |
| LAB-UC01    | Lihat Ketersediaan Peralatan | Peminjam                       | Asosiasi            | LAB-UC01 Lihat Ketersediaan Peralatan  |
| LAB-UC03    | Ajukan Peminjaman            | Peminjam                       | Asosiasi            | LAB-UC03 Ajukan Peminjaman             |
| LAB-UC05    | Cetak Bukti Pengajuan        | Mahasiswa                      | Asosiasi            | LAB-UC05 Cetak Bukti Pengajuan         |
| LAB-UC01    | Lihat Ketersediaan Peralatan | Mahasiswa                      | Generalisasi        | Peminjam                               |
| LAB-UC01    | Lihat Ketersediaan Peralatan | Dosen                          | Generalisasi        | Peminjam                               |
| LAB-UC02    | Kelola Data Peralatan        | Petugas Laboratorium           | Asosiasi            | LAB-UC02 Kelola Data Peralatan         |
| LAB-UC06    | Proses Keputusan Peminjaman  | Petugas Laboratorium           | Asosiasi            | LAB-UC06 Proses Keputusan Peminjaman   |
| LAB-UC11    | Catat Pengembalian Peralatan | Petugas Laboratorium           | Asosiasi            | LAB-UC11 Catat Pengembalian Peralatan  |
| LAB-UC07    | Lihat Laporan Peminjaman     | Kepala Laboratorium            | Asosiasi            | LAB-UC07 Lihat Laporan Peminjaman      |
| LAB-UC04    | Periksa Ketersediaan         | LAB-UC03 Ajukan Peminjaman     | «include»           | LAB-UC04 Periksa Ketersediaan          |
| LAB-UC05    | Cetak Bukti Pengajuan        | LAB-UC05 Cetak Bukti Pengajuan | «extend»            | LAB-UC03 Ajukan Peminjaman             |
| LAB-UC08    | Tambah Data Peralatan        | LAB-UC08 Tambah Data Peralatan | Generalisasi        | LAB-UC02 Kelola Data Peralatan         |
| LAB-UC09    | Ubah Data Peralatan          | LAB-UC09 Ubah Data Peralatan   | Generalisasi        | LAB-UC02 Kelola Data Peralatan         |
| LAB-UC10    | Hapus Data Peralatan         | LAB-UC10 Hapus Data Peralatan  | Generalisasi        | LAB-UC02 Kelola Data Peralatan         |
| LAB-UC12    | Periksa Kondisi Peralatan    | LAB-UC11 Catat Pengembalian    | «include»           | LAB-UC12 Periksa Kondisi Peralatan     |
| LAB-CO01    | Ajukan Peminjaman            | LAB-CO01 Ajukan Peminjaman     | Realisasi           | LAB-UC03 Ajukan Peminjaman             |
| LAB-CO02    | Catat Pengembalian Peralatan | LAB-CO02 Catat Pengembalian    | Realisasi           | LAB-UC11 Catat Pengembalian Peralatan  |