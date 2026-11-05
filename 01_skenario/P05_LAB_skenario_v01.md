<!-- Tabel 5.2 Indeks tabel skenario studi kasus LAB r -->

|ID      |                  Nama use case                 |
|--------|------------------------------------------------|
|LAB-UC01| Lihat Ketersediaan Peralatan  Ajukan Peminjaman|
|LAB-UC03|                Ajukan Peminjaman               |
|LAB-UC04|              Periksa Ketersediaan              |
|LAB-UC05|             Cetak Bukti Pengajuan              |
|LAB-UC02|              Kelola Data Peralatan             |
|LAB-UC08|             Tambah Data Peralatan              |
                
|ID      |       Nama use case        |
|--------|----------------------------|
|LAB-UC09|    Ubah Data Peralatan     |
|LAB-UC10|    Hapus Data Peralatan    |
|LAB-UC06|Proses Keputusan Peminjaman |
|LAB-UC07|  Lihat Laporan Peminjaman  |
|LAB-UC11|Catat Pengembalian Peralatan|
|LAB-UC12| Periksa Kondisi Peralatan  |

Kelompok peminjaman terdiri atas UC01, UC03, UC04, dan UC05. Tabel 
UC03 sudah disajikan sebagai Tabel 5.1 pada bab teori; tiga tabel berikut 
melengkapinya.


<!-- Tabel 5.3 Skenario Use Case LAB-UC01 Lihat Ketersediaan Peralatan -->

| Nama use case | LAB-UC01 Lihat Ketersediaan Peralatan                                                                |
| Aktor         | Peminjam (berlaku untuk Mahasiswa dan Dosen)                                                         |
| Tujuan        | Peminjam dapat mengetahui peralatan yang tersedia sebelum mengajukan peminjaman                      |
| Deskripsi     | Peminjam membuka fungsi ketersediaan dan melihat daftar peralatan beserta status ketersediaannya     |

| Kegiatan                                                             | Respon sistem                                                        |
| Skenario Normal                                                      |                                                                      |
| 1. Peminjam membuka fungsi Lihat Ketersediaan Peralatan              | 2. Sistem menampilkan daftar peralatan beserta status ketersediaannya|
| Skenario Alternative                                                 |                                                                      |
| 3. Tidak ada peralatan yang tersedia pada daftar (cabang langkah 2)  | 4. Sistem menampilkan pesan tidak ada peralatan yang tersedia        |
| Skenario Akhir                                                       | Use case selesai jika daftar peralatan beserta status ketersediaannya ditampilkan; jika tidak ada peralatan yang tersedia, use case selesai dengan pesan tersebut. |

---

<!-- Tabel 5.4 Skenario Use Case LAB-UC04 Periksa Ketersediaan -->

| Nama use case | LAB-UC04 Periksa Ketersediaan                                                                        |
| Aktor         | Peminjam (berjalan di dalam LAB-UC03 Ajukan Peminjaman)                                              |
| Tujuan        | Ketersediaan peralatan yang dipilih terperiksa sebelum pengajuan disimpan                            |
| Deskripsi     | Sistem memeriksa jumlah dan status peralatan yang dipilih peminjam dan menyampaikan hasilnya kepada alur pengajuan. Use case ini berjalan di dalam UC03 dan tidak mempunyai interaksi langsung dengan aktor |

| Kegiatan                                                             | Respon sistem                                                                                                                                                  |
| Skenario Normal                                                      |                                                                                                                                                                |
| 1. Alur pengajuan memanggil Periksa Ketersediaan dengan peralatan    | 2. Sistem memeriksa jumlah dan status peralatan tersebut                                                                                                        
| 3. Sistem menyatakan peralatan tersedia                              | 4. Alur pengajuan melanjutkan penyimpanan pengajuan                                                                                                            |
| Skenario Alternative                                                 |                                                                                                                                                                |
| 5. Peralatan tidak tersedia atau jumlah tidak mencukupi (cabang langkah 2) | 6. Sistem menyampaikan hasil tidak tersedia sehingga alur pengajuan berhenti |
|  Skenario Akhir                                                      | Use case selesai jika hasil pemeriksaan tersampaikan kepada alur pengajuan; hasil tersedia melanjutkan pengajuan, hasil tidak tersedia menghentikan pengajuan. |

