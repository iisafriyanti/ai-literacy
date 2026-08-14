# Panduan Tools AI

Sebagai mahasiswa tingkat kedua (tahun kedua) di Fakultas Ilmu Komputer Universitas Indonesia (Fasilkom UI), Anda berhadapan dengan alur pengerjaan praktikum dan proyek yang makin kompleks pada mata kuliah seperti Struktur Data & Algoritma (SDA), Pemrograman Berbasis Platform (PBP), Sistem Basis Data (Basdat), dan Analisis & Perancangan Sistem (APS).

Panduan praktis ini berfokus pada **langkah-langkah praktis pemanfaatan perangkat AI** (*how-to guide*) sesuai dengan tugas perkuliahan Anda.

> **Catatan Konsep**: Untuk penjelasan konseptual mengenai dasar-dasar LLM, antarmuka percakapan web, dan teknik menyusun prompt umum, silakan merujuk ke [Mengenal Chatbot AI](mengenal-chatbot-ai.md) dan [Teknik Prompting Dasar](teknik-prompting.md).

---

## 1. Memahami Konsep Teori & Algoritma (Menggunakan Web Chat)

Ketika berhadapan dengan materi teori yang abstrak (seperti struktur data lanjutan atau konsep *multi-threading*), Anda dapat memanfaatkan antarmuka percakapan web (seperti ChatGPT atau Google Gemini) sebagai mitra diskusi.

### Langkah-langkah Praktis:
1. **Buka Antarmuka Chatbot**: Gunakan peramban web untuk mengakses layanan chatbot berbasis web.
2. **Sediakan Konteks Peran & Topik**: Tuliskan prompt yang menyertakan topik perkuliahan spesifik tanpa meminta jawaban tugas langsung.
   * *Contoh*: "Saya sedang mempelajari perbedaan algoritma pencarian BFS dan DFS pada mata kuliah SDA. Berikan penjelasan perbandingan kompleksitas ruang keduanya dengan analogi sederhana."
3. **Minta Penjelasan Bertahap**: Jika jawaban pertama terlalu umum, berikan instruksi lanjutan untuk memperdalam bagian tertentu.
4. **Verifikasi Mandiri**: Cocokkan poin penjelasan dari AI dengan slide materi perkuliahan Fasilkom UI atau buku teks resmi sebelum menggunakannya dalam pemahaman Anda.

---

## 2. Menulis & Debugging Kode di Editor (Menggunakan IDE Copilot)

Untuk mempercepat penulisan kode rutin dan menyelesaikan error saat pengerjaan tugas pemrograman di editor (seperti VS Code atau JetBrains), manfaatkan *IDE Embedded Copilot* (seperti GitHub Copilot atau Cursor).

### Langkah-langkah Praktis:
1. **Tuliskan Komentar Niat (*Intent Comment*)**: Sebelum meminta saran kode, tuliskan komentar ringkas di atas fungsi atau variabel yang menjelaskan tujuan kode tersebut.
   * *Contoh*: `// Fungsi untuk memvalidasi format email pada form pendaftaran PBP`
2. **Evaluasi Saran Autocomplete**: Tekan `Tab` untuk menerima saran kode **hanya jika** Anda sudah membaca dan memahami setiap baris logika yang disarankan.
3. **Gunakan Inline Debugging untuk Pesan Error**:
   * Sorot (*highlight*) baris kode yang mengalami kegagalan atau pesan error terminal.
   * Buka panel *IDE Chat* dan minta penjelasan penyebab error beserta saran perbaikannya.
4. **Jalankan Pengujian Lokal**: Selalu jalankan *unit test* atau tes manual di lingkungan lokal Anda setelah menerima perbaikan kode.

---

## 3. Mengelola & Refactoring Proyek Multi-Berkas (Menggunakan Autonomous Coding Agent)

Saat mengerjakan proyek skala menengah hingga besar yang melibatkan banyak berkas (seperti proyek kelompok PBP atau APS), Anda dapat menggunakan *Autonomous Coding Agent* (seperti Claude Code atau Google Antigravity) yang berjalan di lingkungan terminal/workspace.

### Langkah-langkah Praktis:
1. **Buka Agent di Workspace Proyek**: Jalankan perintah Agent melalui terminal di direktori utama repositori proyek Anda.
2. **Berikan Instruksi Berbasis Tugas**: Sampaikan tujuan revisi atau pelacakan bug yang spesifik.
   * *Contoh*: "Periksa repositori ini, cari berkas pemrosesan autentikasi pengguna, dan buatkan skenario pengujian unit untuk penanganan error login."
3. **Tinjau Rencana Aksi (*Action Plan*)**: Baca daftar berkas yang diusulkan oleh Agent sebelum memberikan konfirmasi eksekusi.
4. **Audit Perubahan Kode via Git**:
   * Jalankan perintah `git diff` untuk memeriksa perubahan baris demi baris pada setiap berkas yang dimodifikasi oleh Agent.
   * Pastikan Anda memahami struktur arsitektur baru yang dihasilkan.
5. **Uji Pengujian Penuh**: Jalankan perintah *build* dan pengujian otomatis proyek secara lokal sebelum melakukan *commit*.

---

## 4. Menyusun Transparansi & Refleksi Penggunaan AI

Penggunaan AI dalam pengerjaan tugas di Fasilkom UI wajib disertai dengan transparansi dan refleksi proses berpikir.

### Langkah-langkah Praktis:
1. **Catat Riwayat Penggunaan**: Simpan daftar perangkat AI yang Anda gunakan serta jenis bantuan yang Anda minta selama pengerjaan tugas.
2. **Identifikasi Proses Verifikasi**: Tuliskan minimal 2-3 poin mengenai apa yang Anda periksa, kritisi, atau perbaiki dari keluaran AI tersebut secara mandiri.
3. **Lampirkan Pernyataan Refleksi**: Tambahkan bagian *Acknowledgement / Refleksi Penggunaan AI* pada berkas `README.md` repositori tugas atau laporan sesuai dengan ketentuan mata kuliah (lihat [Panduan Praktis DDP 1](panduan-praktis-ddp1.md) dan [Panduan Praktis PBP](panduan-praktis-pbp.md)).

---

## 5. Referensi Dokumen Terkait

* [Mengenal Chatbot AI](mengenal-chatbot-ai.md) — Konsep dasar LLM, antarmuka percakapan, dan penanganan halusinasi.
* [Teknik Prompting Dasar](teknik-prompting.md) — Kerangka penyusunan prompt terstruktur (T-K-F-N).
* [Panduan Praktis untuk DDP 1](panduan-praktis-ddp1.md) — Kebijakan penggunaan AI pada mata kuliah DDP 1.
* [Panduan Praktis untuk PBP](panduan-praktis-pbp.md) — Kebijakan penggunaan AI pada mata kuliah PBP.
