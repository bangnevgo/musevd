# Kartun

Membuat video kartun pendek vertikal dari kode: bukan generate video AI, bukan slideshow. Model menulis satu file HTML yang menggambar kartunnya sendiri (Canvas 2D), dan file itu dirender menjadi MP4. Metode ini terbukti end-to-end lewat uji coba "Kartun Toko Rani" (31 detik, 6 scene) — implementasi acuannya (file HTML, skrip build timing, skrip render, timing.json, folder QC) disimpan sebagai acuan lokal dan tidak disertakan di repo ini. Pelajari polanya sebelum produksi pertama.

## Kapan pakai, kapan jangan

- Pakai untuk: cerita kartun pendek 20–40 detik (satu kalimat = satu scene), konten faceless Shorts/Reels/TikTok, seri berkarakter tetap (karakter digambar dari fungsi kode yang sama, jadi konsisten antar video), produksi murah dan cepat tanpa kredit generate video.
- Jangan pakai untuk: footage realistis, adegan sinematik kompleks, atau klaim/bukti nyata (itu wilayah pipeline scene sinematik dan rekaman asli). Kartun kode adalah gaya ilustrasi datar yang disengaja, bukan pengganti video gerak realistis.

## Pipeline produksi (7 tahap, jangan dilompati)

1. **Cerita & naskah.** Tulis cerita pendek yang terbaca 20–40 detik. Satu kalimat = satu scene; tiap kalimat harus bisa digambar sebagai satu tempat + satu aksi. Simpan teks naskah PERSIS seperti yang akan diucapkan — teks ini sumber semua timing.
2. **Suara dulu.** Sintesis naskah menjadi MP3 dengan tool TTS yang tersedia di environment (suara narator sesuai bahasa naskah). Ukur durasi dan jeda bicaranya dengan `ffmpeg silencedetect` (ambang sekitar −35 dB, hening minimum 0,25 detik).
3. **Tabel timing kata (inti metode).** Pecah naskah jadi potongan per tanda baca, beri bobot tiap potongan (jumlah huruf + jumlah kata; digit dihitung 3 huruf), selaraskan potongan ke rentang bicara hasil deteksi jeda secara berurutan (dynamic programming: 1–4 potongan per rentang, atau 1 potongan melintasi 1–3 rentang, biaya dari selisih log laju bicara), lalu sebar kata di dalam rentangnya sebanding (huruf + 1). Hasilnya: setiap kata punya waktu mulai–selesai. SEMUA elemen — batas scene, caption, aksi, efek suara — mengambil waktu dari tabel ini. Tidak ada detik yang diketik manual untuk elemen-elemen itu.
4. **Tulis file HTML-nya.** Satu file mandiri, Canvas 2D saja, tanpa aset/library/font/gambar eksternal. Kontrak wajib:
   - `window.renderAt(t)` menggambar frame yang persis untuk detik t, DETERMINISTIK: tanpa Date, tanpa performance.now, tanpa Math.random bebas (pakai fungsi acak berseed). `window.DURATION` = durasi narasi.
   - Caption gaya karaoke: 1–3 kata sekali tampil mengikuti tabel kata, kata yang sedang diucapkan berwarna kuning, bold besar (skala ±110px pada kanvas selebar 1080), di sepertiga atas, maksimal 84% lebar frame, tidak menimpa wajah.
   - Efek suara sintesis WebAudio murni (tanpa file audio) dalam satu fungsi `window.scheduleSfx(audioCtx, destination, startTime)` yang juga jalan di OfflineAudioContext; 8–12 efek terikat kata/aksi, dibangun berlapis (noise terfilter + nada, attack cepat, fade natural) — bukan bunyi beep mentah.
   - Tiga tombol standalone + garis status: Choose voice file, Play, Save video (MediaRecorder dari canvas.captureStream + AudioContext MediaStreamDestination; unduh MP4 bila browser mendukung, selain itu WebM). File ini adalah deliverable kedua: pengguna bisa membukanya di Chrome dan mengekspor sendiri.
