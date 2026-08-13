# Literasi AI — Buku Digital (MkDocs Material)

Draf situs buku "Literasi AI: Memahami dan Menggunakan Kecerdasan Buatan" dibangun menggunakan [MkDocs](https://www.mkdocs.org/) dengan tema [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## Struktur Proyek

```
ai-literacy-book/
├── mkdocs.yml                  # Konfigurasi situs
├── requirements.txt            # Dependensi Python
└── docs/
    ├── index.md                 # Beranda
    ├── bab1-pengantar-literasi-ai.md
    ├── bab2-dasar-dasar-ai.md
    ├── bab3-sejarah-ai.md
    ├── bab4-jenis-jenis-ai.md
    ├── bab5-ai-dalam-kehidupan.md
    ├── panduan-praktis/
    │   ├── mengenal-chatbot-ai.md
    │   ├── teknik-prompting.md
    │   ├── ai-untuk-produktivitas.md
    │   └── ai-untuk-kreativitas.md
    ├── bab6-etika-ai.md
    ├── bab7-risiko-keterbatasan.md
    └── glosarium.md
```

## Cara Menjalankan Secara Lokal

1. Buat _virtual environment_ Python:
   ```shell
   python -m venv .venv
   ```
2. Aktifkan _virtual environment_ sesuai sistem operasi yang digunakan:
   ```shell
   # Mac OS, Linux
   source .venv/bin/activate
   # Windows
   .venv/bin/activate
   ```
3. Instal dependensi:
   ```bash
   pip install -r requirements.txt
   ```
4. Jalankan server pengembangan:
   ```bash
   mkdocs serve
   ```
5. Buka `http://127.0.0.1:8000` di peramban.

## Cara Build Situs Statis

```bash
mkdocs build
```

Hasil situs statis akan tersedia di folder `site/`, siap diunggah ke layanan hosting seperti GitHub Pages, Netlify, atau server web biasa.

## Deploy ke GitHub Pages (opsional)

```bash
mkdocs gh-deploy
```

## Langkah Pengembangan Selanjutnya

- Tambahkan gambar/ilustrasi pendukung di setiap bab (folder `docs/assets/` disarankan)
- Perkaya studi kasus dengan contoh lokal yang relevan dengan audiens target
- Tambahkan halaman kuis/latihan interaktif jika diperlukan
- Sesuaikan `site_author`, logo, dan warna tema pada `mkdocs.yml` sesuai identitas buku
- Pertimbangkan menambahkan plugin `mkdocs-material` seperti `blog`, `tags`, atau `search` lanjutan sesuai kebutuhan
