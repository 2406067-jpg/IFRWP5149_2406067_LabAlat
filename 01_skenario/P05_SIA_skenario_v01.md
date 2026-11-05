<!-- Tabel 5.14 Indeks tugas skenario SIA -->

| ID       | Nama use case           | Aktor             | Catatan pemetaan |
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika | Ditulis satu kali atas nama Civitas Akademika; berlaku untuk Mahasiswa dan Dosen |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen             | Prasyarat: dosen pengampu mata kuliah; alternatif: nilai di luar rentang yang sah ditolak; direalisasikan SIA-CO01 |
| SIA-UC09 | Lihat KHS               | Mahasiswa         | Hanya nilai yang sudah dipublikasikan yang ditampilkan; direalisasikan SIA-CO02 |
| SIA-UC10 | Kelola Data Mahasiswa   | Admin Akademik    | Skenario umum pengelolaan; langkah bersama yang dirujuk UC11, UC12, dan UC13 |
| SIA-UC11 | Tambah Data Mahasiswa   | Admin Akademik    | Khusus dari UC10; perilaku pembeda: data mahasiswa baru tersimpan |
| SIA-UC12 | Ubah Data Mahasiswa     | Admin Akademik    | Khusus dari UC10; perilaku pembeda: data mahasiswa berubah |
| SIA-UC13 | Hapus Data Mahasiswa    | Admin Akademik    | Khusus dari UC10; perilaku pembeda: data mahasiswa terhapus; syarat: tidak ada data akademik aktif |



<!-- Tabel 5.15 Skenario Use Case SIA-UC07 Lihat Kalender Akademik -->

| Nama use case | SIA-UC07 Lihat Kalender Akademik                                                                    |
|---|---|
| Aktor         | Civitas Akademika (berlaku untuk Mahasiswa dan Dosen)                                               |
| Tujuan        | Civitas Akademika dapat mengetahui jadwal dan agenda akademik yang berlaku                           |
| Deskripsi     | Civitas Akademika membuka fungsi kalender akademik dan melihat daftar agenda akademik semester aktif|

| Kegiatan                                                             | Respon sistem                                                        |
|---|---|
| Skenario Normal                                                      |                                                                      |
| 1. Civitas Akademika membuka fungsi Lihat Kalender Akademik           | 2. Sistem menampilkan daftar agenda dan jadwal akademik semester aktif|
| Skenario Alternative                                                 |                                                                      |
| 3. Belum ada kalender akademik yang diterbitkan (cabang langkah 2)   | 4. Sistem menampilkan pesan kalender akademik belum tersedia         |
| Skenario Akhir                                                       | Use case selesai jika jadwal agenda akademik ditampilkan; jika belum diterbitkan, use case selesai dengan pesan tersebut. |

Catatan: Mahasiswa dan Dosen mewarisi use case ini dari Civitas Akademika (generalization aktor). Skenario ditulis satu kali atas nama Civitas Akademika.


<!-- Tabel 5.16 Skenario Use Case SIA-UC08 Input Nilai Mata Kuliah -->

| Nama use case | SIA-UC08 Input Nilai Mata Kuliah                                                                    |
|---|---|
| Aktor         | Dosen                                                                                                |
| Tujuan        | Nilai mata kuliah mahasiswa tercatat dan tersimpan oleh dosen pengampu                                |
| Deskripsi     | Dosen pengampu memilih mata kuliah, memasukkan nilai mahasiswa, dan menyimpan data nilai. Prasyarat: Dosen merupakan pengampu mata kuliah tersebut |

| Kegiatan                                                             | Respon sistem                                                        |
|---|---|
| Skenario Normal                                                      |                                                                      |
| 1. Dosen memilih mata kuliah yang diampu                             | 2. Sistem menampilkan daftar mahasiswa peserta mata kuliah           |
| 3. Dosen memasukkan nilai angka/huruf mahasiswa                      | 4. Sistem memeriksa rentang keabsahan nilai                          |
| 5. Dosen menyimpan pengisian nilai                                   | 6. Sistem menyimpan data nilai dan menampilkan konfirmasi            |
| Skenario Alternative                                                 |                                                                      |
| 7. Nilai di luar rentang sah (cabang dari langkah 4)                 | 8. Sistem menolak penyimpanan dan menampilkan pesan nilai tidak sah  |
| 9. Dosen bukan pengampu mata kuliah (cabang dari langkah 1)           | 10. Sistem menolak akses dan menampilkan pesan otorisasi             |
| Skenario Akhir                                                       | Use case selesai jika data nilai berhasil tersimpan; jika nilai tidak sah atau dosen bukan pengampu, nilai tidak tersimpan. |

Keterangan: use case ini direalisasikan oleh collaboration SIA-CO01 Input Nilai Mata Kuliah.


<!-- Tabel 5.17 Skenario Use Case SIA-UC09 Lihat KHS -->