---

<!-- Tabel 5.5 Skenario Use Case LAB-UC05 Cetak Bukti Pengajuan -->

| Nama use case | LAB-UC05 Cetak Bukti Pengajuan                                                                                                                                                                                                    |

| Aktor         | Mahasiswa (asosiasi khusus)                                                                                                                                                                                                       |
| Tujuan        | Bukti pengajuan tercetak sebagai tambahan bersyarat pada pengajuan                                    |
| Deskripsi     | Mahasiswa yang memilih cetak pada konfirmasi pengajuan menerima bukti pengajuan dengan nomor pengajuan. Cabang ini berlaku dengan condition [mahasiswa memilih cetak] dan extension point Bukti pengajuan tersedia pada LAB-UC03 |

| Kegiatan                                                             | Respon sistem                                                                                                                  |
| Skenario Normal                                                      |                                                                                                                                |
| 1. Mahasiswa memilih cetak bukti pada konfirmasi pengajuan           | 2. Sistem menampilkan bukti pengajuan dengan nomor pengajuan dan status Menunggu Keputusan                                     |
| 3. Mahasiswa mengonfirmasi pencetakan                                | 4. Sistem mencetak bukti pengajuan                                                                                             |
| Skenario Alternative                                                 |                                                                                                                                |
| 5. Mahasiswa tidak memilih cetak (cabang dari langkah 1)             | 6. Sistem menutup konfirmasi tanpa mencetak bukti dan pengajuan tetap tersimpan |  
| Skenario Akhir                                                       | Use case selesai jika bukti pengajuan tercetak; jika mahasiswa tidak memilih cetak, pengajuan tetap selesai tanpa bukti cetak. |

---

<!-- Tabel 5.6 Skenario Use Case LAB-UC02 Kelola Data Peralatan -->

| Nama use case | LAB-UC02 Kelola Data Peralatan                                                                                                                                                       |
| Aktor         | Petugas Laboratorium                                                                                                                                                                 |
| Tujuan        | Data peralatan terkelola melalui satu fungsi pengelolaan bersama                                                                                                                     |
| Deskripsi     | Petugas membuka fungsi pengelolaan data peralatan, memilih bentuk pengelolaan, dan menyimpan perubahan. Bentuk tambah, ubah, dan hapus dijabarkan pada tabel khususnya masing-masing |

| Kegiatan                                                             | Respon sistem                                                        |
| Skenario Normal                                                      |                                                                      |
| 1. Petugas membuka fungsi Kelola Data Peralatan                      | 2. Sistem menampilkan daftar data peralatan                          |
| 3. Petugas memilih bentuk pengelolaan, yaitu tambah, ubah, atau hapus| 4. Sistem menampilkan formulir sesuai bentuk pengelolaan yang dipilih|
| 5. Petugas mengisi atau mengonfirmasi data                           | 6. Sistem memeriksa kelengkapan dan keabsahan data                   |
| 7. Petugas menyimpan perubahan                                       | 8. Sistem menyimpan perubahan dan menampilkan konfirmasi             |
| Skenario Alternative                                                 |                                                                      |
| 9. Data tidak lengkap atau tidak sah (cabang dari langkah 6)         | 10. Sistem menolak penyimpanan dan menampilkan pesan kesalahan data  |
| Skenario Akhir                                                       | Use case selesai jika perubahan data peralatan tersimpan; jika data tidak lengkap atau tidak sah, perubahan tidak tersimpan. |

---

<!-- Tabel 5.7 Skenario Use Case LAB-UC08 Tambah Data Peralatan -->

| Nama use case | LAB-UC08 Tambah Data Peralatan                                                                                     |
| Aktor         | Petugas Laboratorium                                                                                               |
| Tujuan        | Data peralatan baru tersimpan sebagai bentuk khusus dari pengelolaan data peralatan                                |
| Deskripsi     | Petugas mengisi data peralatan baru dan menyimpan data tersebut; langkah bersama mengikuti Tabel skenario LAB-UC02 |

