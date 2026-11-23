# Teknik Prompt MeiGen — Foto & Video Penawaran Produk

Hasil studi mendalam galeri prompt MeiGen (kategori Ads & Product dan Videos), 20 Nov 2026: 12 prompt produk lengkap dibedah satu per satu. File ini menyimpan POLA dan TEKNIKNYA saja, untuk dipakai dengan alat generate kita sendiri (Flow/Nano Banana, pipeline media Muse, GPT Image bila tersedia). Kita tidak bergantung pada generator MeiGen; galerinya hanya perpustakaan resep. Contoh kartu yang dipelajari: poster tumbler MODOFO, poster sabun prerana wellness, iklan scrub CITRON CRUSH, poster roti Naturia, poster donat Sweet Haven, hero shot velvet [product], iklan skincare [product]+buah, serum amber sinematik, poster speaker "MORE THAN SOUND", storyboard Nike Air Zoom 6-frame, dan video baguette Minuit (Seedance). Tautan kartu ada di riwayat studi; pola di bawah ini yang dipakai sehari-hari.

## Anatomi prompt foto produk yang kuat (urutan lapisannya)

Prompt produk terbaik di galeri selalu menyusun lapisan dengan urutan yang sama. Jangan dibalik:

1. **Format dulu.** Rasio dan kanvas disebut pertama: "vertical 4:5", "9:16 poster", "1:1", plus target pemakaian ("suitable for Instagram, Facebook, and print"). Model gambar mengunci komposisi dari sini.
2. **Satu hero product, disebut spesifik materialnya.** Bukan "a jar" tapi ketebalan kaca, posisi tutup, label kecil di depan, isi yang terlihat berlapis. Satu produk jangkar; semua elemen lain sekunder dan dinyatakan sekunder.
3. **Properti dengan tugas cerita.** Pola terkuat: *ingredient storytelling* — produk diletakkan di atas dan dikelilingi bahan baku aslinya (buah, rempah, gandum), sehingga gambar sendiri yang berargumen "produk ini terbuat dari ini". Properti lain diatur posisinya secara eksplisit (diagonal di foreground, jejak tumpahan sempit, satu gulungan kulit jeruk di samping alas).
4. **Koordinat komposisi.** Posisi dinyatakan dalam bahasa ruang: "upper-right half", "center-right", "foreground diagonal pointing into the scene", dan yang penting untuk iklan: **ruang negatif yang disisakan dengan sengaja** — "leave the upper-left field open for a bold headline". Poster dibagi zona persen: atas 25% brand, tengah 50% hero, bawah 25% headline + CTA.
5. **Cahaya sebagai kalimat kerja.** Bukan "good lighting" tapi arah + kualitas + tugasnya: cahaya siang terarah dari kiri yang membuat kristal menyala di tepinya, satu highlight poles pada sendok, bayangan pendek berwarna biru, rim light yang menggarisi tepi gelas, sorotan tunggal dari atas di atas beludru gelap.
6. **Palet warna tertutup.** Daftar warna disebut satu-satu dan dikunci (citron green, cool white, pale blue; atau dark green, cream, gold). Untuk ingredient ads, palet disamakan dengan warna bahan bakunya.
7. **Blok teks eksak.** Untuk poster: semua copy ditulis persis dan diberi hierarki — headline, subheadline, tagline, benefit callouts, CTA — masing-masing dengan posisi dan gaya fontnya. Formula pengaman: "Render only this exact copy: ..." Teks di gambar dijaga PENDEK; daftar copy panjang menurunkan akurasi render (lihat anti-pola).
8. **Ekor kualitas.** Ditutup istilah kualitas komersial: 8K, ultra realistic, macro detail, commercial photography, sharp, editorial. Ekor ini tidak pernah berdiri sendiri — ia hanya mengunci scene yang sudah spesifik di lapisan 1–7.

## Dua gaya prompt, dua mesin

- **Template pendek berparameter** (gaya Nano Banana): satu paragraf padat atau satu baris koma dengan placeholder `[product]`, `[fruit_or_vegetable]`. Contoh pola: "[product], luxury product hero shot, dark velvet background, single spotlight top down, thin mist haze, dramatic rim light, 85mm lens look, f/4, 1:1". Cepat, bisa dipakai ulang untuk banyak produk, cocok untuk hero shot dan ingredient ads tanpa teks.
- **Brief lengkap berlabel** (gaya GPT Image): dokumen mini dengan seksi PRODUCT / BRANDING / TYPOGRAPHY / LAYOUT & COMPOSITION / COLOR PALETTE / QUALITY / DEPTH & LIGHTING. Dipakai untuk poster yang memuat teks dan banyak elemen (callout fitur, inset detail, badge). Lebih panjang, lebih patuh soal layout, lebih rapuh soal teks kecil — batasi jumlah callout.
- Prompt Nano Banana non-template (serum amber) membuktikan gaya ketiga: **paragraf sinematik satu napas** — subjek, penataan simetris, latar, cahaya kontras tinggi, palet, komposisi low-angle + bokeh, mood — semua dalam 2–3 kalimat panjang bersemikolon. Cocok untuk satu hero shot mewah tanpa teks.

