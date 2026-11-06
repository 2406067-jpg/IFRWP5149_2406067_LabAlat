<!-- Tabel analisis model P05 SIA -->

| ID Skenario | Nama Use Case                  | Sumber / Aktor                   | Hubungan / Pemetaan  | Tujuan / Use Case Target          |
| SIA-UC07    | Lihat Kalender Akademik        | Civitas Akademika                | Asosiasi             | SIA-UC07 Lihat Kalender Akademik  |
| SIA-UC07    | Lihat Kalender Akademik        | Mahasiswa                        | Generalisasi         | Civitas Akademika                 |
| SIA-UC07    | Lihat Kalender Akademik        | Dosen                            | Generalisasi.        | Civitas Akademika                 |
| SIA-UC08    | Input Nilai Mata Kuliah        | Dosen                            | Asosiasi             | SIA-UC08 Input Nilai Mata Kuliah  |
| SIA-UC09    | Lihat KHS                      | Mahasiswa                        | Asosiasi             | SIA-UC09 Lihat KHS                |
| SIA-UC10    | Kelola Data Mahasiswa          | Admin Akademik                   | Asosiasi             | SIA-UC10 Kelola Data Mahasiswa    |
| SIA-UC11    | Tambah Data Mahasiswa          | SIA-UC11 Tambah Data Mahasiswa   | Generalisasi         | SIA-UC10 Kelola Data Mahasiswa    |
| SIA-UC12    | Ubah Data Mahasiswa            | SIA-UC12 Ubah Data Mahasiswa.    | Generalisasi         | SIA-UC10 Kelola Data Mahasiswa    |  
| SIA-UC13    | Hapus Data Mahasiswa           | SIA-UC13 Hapus Data Mahasiswa    | Generalisasi         | SIA-UC10 Kelola Data Mahasiswa    |
| SIA-CO01    | Input Nilai Mata Kuliah        | SIA-CO01 Input Nilai Mata Kuliah | Realisasi            | SIA-UC08 Input Nilai Mata Kuliah  |
| SIA-CO02    | Lihat KHS                      | SIA-CO02 Lihat KHS               | Realisasi            | SIA-UC09 Lihat KHS                |                     