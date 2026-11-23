# Prompt Produk

Ilmu menulis prompt visual komersial, didistilasi dari studi galeri prompt MeiGen: 56 prompt dibedah utuh (30 Ads & Product, 6 Brand & Logo, 6 Videos, 6 Posters & Visuals, 8 Storyboard & Characters) ditambah 2 prompt pilihan unggulan. Indeks lengkapnya ada di [Katalog Referensi MeiGen](references/katalog-meigen.md) — judul, kategori, model, dan tautan ke teks prompt aslinya di MeiGen.

Prinsip dasar: **galeri hanya perpustakaan resep; alat generate tetap punya kita sendiri** (pipeline media bawaan agen, Google Flow). Yang dipelajari dan dipakai ulang adalah struktur dan teknik penulisannya, bukan teks prompt orang lain.

## Lima keluarga prompt (pilih dulu, baru tulis)

### A. Template pendek ber-placeholder (gaya Nano Banana)

Satu paragraf padat atau satu baris koma dengan slot `[product]`, `[ingredients]`, `[background]`. Satu-satunya variabel diganti, sisanya sistem visual tetap. Varian yang terbukti: hero bahan baku (produk dikelilingi bahannya), hero mewah beludru + spotlight, flat lay dari atas + cipratan air beku, shot studio generik, reveal unboxing kemasan mewah, potret campaign dengan slot per elemen (model, produk, pose tangan, cahaya, palet).

- Kapan pakai: hero shot dan visual produk tanpa teks, perlu dipakai ulang untuk banyak produk, butuh cepat.
- Kerangka: `[produk], [satu konsep penataan], [properti bercerita], [palet tertutup], [cahaya spesifik], [lensa/rasa kamera], [ekor kualitas], [rasio]`.

### B. Brief lengkap berlabel (gaya GPT Image)

Dokumen mini berseksi bernama: FORMAT → LINGKUNGAN → KARAKTER HERO → VISUAL UTAMA → ELEMEN PENDUKUNG → TIPOGRAFI → BLOK INFORMASI BRAND → PALET → CAHAYA → KOMPOSISI (dengan persen zona) → GAYA RENDER → NEGATIF. Inilah keluarga dua prompt pilihan unggulan di katalog (poster jasa growth Instagram dan poster agensi Next Door Tech), dan keluarga yang dipakai untuk poster promo produk digital kita.

- Kapan pakai: poster penawaran/jasa yang memuat teks, banyak elemen, dan hierarki layout yang harus patuh.
- Wajib ada: blok copy eksak (headline, subheadline, fitur, harga, CTA, kontak/handle) ditulis lengkap di dalam prompt; komposisi dinyatakan dalam persen (mis. kiri 45% karakter, tengah 30% visual utama, kanan 25% tipografi); palet boleh hex persis.
- Batasnya: makin banyak teks kecil, makin banyak yang rusak — batasi jumlah kartu/callout, teks panjang pindah ke caption.

### C. Prompt JSON terstruktur

Objek JSON: satu `variable` + `core_instruction` + `fixed_visual_system` (output, background, objek, komposisi, lighting, camera, realism) + daftar `negative_constraints` + `generation_rule` yang memerintahkan model mengadaptasi variabel sambil menjaga sistem tetap. Terbukti pada sistem foto jus kantong jaring (satu variabel buah mengganti seluruh isi) dan editorial fashion monokrom.

- Kapan pakai: satu sistem visual harus dipakai ulang berkali-kali dengan satu variabel berganti (varian rasa, varian produk, varian warna) dan konsistensi adalah segalanya.

### D. Poster konseptual satu ide

Kerangka pendek berulang dari beberapa poster terbaik galeri: format premium → **Main Subject** (satu subjek + satu metafora visual: dunia-dunia kecil di dalam mesh speaker, rumah yang dilukis dari blueprint oleh rol cat raksasa, dunia yang hanya terlihat di dalam sorotan senter) → **Typography** (satu baris persis) → **Style** (konseptual, storytelling, campaign premium) → ekor kualitas.

- Kapan pakai: campaign yang butuh berhenti-scroll. Satu ide visual yang kuat mengalahkan sepuluh elemen generik — poster bersih tanpa ide ditolak sebagai generik (standar rasa).

### E. Storyboard & prompt video

