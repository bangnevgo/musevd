# Pipeline Video Scene (Pamflet → Video)

Standar produksi video dari bahan pamflet/infografis, dibuktikan pada video patokan versi full-frame (disetujui user 20 Nov 2026) dan tiga video lanjutan di hari yang sama. Pakai pipeline ini setiap kali user memberi pamflet/sheet langkah-langkah untuk dijadikan video.

## Prinsip inti

- Pamflet adalah REFERENSI cerita & gaya, BUKAN bahan mentah. Dilarang meng-crop panel pamflet menjadi scene: hasilnya terlihat seperti tempelan berbingkai dan ditolak user ("crop crop terus", "kamu terlalu terpaku pada pamflet").
- Pecah isi pamflet menjadi scene-scene BARU: 1 hook visual + 1 scene per langkah, mengikuti urutan langkah di pamflet persis.
- Gambar scene selalu generate SENDIRI. Gambar contoh yang kadang dikirim user adalah standar gaya & metode, bukan aset — kecuali user secara eksplisit menyuruh memakai gambarnya.

## Tahapan

1. Generate gambar scene satu per satu dari nol, mengikuti karakter & gaya pamflet: full-frame vertikal 9:16, angle lebar/medium-wide (meja kerja & ruang studio terlihat, karakter tidak memenuhi frame), TANPA bingkai panel/kartu, karakter konsisten antar-scene (wajah & rambut, partner robot, palet warna — busana karakter seri BEBAS, tidak wajib sama antar-scene; aturan user 20 Nov 2026).
2. QC tiap gambar sebelum dianimasikan: konsistensi karakter, tidak ada bingkai, tidak ada teks garbled yang mencolok. Generate ulang yang gagal standar.
3. Animasikan tiap gambar menjadi klip (image-to-video) dengan gerak NYATA: karakter bergerak, elemen layar berdenyut/mengalir, kamera hampir statis atau bergerak halus. Untuk transisi dua beat (mis. Hook → Scene 1) boleh satu klip dengan start-frame dan end-frame.
4. Rakit: urutan Hook → langkah 1 sampai terakhir, ±5 detik per scene, crossfade ±0,5 detik, vertikal 720×1280, 24 fps.
5. QC file final: ekstrak frame tiap scene dari FILE JADI (bukan dari klip sumber) dan periksa satu per satu — karakter konsisten, teks (bila ada) terbaca penuh, tidak ada bingkai/padding.

## Aturan teks

- Default seri pamflet (mengikuti video patokan yang disetujui): judul scene dibakar sebagai overlay bersih (pill navy + badge nomor oranye), hook tampil di 2 detik pertama, kartu penutup didesain full-frame (bukan crop).
- Bila user menginstruksikan caption/teks dikosongkan (ia memasang font sendiri di CapCut): TANPA overlay judul, TANPA kartu judul/penutup, dan minimalkan teks di dalam gambar generate (elemen layar cukup ikon & garis sederhana). Tiga video lanjutan di hari yang sama diproduksi dengan mode ini.
- Tanpa caption postingan kecuali user meminta: deliverable adalah file video jadi.

## Batas pipeline media Muse (sudah terbukti di lapangan)

- Maksimal 6 generate video berhasil per putaran kerja. Video 7 scene diatasi dengan: (a) menggabung Hook + Scene 1 menjadi satu klip dua-beat ±10 detik, atau (b) putaran lanjutan khusus untuk klip yang kurang, lalu rakit ulang. JANGAN PERNAH mengganti klip yang kurang dengan zoom/Ken Burns atau slideshow — itu kegagalan QC, bukan jalan keluar. Bila terlanjur kurang, laporkan sisa pekerjaannya dengan jelas.
- Jalankan generate video SATU PER SATU secara berurutan. Jangan memanggil generate video paralel dengan penyalinan file: pernah gagal massal karena tool membuka file gambar sebelum salinannya selesai ditulis.
- Klip hasil generate bisa berubah skala/komposisi (kamera push-in, karakter membesar): periksa frame tengah & akhir tiap klip; generate ulang dengan prompt kamera statis bila elemen penting keluar frame.
- Gagal generate atau jalur tidak tersedia: berhenti dan laporkan apa adanya. Dilarang menurunkan standar diam-diam.

## Patokan hasil yang disetujui user (20 Nov 2026)

- Satu video patokan utama: ±40 detik, vertikal full-frame, dengan overlay judul — patokan gaya seri ini.
- Tiga video lanjutan di hari yang sama: masing-masing ±32–35 detik, tanpa teks (mode teks kosong di atas).
