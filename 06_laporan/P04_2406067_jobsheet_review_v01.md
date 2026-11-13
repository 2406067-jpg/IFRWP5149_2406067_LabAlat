
A. Tujuan Pembelajaran
Setelah mengikuti praktikum, mahasiswa mampu:

1. Mengidentifikasi satu aktor umum dan minimal dua aktor khusus dari skenario yang diberikan, lalu menyusun hierarki generalization aktor dengan arah panah yang benar (aktor khusus menuju aktor umum) tanpa menggambar ulang asosiasi yang diwarisi.
2. Menyusun generalization use case yang memuat satu use case umum dan minimal dua use case khusus, serta menjelaskan perilaku yang diwarisi dari use case umum dan perilaku yang membedakan setiap use case khusus.
3. Menempatkan minimal dua collaboration (elips garis putus-putus) yang namanya sama persis dengan use case yang direalisasikan, dan menghubungkannya dengan relasi realization (garis putus-putus berujung segitiga kosong) dari collaboration menuju use case.
4. Membuat use case diagram kumulatif Pertemuan 4 pada kasus laboratorium, yaitu diagram Pertemuan 3 yang dipertahankan utuh (LABUC01 sampai LAB-UC07, relasi «include», relasi «extend» beserta kondisi dan extension point-nya, dan ketiga aktor Pertemuan 3) lalu ditambah elemen baru Pertemuan 4, dengan seluruh aktor di luar batas sistem dan seluruh use case di dalam batas sistem.
5. Menyusun satu use case description baru (Catat Pengembalian Peralatan) yang memuat pemicu, prasyarat, alur utama, alur alternatif, pascakondisi berhasil, dan pascakondisi gagal, serta konsisten dengan diagram.
6. Menunjukkan keterlacakan setiap elemen baru (aktor, use case, collaboration) ke kebutuhan yang mendasarinya, memperbaiki model berdasarkan review, dan mendokumentasikan perubahan pada versi berikutnya (v02).

B. Dasar Teori
Use Case Diagram merupakan salah satu diagram dalam UML (Unified Modeling Language) yang digunakan untuk menggambarkan hubungan antara aktor dengan fungsi-fungsi yang terdapat di dalam suatu sistem. Diagram ini bertujuan untuk menunjukkan bagaimana pengguna berinteraksi dengan sistem untuk mencapai tujuan tertentu. Pada pertemuan sebelumnya, use case diagram telah mempelajari aktor, use case, batas sistem, association, include, dan extend. Pada pertemuan ini, materi dikembangkan dengan menambahkan konsep generalization dan collaboration.

1. Generalization Aktor
   Generalization aktor merupakan hubungan antara aktor umum (general) dengan aktor khusus (specialized). Aktor khusus mewarisi seluruh fungsi yang dimiliki oleh aktor umum, sehingga tidak perlu menggambarkan ulang hubungan yang sama pada setiap aktor khusus.

Contohnya pada Sistem Informasi Akademik, Civitas Akademika menjadi aktor umum, sedangkan Mahasiswa dan Dosen menjadi aktor khusus. Keduanya dapat menggunakan fungsi melihat kalender akademik karena fungsi tersebut diwariskan dari aktor umum.

2. Generalization Use Case
   Generalization use case merupakan hubungan antara use case umum dengan use case khusus. Use case khusus mewarisi tujuan dan perilaku dasar dari use case umum, tetapi memiliki fungsi tambahan atau hasil yang lebih spesifik.

Contohnya adalah Kelola Data Mahasiswa sebagai use case umum yang memiliki tiga use case khusus, yaitu Tambah Data Mahasiswa, Ubah Data Mahasiswa, dan Hapus Data Mahasiswa. Ketiga fungsi tersebut memiliki tujuan yang sama, yaitu mengelola data mahasiswa, tetapi proses dan hasilnya berbeda.

3. Collaboration
   Collaboration merupakan kumpulan elemen yang saling bekerja sama untuk menjalankan suatu fungsi dalam sistem. Collaboration digunakan untuk menunjukkan bagaimana bagian-bagian di dalam sistem bekerja sama dalam mewujudkan suatu use case.

