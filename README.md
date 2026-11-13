
# Sistem Informasi Peminjaman Peralatan Laboratorium (`LabAlat`)

![Mata Kuliah](https://img.shields.io/badge/Mata_Kuliah-IFRWP5149_Praktikum_ADBO-blue?style=flat-square)
![UML](https://img.shields.io/badge/Standar_Notasi-UML_2.5.1-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Pertemuan_06_Selesai-success?style=flat-square)

Repositori resmi dokumentasi, skenario, dan artefak pemodelan untuk mata kuliah **Praktikum Analisis dan Desain Berorientasi Objek (IFRWP5149)**. Berisi seluruh rangkaian pengerjaan dari Pertemuan 01 hingga Pertemuan 06 untuk dua studi kasus:

1. **Studi Kasus Utama (`LAB`):** Sistem Informasi Peminjaman Peralatan Laboratorium.
2. **Studi Kasus Pembanding (`SIA`):** Sistem Informasi Akademik.

---

## Identitas Mahasiswa

| Atribut                   | Keterangan                                                       |
| :------------------------ | :--------------------------------------------------------------- |
| **Nama Lengkap**    | DICKI FIRGIAWAN                                                  |
| **NIM**             | `2406067`                                                      |
| **Mata Kuliah**     | Praktikum Analisis dan Desain Berorientasi Objek (`IFRWP5149`) |
| **Kakas Pemodelan** | draw.io (OMG UML 2.5.1)                                          |
| **Editor & VCS**    | Visual Studio Code & Git                                         |

---

## Struktur Direktori Repositori

```text
IFRWP5149_2406067_LabAlat/
├── 00_administrasi/
│   ├── P01_2406067_logbook_v01.md
│   ├── P02_2406067_logbook_v01.md
│   ├── P03_2406067_logbook_v01.md
│   ├── P04_2406067_logbook_v01.md
│   ├── P05_2406067_logbook_v01.md
│   └── P06_2406067_logbook_v01.md
├── 01_skenario/
│   ├── P02_LAB_skenario_v01.md & P02_SIA_skenario_v01.md
│   ├── P03_LAB_skenario_v01.md & P03_SIA_skenario_v01.md
│   ├── P04_LAB_kebutuhan_v01.md & P04_LAB_skenario_v01.md
│   ├── P04_SIA_kebutuhan_v01.md & P04_SIA_skenario_v01.md
│   ├── P05_2406067_LAB_telaah_skenario_v01.docx
│   ├── P05_2406067_SIA_skenario_v01.docx
│   ├── P05_LAB_skenario_v01.md & P05_SIA_skenario_v01.md
│   └── S-ORI-01_orientasi_kasus_v01.md
├── 02_template/
│   ├── P02_metadata_artefak.v01.md
│   ├── P03_metadata_artefak.v01.md
│   ├── P04_metadata_artefak_v01.md
│   ├── P05_metadata_artefak_v01.md
│   ├── P06_metadata_artefak.v01.md
│   └── template_metadata_artefak_v01.md
├── 03_latihan_tools/
│   ├── P01_2406067_latihan_activity_v01.drawio (.png)
│   ├── P02/ (LAB & SIA)
│   ├── P03/ (LAB & SIA)
│   └── P04/ (LAB & SIA)
├── 04_model_analisis/
│   ├── P03/
│   ├── P04/ (LAB & SIA)
│   ├── P05/
│   └── P06/
│       ├── LAB/                            # 7 Activity Diagram LAB (.drawio & .png)
│       └── SIA/                            # 7 Activity Diagram SIA (.drawio & .png)
├── 05_model_desain/                        # Artefak model desain (tahap lanjutan)
├── 06_laporan/
│   ├── P01_2406067_laporan_singkat_v01.md
│   ├── P02_2406067_jobsheet_review_v01.md
│   ├── P03_2406067_jobsheet_review_v01.md
│   ├── P04_2406067_jobsheet_review_v01.md
│   ├── P05_2406067_jobsheet_review_v01.md
│   └── P06_2406067_jobsheet_review_v01.md
└── README.md


Log Progres Praktikum
Pertemuan	Fokus Materi & Pemodelan	Artefak Utama yang Dihasilkan	Status
P01	Pengenalan Kakas & Orientasi Kasus	Logbook, Orientasi Kasus (S-ORI-01), Latihan Activity Diagram, & Laporan Singkat	Selesai
P02	Pemodelan Use Case Dasar	Logbook, Skenario & Latihan Use Case (LAB & SIA), Metadata, & Jobsheet Review	Selesai
P03	Spesifikasi Use Case & System Boundary	Logbook, Skenario & Model Analisis Use Case (LAB & SIA), Metadata, & Review	Selesai
P04	Relasi Use Case (Include, Extend, Generalization)	Logbook, Kebutuhan & Skenario, Diagram Kumulatif (LAB & SIA), Metadata, & Review	Selesai
P05	Skenario Use Case (Normal & Alternative Flow)	Logbook, Skenario & Telaah Skenario (.md & .docx), Metadata, & Jobsheet Review	Selesai
P06	Pemodelan Proses Bisnis (Activity Diagram)	Logbook, 7 Activity Diagram LAB, 7 Activity Diagram SIA, Metadata, & Review	Selesai
Katalog Artefak Pertemuan 06 (Activity Diagram)
Seluruh diagram di bawah ini disusun menggunakan partisi (swimlane), control flow, decision & guard, merge, serta fork-join sesuai standar UML 2.5.1 dan selaras dengan skenario Pertemuan 05.
1. Studi Kasus Laboratorium (04_model_analisis/P06/LAB/)
No	Nama Berkas (.drawio / .png)	Use Case Terkait	Aktor / Swimlane
1	P06_2406067_LAB_activity_peminjaman_v01	LAB-UC03, UC04, UC05	Mahasiswa, Sistem, Petugas Lab
2	P06_2406067_LAB_activity_pengembalian_v01	LAB-UC11, UC12	Mahasiswa, Petugas Lab, Sistem
3	P06_2406067_LAB_activity_lihat_ketersediaan_v01	LAB-UC01	Peminjam, Sistem
4	P06_2406067_LAB_activity_kelola_data_v01	LAB-UC02, UC08–UC10	Petugas Lab, Sistem
5	P06_2406067_LAB_activity_cetak_bukti_v01	LAB-UC05	Mahasiswa, Sistem
6	P06_2406067_LAB_activity_keputusan_v01	LAB-UC06	Petugas Lab, Sistem
7	P06_2406067_LAB_activity_laporan_v01	LAB-UC07	Kepala Lab, Sistem
2. Studi Kasus Sistem Informasi Akademik (04_model_analisis/P06/SIA/)
No	Nama Berkas (.drawio / .png)	Use Case Terkait	Aktor / Swimlane
1	P06_2406067_SIA_activity_pengajuan_krs_v01	SIA-UC01	Mahasiswa, Sistem
2	P06_2406067_SIA_activity_persetujuan_krs_v01	SIA-UC02	Dosen, Sistem
3	P06_2406067_SIA_activity_kelola_jadwal_v01	SIA-UC03	Admin Akademik, Sistem
4	P06_2406067_SIA_activity_input_nilai_v01	SIA-UC08	Dosen, Sistem
5	P06_2406067_SIA_activity_pengesahan_nilai_v01	SIA-UC05	Admin Akademik, Sistem
6	P06_2406067_SIA_activity_lihat_khs_v01	SIA-UC09	Mahasiswa, Sistem
7	P06_2406067_SIA_activity_cetak_transkrip_v01	SIA-UC07	Mahasiswa, Sistem

```
