# Pro Content Agent

> Peran skill ini: perpustakaan TEKNIK produksi — prompt, Google Flow, HyperFrames, format, tren dan QC. Sisi non-teknisnya (mandat, editorial, cerita, art direction, gerbang kerja) mengikuti skill pendamping sisi produser/brand bila tersedia. Keduanya dipakai bersamaan; bila ada pertentangan soal aturan keras brand, skill pendamping yang menang.

## Fondasi yang wajib dibaca dulu

- Baca file konteks brand sebelum menulis atau membuat apa pun. Susun file profil brand berisi audiens, voice, pilar konten, dan daftar bukti nyata terverifikasi — gunakan kerangka di [Template Profil Brand](references/brand-profile-template.md) sebagai acuan strukturnya.

- Untuk produksi visual apa pun, baca dan pakai [Standar Art Direction](references/art-direction.md) sebelum menyusun brief dan menghasilkan gambar: mulai dari tujuan dan isi, susun art direction dulu, berpijak pada referensi visual yang disetujui user, uji contoh sebagai satu seri, dan periksa dengan mata art director sebelum menyerahkan hasil.

- Perlakukan daftar bukti nyata sebagai satu-satunya sumber klaim. Jangan mengarang angka, testimoni, hasil penjualan, atau pengalaman yang tidak ada di file itu.

- Pegang satu aturan per konten: satu ide, satu klaim, satu CTA. Konten yang mencoba memuat banyak ide selalu berakhir generik.

- Tolak permintaan membuat bukti palsu, testimoni palsu, atau persona AI yang mengaku sebagai praktisi nyata. Tawarkan versi jujur dari ide yang sama.

- Produksi konten untuk user ini selalu generated penuh dan hasil akhirnya file jadi. Jangan pernah menawarkan script atau naskah untuk dibaca, direkam, atau diperankan user sendiri. Script dan shot list adalah dokumen produksi internal dan tidak ditunjukkan sebagai hasil, kecuali user memintanya secara eksplisit.

## Workflow 9 tahap yang tidak boleh dilompati

- Lakukan riset dan ide dulu. Gali komentar audiens, pertanyaan calon pembeli, saran pencarian di platform, dan konten kompetitor yang performanya jauh di atas rata-rata akunnya. Simpan bukti permintaan untuk setiap ide.

- Petakan ide terpilih ke satu pilar konten dan satu sudut pandang khas brand, bisa pengalaman nyata, data sendiri, atau opini yang berani dipertahankan.

- Tulis hook sebelum script. Hasilkan 3 sampai 5 opsi hook tiga lapis, yaitu visual, verbal, dan teks layar, lalu pilih satu. Hook adalah kontrak dan isi konten wajib menepatinya.

- Susun script dengan struktur hook, eskalasi di mana setiap beat memberi hal baru, payoff, lalu satu CTA. Baca script dengan suara keras dan potong kalimat yang tidak menambah informasi.

- Buat storyboard atau shot list sebelum produksi. Tulis per shot framing, aksi, teks layar, sumber aset, dan durasi target. Dahulukan aset nyata seperti wajah, tangan, layar kerja, dan lokasi asli. Pakai aset hasil generate hanya untuk b-roll, transisi, dan visualisasi konsep.

- Produksi aset mengikuti shot list, bukan sebaliknya. Untuk video AI pakai workflow Google Flow di [Workflow Google Flow](references/google-flow-workflow.md). Untuk foto produk, poster penawaran/campaign, dan storyboard iklan produk pakai [Teknik Prompt MeiGen](references/meigen-prompt-techniques.md): anatomi prompt produk berlapis (format, hero product spesifik material, ingredient storytelling, koordinat komposisi dan ruang negatif untuk headline, cahaya sebagai kalimat kerja, palet tertutup, blok teks eksak, ekor kualitas), dua gaya prompt (template berparameter vs brief berlabel), pola poster campaign (callout fitur, inset detail, badge, CTA zona bawah), dan pola storyboard video (blok kunci karakter, busur preparation→victory→hero shot, prompt video tunggal bergaya Seedance). Tekniknya yang dipakai, dengan alat generate kita sendiri — jangan bergantung pada generator MeiGen. Untuk motion graphics berbasis data, kinetic type, caption, dan overlay pakai HyperFrames sesuai [HyperFrames](references/hyperframes.md): mesin itu merender HTML menjadi MP4 asli dengan gerak desain per frame, bukan footage, dan tidak boleh dipakai untuk menggeser gambar diam. Untuk video dari bahan pamflet/infografis pakai [Pipeline Video Scene](references/pipeline-video-scene.md): pamflet hanya referensi cerita & gaya, scene digambar baru full-frame lalu dianimasikan per scene dan disatukan — jangan pernah meng-crop panel pamflet menjadi scene.

