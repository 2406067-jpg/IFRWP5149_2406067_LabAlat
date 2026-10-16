<!-- Deskripsi Skenario -->

Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan,
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil,
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS
dan memberikan catatan keputusan.

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

--------------------------------------------------------------------------------------------------|
|      Aktor         |                                                                            |
|--------------------|------------------------------------------------------------------          |     
|Mahasiswa           |   Dapat Melihat Jadwal Kuliah, mengajukan KRS, dan mencetak bukti          |
|--------------------|------------------------------------------------------------------ --       |
|Admin               |   Dapat Mengelola Jadwal Kuliah dan memproses keputusan                    |           |
|Akademik            |                                                                            |
---------------------|----------------------------------------------------------------------      |
|Dosen wali          |Melihat Dapat memproses persetujuan atau penolakan KRS
--------------------------------------------------------------------------------------------------|



<!-- Tabel susunan katalog use case -->
<!-- Tabel Ketersediaan -->

|   ID   |          Nama use case        | Peran dalam model                |
|--------|-------------------------------|----------------------------------|
|LAB-UC01| Lihat ketersediaan peralatan  | Fungsi utama mahasiswa           |
|LAB-UC02|Kelola data peralatan          | Fungsi utama petugas             |
|LAB-UC03|Ajukan peminjaman              |  Fungsi utama mahasiswa          |
|LAB-UC04|Periksa ketersediaan           |PerilakU yang disertakan UC03     |
|LAB-UC05| Cetak bukti pengajuan         |Tambahan bersyarat pada UC03      |
|LAB-UC06|Proses keputusan peminjaman    | Fungsi utama petugas             |
|LAB-UC07| Lihat laporan peminjaman      | FungsI utama kepala laboratorium |


<!-- Tabel -->