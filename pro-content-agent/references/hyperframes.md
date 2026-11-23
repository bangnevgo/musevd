# HyperFrames — Mesin Motion Graphics (dipelajari 20 Nov 2026)

Sumber: repo resmi heygen-com/hyperframes (dibaca langsung: README, AGENTS.md, skill `/hyperframes` dan `/hyperframes-cli`). Lisensi Apache 2.0, gratis, dipakai produksi oleh HeyGen. Repo sangat aktif (87 ribu star saat dibaca).

## Apa ini

Framework open-source yang mengubah HTML, CSS, media, dan animasi yang bisa di-seek (GSAP, CSS, Lottie, Three.js, Anime.js, WAAPI) menjadi MP4 yang deterministik: input sama, output sama persis. Renderer men-seek tiap frame di headless Chrome lalu meng-encode dengan FFmpeg. Beda dengan Remotion: HyperFrames bertaruh pada HTML polos tanpa build step dan tanpa React, Remotion pada komponen React.

Hasil akhirnya adalah file MP4 asli yang bisa diedit sampai level frame (sumber HTML-nya tetap bisa diubah di Studio/desktop app), BUKAN halaman HTML dan bukan slideshow gambar diam.

## Kontrak render (inti skill /hyperframes)

- `index.html` adalah komposisi akar: satu scene per sub-komposisi di `compositions/`, media dan font di `assets/`.
- Setiap elemen berwaktu wajib `class="clip"` + `data-start` + `data-duration` (detik); durasi video = `data-duration` akar.
- Tiap komposisi membangun SATU timeline yang di-pause dan didaftarkan ke `window.__timelines`.
- Deterministik: dilarang `Date.now()`, `Math.random()` tanpa seed, fetch jaringan, timer, `repeat: -1`. Semua yang terlihat adalah fungsi dari waktu timeline.
- Jangan men-tween `display`/`visibility`; jangan CSS transform pada elemen yang dianimasikan GSAP; media `<video>` tidak pernah di-play/pause/seek oleh kode.
- Hanya font bawaan yang resolve by name; font lain wajib `@font-face` ke file di `assets/fonts/`.
- Grading/grain/blur pada footage lewat `media-treatment`, bukan filter CSS.
- Konten di dalam kotak aman 90%, caption dan teks kunci di dalam 80%.

## Loop kerja (mirip workflow 9 tahap kita)

1. Film baru di atas ±15 detik yang bercerita: susun 3 storyline yang benar-benar berbeda (kata-kata saja), user memilih, lalu tulis SPEC.md (setiap kata sifat jadi angka, shot per frame).
2. Tulis komposisi, `lint` setelah draf pertama dan setelah perubahan struktural.
3. `check --json` sebagai gerbang (lint, runtime, layout, kontras WCAG) — perbaiki semua error. Catatan penting: video 3 detik+ tanpa perubahan visual yang terlihat GAGAL di pemeriksaan `sweep_static`.
4. `snapshot` untuk melihat frame sebagai PNG (tengah tiap scene) dan review film ke REVIEW.md.
5. Render hanya setelah preview disetujui user, atau user meminta file / tanpa berhenti. Kualitas render: draft / looks / delivery; render lokal, Docker, AWS Lambda, atau cloud.

## Ekosistemnya

- 9 skill terbitan; set inti = `/hyperframes`, `/hyperframes-cli`, `/hyperframes-registry`, `/media-use`, `/reverse-any-video`, `/style-sampling`. On-demand: `/figma`, `/slideshow` (output deck, bukan MP4), `/remotion-to-hyperframes`. Instalasi: plugin Claude Code (`claude plugin marketplace add heygen-com/hyperframes`) atau `npx hyperframes skills update` (set inti saja).
- Registry: ±450 blok/komponen siap pakai sebagai source yang bisa diedit — transisi shader, overlay, judul, kinetic type, caption, chart animasi, peta, 3D, camera moves. Perintah: `npx hyperframes add <nama>`.
- `frame.md`: menerjemahkan design system brand (design.md) menjadi DESIGN.md versi kamera agar agent bisa menyusun video promo tanpa menebak skala.
- CLI lengkap: init, capture (website jadi bahan video), timeline edit (move/trim/split/set/duplicate/delete/apply/undo), tts, transcribe, beats, normalize-audio, remove-background, share, history (setiap perubahan tercatat dan bisa di-undo).
- Fitur Pro (berbayar, lewat HeyGen): `/reverse-any-video` (membangun ulang video apa pun jadi proyek HyperFrames yang bisa diedit, dicek frame per frame) dan `/style-sampling` (episode baru dengan 5 gaya terbukti: Collage Explainer, Finance Explainer, Animated Science Explainer, 3D Brand Explainer, 3D True Crime). Studio app gratis; plan Pro Studio membuka model video/gambar/suara/musik HeyGen.
- Syarat: Node.js 22+ dan FFmpeg — periksa ketersediaannya di mesin kerja sebelum produksi.

## Posisi terhadap aturan produksi kita (penting)

- HyperFrames adalah mesin MOTION GRAPHICS, bukan mesin footage. Ia tidak menggantikan Google Flow / generate video untuk scene berkarakter dan aksi sinematik.
- Cocok untuk: explainer berbasis angka dan chart animasi (pas untuk niche YouTube faceless bedah bisnis), kinetic type dan caption, title card dan overlay di atas footage, peta dan data visualization, segmen penjelasan di dalam video yang footage-nya dari Flow/rekaman.
- Geraknya adalah gerak desain yang nyata dan terencana per frame, dan gerbang `check`-nya sendiri menolak video statis — sejalan dengan aturan keras anti-slideshow. Yang dilarang tetap dilarang: memakai HyperFrames untuk menggeser-geser gambar diam (itu slideshow dengan mesin lain) tetap gagal QC kita.
- Aturan persetujuan tetap berlaku: render final hanya setelah user menyetujui preview, sama seperti aturan publikasi kita.
- Skill `/slideshow` HyperFrames menghasilkan deck presentasi, bukan video — jangan pakai untuk deliverable video.