| Kegiatan                                                             | Respon sistem                                                                                       |
| Skenario Normal                                                      |                                                                                                     |
| 1. Petugas membuka fungsi Tambah Data Peralatan                      | 2. Sistem menampilkan formulir data peralatan baru                                                  |
| 3. Petugas mengisi data peralatan baru                               | 4. Sistem memeriksa kelengkapan data                                                                |
| 5. Petugas menyimpan data                                            | 6. Sistem menyimpan data peralatan baru dan menampilkan konfirmasi                                  |
| Skenario Alternative                                                 |                                                                                                     |
| 7. Data tidak lengkap (cabang dari langkah 4)                        | 8. Sistem menolak penyimpanan dan meminta petugas melengkapi data                                   |
| Skenario Akhir                                                       | Use case selesai jika data peralatan baru tersimpan; jika data tidak lengkap, data tidak tersimpan. |

Keterangan: use case khusus dari LAB-UC02 Kelola Data Peralatan. Perilaku pembeda: data baru tersimpan. Langkah bersama mengikuti Tabel skenario LAB-UC02.

---

<!-- Tabel 5.8 Skenario Use Case LAB-UC09 Ubah Data Peralatan -->

| Nama use case | LAB-UC09 Ubah Data Peralatan                                                                                                 |
| Aktor         | Petugas Laboratorium                                                                                                         |
| Tujuan        | Data peralatan berubah sebagai bentuk khusus dari pengelolaan data peralatan                                                 |
| Deskripsi     | Petugas memilih data peralatan, mengubah datanya, dan menyimpan perubahan; langkah bersama mengikuti Tabel skenario LAB-UC02 |

| Kegiatan                                                             | Respon sistem                                                                                                  |
| Skenario Normal                                                      |                                                                                                                |
| 1. Petugas memilih data peralatan yang akan diubah                   | 2. Sistem menampilkan data peralatan saat ini                                                                  |
| 3. Petugas mengubah data peralatan                                   | 4. Sistem memeriksa perubahan data                                                                             |
| 5. Petugas menyimpan perubahan                                       | 6. Sistem menyimpan data yang diubah dan menampilkan konfirmasi                                                |
| Skenario Alternative                                                 |                                                                                                                |
| 7. Data peralatan tidak ditemukan (cabang dari langkah 2)            | 8. Sistem menampilkan pesan data peralatan tidak ditemukan                                                     |
| Skenario Akhir                                                       | Use case selesai jika perubahan data peralatan tersimpan; jika data tidak ditemukan, perubahan tidak tersimpan. |

Keterangan: use case khusus dari LAB-UC02 Kelola Data Peralatan. Perilaku pembeda: data peralatan berubah. Langkah bersama mengikuti Tabel skenario LAB-UC02.

---

<!-- Tabel 5.9 Skenario Use Case LAB-UC10 Hapus Data Peralatan -->

| Nama use case | LAB-UC10 Hapus Data Peralatan                                                                                                                    |
| Aktor         | Petugas Laboratorium                                                                                                                             |
| Tujuan        | Data peralatan terhapus sebagai bentuk khusus dari pengelolaan data peralatan                                                                    |
| Deskripsi     | Petugas memilih data peralatan, mengonfirmasi penghapusan, dan sistem menghapus data tersebut; langkah bersama mengikuti Tabel skenario LAB-UC02 |

| Kegiatan                                                             | Respon sistem                                                                                                                 |
| Skenario Normal                                                      |                                                                                                                               |
| 1. Petugas memilih data peralatan yang akan dihapus                  | 2. Sistem memeriksa peralatan tidak sedang dipinjam & pengajuan aktif                                                         |
| 3. Petugas mengonfirmasi penghapusan                                 | 4. Sistem menghapus data peralatan dan menampilkan konfirmasi                                                                 |
| Skenario Alternative                                                 |                                                                                                                               |
| 5. Peralatan sedang dipinjam/pengajuan aktif (cabang dari langkah 2) | 6. Sistem menolak penghapusan dan menampilkan pesan peralatan terpakai                                                        |
| Skenario Akhir                                                   | Use case selesai jika data peralatan terhapus; jika peralatan sedang dipinjam atau memiliki pengajuan aktif, data tidak terhapus. |

