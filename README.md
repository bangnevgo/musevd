# Muse Video Skills

Kumpulan skill produksi video faceless untuk agen Muse: dari penulisan cerita dan prompt sampai render dan QC, semuanya berjalan sebagai alur kerja (workflow) yang terdokumentasi di dalam folder skill.

## Isi

| Folder | Skill | Ringkasan |
| --- | --- | --- |
| `pipeline-video/` | Pipeline Video | Pipeline produksi video seri faceless 57–75 detik (Shorts/Reels/TikTok): twist ditulis duluan, struktur loop, subtitle kinetik satu kata, enam tahap produksi sampai QC dari file final. |
| `kartun/` | Kartun | Video kartun pendek vertikal 20–40 detik dari SATU file HTML: animasi Canvas 2D deterministik yang ditulis sebagai kode, narasi TTS diselaraskan lewat tabel timing kata, efek suara sintesis WebAudio, dirender frame demi frame menjadi MP4. |
| `prompt-produk/` | Prompt Produk | Menulis prompt gambar dan video produk/promosi kelas komersial: template pendek ber-placeholder, brief lengkap berlabel, prompt JSON terstruktur, poster konseptual satu ide, storyboard dan prompt video bertimeline. |
| `stickman-video-director/` | Stickman Video Director | Penyutradaraan video stickman: kontrak prompt, katalog gaya, template storyboard, dan batas eksekusi per mode. |
| `pro-content-agent/` | Pro Content Agent | Workflow produksi konten profesional 9 tahap untuk gambar, carousel, dan video pendek (Instagram, TikTok, YouTube): riset dan ide, hook, script, storyboard, produksi aset (Google Flow, teknik prompt produk, HyperFrames, pipeline scene dari pamflet), edit, subtitle, dan gerbang QC — dengan standar anti AI-slop, gerbang patokan, dan pemeriksa independen. |

## Cara pakai

1. Salin folder skill yang dibutuhkan ke direktori skills agenmu (mis. `~/.claude/skills/` atau direktori custom skills pada runtime agen yang kamu pakai).
2. Baca `SKILL.md` di dalam folder itu sebelum produksi pertama; file di `references/` adalah bahan pendalaman yang dirujuk dari `SKILL.md`.
3. Ikuti gerbang kualitasnya: hasil akhir selalu diperiksa dari file final, bukan dari bahan sumber.

## Prinsip bersama

- Video harus bergerak nyata — bukan slideshow gambar diam.
- Karakter dan gaya dikunci lewat referensi yang konsisten antar adegan.
- Klaim angka dan teks di dalam konten hanya dari fakta yang terverifikasi.
- Tidak ada publikasi tanpa keputusan pemilik akun.

## Lisensi

MIT — lihat file `LICENSE`.

---

## English summary

A collection of faceless video production skills for the Muse agent: a serial faceless-video pipeline (twist-first stories, loop structure, one-word kinetic subtitles), a code-drawn Canvas 2D cartoon engine rendered frame-by-frame to MP4, commercial product/ad prompt writing (templates, structured JSON prompts, storyboards), a stickman video director skill, and a 9-stage professional content production workflow (research, hooks, scripts, storyboards, Google Flow asset production, editing, subtitles, and a QC gate with an independent reviewer). To use a skill, copy its folder into your agent's skills directory and follow its `SKILL.md`. Licensed under MIT.