## Pola poster penawaran & campaign

- **Callout fitur** sebagai panel teks berbatas rounded + **inset lingkaran detail** berlabel di bagian bawah (sedotan, infuser, tali gantung) — cara menampilkan 3 detail produk tanpa mengotori hero shot.
- **Badge manfaat** tebal di tengah ("100% Whole Wheat — No Preservatives"), **pita ribbon** di pojok ("PREMIUM QUALITY SINCE 2024"), dan **strip footer** berisi 3 mini-badge kepercayaan.
- **Speech bubble** berisi satu janji pendek di dekat model ("Stay Fresh Longer, Anytime!").
- **Model lifestyle + produk raksasa** berdampingan: orang memakai produk di satu sisi, produk versi hero besar di sisi lain — poster dibaca sebagai cerita sekaligus katalog.
- **CTA selalu di zona bawah** dan konkret: nomor telepon/URL ditulis penuh di prompt.
- **Poster konseptual satu kalimat** (speaker "MORE THAN SOUND"): satu subjek memenuhi frame, satu metafora visual (dunia-dunia kecil di dalam mesh speaker = manfaat), satu baris tipografi. Bukti bahwa campaign tidak selalu butuh banyak elemen — butuh satu ide visual.

## Storyboard video campaign

Dua pola berbeda, keduanya efektif:

**A. Storyboard multi-frame (untuk dirender jadi panel, lalu dianimasikan per frame):**
- **Blok kunci karakter di atas**: protagonis dideskripsikan sekali secara tetap (umur, postur, rambut, pakaian dengan warna persis, sepatu identik) + negatif eksplisit ("not wearing a smartwatch", "keep the shoe identical in all frames").
- **Busur naratif bernama**: preparation → speed → victory → product hero shot sebagai frame terakhir. Setiap frame satu aksi, satu ukuran shot (wide, extreme close-up, long shot, low-angle close-up, medium shot), dengan progresi waktu yang terasa (golden hour → dusk → neon night).
- **Disiplin teks**: overlay teks dibatasi hanya yang disebut persis ("JUST RUN.", nama produk di end frame); selain itu dilarang.
- Format (9:16) dan durasi total (~40 detik) dinyatakan di prompt.

**B. Prompt video tunggal (gaya Seedance):**
- Kepala prompt: durasi + rasio + energi ("20-second, 16:9, ultra-photorealistic 4K", "explosive pacing, speed ramps").
- Shot dienumerasi dan dipaksa berbeda radikal: "9 radically different camera shots, no repeated angles" — tiap shot satu baris: ukuran + aksi + detail makro.
- Satu baris dialog ditulis persis dengan bahasa dan tuntutan lip-sync; desain suara dispesifikasi (SFX tersinkron, bunyi CRUNCH) dan ekor negatif eksplisit: "no music, no subtitle".
- Transisi dinamai (match cuts, whip transitions) dan video selalu ditutup **hero shot produk**.

## Adaptasi untuk produk digital

- Hero product produk digital bukan benda fisik: pakai **mockup HP/laptop berisi dashboard penjualan dan notifikasi order** sebagai jangkar komposisi, diperlakukan dengan lapisan yang sama (material = kaca layar, pantulan, posisi diagonal).
- Ingredient storytelling diterjemahkan menjadi **bukti sebagai properti**: angka nyata terverifikasi dari daftar bukti brand tampil sebagai badge/strip kepercayaan — hanya angka dari daftar bukti itu, tidak pernah karangan.
- Poster penawaran produk digital: zona atas brand, tengah hero (dashboard + karakter seri), bawah headline + harga jangkar (harga coret dan harga promo dari profil brand) + badge kelangkaan (batas kuota) + CTA ke halaman pendaftaran. Teks di gambar tetap pendek; detail panjang di caption.
- Storyboard video campaign: frame 1 = bunyi notifikasi order masuk (hook), frame tengah = proses satu-dua langkah, frame terakhir = hero produk + harga. Kunci karakter seri dipakai persis seperti blok kunci protagonis pada contoh storyboard di atas.

## Temuan lanjutan — kategori Ads & Product (studi kedua, 20 Nov 2026)

Sembilan prompt tambahan dibedah dari halaman kategori produk langsung (termasuk set campaign Poppi 6 gambar yang kali ini tertangkap lengkap, board campaign DAYGLASS dan TONAL, infografis earbuds BOLT, poster Apple Watch, grid Nike Air Max 95, hand cream AFTER THE GARDEN, poster penawaran donat Arab, serum FRESH HARVEST). Pola baru yang belum ada di studi pertama:

