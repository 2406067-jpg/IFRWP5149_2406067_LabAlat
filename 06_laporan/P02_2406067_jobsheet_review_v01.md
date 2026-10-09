|NO|--------------------|Temuan|----------------------------------------|------------------Perbaikan yang di perlukan-----------------------------------------------
|1| Aktor Mahasiswa diletakkan di dalam system boundary (batas sistem). | Pindahkan mahasiswa ke luar kotak
|2| Fungsi Lihat jadwal kuliah digambar sebagai kotak biasa.            | Ubah notasi fungsi menjadi simbol elips (oval).
|3| Aktor Mahasiswa dihubungkan dengan Kelola jadwal kuliah.            | Mahasiswa → Lihat jadwal kuliah, dan Admin akademik → Kelola jadwal kuliah.
|4| Identitas diagram menggunakan judul sistem laboratorium.            | Ubah judul system boundary dan isi metadata menjadi Sistem Informasi Akademik.

|N0|--------------------------------------------------------|Alasan|-------------------------------------------------------------------------------------------------
|1| Aktor merupakan entitas eksternal (pengguna/sistem luar) yang berinteraksi dengan sistem, sehingga secara notasi wajib berada di luar batas sistem.
|2|Dalam standar notasi UML Use Case Diagram, use case disimbolkan dengan elips, sedangkan bentuk persegi digunakan untuk class, component, atau boundary.
|3|Garis asosiasi harus sesuai dengan hak akses pada skenario. Mahasiswa hanya membaca jadwal, sedangkan pengelolaan data merupakan wewenang khusus Admin akademik.
|4|Nama sistem pada artefak harus konsisten dengan skenario yang dibahas agar tidak terjadi ketidaksesuaian artefak (artifact mismatch).