Dalam diagram UML, collaboration digambarkan menggunakan bentuk elips dengan garis putus-putus. Nama collaboration harus sama persis dengan nama use case yang direalisasikannya.

4. Realization
   Realization merupakan hubungan yang menunjukkan bahwa sebuah collaboration merealisasikan atau mewujudkan perilaku dari suatu use case. Hubungan ini digambarkan menggunakan garis putus-putus dengan ujung panah segitiga kosong yang mengarah dari collaboration menuju use case.

Contohnya, collaboration Input Nilai Mata Kuliah merealisasikan use case Input Nilai Mata Kuliah.

5. Relasi Include dan Extend
   Include merupakan hubungan yang menunjukkan bahwa suatu use case selalu membutuhkan atau menyertakan perilaku dari use case lainnya. Sementara itu, extend merupakan hubungan yang menunjukkan adanya perilaku tambahan yang hanya dijalankan apabila kondisi tertentu terpenuhi.

Kedua relasi tersebut digunakan untuk menggambarkan hubungan antar-use case agar fungsi sistem menjadi lebih jelas dan terstruktur.

6. Use Case Description
   Use case description merupakan penjelasan secara rinci mengenai proses yang terjadi pada suatu use case. Deskripsi ini mencakup identitas use case, tujuan, aktor, pemicu, prasyarat, alur utama, alur alternatif, serta kondisi akhir setelah proses berhasil atau gagal.
   Dengan adanya use case description, setiap fungsi yang terdapat pada diagram dapat dijelaskan secara lebih terperinci sehingga memudahkan proses analisis dan pengembangan sistem.
   Dasar teori ini mengacu pada materi UML dalam Jobsheet Praktikum Pertemuan 4 dan OMG UML 2.5.1.

C. Hasil Praktikum
Pada praktikum pertemuan 4, dilakukan pengembangan Use Case Diagram pada Sistem Informasi Akademik (SIA) dengan menerapkan konsep generalization dan collaboration. Diagram yang dibuat merupakan pengembangan dari diagram pertemuan sebelumnya, sehingga fungsi-fungsi yang sudah ada tetap dipertahankan dan ditambahkan beberapa fungsi baru sesuai kebutuhan sistem.

1. Identifikasi Aktor
   Berdasarkan skenario Sistem Informasi Akademik, terdapat beberapa aktor yang berinteraksi dengan sistem, yaitu:
   Civitas Akademika: Aktor umum yang memiliki fungsi untuk melihat kalender akademik.
   Mahasiswa: Aktor khusus yang mewarisi fungsi dari Civitas Akademika serta dapat melihat Kartu Hasil Studi (KHS).
   Dosen: Aktor khusus yang mewarisi fungsi dari Civitas Akademika serta dapat menginput nilai mata kuliah yang diampunya.
   Admin Akademik: Bertugas mengelola data mahasiswa, seperti menambah, mengubah, dan menghapus data mahasiswa.
   Dosen Wali: Memiliki fungsi untuk memproses keputusan pengajuan KRS sesuai diagram dari pertemuan sebelumnya.
2. Penerapan Generalization Aktor
   Pada bagian ini, dibuat hubungan generalization antara Civitas Akademika dengan Mahasiswa dan Dosen. Civitas Akademika menjadi aktor umum, sedangkan Mahasiswa dan Dosen menjadi aktor khusus.
   Hubungan tersebut dibuat karena Mahasiswa dan Dosen memiliki fungsi yang sama, yaitu melihat kalender akademik. Dengan menggunakan generalization, hubungan ke fungsi tersebut cukup digambarkan satu kali melalui aktor umum tanpa harus menghubungkannya kembali dari masing-masing aktor khusus.
3. Identifikasi Use Case
   Use case pada Sistem Informasi Akademik terdiri dari fungsi lama yang dipertahankan dari pertemuan sebelumnya dan fungsi baru yang ditambahkan pada pertemuan 4.