| Nama use case | SIA-UC09 Lihat KHS                                                                                  |
|---|---|
| Aktor         | Mahasiswa                                                                                            |
| Tujuan        | Mahasiswa dapat melihat Kartu Hasil Studi (KHS) pada semester tertentu                               |
| Deskripsi     | Mahasiswa memilih semester dan melihat daftar nilai mata kuliah yang telah dipublikasikan            |

| Kegiatan                                                             | Respon sistem                                                        |
|---|---|
| Skenario Normal                                                      |                                                                      |
| 1. Mahasiswa memilih semester yang ingin dilihat                     | 2. Sistem memeriksa status publikasi nilai semester tersebut         |
| 3. Mahasiswa membuka tampilan KHS                                    | 4. Sistem menampilkan daftar nilai dan IPK semester terpilih         |
| Skenario Alternative                                                 |                                                                      |
| 5. Nilai semester belum dipublikasikan (cabang dari langkah 2)        | 6. Sistem menampilkan pesan nilai semester ini belum dipublikasikan  |
| Skenario Akhir                                                       | Use case selesai jika KHS berhasil ditampilkan; jika nilai belum dipublikasikan, KHS tidak ditampilkan. |

Keterangan: use case ini direalisasikan oleh collaboration SIA-CO02 Lihat KHS.


<!-- Tabel 5.18 Skenario Use Case SIA-UC10 Kelola Data Mahasiswa -->

| Nama use case | SIA-UC10 Kelola Data Mahasiswa                                                                      |
| Aktor         | Admin Akademik                                                                                       |
| Tujuan        | Data mahasiswa terkelola melalui satu fungsi pengelolaan bersama                                     |
| Deskripsi     | Admin Akademik membuka fungsi pengelolaan data mahasiswa, memilih bentuk pengelolaan, dan menyimpan perubahan. Bentuk tambah, ubah, dan hapus dijabarkan pada tabel khususnya |

| Kegiatan                                                             | Respon sistem                                                        |
| Skenario Normal                                                      |                                                                      |
| 1. Admin Akademik membuka fungsi Kelola Data Mahasiswa               | 2. Sistem menampilkan daftar data mahasiswa                          |
| 3. Admin memilih bentuk pengelolaan (tambah, ubah, atau hapus)       | 4. Sistem menampilkan formulir sesuai bentuk pengelolaan             |
| 5. Admin mengisi atau mengonfirmasi data                             | 6. Sistem memeriksa kelengkapan dan keabsahan data                   |
| 7. Admin menyimpan perubahan                                         | 8. Sistem menyimpan perubahan dan menampilkan konfirmasi             |
| Skenario Alternative                                                 |                                                                      |
| 9. Data tidak lengkap atau tidak sah (cabang dari langkah 6)         | 10. Sistem menolak penyimpanan dan menampilkan pesan kesalahan data  |
| Skenario Akhir                                                       | Use case selesai jika perubahan data mahasiswa tersimpan; jika data tidak sah, perubahan tidak tersimpan. |

<!-- Tabel 5.19 Skenario Use Case SIA-UC11 Tambah Data Mahasiswa -->

| Nama use case | SIA-UC11 Tambah Data Mahasiswa                                                                      |
| Aktor         | Admin Akademik                                                                                       |
| Tujuan        | Data mahasiswa baru tersimpan sebagai bentuk khusus dari pengelolaan data mahasiswa                  |
| Deskripsi     | Admin mengisi data mahasiswa baru dan menyimpan data tersebut; langkah bersama mengikuti Tabel skenario SIA-UC10 |

| Kegiatan                                                             | Respon sistem                                                        |
| Skenario Normal                                                      |                                                                      |
| 1. Admin Akademik membuka fungsi Tambah Data Mahasiswa               | 2. Sistem menampilkan formulir data mahasiswa baru                   |
| 3. Admin mengisi identitas dan data akademik mahasiswa baru          | 4. Sistem memeriksa kelengkapan data dan keunikan NIM                |
| 5. Admin menyimpan data                                              | 6. Sistem menyimpan data mahasiswa baru dan menampilkan konfirmasi   |
| Skenario Alternative                                                 |                                                                      |
| 7. NIM sudah terdaftar atau data tidak lengkap (cabang langkah 4)    | 8. Sistem menolak penyimpanan dan menampilkan pesan duplikasi/kesalahan |
| Skenario Akhir                                                       | Use case selesai jika data mahasiswa baru tersimpan; jika NIM duplikat, data tidak tersimpan. |

Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa baru tersimpan. Langkah bersama mengikuti Tabel skenario SIA-UC10.


<!-- Tabel 5.20 Skenario Use Case SIA-UC12 Ubah Data Mahasiswa -->

| Nama use case | SIA-UC12 Ubah Data Mahasiswa                                                                        |
| Aktor         | Admin Akademik                                                                                       |
| Tujuan        | Data mahasiswa berubah sebagai bentuk khusus dari pengelolaan data mahasiswa                         |
| Deskripsi     | Admin memilih data mahasiswa, mengubah datanya, dan menyimpan perubahan; langkah bersama mengikuti Tabel skenario SIA-UC10 |

