1. Jelaskan keputusan grid-cols/gap di tiap breakpoint — kenapa begitu?
Mobile (grid-cols-1) → feed 1 kolom agar gambar penuh lebar, mudah di-scroll.
Tablet (sm:grid-cols-2) → layar lebih lebar, jadi 2 kolom supaya lebih efisien.
Medium (md:grid-cols-3) → laptop sedang, tampilkan 3 foto per baris agar mirip layout Instagram asli.
Desktop (lg:grid-cols-4) → layar besar, 4 kolom untuk memaksimalkan ruang.
Gap-2 dipilih supaya antar gambar tetap punya jarak, tidak menempel, dan menjaga keterbacaan visual.

2. Bagaimana kamu memanfaatkan utility responsive Tailwind untuk memecahkan masalah layout yang muncul di mobile?
Contoh di kode:
Tombol Follow → ukurannya berubah (px-3 py-1 di mobile → md:px-5 md:py-2 di desktop). Jadi tombol tetap nyaman ditekan di layar kecil.
Flex direction → flex-col md:flex-row, jadi di mobile elemen menumpuk ke bawah, sementara di desktop jadi horizontal agar lebih efisien.
Text size → text-sm md:text-base, agar tulisan tetap terbaca sesuai device.
Dengan utility Tailwind responsif (sm:, md:, lg:), kamu bisa mengatur tiap elemen agar selalu nyaman dilihat & diakses di layar kecil tanpa bikin CSS tambahan.

3. Jelaskan trade-off antara memakai banyak utility classes vs membuat component CSS tersendiri.
Utility Classes (Tailwind):
Cepat, langsung styling di HTML.
Konsisten, mudah menyesuaikan per breakpoint.
Bisa bikin HTML terlihat panjang/ramai (class menumpuk).
Custom Component CSS:
HTML lebih bersih (cukup pakai 1 class).
Bisa dipakai ulang di banyak tempat.
Perlu maintain CSS terpisah, styling responsif lebih ribet dibanding utility.
rade-off: kalau proyek kecil/medium → utility lebih praktis. Kalau proyek besar dengan banyak elemen yang sama → lebih baik buat component CSS biar scalable.