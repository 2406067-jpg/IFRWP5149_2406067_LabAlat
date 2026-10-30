<!-- Deskripsi Skenario -->

Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan.

<!-- Tabel Kebutuhan -->
|  ID   |                             Kebutuhan_tugas                              |
|-------|--------------------------------------------------------------------------|
|SIA-R01|                  Mahasiswa dapat melihat jadwal kuliah                   |
|SIA-R02|               Admin akademik dapat mengelola jadwal kuliah               |
|SIA-R03|                      Mahasiswa dapat mengajukan KRS                      |
|SIA-R04|             Sistem memvalidasi KRS sebagai bagian pengajuan              |
|SIA-R05|Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
|SIA-R06|        Dosen wali dapat memproses persetujuan atau penolakan KRS         |

<!--Batasan sistem dan aturan -->
• Pengguna telah terautentikasi.
• Data mata kuliah, prasyarat, dan jadwal tersedia.
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
• KRS tersimpan belum berarti disetujui.
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas.

<!-- Tabel Identifikasi -->
|    Aktor     |                         Tujuan Terhadap Sistem                                    |
|--------------|-----------------------------------------------------------------------------------|
|Mahasiswa     |Melihat jadwal kuliah, mengajukan KRS, dan mengunduh bukti pengajuan               |
|Dosen Wali    |Memproses pengajuan KRS, menyetujui atau menolak, dan memberikan catatan keputusan |

<!-- Tabel susunan katalog use case -->
| ID      |         Nama Use Case                |  Aktor Sumber Kebutuhan  |
|---------|--------------------------------------|--------------------------|
|UC-01    | Melihat Jadwal Kuliah Mahasiswa      | SIA-R01                  |
|UC-02    | Ajukan KRS Mahasiswa                 | SIA-R03                  |
|UC-03    | Validasi KRS Sistem (proses internal)| SIA-R04                  |
|UC-04    | Unduh Bukti Pengajuan KRS Mahasiswa  | SIA-R05                  |
|UC-05    | Proses Keputusan KRS Dosen Wali      | SIA-R06                  |

<!-- Relasi include-->
SIA-UC01 «include» SIA-UC02
Alasan: Validasi KRS menjadi bagian wajib dari proses pengajuan KRS. Sistem harus memeriksa kelengkapan pengajuan, prasyarat mata kuliah, dan benturan jadwal sebelum pengajuan dapat disimpan.

<!-- Relasi Extend -->
SIA-UC03 «extend» SIA-UC01
Extension point: Konfirmasi penyimpanan.
Kondisi: [mahasiswa memilih unduh bukti setelah pengajuan berhasil disimpan].
Alasan: Pengunduhan bukti merupakan proses tambahan yang bersifat opsional. Pengajuan KRS tetap berhasil meskipun mahasiswa tidak memilih untuk mengunduh bukti.
