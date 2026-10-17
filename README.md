# Jejak Gandong — Pulang ke Timur

RPG eksplorasi web 2.5D dengan gambar Canvas orisinal. Nuansa fantasi pulau tropis, pilihan karakter Nest/Lala/Etta (perempuan) atau Theo/Zeva (laki-laki), NPC, lima bab misi, musyawarah interaktif, peta, jurnal budaya, dan penyimpanan progres otomatis. Gambar dunia dan karakter digambar oleh kode; QRIS memakai gambar asli yang diberikan pengguna, tanpa aset atau karakter Genshin Impact. Ini RPG pendek berbasis cerita, bukan game 3D open-world berskala Genshin.

## Main di komputer
Ekstrak ZIP, lalu buka `index.html` dengan browser modern. Tidak perlu npm, database, API key, atau koneksi untuk aset. Sebagian browser membatasi penyimpanan saat file dibuka langsung; gunakan GitHub Pages atau server lokal agar penyimpanan lebih konsisten.

Opsional: dari folder ini jalankan `python -m http.server 8080`, lalu buka http://localhost:8080.

## Upload dan main di GitHub Pages
1. Buat repository bernama `jejak-gandong`. Pilih Public untuk cara paling sederhana.
2. Ekstrak ZIP. Unggah **isi** folder game: `index.html`, `style.css`, `game.js`, `README.md`, folder `assets`, dan `.nojekyll` jika terlihat. Jangan hanya mengunggah ZIP.
3. Pastikan `index.html` berada di bagian paling luar repository, bukan dalam subfolder.
4. Simpan dengan Commit changes.
5. Buka Settings → Pages. Pada Build and deployment, pilih Deploy from a branch.
6. Pilih branch `main` dan folder `/ (root)`, lalu Save.
7. Tunggu proses publikasi selesai. Buka URL Pages yang ditampilkan GitHub. Bentuk umumnya `https://USERNAME.github.io/jejak-gandong/`.
8. Setelah memperbarui file, commit kembali dan tunggu publikasi selesai. Muat ulang halaman jika versi lama masih muncul.

Jika menu Pages tidak tersedia, periksa hak akses repository dan kebijakan akun/organisasi. Paket ini tidak otomatis membuat repository atau mengaktifkan Pages pada akun kamu.

## Kontrol
- WASD / panah: berjalan. Atas menuju bagian atas pulau, kanan ke timur.
- Shift: tahan untuk lari.
- E: bicara atau mengambil benda dalam jarak dekat.
- J: jurnal. Escape: tutup panel.
- HP: tombol arah kiri bawah, interaksi dan lari kanan bawah.
- Tombol ♪: mengaktifkan atau mematikan suara sintetis.
- Titik putih pada peta: pemain. Titik emas: NPC tujuan.

## Alur permainan
1. Dari dermaga awal, berjalan ke utara menuju Mama Ina di depan baileo.
2. Ambil tiga bekal sagu bercahaya di kebun barat, kembali kepada Mama Ina.
3. Temui Nala di timur. Ambil tiga kayu hanyut di pesisir selatan lalu kembali untuk memperbaiki jembatan.
4. Seberangi jembatan dan temui Yopi. Selesaikan tiga refleksi musyawarah. Setiap pilihan disertai makna dan rujukan halaman buku.
5. Temui Kaka Eli di bukit timur laut. Kembali ke Mama Ina dan selesaikan refleksi.
6. Setelah epilog, dunia tetap bisa dijelajahi. Perjalanan dapat diulang melalui jurnal dengan konfirmasi.

## Penyimpanan
Progres disimpan di localStorage browser setiap tiga detik dan saat misi berubah. Progres terpisah per browser/perangkat/alamat situs. Menghapus data situs menghapus progres. Tidak ada akun, pelacakan, atau pengiriman data pemain. Memilih Mulai perjalanan mengganti progres lama; Lanjutkan perjalanan mempertahankannya.

## Budaya dan atribusi
Teluk Nusa, karakter, tokoh, dialog, dan kejadian adalah fiksi. Pakaian dan arsitektur distilisasi. Game mengangkat nilai kepedulian, kerja bersama, dan persaudaraan, tanpa merekonstruksi upacara adat atau hubungan dua negeri nyata. Pela dan gandong memiliki konteks sejarah yang beragam, terutama di Maluku Tengah. Alur dan makna sekarang memakai buku terlampir tahun 2000 sebagai sumber utama. Pengembangan materi adat lebih lanjut perlu melibatkan komunitas pemilik budaya.

