A. TUJUAN PEMBELAJARAN
Setelah mengikuti praktikum, mahasiswa mampu:

1. Menyusun alur utama sebuah activity diagram dari Skenario Normal pada
   tabel skenario Pertemuan 5, dengan tepat satu initial node, action yang
   berurutan mengikuti langkah skenario, dan tepat satu activity final node,
   tanpa alur yang terputus (Indikator 4.1).
2. Mengubah Skenario Alternative pada tabel skenario menjadi cabang
   decision dengan guard yang lengkap dan benar, lalu mengembalikan
   cabangnya ke alur utama melalui merge atau mengakhirinya pada jalur akhir
   yang jelas (Indikator 4.2).
3. Menggunakan fork dan join sebagai pasangan untuk dua proses yang
   berjalan paralel, dengan join yang menyatukan kembali kedua proses
   sebelum alur dilanjutkan (Indikator 4.2).
4. Mengelompokkan setiap action ke dalam swimlane yang sesuai dengan
   aktor pada tabel skenario, sehingga tanggung jawab setiap action terbaca
   dari partisinya (Indikator 4.1 dan 4.2).
5. Menelusurkan setiap action pada activity diagram ke langkah tabel skenario
   Pertemuan 5 yang menjadi sumbernya, dan memeriksa hasil akhir dengan
   checklist penilaian sebelum berkas dikumpulkan.
   Tujuan di atas terukur melalui produk yang dihasilkan mahasiswa, yaitu tujuh
   activity diagram studi kasus LAB untuk tujuh use case utama, satu activity diagram
   tugas akademik, dan catatan perbandingan tugas mandiri, yang masing masing
   diperiksa dengan checklist pada Bagian C.4. Satu dari tujuh activity LAB, yaitu
   Activity Proses Keputusan Peminjaman, dikerjakan sebagai tugas mandiri dengan
   cara khusus pada Langkah 10 Bagian C.2.

B. Dasar Teori
Activity Diagram merupakan salah satu diagram dalam UML (Unified Modeling Language) yang digunakan untuk menggambarkan alur aktivitas atau proses dalam sebuah sistem. Diagram ini menunjukkan urutan kegiatan yang dilakukan oleh aktor maupun sistem, mulai dari proses awal hingga proses berakhir.

Activity Diagram dibuat berdasarkan tabel skenario use case yang telah disusun pada Pertemuan 5. Jika use case diagram menggambarkan fungsi yang tersedia dalam sistem, maka activity diagram menjelaskan bagaimana fungsi tersebut dijalankan melalui urutan aktivitas yang lebih terperinci.

1. Initial Node
   Initial node merupakan simbol yang digunakan untuk menunjukkan titik awal dari suatu aktivitas. Setiap activity diagram harus memiliki tepat satu initial node sebagai awal proses.
   Contohnya pada Sistem Informasi Akademik, proses dimulai ketika dosen melakukan aktivitas memasukkan nilai mata kuliah ke dalam sistem.
2. Action
   Action merupakan simbol yang digunakan untuk menggambarkan suatu kegiatan atau tindakan yang dilakukan oleh aktor maupun sistem. Penulisan action menggunakan kata kerja dan objek agar aktivitas yang dilakukan lebih mudah dipahami.
   Contohnya adalah Memasukkan Nilai Mata Kuliah, Menyimpan Nilai, Memeriksa Kelengkapan Nilai, dan Melihat KHS.
3. Control Flow
   Control flow merupakan garis panah yang menghubungkan satu aktivitas dengan aktivitas lainnya. Simbol ini menunjukkan urutan pelaksanaan kegiatan dari satu proses ke proses berikutnya.
   Dengan adanya control flow, alur aktivitas dalam sistem dapat terlihat secara berurutan dan tidak terputus.
4. Decision dan Merge
   Decision merupakan simbol yang digunakan untuk menunjukkan percabangan berdasarkan kondisi tertentu. Setiap jalur keluar dari decision harus memiliki keterangan kondisi atau guard yang ditulis menggunakan tanda kurung siku.
   Contohnya pada proses pemeriksaan nilai, terdapat dua kondisi, yaitu [lengkap] dan [belum lengkap]. Jika nilai belum lengkap, dosen harus melengkapi nilai terlebih dahulu. Sementara itu, jika nilai sudah lengkap, proses dilanjutkan ke tahap berikutnya.
   Merge merupakan simbol yang digunakan untuk menggabungkan kembali beberapa jalur aktivitas yang sebelumnya bercabang menjadi satu alur utama.
