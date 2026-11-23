# Pipeline Video

Pipeline produksi video faceless, dibuktikan end-to-end lewat produksi acuan "Kentongan Jam Tiga" (58,2 detik, 1080×1920, lolos QC penuh). Resep formatnya diadopsi dari studi atas kanal cerita kampung absurd yang tembus jutaan views lintas platform, lalu dibuktikan di dapur sendiri. Skill ini adalah payungnya: ia mengatur format dan alur; mesin gambarnya adalah skill `kartun` (kartun kode), pipeline scene sinematik, dan motion graphics HTML.

## Kapan pakai, kapan jangan

- Pakai untuk: video seri faceless 57–75 detik (Shorts/Reels/TikTok), cerita satu tarikan napas dengan twist, seri berkarakter tetap yang diproduksi berulang.
- Jangan pakai untuk: video bukti/klaim nyata (pakai rekaman asli), poster/campaign satu gambar (wilayah `prompt_produk`), atau kartun kilat 20–40 detik tanpa struktur loop (skill `kartun` saja cukup).

## Format baku (terkunci)

- **Durasi 57–75 detik**, 1080×1920, 30 fps, file akhir di bawah 100 MB.
- **Twist ditulis duluan.** Ide dari hal sehari-hari; kejutan/penjelasan sebenarnya dirancang sebelum kalimat pembuka ditulis.
- **Struktur loop:** adegan terakhir memakai komposisi yang sama persis dengan adegan pertama (framing master dipakai ulang), dan kalimat penutup mengembalikan penonton ke situasi pembuka — akhir menyambung ke awal supaya ditonton dua kali.
- **Subtitle kinetik SATU KATA:** satu kata besar (skala ±148px di kanvas 1080) di sepertiga atas, aman dari zona UI platform, muncul tepat pada kata yang diucapkan menurut tabel timing. Kata penekanan boleh dibedakan (mis. bunyi khas berwarna kuning lebih besar). Bukan karaoke, bukan caption multi-kata. Pengecualian terarah boleh: pada scene close-up, kata digambar di area kosong frame asal tidak menimpa subjek twist.
- **Audio:** narasi TTS + SFX tersintesis terikat kata; loudness final dinormalkan ke sekitar −14 LUFS (true peak ≤ −1 dB).
- **Angka & teks dalam adegan:** hanya yang dibutuhkan cerita dan selalu dari fakta terverifikasi; teks kecil dekoratif yang tidak bisa dijaga kebenarannya jangan ditampilkan.

## Enam tahap produksi

1. **Cerita.** Tulis twist-nya dulu, baru kalimat pembuka. Satu kalimat = satu scene; tiap kalimat harus bisa digambar sebagai satu tempat + satu aksi. Patokan pacing dari produksi acuan: ±111 kata pada kecepatan TTS 95 menghasilkan ±58 detik — kalibrasi kecepatan TTS terhadap target durasi sebelum render, bukan sesudah.
2. **Naskah & suara.** Naskah final dibekukan persis seperti yang diucapkan, disintesis jadi MP3 lebih dulu, lalu dibangun **tabel timing kata** (deteksi jeda + penyelarasan) — semua elemen (batas scene, subtitle, aksi, SFX) mengambil waktu dari tabel ini, tidak ada detik yang diketik manual. Mekaniknya mengikuti skill `kartun` tahap 2–3.
3. **Visual — pilih satu mesin per proyek:**
   - **Kartun kode** (skill `kartun`): karakter bean-head pipih digambar Canvas 2D di dunia bergaya lukisan; karakter terkunci 100% karena fungsi gambarnya sama; paling murah dan paling bisa diulang persis. Mesin utama untuk seri cerita.
   - **Scene sinematik**: gambar scene bersih full-frame digenerate lalu dianimasikan jadi klip gerak nyata (pipeline media bawaan agen atau Google Flow). Untuk adegan yang butuh kekayaan visual di luar gambar kode. Dilarang keras slideshow/Ken Burns.
   - **Motion graphics HTML**: motion graphics HTML→MP4 untuk chart animasi, kinetic type, title card — pelengkap, bukan pengganti scene berkarakter.
4. **Rakit di mesin lokal.** Render headless + ffmpeg menjadi MP4 (H.264 yuv420p + AAC), normalisasi loudness, periksa spesifikasi dengan ffprobe.
5. **QC dari file final** (bukan dari frame sumber). Wajib lulus: (a) loop — frame pertama vs terakhir satu komposisi (target kemiripan SSIM ≥ 0,94; selisih hanya animasi ambient); (b) subtitle tepat satu kata di semua frame sampel dan tidak menimpa subjek; (c) adegan twist terbaca jelas; (d) durasi di dalam 57–75 detik; (e) geometri karakter waras — tidak melayang, tidak terpotong tepi, tidak tertimpa properti. Perbaikan selalu terarah (ubah hanya titik yang rusak, render ulang, QC ulang) — jangan menulis ulang seluruh file untuk kesalahan lokal.
6. **Tayang & catat.** Posting multi-platform (mesin publisher bila tersedia; kanal lain sesuai pemiliknya). Catat angka tiap platform per video (views, retensi bila ada, like, komentar, share, simpan) di lembar catat seri itu. Yang jelek dicoret, yang menang dijadikan templat episode berikutnya. Selera akhir tetap manusia: AI yang kerja, pemilik yang memutuskan tayang atau coret.

## Produksi acuan

- Bukti mesin kartun kode: produksi uji "Kartun Toko Rani" (31 detik, format lama 20–40 detik) — implementasi acuan lokal, tidak disertakan di repo ini.
- Bukti format baku penuh: "Kentongan Jam Tiga" (12 scene, 111 kata, loop SSIM 0,948, −14,02 LUFS, 1 putaran perbaikan 7 titik) — implementasi acuan lokal, tidak disertakan di repo ini. Pelajari pola produksinya sebelum produksi pertama dengan skill ini.

## Deliverable

MP4 final yang lolos QC + file sumber produksinya (HTML mandiri untuk kartun kode) + laporan jujur: durasi, resolusi, ukuran file, loudness, hasil QC per poin, dan sisa minor apa adanya. Tidak ada publikasi tanpa keputusan pemilik.