Bacaan:
- BPNB Maluku, “Perwujudan Pela Membentuk Perilaku Kebangsaan”: https://kebudayaan.kemdikbud.go.id/bpnbmaluku/perwujudan-pela-membentuk-perilaku-kebangsaan/
- Repositori Kemendikbud, “Lembaga budaya pela dan gandong di Maluku: latar sejarah, peranan dan fungsinya”: https://repositori.kemendikdasmen.go.id/28892/

## Berkas dan pengembangan
- `index.html`: antarmuka dan panel permainan.
- `style.css`: layout desktop/ponsel, panel, kontrol.
- `game.js`: dunia, gambar, gerakan, dialog, misi, suara, simpan progres.

Ubah quest pada array `quests`, tokoh pada `npcs`, dan benda pada `pickups`. Semua path relatif sehingga mendukung subpath repository GitHub Pages.

## Pemeriksaan versi ini
Sintaks JavaScript dan uji alur lima bab, inventaris, jembatan, musyawarah interaktif, refleksi akhir, jurnal, serta pemanggilan render menggunakan lingkungan tiruan telah lulus. Pemeriksaan browser dan perangkat nyata belum dilakukan; uji pada HP/komputer setelah publikasi dianjurkan.

## Pembaruan pilihan karakter, cerita, dan dukungan
Nama terpilih digunakan dalam sapaan, jurnal, dan hasil akhir. Warna pakaian dan rambut karakter ikut berubah. Semua karakter memiliki misi yang sama. Simpanan versi ini terpisah dari versi awal karena struktur cerita berubah.

Hasil akhir menampilkan karakter, 5 bab selesai, 3 refleksi musyawarah, dan penjelasan makna. Tombol piala membuka hasil kembali setelah tamat. Bagian bawah hasil memuat QRIS dukungan sukarela, tautan gambar penuh, dan tombol simpan gambar. Gambar QRIS asli disalin tanpa modifikasi ke `assets/qris-developer.jpeg`. Pastikan folder ini ikut diunggah.

### Sumber utama
Lembaga Budaya Pela dan Gandong di Maluku: Latar Sejarah, Peranan dan Fungsinya. Proyek Pengembangan Media Kebudayaan, Direktorat Jenderal Kebudayaan, Departemen Pendidikan Nasional RI, 2000. Mengacu pada PDF yang diberikan pengguna. Nomor rujukan berikut mengikuti halaman cetak buku, bukan nomor halaman pembaca PDF.

| Bagian game | Landasan buku | Bentuk adaptasi |
| --- | --- | --- |
| Bekal saudara | Hlm. 104: menjamu anggota sepela. Hlm. 110–111: saling membantu pangan dalam kisah Laha dan Amahusu. | Tiga bekal sagu di kebun dan dialog Mama Ina. |
| Perbaikan jembatan | Hlm. 104–105: saling membantu dalam krisis dan pekerjaan kemasyarakatan. | Jembatan fiktif, bukan kejadian sejarah dalam buku. |
| Musyawarah | Hlm. 107, 112–113: mufakat, saling menghargai, penyelesaian masalah melalui musyawarah. | Tiga situasi pilihan dengan umpan balik. |
| Menghormati perbedaan | Hlm. 104–105: hubungan pela seagama maupun lintas agama, serta gotong royong. | Memilih membantu tanpa membatasi berdasarkan agama. |
| Cerita Kaka Eli | Hlm. 103–105: ikrar antarnegeri dan hubungan genealogis gandong. | Dialog edukasi yang membedakan kedua pengertian. |
| Kepulangan dan hasil | Hlm. 112–113: pewarisan nilai kepada generasi muda. | Ringkasan makna tindakan pemain. |

Cerita tidak menyatakan tokoh-tokoh ini membentuk pela/gandong baru. Tidak semua bantuan biasa merupakan ikatan adat. Unsur visual dunia merupakan interpretasi artistik. PDF sumber terlampir disertakan dalam `assets/buku-pela-gandong.pdf` sesuai permintaan pengguna. Atribusi penerbit tetap dicantumkan; akses baca ini tidak mengubah status hak cipta atau memberikan lisensi terbuka.

Pemeriksaan pembaruan: kelima karakter, semua bab, pilihan musyawarah benar/salah, jurnal sumber, hasil, serta referensi berkas QRIS. Verifikasi browser/perangkat nyata belum dilakukan.

## Tombol buku sumber
Tombol Baca Buku Sumber tersedia di pojok kiri bawah, termasuk pada halaman awal. Di HP tombol ditempatkan di atas kontrol arah agar tidak menutup tombol gerakan. PDF dibuka di tab baru sehingga game tetap tersedia. Upload folder assets secara lengkap, termasuk buku-pela-gandong.pdf. Tautan buku juga tersedia di jurnal dan hasil akhir.
