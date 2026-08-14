# Panduan Tools AI

Panduan ini bertujuan untuk memberikan contoh penggunaan _tools_ AI dalam kegiatan pembelajaran di program studi Ilmu Komputer, Sistem Informasi, dan Kecerdasan Artifisial.

> **Catatan Konsep**: Untuk penjelasan konseptual mengenai dasar-dasar LLM, antarmuka percakapan web, dan teknik menyusun prompt umum, silakan merujuk ke [Mengenal Chatbot AI](mengenal-chatbot-ai.md) dan [Teknik Prompting Dasar](teknik-prompting.md).

## Sycophancy / "Yes Bos"

Penyedia layanan _generative_ AI seperti OpenAI dan Anthropic telah melatih LLM mereka agar dapat berperan sebagai asisten yang berusaha menolong sebaik mungkin penggunanya. Peran tersebut menjadi _default_ yang dipakai oleh pengguna _tools_ yang diharapkan sudah mencakup mayoritas kebutuhan penggunanya.

Ada kemungkinan peran _default_ tidak sesuai dengan konteks kebutuhan pengguna _tools_ AI. Jika mengambil contoh peran AI yang diatur supaya menjadi asisten yang baik, ada kemungkinan asisten tersebut merespon perintah pengguna dengan bahasa yang sangat positif, bahkan bisa menutupi hal negatif yang sebenarnya sudah diidentifikasi oleh asisten. Hal ini umum disebut sebagai _sycophancy_.

> Braindump on

Dalam kasus AI yang sangat membantu, bisa jadi AI langsung mengerjakan instruksi yang diberikan tanpa memikirkan kembali konteks dibalik instruksi tersebut. Misalnya seorang mahasiswa meminta AI untuk membantunya menulis sebuah fungsi _sort_ koleksi elemen integer sebagai bagian dari sebuah tugas pemrograman. Dengan konfigurasi AI default yang cenderung _sycophant_, maka AI akan menyanggupi permintaan si mahasiswa dan membuatkan kodenya. Hal ini menyebabkan pengguna tidak belajar.

> Braindump off

## Role Prompting

Setelah mengetahui isu mengenai _sycophancy_ dan tendensi AI untuk terlalu "membantu" penggunanya, Anda perlu mampu menginstruksikan AI agar lebih tepat guna dalam membantu Anda dalam belajar. Mengingat Anda akan sering berinteraksi dengan AI, maka Anda perlu mengatur "sifat" AI yang akan digunakan secara _default_. Hal ini dapat dicapai dengan cara membuat instruksi bagi AI agar berperan sesuai instruksi yang diinginkan, atau dikenal sebagai _role prompt_.

### Contoh: Burhan (Role Asdos)

TBD.

### Memasang Role Prompt pada Web Chat Assistant

Layanan _web chat_ AI seperti ChatGPT dan Google Gemini menyediakan fitur _custom instructions_ (instruksi kustom) yang memungkinkan Anda menetapkan _role prompt_ secara permanen — artinya instruksi tersebut akan otomatis disisipkan ke setiap percakapan baru tanpa harus Anda ketik ulang setiap kali.

Berikut langkah-langkah memasang _role prompt_ pada ChatGPT (antarmuka web):

1. **Buka Pengaturan _Custom Instructions_**: Klik ikon profil Anda pada sidebar kiri, kemudian pilih **Customize ChatGPT** (atau navigasi melalui **Settings → Personalization → Custom Instructions**).
2. **Isi Kolom "What would you like ChatGPT to know about you?"**: Tuliskan informasi konteks tentang diri Anda yang relevan untuk pembelajaran.
   * *Contoh*: "Saya mahasiswa Ilmu Komputer Universitas Indonesia yang sedang mengambil mata kuliah DDP 1. Saya sedang belajar fundamental pemrograman dan ingin memahami konsep, bukan hanya mendapatkan jawaban jadi."
3. **Isi Kolom "How would you like ChatGPT to respond?"**: Tuliskan _role prompt_ yang mendefinisikan perilaku AI yang Anda inginkan.
   * *Contoh*: "Bertindaklah sebagai asisten dosen (asdos) yang berdedikasi. Jika saya meminta solusi langsung untuk tugas pemrograman, tolak dan arahkan saya untuk berpikir tahap demi tahkah. Berikan pertanyaan pemandu, bukan jawaban final. Gunakan Bahasa Indonesia."
4. **Simpan dan Aktifkan**: Klik tombol **Save**. Pastikan _toggle_ _Custom Instructions_ dalam keadaan aktif (ON). _Role prompt_ kini akan diterapkan pada setiap percakapan baru.

!!! tip "Satu Set Aktif pada Satu Waktu"
    ChatGPT hanya mendukung satu set _custom instructions_ yang aktif pada satu waktu. Jika Anda mengganti peran (misalnya dari "asisten dosen" ke "partner _code review_"), Anda perlu menimpa isi kolom yang ada. Simpan _role prompt_ Anda di berkas terpisah (misalnya di _notes_ atau _markdown_) agar mudah dipasang ulang saat dibutuhkan.

!!! warning "Batas Karakter"
    Setiap kolom _custom instructions_ memiliki batas sekitar 1.500 karakter. Tuliskan instruksi secara ringkas dan padat — setiap kalimat harus memberikan dampak yang jelas pada perilaku AI.

> **Catatan platform lain**: Google Gemini menyediakan fitur serupa melalui **Gemini Apps → Settings → System instructions** (tersedia pada versi tertentu). Antarmuka mungkin berbeda, tetapi prinsipnya sama: Anda menuliskan instruksi peran yang akan disisipkan ke setiap percakapan baru.

## 1. Memahami Konsep Teori & Algoritma (Menggunakan Web Chat)

Ketika berhadapan dengan materi teori yang abstrak (seperti struktur data lanjutan atau konsep *multi-threading*), Anda dapat memanfaatkan antarmuka percakapan web (seperti ChatGPT atau Google Gemini) sebagai mitra diskusi.

### Langkah-langkah Praktis:
1. **Buka Antarmuka Chatbot**: Gunakan peramban web untuk mengakses layanan chatbot berbasis web.
2. **Sediakan Konteks Peran & Topik**: Tuliskan prompt yang menyertakan topik perkuliahan spesifik tanpa meminta jawaban tugas langsung.
   * *Contoh*: "Saya sedang mempelajari perbedaan algoritma pencarian BFS dan DFS pada mata kuliah SDA. Berikan penjelasan perbandingan kompleksitas ruang keduanya dengan analogi sederhana."
3. **Minta Penjelasan Bertahap**: Jika jawaban pertama terlalu umum, berikan instruksi lanjutan untuk memperdalam bagian tertentu.
4. **Verifikasi Mandiri**: Cocokkan poin penjelasan dari AI dengan slide materi perkuliahan Fasilkom UI atau buku teks resmi sebelum menggunakannya dalam pemahaman Anda.

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

## 5. Referensi Dokumen Terkait

* [Mengenal Chatbot AI](mengenal-chatbot-ai.md) — Konsep dasar LLM, antarmuka percakapan, dan penanganan halusinasi.
* [Teknik Prompting Dasar](teknik-prompting.md) — Kerangka penyusunan prompt terstruktur (T-K-F-N).
* [Panduan Praktis untuk DDP 1](panduan-praktis-ddp1.md) — Kebijakan penggunaan AI pada mata kuliah DDP 1.
* [Panduan Praktis untuk PBP](panduan-praktis-pbp.md) — Kebijakan penggunaan AI pada mata kuliah PBP.