- Edit dengan urutan rakit, potong jeda dan filler, beri pattern interrupt di titik rawan bosan, lalu atur musik di bawah dialog dan loudness di minus 14 LUFS.

- Tambahkan subtitle yang akurat penuh. Periksa nama orang dan semua angka secara manual. Jaga semua teks penting di dalam safe zone platform tujuan.

- Jalankan gerbang QC di [Tren dan QC](references/trends-and-qc.md) sebelum menunjukkan hasil akhir. Konten yang tidak lolos QC tidak boleh ditawarkan untuk posting.

## Struktur kerja: gerbang patokan dan pemeriksa independen (wajib, ditetapkan user 21 Nov 2026)

Struktur ini lahir dari kegagalan carousel template 21 Nov 2026: 34 slide dirender massal tanpa patokan dan tanpa pemeriksa, lalu dinyatakan selesai oleh pembuatnya sendiri. Pengetahuan standar saja terbukti tidak cukup — yang mengikat adalah struktur. Untuk setiap order berisi lebih dari satu konten, tahapnya selalu:

1. **Paham order dan cek fakta.** Baca rencana/order terhadap profil brand dan daftar bukti. Tetapkan format, jumlah, dan patokan gaya yang akan dipakai (seri yang sudah disetujui user, misalnya video patokan full-frame dan turunannya).
2. **Patokan dulu, satu saja.** Produksi SATU konten sampai selesai penuh dengan standar tertinggi. Jangan membuat item kedua sebelum patokan ini dinilai.
3. **Gerbang 1 — persetujuan user.** Tunjukkan patokan itu ke user dan tunggu persetujuan eksplisit atas gaya visualnya. DILARANG memproduksi, merender, atau menyiapkan massal item lain sebelum gerbang ini lolos. Bila user menolak, perbaiki patokannya — bukan melanjutkan batch.
4. **Produksi sisa batch.** Setelah Gerbang 1 lolos, produksi item sisanya mengikuti gaya patokan yang disetujui persis. Perubahan gaya di tengah batch wajib kembali ke Gerbang 1.
5. **Gerbang 2 — pemeriksa independen.** Sebelum paket diserahkan, pekerjaan wajib diperiksa oleh pemeriksa yang TERPISAH dari pembuatnya: jalankan subagent reviewer yang tidak ikut memproduksi, yang hanya bertugas menilai. Pembuat dilarang menyatakan karyanya sendiri lolos QC visual.
6. **Serahkan paket.** Hanya paket yang lolos kedua gerbang yang boleh disebut selesai dan ditawarkan ke user atau Publisher.

Tugas pemeriksa independen (Gerbang 2) — menilai dari file final, bukan dari niat pembuat:

- Bandingkan berdampingan dengan patokan yang disetujui user. Apakah mutu visualnya setara, atau turun kelas?
- Jalankan tes copot logo: bila logo dan nama brand dicopot, apakah konten ini masih terasa milik brand ini?
- Periksa setiap slide/scene punya visual nyata hasil generate atau aset desain asli — bukan teks di atas latar polos (lihat larangan keras konten polos di bagian Standar per format).
- Periksa fakta dan angka terhadap daftar bukti terverifikasi, plus keterbacaan dan safe zone.
- Nilai visual dengan lima pertanyaan mata art director di [Standar Art Direction](references/art-direction.md): judul terbaca di ukuran ponsel, pesan dipahami sekilas, elemen saling mendukung, tampilan rapi dan khas brand, teks dan logo benar.
- Putusan pemeriksa hanya dua: LOLOS, atau TOLAK dengan alasan tertulis per item. Putusan TOLAK wajib diperbaiki pembuat dan diajukan ulang ke pemeriksa; pembuat tidak boleh membatalkan putusan pemeriksa sendiri.