5. **Render di mesin lokal.** Pakai Chrome/Chromium headless lewat CDP: muat HTML, untuk tiap frame t = i/30 panggil `renderAt(t)` dan tangkap canvas sebagai PNG. Bila build Chromium setempat mensyaratkan switch kebijakan WebGL, sertakan switch dan file kebijakannya (kartunnya sendiri hanya Canvas 2D). Campur audio (MP3 narasi + SFX) lewat OfflineAudioContext di dalam halaman menjadi WAV, lalu rakit dengan ffmpeg: frames + audio → MP4 (libx264, yuv420p, AAC). Produksi: kanvas 1080×1920; uji cepat boleh 720×1280 (nyatakan ukurannya di laporan).
6. **QC dari file final.** Ekstrak minimal satu frame per scene dari MP4 JADI (bukan dari frame sumber) + dua frame berjarak 0,5 detik dalam satu scene sebagai bukti gerak. Periksa: caption terbaca dan posisinya benar, karakter konsisten antar scene, tiap scene tempatnya berbeda, tidak ada geometri rusak, karakter tidak terpotong tepi frame (terutama saat punch-in), tidak ada elemen melayang/overlap tak disengaja.
7. **Perbaikan terarah.** Bila ada yang rusak, ubah HANYA bagian itu (satu scene/fungsi), render ulang yang perlu, QC ulang. Jangan menulis ulang seluruh file untuk satu kesalahan lokal — dan jangan menyerahkan hasil rusak sebagai final.

## Aturan animasi (distilasi dari produksi yang terbukti)

- Shot lebar/medium sebagai default: karakter berdiri 30–45% tinggi frame supaya ada ruang beraksi; close-up hanya untuk reaksi wajah.
- Garis tanah sekitar 70% frame; aksi terjadi di tengah frame, bukan menempel di tepi bawah.
- Ada hal baru minimal sekali per detik: siklus kedip, napas, goyangan kecil, properti bergerak. Karakter membeku = gagal QC.
- Kamera tidak pernah diam total: push-in/pan halus mengikuti aksi, punch-in pada momen lucu atau penekanan.
- Kedalaman berlapis: latar jauh, latar tengah, karakter, properti depan — dengan parallax ringan.
- Cahaya mengikuti cerita (malam → fajar → pagi, atau perubahan mood antar scene).
- Anatomi waras: sendi menekuk ke arah yang benar untuk jenis karakternya, kaki menapak tanah, tangan menyentuh benda yang dipegang. Periksa siklus jalan/lari terhadap arah gerak (tidak ada moonwalk).
- Gaya gambar: outline gelap tegas, warna flat + satu sisi shading lebih gelap, bayangan lembut di titik kontak tanah. Karakter digambar dari fungsi yang sama di semua scene.

## Catatan lapangan dari uji coba pertama

- Scene penutup paling rawan rusak (geometri karakter duduk + punch-in memotong robot ke tepi frame). Sisakan waktu untuk satu putaran perbaikan di scene terakhir.
- Caption boleh melintasi properti latar asal outline-nya tebal dan tetap terbaca; yang dilarang hanya menimpa wajah.
- Level audio campuran mentah cenderung pelan (uji coba: rata-rata −24,8 dB). Normalisasi loudness ke standar platform (sekitar −14 LUFS) sebagai langkah akhir sebelum deliverable disebut siap posting.
- Tombol Save video di HTML adalah jalur manual untuk pengguna; jalur produksi utama tetap render headless di mesin lokal karena hasilnya lebih bersih dan terverifikasi.

## Deliverable

Selalu dua file: (1) MP4 final yang sudah lolos QC, (2) file HTML mandirinya. Laporkan durasi, resolusi, ukuran file, dan catatan QC apa adanya — termasuk sisa minor yang belum sempurna.