Keterangan: use case khusus dari LAB-UC02 Kelola Data Peralatan. Perilaku pembeda: data peralatan terhapus, dengan syarat peralatan tidak sedang dipinjam dan tidak memiliki pengajuan aktif. Langkah bersama mengikuti Tabel skenario LAB-UC02.

---

<!-- Tabel 5.10 Skenario Use Case LAB-UC06 Proses Keputusan Peminjaman -->

| Nama use case | LAB-UC06 Proses Keputusan Peminjaman                                                                                                             |
| Aktor         | Petugas Laboratorium                                                                                                                             |
| Tujuan        | Pengajuan peminjaman mendapat keputusan setuju atau tolak                                                                                        |
| Deskripsi     | Petugas memeriksa pengajuan yang berstatus Menunggu Keputusan, menetapkan persetujuan atau penolakan, dan sistem menyampaikan keputusan tersebut |

| Kegiatan                                                             | Respon sistem                                                                                                                     |
| Skenario Normal                                                      |                                                                                                                                   |
| 1. Petugas membuka daftar pengajuan berstatus Menunggu Keputusan     | 2. Sistem menampilkan daftar pengajuan                                                                                            |
| 3. Petugas memilih pengajuan dan menetapkan persetujuan              | 4. Sistem mengubah status pengajuan menjadi Disetujui                                                                             |
| Skenario Alternative                                                 |                                                                                                                                   |
| 5. Petugas menetapkan penolakan (cabang dari langkah 4)              | 6. Sistem mengubah status pengajuan menjadi Ditolak                                                                               |
| 7. Pengajuan tidak ditemukan / status berubah (cabang langkah 2)     | 8. Sistem menampilkan pesan pengajuan tidak dapat diproses                                                                        |
| Skenario Akhir                                                       | Use case selesai jika pengajuan berstatus Disetujui atau Ditolak; jika pengajuan tidak dapat diproses, status tidak berubah.      |
 
---

<!-- Tabel 5.11 Skenario Use Case LAB-UC07 Lihat Laporan Peminjaman -->

| Nama use case | LAB-UC07 Lihat Laporan Peminjaman                                                                    |
| Aktor         | Kepala Laboratorium                                                                                  |
| Tujuan        | Laporan peminjaman dapat dilihat oleh kepala laboratorium                                            |
| Deskripsi     | Kepala Laboratorium membuka fungsi laporan dan melihat laporan peminjaman pada periode yang dipilih |
 
| Kegiatan                                                             | Respon sistem                                                                                                                |
| Skenario Normal                                                      |                                                                                                                              |
| 1. Kepala Laboratorium membuka fungsi Lihat Laporan Peminjaman       | 2. Sistem menampilkan daftar periode laporan                                                                                 |
| 3. Kepala Laboratorium memilih periode                               | 4. Sistem menampilkan laporan peminjaman periode tersebut                                                                    |
| Skenario Alternative                                                 |                                                                                                                              |
| 5. Tidak ada data peminjaman pada periode dipilih (cabang langkah 4) | 6. Sistem menampilkan pesan tidak ada data peminjaman                                                                        |
| Skenario Akhir                                                       | Use case selesai jika laporan periode yang dipilih ditampilkan; jika tidak ada data, use case selesai dengan pesan tersebut. |

Keterangan: satu-satunya use case Kepala Laboratorium. Tabel ini berdiri sendiri dan tidak memuat langkah include, extend, generalization, atau realization.

---

<!-- Tabel 5.12 Skenario Use Case LAB-UC11 Catat Pengembalian Peralatan -->