- **Sistem campaign berseri dengan suffix gaya bersama.** Set Poppi = 6 prompt berbeda (hero shot, pour shot beraksi, lifestyle dengan orang, susunan geometris banyak produk, makro ekstrem, scene piknik) yang semuanya diakhiri suffix identik: rasio + saturasi + gaya cahaya + label estetika ("dopamine aesthetic, Gen Z internet energy..."). Satu suffix mengunci dunia visual; isi prompt berganti per jenis shot. Ini resep membuat SATU campaign utuh yang konsisten tanpa mengulang deskripsi gaya enam kali — dan daftar jenis shot-nya sendiri adalah checklist cakupan campaign: hero, aksi, orang, susunan, makro, suasana.
- **Campaign board 3×3.** Satu board berisi 3 produk × 3 sudut pandang dalam grid rapi berjarak lega, dengan aturan identitas produk yang kaku: nama brand tampil di setiap kemasan dengan font, ukuran, dan posisi yang sama; skala, komposisi, dan posisi kamera seragam antar sel; teks kemasan wajib tajam dan tidak terdistorsi. Cocok untuk board lini produk dan carousel katalog.
- **Infografis e-commerce yang dipimpin penawaran.** Urutannya dibalik dari poster brand: headline besar → produk + 4 inset close-up fitur berikon dan berlabel → strip penawaran di bawah (persen diskon, pengiriman cepat, garansi) → tombol BUY NOW yang ikut digambar → inset lifestyle kecil di sisi. Hierarki konversi, bukan hierarki brand.
- **Kemewahan lewat ruang kosong.** Poster Apple Watch membuktikan wow juga bisa berarti restraint: satu produk melayang di gradien gelap dengan glow radial, tipografi tipis elegan, tiga blok fitur sebaris berikon garis, dan dua frame produk terpotong di tepi kiri-kanan sebagai bingkai. Untuk brand premium, negative space adalah kemewahannya — bedakan dari poster maksimalis; pilih satu arah dan total di arah itu.
- **Grid storyboard varian identitas-terkunci.** Berbeda dari busur naratif Nike sebelumnya: di grid Air Max, produk tampil dari sudut sisi yang PERSIS sama di 6 frame dan yang berubah hanya scene/lokasi/mood-nya (hero studio → lifestyle jalan → makro → urban → detail teknologi → finale runway, teks hanya di frame pertama dan terakhir). Polanya: kunci produk, variasikan dunia.
- **Realisme ketidaksempurnaan.** Prompt hand cream AFTER THE GARDEN sengaja memesan produk yang terlihat terpakai (lipatan squeeze di tube, tutup terlepas di samping), garis tangan asli, bahkan sisa tanah kebun di dekat kuku — detail anti-slop yang membuat iklan terasa difoto, bukan di-render. Dan tetap disiplin: area tenang disisakan di kiri atas untuk judul serif.
- **Prompt satu kalimat + gambar referensi.** Poster penawaran donat berbahasa Arab hanya satu kalimat (produk, harga dengan simbol mata uang, promo kedua gratis, momen hari nasional, latar hijau dari referensi). Bukti bahwa untuk penawaran sederhana, gambar referensi yang kuat bisa menggantikan brief panjang — tapi kendali atas hasilnya jauh lebih kecil; pakai hanya bila referensinya memang persis yang diinginkan.

## Standar rasa user (ditetapkan 20 Nov 2026)

- Poster yang bersih, rapi, dan aman secara layout tapi tanpa ide visual yang kuat DITOLAK user sebagai "generik, kurang wow". Poster campaign wajib punya **satu ide visual sinematik** yang langsung terasa: metafora visual tunggal (mis. kreator sebagai pusat komando bisnisnya, dikelilingi panel hologram penjualan, HP raksasa diagonal yang meledak cahaya), latar dramatis kontras tinggi, dan skala elemen yang berani. Layout korporat terang yang generik tidak boleh diserahkan sebagai hasil akhir.
- Panel UI dekoratif di dalam gambar tidak boleh memuat angka karangan (mis. "+12 order") — angka apa pun yang terbaca di gambar tunduk pada daftar bukti terverifikasi, sama seperti copy utama.

## Anti-pola yang terlihat di galeri (jangan ditiru)

- **Sisa copy-paste**: poster sabun yang menyebut "steam from the tea cup" dan CTA "Brew Your Daily Ritual" — residu template produk teh. Selalu baca ulang prompt untuk elemen warisan yang tidak nyambung.
- **Typo ikut ter-render**: "gentle on sikn" lolos sampai kartu publik. Periksa ejaan copy persis sebelum generate.
- **Blok ganda**: satu poster mengulang seksi COLOR PALETTE dan QUALITY dua kali dengan isi bertabrakan — model bingung, hasil tidak konsisten. Satu prompt, satu versi tiap seksi.
- **Daftar teks terlalu panjang** di satu gambar: makin banyak callout kecil, makin banyak teks rusak. Pecah jadi beberapa visual atau pindahkan ke caption.
- Ekor kualitas tanpa scene spesifik = slop. Lapisan 1–6 yang membuat prompt bekerja; "8K ultra realistic" sendirian tidak menyelamatkan apa pun.
