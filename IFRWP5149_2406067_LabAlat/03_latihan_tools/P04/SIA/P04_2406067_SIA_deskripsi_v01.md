| Elemen              | SIA-UC08: Input Nilai Mata Kuliah                                                      |
|---------------------|----------------------------------------------------------------------------------------|
| Tujuan              | Menyimpan data nilai mahasiswa untuk mata kuliah yang diampu dosen                      |
| Aktor utama         | Dosen                                                                                  |
| Sumber kebutuhan    | SIA-R08 dan SIA-R12                                                                    |
| Pemicu              | Dosen memilih fungsi input nilai dan menentukan kelas yang diampu                      |
| Prasyarat           | Dosen terautentikasi dan merupakan pengampu sah dari mata kuliah terpilih               |
| Pascakondisi berhasil| Nilai mata kuliah tersimpan di dalam sistem                                            |
| Pascakondisi gagal  | Nilai tidak tersimpan dan data nilai sebelumnya tidak berubah                          |
| Collaboration       | SIA-CO01 Input Nilai Mata Kuliah                                                       |


| Elemen              | SIA-UC09: Lihat KHS                                                                    |
|---------------------|----------------------------------------------------------------------------------------|
| Tujuan              | Menampilkan Kartu Hasil Studi (KHS) mahasiswa pada semester terpilih                   |
| Aktor utama         | Mahasiswa                                                                              |
| Sumber kebutuhan    | SIA-R09 dan SIA-R12                                                                    |
| Pemicu              | Mahasiswa memilih menu KHS dan menentukan semester                                     |
| Prasyarat           | Mahasiswa telah terautentikasi di dalam sistem                                         |
| Pascakondisi berhasil| Sistem menampilkan lembar KHS yang hanya berisi nilai publikasi resmi                 |
| Pascakondisi gagal  | KHS tidak ditampilkan atau menampilkan pesan nilai belum dipublikasikan                |
| Collaboration       | SIA-CO02 Lihat KHS                                                                     |