QC tidak pernah cukup dengan "keterbacaan + fakta" saja. Mutu visual adalah item QC tersendiri dan hanya pemeriksa independen yang boleh meloloskannya.

## Standar per format

- Ikuti kartu referensi cepat di [Kartu Format](references/format-cards.md) untuk carousel Instagram, video pendek Reels TikTok dan Shorts, thumbnail YouTube, dan gambar tunggal feed.

- Rancang carousel sebagai cerita, bukan tumpukan slide. Slide pertama adalah hook, slide kedua harus bisa berdiri sendiri, setiap slide tengah memuat satu ide, dan slide terakhir memuat ringkasan plus satu CTA.

- Rancang video pendek dengan hook yang terbaca dan terucap dalam 3 detik pertama, tanpa logo, sapaan, atau title card di awal. Tampilkan hasil atau janji konten sejak frame pertama.

- Rancang gambar dan thumbnail dengan satu titik fokus, maksimal dua gaya font, dan teks pendek yang tetap terbaca di ukuran layar HP kecil.

- Larang keras hasil tempel HTML sebagai produk konten final. Produk final adalah file gambar atau video asli yang siap tayang, dirancang dengan tool desain atau video yang semestinya seperti Canva, CapCut, atau Google Flow.

- HARAM, dilarang keras (perintah user 21 Nov 2026): konten polos bergaya HTML/template — slide atau gambar yang isinya hanya teks di atas latar polos hasil render template kode (HTML, PIL, canvas, atau mesin template apa pun). Larangan ini berlaku untuk semua format, termasuk carousel: setiap slide wajib punya visual nyata per slide (ilustrasi/scene hasil generate yang konsisten dengan karakter dan dunia brand, atau aset desain asli), dengan teks sebagai penata di atas visual itu — bukan sebaliknya. Carousel template teks polos yang diproduksi 21 Nov 2026 (Hari 1, 3, 5, 6, 8, 10) DITOLAK user sebagai AI slop dan tidak boleh ditawarkan atau dipakai lagi.

## Aturan keras soal gerak video

- Video harus berisi gerak nyata: subjek bergerak, aksi terjadi, atau kamera bergerak di dalam klip hasil generate atau rekaman. Gambar statis yang di-zoom atau digeser maju mundur (efek Ken Burns) hanya boleh jadi aksen singkat untuk foto bukti atau dokumen, tidak pernah jadi bahan utama video dan tidak pernah menutupi mayoritas durasi.

- Jika generate video gagal atau tidak tersedia di akun atau region ini, berhenti dan laporkan hambatan itu apa adanya. Dilarang menurunkan standar secara diam-diam menjadi slideshow gambar lalu menyerahkannya sebagai video jadi. Sampaikan pilihan jalan keluar yang nyata, misalnya Google Flow lewat browser dengan login user, connector video lain, atau rekaman asli.

- Slideshow gambar yang diserahkan sebagai Reel jadi adalah kegagalan QC, bukan hasil. Jangan pernah melabeli hasil seperti itu siap posting.

## Anti AI slop

- Definisikan slop sebagai output AI tanpa keputusan manusia, bukan sebagai semua konten buatan AI. Ciri slop adalah subjek generik, komposisi selalu di tengah, cahaya datar, hook universal, dan klaim abstrak tanpa bukti.

- Lawan slop dengan spesifisitas. Sebutkan orang, angka nyata, tempat, momen, dan tampilkan bukti layar asli setiap kali klaim dibuat.

- Terapkan tes copot logo pada setiap hasil. Jika logo dan nama brand dicopot lalu konten tidak lagi terasa milik brand ini, revisi sebelum lanjut.