| Nama use case | LAB-UC11 Catat Pengembalian Peralatan                                                                                                                  |
| Aktor         | Petugas Laboratorium                                                                                                                                   |
| Tujuan        | Pengembalian tercatat dan status peminjaman serta kondisi peralatan terbarui                                                                           |
| Deskripsi     | Petugas memilih peminjaman yang akan dikembalikan, mengonfirmasi alat yang kembali, dan menyimpan pencatatan. Prasyarat: peminjaman berstatus Dipinjam |

| Kegiatan                                                             | Respon sistem                                                                                                                                                                                           |
| Skenario Normal                                                      |                                                                                                                                                                                                         |
| 1. Petugas memilih peminjaman yang akan dikembalikan                 | 2. Sistem menampilkan data peminjaman terpilih dan statusnya                                                                                                                                            |
| 3. Petugas mengonfirmasi alat yang kembali dan jumlahnya             | 4. Sistem menampung konfirmasi petugas                                                                                                                                                                  |
| 5. Sistem memeriksa status peminjaman harus Dipinjam                 | 6. Sistem menjalankan Periksa Kondisi Peralatan (lihat LAB-UC12)                                                                                                                                        |
| 7. Petugas menyimpan pencatatan pengembalian                         | 8. Sistem menyimpan tanggal kembali & mengubah status jadi Selesai                                                                                                                                      |
| 9. Petugas melihat konfirmasi                                        | 10. Sistem menampilkan ringkasan pengembalian                                                                                                                                                           |
| Skenario Alternative                                                 |                                                                                                                                                                                                         |
| 11. Status bukan Dipinjam (cabang dari langkah 5)                    | 12. Sistem menolak pencatatan dan menampilkan status saat ini                                                                                                                                           |
| 13. Kondisi Rusak dicatat pada langkah 6 (cabang dari langkah 6)     | 14. Sistem tetap menyimpan pencatatan & menandai kondisi alat                                                                                                                                           |
| 15. Jumlah alat yang kembali tidak sesuai (cabang dari langkah 3)    | 16. Sistem meminta petugas memeriksa kembali isian                                                                                                                                                       |
| Skenario Akhir                                                       | Use case selesai jika pengembalian tercatat dengan tanggal kembali dan kondisi peralatan serta status peminjaman menjadi Selesai; jika status bukan Dipinjam, tidak ada pengembalian baru yang tercatat. |

Keterangan: use case ini direalisasikan oleh collaboration LAB-CO02 Catat Pengembalian Peralatan, tanpa langkah kegiatan sendiri.

---

<!-- Tabel 5.13 Skenario Use Case LAB-UC12 Periksa Kondisi Peralatan -->

| Nama use case | LAB-UC12 Periksa Kondisi Peralatan                                                                                                                                                                              |
| Aktor         | Petugas Laboratorium (berjalan di dalam LAB-UC11 Catat Pengembalian Peralatan)                                                                                                                                  |
| Tujuan        | Kondisi peralatan yang dikembalikan terperiksa dan tercatat                                                                                                                                                     |
| Deskripsi     | Sistem memeriksa kondisi peralatan yang dikembalikan dan mencatat nilainya sebagai bagian dari pencatatan pengembalian. Use case ini berjalan di dalam UC11 dan tidak mempunyai interaksi langsung dengan aktor |

| Kegiatan                                                             | Respon sistem                                                                                                                        |
|Skenario Normal                                                       |                                                                                                                                      |
| 1. Alur pengembalian memanggil Periksa Kondisi Peralatan             | 2. Sistem menampilkan pilihan kondisi (Baik, Rusak Ringan, Rusak Berat)                                                              |
| 3. Petugas memilih nilai kondisi peralatan                           | 4. Sistem mencatat nilai kondisi pada data pengembalian                                                                              |
| Skenario Alternative                                                 |                                                                                                                                      |
| 5. Petugas belum memilih nilai kondisi (cabang dari langkah 4)       | 6. Sistem meminta petugas memilih nilai kondisi                                                                                      |
| Skenario Akhir                                                       | Use case selesai jika nilai kondisi peralatan tercatat pada data pengemba lian; jika nilai belum dipilih, pencatatan tidak disimpan. |
