<!-- Tabel analisis model P04 SIA -->

|               Sumber               |  Hubungan   |              Tujuan               |
|------------------------------------|-------------|-----------------------------------|
| Civitas_akademika                  | Asosiasi    | SIA-UC07 Lihat Kalender Akademik  |
| Mahasiswa                          | Asosiasi    | SIA-UC03 Ajukan KRS               |
| Mahasiswa                          | Asosiasi    | SIA-UC05 Unduh Bukti KRS          |
| Mahasiswa                          | Asosiasi    | SIA-UC09 Lihat KHS                |
| Mahasiswa                          | Generalisasi| Civitas_akademika                 |
| Dosen                              | Asosiasi    | SIA-UC08 Input Nilai Mata Kuliah  |
| Dosen                              | Generalisasi| Civitas_akademika                 |
| Dosen_wali                         | Asosiasi    | SIA-UC04 Validasi KRS             |
| Admin_akademik                     | Asosiasi    | SIA-UC02 Kelola Jadwal Kuliah     |
| Admin_akademik                     | Asosiasi    | SIA-UC06 Proses Keputusan KRS     |
| Admin_akademik                     | Asosiasi    | SIA-UC10 Kelola Data Mahasiswa    |
| SIA-UC03 Ajukan KRS                | «include»   | SIA-UC04 Validasi KRS             |
| SIA-UC05 Unduh Bukti KRS           | «extend»    | SIA-UC03 Ajukan KRS               |
| SIA-UC11 Tambah Data Mahasiswa     | Generalisasi| SIA-UC10 Kelola Data Mahasiswa    |
| SIA-UC12 Ubah Data Mahasiswa       | Generalisasi| SIA-UC10 Kelola Data Mahasiswa    |
| SIA-UC13 Hapus Data Mahasiswa      | Generalisasi| SIA-UC10 Kelola Data Mahasiswa    |
| SIA-CO01 Input Nilai Mata Kuliah   | Realisasi   | SIA-UC08 Input Nilai Mata Kuliah  |
| SIA-CO02 Lihat KHS                 | Realisasi   | SIA-UC09 Lihat KHS                |