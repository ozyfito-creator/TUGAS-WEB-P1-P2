1. Mengapa memilih konfigurasi col tertentu untuk tiap breakpoint?
Karena setiap breakpoint menyesuaikan ukuran layar:
Mobile (col-4, col-12, dll.) → tampilan lebih sempit, konten ditampilkan lebih ringkas (misalnya 3 foto per baris).
Tablet (col-sm-*) → tata letak mulai melebar, tombol bisa sejajar, foto bisa lebih banyak per baris.
Desktop (col-lg-*) → layar besar, sehingga grid lebih lebar (4 foto per baris), tombol & teks bisa tampil lengkap.
Singkatnya: konfigurasi col berbeda dipakai agar tata letak tetap rapi, mudah dibaca, dan konsisten di semua ukuran layar.

2. Bagaimana memastikan tombol Follow/Edit Profile tetap mudah dijangkau di mobile?
Pada kode ada penggunaan d-none d-sm-block dan d-sm-none:
Di desktop/tablet, tombol "Ikuti/Kirim Pesan" ada di samping profil.
Di mobile, tombol dipindah ke bawah foto profil dan ditampilkan lebar (w-50) agar mudah ditekan dengan jempol.
Pendekatan: gunakan responsif utility classes dari Bootstrap (display, width, margin) supaya tombol selalu muncul di tempat yang strategis sesuai perangkat.

3. Jika postingan bertambah jadi 50, apa potensi masalah dan bagaimana solusi gridmu mengatasinya?
Potensi masalahnya:
Loading lama karen terlalu banyak gambar di-load sekaligus.
Scroll jadi panjang, pengguna cepat bosan.
Grid bisa terlihat “penuh sesak” kalau tidak diatur jarak antar elemen.
Solusi:Grid dengan Bootstrap tetap otomatis wrap meskipun jumlah item banyak (misalnya 50 foto akan tetap tersusun rapi dalam baris & kolom sesuai col-4/col-lg-3).
Bisa tambahkan lazy loading (loading="lazy") pada <img> untuk mengurangi beban awal.
Untuk UX lebih baik, gunakan pagination atau infinite scroll.

jawaban singkatnya:
Breakpoint dipilih supaya layout tetap proporsional di semua ukuran layar.
Tombol dibuat responsif (posisi & ukuran) agar mudah diakses di mobile.
Kalau postingan jadi 50, grid Bootstrap tetap mengatur otomatis, tapi solusi tambahan: lazy load & pagination.