- **Storyboard gambar**: blok kunci karakter di atas (ciri tetap + negatif eksplisit), lalu panel dienumerasi — tiap panel satu aksi + satu ukuran shot; varian lengkap menambahkan metadata per panel (nomor scene, badge durasi, arah kamera, visual, aksi, detail produk) dan header informasi (durasi, gaya, produk, audio). Grid 3×3 memakai urutan panel bernomor kiri→kanan atas→bawah dengan latar & busana dikunci sama.
- **Prompt video**: kepala berisi durasi + rasio + energi; shot dienumerasi dan dipaksa berbeda radikal ("no repeated angles"); timeline per detik untuk video pendek (0–2 dtk hook, dst.); satu baris dialog ditulis persis + tuntutan lip-sync; desain suara dispesifikasi; ditutup hero shot produk; blok negatif eksplisit di akhir (termasuk "misspelled text" dan "changing product labels").
- **Lembar karakter (character bible)**: hero pose + turnaround depan/samping/belakang + seksi gear/detail + baris swatch palet — cara mengunci karakter sebelum produksi seri. Untuk karakter seri kita: kunci wajah, rambut, pendamping, dan paletnya; **busana bebas, tidak harus selalu sama**.

## Anatomi universal (urutan lapis yang tidak boleh dibalik)

1. **Format dulu** — rasio, kanvas, target pemakaian. Model mengunci komposisi dari sini.
2. **Satu hero** disebut spesifik material dan bentuknya; semua elemen lain dinyatakan sekunder.
3. **Properti bertugas cerita** — pola terkuat: produk dikelilingi bahan bakunya sehingga gambar sendiri yang berargumen. Untuk produk digital: bukti nyata adalah propertinya (lihat adaptasi produk digital di bawah).
4. **Koordinat komposisi** — posisi dalam bahasa ruang atau persen zona, termasuk ruang negatif yang DISISAKAN sengaja untuk headline.
5. **Cahaya sebagai kalimat kerja** — arah + kualitas + tugasnya, bukan "good lighting".
6. **Palet tertutup** — warna disebut satu-satu dan dikunci, bernama atau hex; untuk iklan bahan, palet = warna bahannya.
7. **Blok teks eksak** — semua copy ditulis persis dengan hierarkinya; pakai formula pengaman "render only this exact copy". Teks dijaga pendek.
8. **Blok negatif terpisah** — larangan spesifik (tanpa watermark, tanpa teks ekstra, tanpa distorsi produk/logo, tanpa label berubah).
9. **Ekor kualitas** — istilah komersial (8K, editorial, commercial photography) hanya mengunci scene yang sudah spesifik; ekor tanpa lapisan 1–7 adalah slop.

## Disiplin teks & angka (aturan keras)

- Setiap angka yang terbaca di gambar — termasuk angka kecil di panel UI dekoratif seperti statistik dashboard mockup — harus berasal dari daftar bukti terverifikasi brand. Angka karangan model adalah cacat QC, bukan detail sepele.
- Periksa ejaan copy kata per kata sebelum generate; typo di prompt ikut ter-render.
- Baca ulang prompt untuk residu template (elemen warisan produk lain yang tidak nyambung) dan seksi ganda yang bertabrakan; satu prompt memuat satu versi tiap seksi.
- Verifikasi pasangan prompt–gambar saat menambang galeri: ditemukan kartu yang gambarnya tidak cocok dengan prompt-nya (prompt minuman olahraga, gambar storyboard sepatu). Galeri adalah bahan mentah, bukan kebenaran.

## Adaptasi produk digital

- Hero produk digital adalah **mockup HP/laptop berisi dashboard penjualan + notifikasi order**, diperlakukan dengan lapis yang sama seperti produk fisik (material = kaca layar dan pantulannya, posisi diagonal, dsb.).
- Ingredient storytelling → **bukti sebagai properti**: angka terverifikasi milik brand (jumlah order dari satu produk, total penjualan, harga coret, kuota peserta, jumlah sesi) tampil sebagai badge/strip kepercayaan — selalu ambil dari daftar bukti resmi brand, jangan mengarang.
- Poster penawaran standar mengikuti keluarga B: zona atas brand, tengah hero (dashboard + karakter seri), kanan/bawah tipografi + kartu fitur + bottom bar berisi tanggal, harga, dan CTA.
- Storyboard campaign: frame pertama bunyi notifikasi order (hook), tengah proses, frame terakhir hero produk + penawaran.

## Alur kerja

1. Tentukan deliverable dan keluarga prompt-nya (A–E).
2. Kumpulkan copy eksak dan bukti terverifikasi dulu; jangan menulis prompt sebelum copy-nya final.
3. Susun prompt mengikuti anatomi universal; tulis dalam Bahasa Inggris (model gambar mengikuti brief Inggris lebih patuh), copy di dalam gambar tetap bahasa aslinya.
4. Generate dengan alat sendiri; QC hasil: ejaan semua teks, angka (cocokkan daftar bukti), distorsi produk/tangan, kepatuhan zona komposisi.
5. Iterasi terarah: ubah satu lapisan pada satu waktu supaya tahu lapisan mana yang bekerja.