5. Fork dan Join
   Fork merupakan simbol yang digunakan untuk membagi satu alur aktivitas menjadi dua atau lebih proses yang berjalan secara bersamaan atau paralel. Sementara itu, join digunakan untuk menggabungkan kembali proses-proses paralel tersebut.
   Contohnya pada Sistem Informasi Akademik, setelah nilai disahkan, sistem menjalankan dua proses secara bersamaan, yaitu menerbitkan KHS pada portal akademik dan mengirimkan pemberitahuan hasil studi kepada mahasiswa. Kedua proses tersebut kemudian digabungkan kembali menggunakan join.
6. Activity Final Node
   Activity final node merupakan simbol yang digunakan untuk menunjukkan bahwa seluruh aktivitas dalam suatu proses telah selesai. Semua jalur aktivitas, termasuk jalur percabangan, harus memiliki akhir proses yang jelas.
   Contohnya adalah ketika mahasiswa berhasil melihat KHS setelah seluruh proses input, pemeriksaan, pengesahan, dan publikasi nilai selesai dilakukan.
7. Swimlane
   Swimlane merupakan bagian dalam activity diagram yang digunakan untuk mengelompokkan aktivitas berdasarkan pihak yang bertanggung jawab dalam menjalankan kegiatan tersebut. Setiap aktivitas ditempatkan pada swimlane sesuai dengan aktor atau sistem yang melakukannya.
   Dalam Sistem Informasi Akademik, swimlane yang digunakan terdiri dari Dosen, Sistem, Admin Akademik, dan Mahasiswa. Dengan adanya swimlane, pembagian tugas dan tanggung jawab setiap pihak dapat terlihat lebih jelas.

C. Hasil Praktikum
Pada praktikum Pertemuan 6 dilakukan pembuatan Activity Diagram untuk Sistem Informasi Akademik (SIA). Praktikum ini merupakan lanjutan dari Pertemuan 5, yaitu penyusunan skenario use case. Pada pertemuan ini, skenario yang telah dibuat diubah menjadi diagram aktivitas agar alur proses dalam sistem dapat digambarkan secara visual dan lebih mudah dipahami.

Tugas SIA pada praktikum ini berfokus pada proses Input Nilai Mata Kuliah sampai Lihat KHS. Activity diagram dibuat dengan menggunakan empat swimlane, yaitu Dosen, Sistem, Admin Akademik, dan Mahasiswa.

1. Identifikasi Aktor dan Swimlane
   Berdasarkan tugas Sistem Informasi Akademik, terdapat empat pihak yang terlibat dalam proses input nilai sampai melihat KHS.

| No. | Aktor/Swimlane | Tugas_dan_Tanggung_Jawab                                                                                  |
| --- | -------------- | --------------------------------------------------------------------------------------------------------- |
| 1   | Dosen          | Memasukkan nilai mata kuliah dan melengkapi nilai apabila masih terdapat kekurangan.                      |
| 2   | Sistem         | Menyimpan nilai, memeriksa kelengkapan nilai, menerbitkan KHS, dan mengirimkan pemberitahuan hasil studi. |
| 3   | Admin          | Akademik Memeriksa dan mengesahkan nilai yang telah dimasukkan oleh dosen.                                |
| 4   | Mahasiswa      | Melihat Kartu Hasil Studi (KHS) yang telah diterbitkan oleh sistem.                                       |

Keempat swimlane tersebut digunakan untuk menunjukkan pembagian aktivitas dan tanggung jawab masing-masing pihak selama proses berlangsung.

2. Alur Utama Activity Diagram
   Alur utama menggambarkan proses normal dari awal hingga akhir. Proses dimulai ketika dosen memasukkan nilai mata kuliah ke dalam sistem. Selanjutnya, sistem menyimpan nilai yang telah dimasukkan.
   Setelah nilai disimpan, sistem melakukan pemeriksaan kelengkapan nilai. Jika nilai sudah lengkap, proses dilanjutkan kepada Admin Akademik untuk memeriksa dan mengesahkan nilai. Setelah disahkan, sistem menyiapkan publikasi hasil studi sebelum KHS diterbitkan.