| ID       | Nama Use Case             |
| -------- | ------------------------- |
| SIA-UC01 | Lihat Jadwal Kuliah       |
| SIA-UC02 | Kelola Jadwal Kuliah      |
| SIA-UC03 | Ajukan KRS                |
| SIA-UC04 | Validasi KRS              |
| SIA-UC05 | Unduh Bukti Pengajuan KRS |
| SIA-UC06 | Proses Keputusan KRS      |
| SIA-UC07 | Lihat Kalender Akademik   |
| SIA-UC08 | Input Nilai Mata Kuliah   |
| SIA-UC09 | Lihat KHS                 |
| SIA-UC10 | Kelola Data Mahasiswa     |
| SIA-UC11 | Tambah Data Mahasiswa     |
| SIA-UC12 | Ubah Data Mahasiswa       |
| SIA-UC13 | Hapus Data Mahasiswa      |

4. Penerapan Generalization Use Case
   Pada praktikum ini, generalization use case diterapkan pada fungsi pengelolaan data mahasiswa. Use case Kelola Data Mahasiswa menjadi use case umum yang memiliki tiga use case khusus, yaitu:
   Tambah Data Mahasiswa: Digunakan untuk menambahkan data mahasiswa baru ke dalam sistem.
   Ubah Data Mahasiswa: Digunakan untuk memperbarui informasi atau data mahasiswa yang sudah tersimpan.
   Hapus Data Mahasiswa: Digunakan untuk menghapus data mahasiswa dengan ketentuan mahasiswa tersebut tidak memiliki data akademik aktif.
   Ketiga use case tersebut memiliki tujuan umum yang sama, yaitu mengelola data mahasiswa, tetapi masing-masing mempunyai proses dan hasil yang berbeda.
5. Penerapan Collaboration dan Realization
   Pada bagian collaboration, terdapat dua collaboration yang digunakan untuk merealisasikan use case utama dalam Sistem Informasi Akademik.

| ID_Collaboration | Nama_Collaboration      | Use_Case_yang_Direalisasikan     |
| ---------------- | ----------------------- | -------------------------------- |
| SIA-CO01         | Input Nilai Mata Kuliah | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02         | Lihat KHS               | SIA-UC09 Lihat KHS               |

Collaboration Input Nilai Mata Kuliah menggambarkan kerja sama elemen sistem dalam mendukung proses penginputan nilai oleh dosen pengampu. Sementara itu, collaboration Lihat KHS menggambarkan kerja sama elemen sistem dalam menyediakan informasi hasil studi mahasiswa.

Kedua collaboration dihubungkan dengan use case masing-masing menggunakan relasi realization.

6. Penyusunan Use Case Description
   Pada praktikum ini, use case description dibuat untuk menjelaskan proses dari fungsi Input Nilai Mata Kuliah dan Lihat KHS.
   Input Nilai Mata Kuliah: Dosen memilih mata kuliah yang diampunya, kemudian memasukkan nilai mahasiswa ke dalam sistem. Sistem melakukan pemeriksaan terhadap nilai yang dimasukkan. Jika nilai berada di luar rentang yang sah, sistem menolak penyimpanan. Jika nilai valid, sistem menyimpan data nilai dan menampilkan konfirmasi bahwa proses berhasil.

Lihat KHS: Mahasiswa memilih semester yang ingin dilihat. Sistem kemudian menampilkan Kartu Hasil Studi yang berisi nilai mata kuliah pada semester tersebut. Nilai yang ditampilkan hanya nilai yang sudah dipublikasikan.
7. Hasil Akhir Praktikum
Hasil akhir praktikum berupa Use Case Diagram Sistem Informasi Akademik yang telah dikembangkan dengan menambahkan konsep generalization dan collaboration. Diagram tersebut menggabungkan fungsi dari pertemuan 2 dan 3 dengan fungsi baru pada pertemuan 4.
Pengembangan diagram menghasilkan beberapa elemen baru, yaitu aktor umum Civitas Akademika, aktor khusus Mahasiswa dan Dosen, use case pengelolaan data mahasiswa beserta tiga bentuk khususnya, serta dua collaboration untuk Input Nilai Mata Kuliah dan Lihat KHS.
Selain itu, diagram tetap mempertahankan fungsi jadwal kuliah dan pengajuan KRS dari pertemuan sebelumnya. Dengan demikian, seluruh fungsi Sistem Informasi Akademik dapat digambarkan dalam satu diagram yang saling berhubungan dan sesuai dengan kebutuhan yang telah ditentukan dalam jobsheet.