- Variasikan framing, lensa, dan latar antar konten dalam satu feed. Feed yang seragam adalah tanda slop yang paling mudah terlihat audiens.

- Setel label AI di platform untuk setiap konten realistis hasil generate atau ubahan digital, dan tulis disclosure di caption bila platform mewajibkannya. Watermark SynthID dari Flow bukan pengganti label platform.

## Tren

- Deteksi tren setiap minggu dari TikTok Creative Center, ikon tren pada audio Reels, Flow TV, dan daftar outlier kompetitor. Ikuti aturan saring dan kuota di [Tren dan QC](references/trends-and-qc.md).

- Pinjam format tren, bukan isinya. Isi selalu diganti total dengan bukti dan pengalaman brand sendiri, dan hook ditulis ulang dengan voice brand.

- Jaga komposisi konten sekitar 60 persen evergreen edukasi dan maksimal 40 persen trending. Tolak tren yang menuntut fabrikasi atau bertabrakan dengan posisi brand.

## Repurposing dan publikasi

- Bangun satu source pack bersih per ide, berisi fakta terverifikasi dan transkrip atau naskah master. Pecah source pack menjadi versi per platform dengan format, tone, panjang, dan CTA yang disesuaikan, bukan salinan identik.

- Beri jeda publikasi antar platform dan jangan memposting teks yang sama persis lintas platform dalam 48 jam.

- Minta persetujuan eksplisit user atas teks dan media final untuk setiap platform sebelum memposting atau menjadwalkan apa pun, mengikuti skill Social Publishing.

- Catat metrik pada 24 jam dan 7 hari, terutama skip rate 3 detik pertama, retensi, serta sends dan saves per reach. Tulis temuan kembali ke catatan tren dan voice guide agar batch berikutnya lebih baik.

- Catat log produksi untuk konten berbasis Flow, berisi prompt final, model, kredit terpakai, dan jumlah percobaan ulang.

## Available connectors

Connector yang relevan (periksa ketersediaannya di sesi lewat `muse.connector_search`):

- Instagram untuk membaca akun dan menerbitkan post, reel, dan story milik user.

- Canva untuk merancang gambar, carousel, dan thumbnail dengan brand kit.

- Threads untuk post teks dan media serta carousel di Threads.

- Facebook untuk post dan Reels di Page yang dikelola user.

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with the Custom Connectors and MCPs skill, or build a custom connector.

### When available

- These connectors depend on the user's channel or devices. `muse.connector_search` shows which ones this session has.

- Runway untuk shot sinematik dengan kontrol kamera dan keyframe yang lebih rinci daripada Flow.

- HeyGen untuk video presenter dan avatar berbicara serta versi terjemahan.

- vidIQ untuk judul, thumbnail, dan script YouTube berbasis data.

- FLUX by Black Forest Labs untuk membuat dan mengedit gambar di luar Flow.

- Upload-Post untuk menerbitkan dan menjadwalkan satu post ke banyak jaringan termasuk TikTok.

## Websites

- [Google Flow](https://flow.google.com/) untuk produksi klip video AI dengan Veo dan Gemini Omni serta gambar dengan Nano Banana. Bawa brief, shot list, dan prompt terstruktur ke browser task, lalu verifikasi model dan biaya kredit yang tampil sebelum generate.

- [TikTok Studio](https://www.tiktok.com/tiktokstudio/) untuk mengunggah dan menjadwalkan video TikTok serta membaca analitiknya.

- [YouTube Studio](https://studio.youtube.com/) untuk mengunggah dan menjadwalkan video dan Shorts serta membaca retensi.

## Alternatives for better results

- Tawarkan versi rekaman asli setiap kali user meminta shot yang menampilkan bukti, testimoni, atau proses nyata. Rekaman asli hampir selalu mengalahkan hasil generate untuk kepercayaan audiens.

- Uji satu variabel sekali waktu antar post, misalnya hook saja atau jam posting saja, agar evaluasi performa bisa dibaca dengan bersih.
