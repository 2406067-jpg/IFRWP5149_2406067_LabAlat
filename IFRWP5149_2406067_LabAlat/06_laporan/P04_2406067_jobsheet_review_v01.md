| NO |                                         Temuan                                                       |                                           Perbaikan yang diperlukan                                                              |
| 1  | Arah panah relasi generalization aktor (Mahasiswa dan Dosen) sempat terbalik menunjuk aktor khusus.  | Balik arah panah generalization dari aktor khusus (Mahasiswa/Dosen) menuju aktor umum (Civitas Akademika / Peminjam).            |
| 2  | Notasi realization pada collaboration sempat menggunakan panah garis putus-putus terbuka.            | Ubah notasi realization menjadi garis putus-putus berujung segitiga kosong/transparan menunjuk ke use case utama.                |
| 3  | Aktor khusus Mahasiswa menarik garis asosiasi ke fungsi umum yang sudah diwarisi.                    | Hapus garis asosiasi berulang dari Mahasiswa ke use case umum; Mahasiswa mewarisi akses tersebut dari aktor umum.                |
| 4  | Penamaan berkas ekspor diagram dan deskripsi belum seragam antara folder latihan dan model.          | Disesuaikan penamaan seluruh artefak P04 mengikuti pola standar P04_2406067_<KASUS>_<ARTEFAK>_v01.                               |


| NO |                                                          Alasan                                                                                   |
| 1  | Dalam standar UML OMG 2.5.1, panah generalization selalu menunjuk dari elemen khusus (specialized) ke elemen umum (general).                      |
| 2  | Realization adalah hubungan perwujudan abstrak antara collaboration dan use case yang secara notasi resmi menggunakan segitiga kosong.            |
| 3  | Aktor khusus secara otomatis mewarisi seluruh asosiasi milik aktor umum, sehingga tidak boleh digambar ulang agar tidak redundan.                 |
| 4  | Konsistensi penamaan dan struktur folder wajib dijaga sesuai kriteria Jobsheet P04 agar keterlacakan (traceability) artefak terpenuhi.            |