3. Penerapan Decision dan Merge
   Pada activity diagram SIA, decision digunakan untuk memeriksa apakah nilai mata kuliah sudah lengkap atau belum. Percabangan tersebut memiliki dua kondisi, yaitu:
   [Lengkap]: Jika seluruh nilai sudah lengkap, proses dilanjutkan ke Admin Akademik untuk pemeriksaan dan pengesahan nilai.
   [Belum lengkap]: Jika masih terdapat nilai yang belum lengkap, dosen diminta melengkapi nilai mata kuliah tersebut.
   Setelah dosen melengkapi nilai, alur kembali bergabung melalui merge sebelum dilanjutkan ke proses pemeriksaan dan pengesahan oleh Admin Akademik.
4. Penerapan Fork dan Join
   Setelah nilai diperiksa dan disahkan oleh Admin Akademik, sistem menyiapkan publikasi hasil studi. Selanjutnya, digunakan fork untuk membagi proses menjadi dua aktivitas yang berjalan secara bersamaan, yaitu:
   Menerbitkan KHS pada portal akademik: Sistem menerbitkan Kartu Hasil Studi agar dapat dilihat oleh mahasiswa.

Mengirim pemberitahuan hasil studi kepada mahasiswa: Sistem mengirimkan informasi kepada mahasiswa bahwa hasil studi telah tersedia.
Setelah kedua aktivitas selesai, proses digabungkan kembali menggunakan join. Selanjutnya, mahasiswa dapat melihat KHS yang telah diterbitkan oleh sistem.

5. Urutan Proses Activity Diagram SIA
   Berikut merupakan urutan aktivitas yang diterapkan dalam diagram:

| No. | Aktor/Swimlane | Aktivitas                                                        |
| --- | -------------- | ---------------------------------------------------------------- |
| 1   | Dosen          | Memasukkan nilai mata kuliah.                                    |
| 2   | Sistem         | Menyimpan nilai mata kuliah.                                     |
| 3   | Sistem         | Memeriksa kelengkapan nilai.                                     |
| 4   | Dosen          | Melengkapi nilai mata kuliah yang belum lengkap jika diperlukan. |
| 5   | Admin_Akademik | Memeriksa dan mengesahkan nilai.                                 |
| 6   | Sistem         | Menyiapkan publikasi hasil studi.                                |
| 7   | Sistem         | Menerbitkan KHS pada portal akademik.                            |
| 8   | Sistem         | Mengirim pemberitahuan hasil studi kepada mahasiswa.             |
| 9   | Mahasiswa      | Melihat KHS.                                                     |

6. Penerapan Initial Node dan Activity Final Node
   Initial node digunakan sebagai titik awal proses ketika dosen mulai memasukkan nilai mata kuliah. Sementara itu, activity final node digunakan sebagai titik akhir setelah mahasiswa berhasil melihat KHS.
   Dengan adanya kedua simbol tersebut, alur proses memiliki awal dan akhir yang jelas sehingga tidak terdapat aktivitas yang menggantung.
7. Hasil Akhir Praktikum
   Hasil akhir praktikum berupa satu Activity Diagram Sistem Informasi Akademik yang menggambarkan proses Input Nilai Mata Kuliah sampai Lihat KHS. Diagram tersebut menggunakan empat swimlane, satu decision untuk pemeriksaan kelengkapan nilai, satu merge untuk menggabungkan kembali jalur percabangan, serta satu pasang fork dan join untuk menggambarkan proses penerbitan KHS dan pengiriman pemberitahuan secara bersamaan.
   Melalui praktikum ini, alur aktivitas dalam Sistem Informasi Akademik dapat digambarkan secara lebih terstruktur. Selain itu, pembagian tanggung jawab antara dosen, sistem, admin akademik, dan mahasiswa menjadi lebih jelas sehingga proses input nilai hingga mahasiswa melihat KHS lebih mudah dipahami.
