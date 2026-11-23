# Workflow Google Flow

Keadaan per 18 November 2026, dirangkum dari Google Flow Help dan blog resmi Google. Lineup model dan tarif kredit Flow berubah cepat, jadi selalu verifikasi model dan biaya kredit yang tampil di prompt box Flow sebelum generate. Jangan menghafal daftar model sebagai fakta permanen.

## Bedakan aplikasi dan model

- Google Flow adalah aplikasi studio kreatifnya di flow.google.com. Flow bukan model.

- Veo 3.1 adalah model video dengan audio bawaan berupa dialog, efek suara, dan ambience. Di Flow tersedia terutama tier Lite setelah tier Fast dan Quality dijadwalkan pensiun pada 5 Desember 2026.

- Gemini Omni Flash adalah model video multimodal yang lebih baru. Ia membuat video dari teks, gambar, audio, dan video, serta mengedit video lewat percakapan.

- Nano Banana adalah keluarga model gambar di dalam Flow untuk membuat frame dan ingredients. Gambar tidak memotong kredit video menurut ulasan berbasis Help Center, tetap verifikasi di aplikasi.

## Aturan kredit

- Semua akun mendapat 50 kredit gratis per hari yang tidak terakumulasi. Jumlah itu setara kira-kira 5 klip Veo 3.1 Lite per hari.

- Biaya acuan non Ultra: Veo 3.1 Lite 10 kredit per klip 4, 6, atau 8 detik. Omni Flash sekitar 1 kredit per detik pada 360p dan 3 kredit per detik pada 720p. Tarif dapat berubah, cek sebelum generate.

- Pakai draft murah dulu. Generate draf di Omni 360p atau Veo Lite, dan hanya hasilkan versi final berkualitas tinggi untuk shot yang sudah disetujui.

- Catat setiap produksi dalam log: prompt final, model, kredit terpakai, jumlah percobaan ulang, dan hasil penilaian.

## Langkah produksi

- Langkah 0, tulis brief satu halaman sebelum membuka Flow. Isinya tujuan, satu klaim, hook terpilih, shot list per shot dengan durasi dan rasio, serta anggaran kredit maksimum. Tanpa brief, jangan generate.

- Langkah 1, bangun aset gambar dulu di Nano Banana. Buat frame pembuka, frame penutup, dan gambar ingredient untuk karakter, produk, dan latar. Kunci konsistensi di tahap gambar yang murah, bukan berharap prompt video memperbaikinya.

- Langkah 2, daftarkan ingredients sebagai aset proyek dengan nama yang jelas dan panggil dengan tanda @ di prompt. Subjek dengan latar polos bekerja paling baik. Beri satu ingredient untuk satu peran.

- Langkah 3, tulis prompt terstruktur untuk setiap shot dengan formula ini: rasio dan durasi, subjek dengan ciri spesifik, satu aksi utama, lingkungan konkret, gerakan kamera dengan istilah yang tepat seperti static, push in, atau natural smartphone zoom, sumber cahaya nyata, gaya visual, dan audio berupa dialog dalam tanda kutip plus satu atau dua efek suara. Tulis prompt dalam Bahasa Inggris karena hasil terbaik menurut panduan Flow. Prompt harus melengkapi frame dan ingredient, bukan menentangnya. Ubah satu variabel per iterasi.

- Langkah 4, buat draf murah dan nilai dua hal: aksi terbaca dalam detik pertama, dan subjek konsisten dengan ingredient. Buat 2 sampai 4 variasi hanya untuk shot hook dan shot payoff.

- Langkah 5, kunci shot kritis dengan Frames to Video. Pakai frame pertama, atau pertama dan terakhir, dari aset Langkah 1 agar komposisi ditentukan manusia. Ini senjata utama melawan tampilan slop.

- Langkah 6, perpanjang klip hanya bila ada beat baru. Gunakan Omni Extend untuk pelanggan berbayar. Jangan memperpanjang klip hanya demi durasi, karena itu penyebab utama retensi turun di tengah.

- Langkah 7, perbaiki klip dengan edit percakapan Omni, satu instruksi tertarget per giliran, maksimal sekitar 3 giliran. Edit lebih murah daripada generate ulang dari nol. Lewat batas itu, kembali ke prompt baru.

- Langkah 8, rakit klip di Scene Builder mengikuti shot list. Potong kepala dan ekor mati, lalu periksa kontinuitas cahaya, pakaian, dan posisi subjek antar klip.

- Langkah 9, upscale hanya klip final terpilih, ke 1080p untuk pelanggan berbayar. Export 9:16 untuk Reels, TikTok, dan Shorts. Buat versi 16:9 sebagai proyek terpisah bila perlu, jangan memotong paksa hasil vertikal.

- Langkah 10, selesaikan di luar Flow. Subtitle, teks layar, loudness, end card, dan QC penuh dikerjakan di editor seperti CapCut atau Descript. Flow tidak menggantikan editor.

## Keterbatasan dan pelengkap

- Durasi per klip pendek, 4 sampai 8 detik untuk Veo dan 3 sampai 15 detik untuk Omni tergantung plan. Berpikirlah per shot, bukan per video utuh.

- Hasil generate tetap acak. Tetapkan anggaran kredit dan jumlah percobaan maksimum sebelum mulai.

- Teks di dalam video hasil generate masih rawan salah eja. Semua teks penting ditambahkan di editor, tidak pernah digenerate di dalam video.

- Periksa tangan, benda kecil, dan interaksi kompleks dengan zoom penuh. Cacat di area ini paling sering lolos.

- Semua output Flow membawa watermark tak terlihat SynthID dan konten Omni membawa C2PA Content Credentials. Ini bukan label platform, jadi kewajiban label AI di TikTok, Meta, dan YouTube tetap berlaku.

- Pakai Runway bila butuh kontrol kamera dan keyframe lebih rinci, HeyGen bila butuh presenter avatar konsisten dalam skala besar, ElevenLabs bila butuh suara narator brand yang sama di banyak episode, dan rekaman asli bila shot menampilkan bukti atau orang nyata.