| Kegiatan                                                             | Respon sistem                                                        |
| Skenario Normal                                                      |                                                                      |
| 1. Admin memilih data mahasiswa yang akan diubah                     | 2. Sistem menampilkan data mahasiswa saat ini                        |
| 3. Admin mengubah informasi data mahasiswa                           | 4. Sistem memeriksa keabsahan perubahan                              |
| 5. Admin menyimpan perubahan                                         | 6. Sistem menyimpan data yang diubah dan menampilkan konfirmasi      |
| Skenario Alternative                                                 |                                                                      |
| 7. Data mahasiswa tidak ditemukan (cabang dari langkah 2)            | 8. Sistem menampilkan pesan data mahasiswa tidak ditemukan           |
| Skenario Akhir                                                       | Use case selesai jika perubahan data mahasiswa tersimpan; jika data tidak ditemukan, perubahan tidak tersimpan. |

Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa berubah. Langkah bersama mengikuti Tabel skenario SIA-UC10.


<!-- Tabel 5.21 Skenario Use Case SIA-UC13 Hapus Data Mahasiswa -->

| Nama use case | SIA-UC13 Hapus Data Mahasiswa                                                                       |
| Aktor         | Admin Akademik                                                                                       |
| Tujuan        | Data mahasiswa terhapus sebagai bentuk khusus dari pengelolaan data mahasiswa                        |
| Deskripsi     | Admin memilih data mahasiswa, mengonfirmasi penghapusan, dan sistem menghapus data tersebut; syarat: tidak ada data akademik aktif |

| Kegiatan                                                             | Respon sistem                                                        |
| Skenario Normal                                                      |                                                                      |
| 1. Admin memilih data mahasiswa yang akan dihapus                    | 2. Sistem memeriksa mahasiswa tidak memiliki status akademik aktif   |
| 3. Admin mengonfirmasi penghapusan                                   | 4. Sistem menghapus data mahasiswa dan menampilkan konfirmasi        |
| Skenario Alternative                                                 |                                                                      |
| 5. Mahasiswa masih memiliki status atau data aktif (cabang langkah 2)| 6. Sistem menolak penghapusan dan menampilkan pesan data masih aktif |
| Skenario Akhir                                                       | Use case selesai jika data terhapus; jika mahasiswa masih memiliki data akademik aktif, data tidak terhapus. |

Keterangan: use case khusus dari SIA-UC10 Kelola Data Mahasiswa. Perilaku pembeda: data mahasiswa terhapus, dengan syarat tidak ada data akademik aktif. Langkah bersama mengikuti Tabel skenario SIA-UC10.


 Lembar Penelusuran Penelaahan Diagram P04 ke Skenario P05 SIA

| ID Skenario | Nama Use Case | Relasi & Elemen Diagram yang Ditelusuri | Hasil Penelaahan & Penjelasannya |
| SIA-UC07 | Lihat Kalender Akademik | Generalization Aktor: Mahasiswa & Dosen -> Civitas Akademika | Sesuai. Skenario ditulis satu kali atas nama Civitas Akademika; berlaku untuk Mahasiswa dan Dosen. |
| SIA-UC08 | Input Nilai Mata Kuliah | Asosiasi: Dosen -> SIA-UC08<br>Realization: SIA-CO01 | Sesuai. Diprasyaratkan hanya untuk dosen pengampu; nilai di luar rentang ditolak pada jalur alternatif. Keterangan collaboration SIA-CO01 dicantumkan. |
| SIA-UC09 | Lihat KHS | Asosiasi: Mahasiswa -> SIA-UC09<br>Realization: SIA-CO02 | Sesuai. Jalur normal hanya menampilkan nilai yang sudah dipublikasikan; alternatif menangani kondisi belum publikasi. Keterangan collaboration SIA-CO02 dicantumkan. |
| SIA-UC10 | Kelola Data Mahasiswa | Asosiasi: Admin Akademik -> SIA-UC10<br>Generalization: Parent dari UC11, UC12, UC13 | Sesuai. Berfungsi sebagai skenario umum pengelolaan yang memuat langkah bersama bagi UC11, UC12, dan UC13. |
| SIA-UC11 | Tambah Data Mahasiswa | Generalization: Child dari SIA-UC10 | Sesuai. Menjelaskan perilaku pembeda (penambahan data mahasiswa baru); langkah bersama merujuk ke SIA-UC10. |
| SIA-UC12 | Ubah Data Mahasiswa | Generalization: Child dari SIA-UC10 | Sesuai. Menjelaskan perilaku pembeda (pengubahan data mahasiswa); langkah bersama merujuk ke SIA-UC10. |
| SIA-UC13 | Hapus Data Mahasiswa | Generalization: Child dari SIA-UC10 | Sesuai. Menjelaskan perilaku pembeda (penghapusan data) dengan syarat tidak memiliki status/data akademik aktif. |