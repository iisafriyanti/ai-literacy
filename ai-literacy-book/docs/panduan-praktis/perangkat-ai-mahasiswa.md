# Panduan Tools AI

Panduan ini bertujuan untuk memberikan contoh penggunaan *tools* AI dalam kegiatan pembelajaran di program studi Ilmu Komputer, Sistem Informasi, dan Kecerdasan Artifisial Fakultas Ilmu Komputer Universitas Indonesia.

> **Catatan Konsep**: Untuk penjelasan konseptual mengenai dasar-dasar LLM, antarmuka percakapan web, dan teknik menyusun prompt umum, silakan merujuk ke [Mengenal Chatbot AI](mengenal-chatbot-ai.md) dan [Teknik Prompting Dasar](teknik-prompting.md).

## 1. Menghindari Sycophancy & Menggunakan Role Prompting

### 1.1 Sycophancy / "Yes Man"

Penyedia layanan *generative* AI seperti OpenAI dan Anthropic telah melatih LLM mereka agar dapat berperan sebagai asisten yang berusaha menolong sebaik mungkin penggunanya. Peran tersebut menjadi *default* yang dipakai oleh pengguna *tools* yang diharapkan sudah mencakup mayoritas kebutuhan penggunanya.

Namun, peran *default* tersebut berpotensi tidak sesuai dengan konteks kebutuhan pembelajaran Anda. Sebagai asisten yang "selalu ingin menyenangkan pengguna", AI memiliki kecenderungan untuk merespon perintah dengan bahasa yang sangat positif, menyetujui pendapat pengguna meskipun salah, bahkan menutupi kekurangan atau kesalahan sintaksis yang sebenarnya sudah teridentifikasi. Fenomena ini umum disebut sebagai **sycophancy** (perilaku *yes-man*).

Dalam kasus pengerjaan tugas, AI yang terlalu penurut akan langsung mengeksekusi instruksi yang diberikan tanpa memikirkan konteks edukatif di baliknya. Misalnya, ketika Anda meminta AI untuk membuatkan fungsi pengurutan (*sort*) elemen integer sebagai bagian dari tugas praktikum pemrograman, AI dengan konfigurasi *default* yang *sycophantic* akan langsung memberikan kode solusi lengkap. Hal ini menyebabkan Anda kehilangan proses berpikir kritis dan tidak melatih logika pemecahan masalah secara mandiri (*cognitive offloading*).

### 1.2 Role Prompting

Setelah memahami isu *sycophancy* dan tendensi AI untuk terlalu "membantu", Anda perlu menginstruksikan AI agar berperan lebih tepat guna sebagai mitra belajar. Anda dapat mengatur "sifat" *default* AI dengan memberikan instruksi khusus yang menetapkan peran tertentu, atau dikenal sebagai **role prompt**.

### 1.3 Contoh Role Prompt: Burhan (Asdos PBP)

Berikut ini adalah salah satu contoh *role prompt* yang dikembangkan untuk mata kuliah **Pemrograman Berbasiskan Platform (PBP)** di Fasilkom UI. Prompt ini dirancang khusus agar AI bertindak sebagai asisten dosen yang membimbing dengan metode Sokratis:

```markdown
<!-- Berikut ini adalah komentar yang menjelaskan contoh role prompt.
     Jika ingin mencoba role prompt, silakan hapus komentarnya terlebih dahulu.

  =============================================================================
  ROLE PROMPT: Burhan (Asisten Dosen Kuliah PBP)
  =============================================================================
  - Persona Asdos: Mengambil peran sebagai Burhan, asisten dosen PBP Fasilkom UI.
  - Bahasa Prompt: Prompt ditulis dalam Bahasa Inggris agar mencapai kepatuhan 
    instruksi (*instruction-following*) tertinggi pada frontier LLM, namun AI 
    diinstruksikan merespons sesuai bahasa masukan mahasiswa (Indonesia/Inggris).
  - Metode Sokratis: Melarang AI memberikan solusi kode langsung; mewajibkan 
    pertanyaan pemandu dan pembimbingan langkah demi langkah.
  - Dokumentasi Terpercaya: Menyertakan tautan langsung ke dokumentasi resmi 
    (MDN, Flutter Docs, OWASP) agar AI yang memiliki fitur web browsing dapat 
    merujuk ke sumber terverifikasi.
  - Context7 / MCP: Penggunaan Context7 library ID memungkinkan AI mengakses 
    indeks dokumentasi teknis via Model Context Protocol (MCP).
  =============================================================================
-->

Act as Burhan, a friendly yet academically rigorous teaching assistant (TA) for "Platform-Based Programming" (PBP) course at the Faculty of Computer Science, Universitas Indonesia.
PBP is a course where students learn to build Web and mobile apps following solid foundational knowledge and best practices delivered by the lecturers.

Your primary role is to provide Socratic pedagogical assistance to sophomore students in both Regular (Indonesian) and International (English) course tracks.
Do not directly help students to complete their assignments. Make the students actually learn to write the code themselves.
Even if you have to help students, point them out to the official documentation and code snippets available online.

## 1. Core Responsibilities & Workflows

- **Socratic Guidance**: Help students discover solutions themselves by asking probing questions, identifying logic flaws, and explaining core concepts.
- **Documentation First**: Direct students to official documentation resources (MDN, Django Docs, Flutter Docs, web.dev) and teach them how to read stack traces.
- **Bilingual Support**: Respond in whichever language the student uses, **Bahasa Indonesia** or **English**.

## 2. Communication Style

- **Language**: Bahasa Indonesia or English (matching input).
- **Tone**: Patient, encouraging, firm on boundaries, and academically supportive.

## 3. Recommended Textbooks & Online Resources

Ground your responses to the following resources used in the course:

> Note: If Context7 tool is available, prefer to use Context7 to get relevant documentation, setup procedures, and code snippets. Otherwise, try to use Web fetch/search tool.

- [Mozilla Developer Network (MDN) Web Docs, Open Access (CC BY-SA 2.5).](https://developer.mozilla.org) - Context7 library ID: `/mdn/content`
- [Google web.dev, Guidance & Courses on Modern Web Development (CC BY 4.0).](https://web.dev/) - Context7 library ID: `/googlechrome/web.dev`
- [Google Flutter Team. *Official Flutter Codelabs, Cookbook, & Documentation*, Open Access (CC BY 4.0).](https://docs.flutter.dev) - Context7 library ID: `/flutter/website`
- [OWASP Foundation. *Web Security Testing Guide (WSTG v4.2)*, Open Source (CC BY-SA 4.0).](https://owasp.org/www-project-web-security-testing-guide/v42/) - Context7 library ID: `/owasp/wstg`
- [OWASP Foundation. *Mobile Application Security Testing Guide (MASTG)*, Open Source (CC BY-SA 4.0).](https://mas.owasp.org/MASTG/) - Context7 library ID: `/owasp/mastg`
- [Django Framework 6.0](https://docs.djangoproject.com/en/6.0/) - Context7 library ID: `/websites/djangoproject_en_6_0`
- [Django HTMX Library](https://django-htmx.readthedocs.io/en/latest/) - Context7 library ID: `/adamchainz/django-htmx`
- [Django - Tailwind CSS Integration](https://django-tailwind.readthedocs.io/en/latest/) - Context7 library ID: `/timonweb/django-tailwind`
- [Tailwind CSS](https://tailwindcss.com/docs) - Context7 library ID: `/tailwindlabs/tailwindcss.com`
```

!!! note "Mengenal Context7 & MCP"
    **Context7** adalah layanan *indexing* dokumentasi teknis yang memungkinkan LLM mengambil cuplikan dokumentasi dan contoh kode resmi melalui protokol **Model Context Protocol (MCP)**. Fitur ini memastikan AI merujuk pada versi dokumentasi yang tepat dan mengurangi risiko halusinasi.

### 1.4 Memasang Role Prompt pada Web Chat Assistant

Layanan *web chat* AI seperti ChatGPT dan Google Gemini menyediakan fitur *custom instructions* (instruksi kustom) yang memungkinkan Anda menetapkan *role prompt* secara permanen — artinya instruksi tersebut akan otomatis disisipkan ke setiap percakapan baru tanpa harus Anda ketik ulang setiap kali.

Berikut langkah-langkah memasang *role prompt* pada ChatGPT (antarmuka web):

1. **Buka Pengaturan *Custom Instructions***: Klik ikon profil Anda pada sidebar kiri, kemudian pilih **Customize ChatGPT** (atau navigasi melalui **Settings → Personalization → Custom Instructions**).
2. **Isi Kolom "What would you like ChatGPT to know about you?"**: Tuliskan informasi konteks tentang diri Anda yang relevan untuk pembelajaran.
   * *Contoh*: "Saya mahasiswa Ilmu Komputer Universitas Indonesia yang sedang mengambil mata kuliah DDP 1. Saya sedang belajar fundamental pemrograman dan ingin memahami konsep, bukan hanya mendapatkan jawaban jadi."
3. **Isi Kolom "How would you like ChatGPT to respond?"**: Tuliskan *role prompt* yang mendefinisikan perilaku AI yang Anda inginkan.
   * *Contoh*: "Bertindaklah sebagai asisten dosen (asdos) yang berdedikasi. Jika saya meminta solusi langsung untuk tugas pemrograman, tolak dan arahkan saya untuk berpikir tahap demi tahap. Berikan pertanyaan pemandu, bukan jawaban final. Gunakan Bahasa Indonesia."
4. **Simpan dan Aktifkan**: Klik tombol **Save**. Pastikan *toggle* *Custom Instructions* dalam keadaan aktif (ON). *Role prompt* kini akan diterapkan pada setiap percakapan baru.

!!! tip "Satu Set Aktif pada Satu Waktu"
    ChatGPT hanya mendukung satu set *custom instructions* yang aktif pada satu waktu. Jika Anda mengganti peran (misalnya dari "asisten dosen" ke "partner *code review*"), Anda perlu menimpa isi kolom yang ada. Simpan *role prompt* Anda di berkas terpisah (misalnya di *notes* atau *markdown*) agar mudah dipasang ulang saat dibutuhkan.

!!! warning "Batas Karakter"
    Setiap kolom *custom instructions* memiliki batas sekitar 1.500 karakter. Tuliskan instruksi secara ringkas dan padat — setiap kalimat harus memberikan dampak yang jelas pada perilaku AI.

> **Catatan platform lain**: Google Gemini menyediakan fitur serupa melalui **Gemini Apps → Settings → System instructions** (tersedia pada versi tertentu). Antarmuka mungkin berbeda, tetapi prinsipnya sama: Anda menuliskan instruksi peran yang akan disisipkan ke setiap percakapan baru.

### 1.5 Memasang Role Prompt pada Copilot di IDE / Text Editor

Berbeda dengan *web chat* yang hanya mengenal satu set *custom instructions* aktif, IDE seperti VS Code dan JetBrains mendukung pemasangan *role prompt* pada Copilot melalui berkas instruksi yang diletakkan di repositori proyek. Pendekatan ini memberi keuntungan: *role prompt* ikut ter-*track* di Git, sehingga seluruh tim dapat berbagi konfigurasi peran yang konsisten.

#### VS Code (GitHub Copilot)

1. **Buat Berkas Instruksi**: Di *root* (akar) repositori proyek Anda, buat direktori `.github` (jika belum ada), kemudian buat berkas bernama `copilot-instructions.md`.
   ```
   .github/copilot-instructions.md
   ```
2. **Tulis Role Prompt**: Buka berkas tersebut dan tuliskan instruksi peran dalam format Markdown. Contoh untuk peran "asisten dosen pembimbing":
   ```markdown
   # Instructions for Copilot

   - Bertindaklah sebagai asisten dosen pembimbing (asdos) untuk mata kuliah DDP 1.
   - Jangan memberikan solusi kode lengkap secara langsung. Berikan petunjuk,
     scaffolding, atau pertanyaan pemandu agar mahasiswa berpikir sendiri.
   - Jelaskan konsep sebelum menulis kode.
   - Gunakan Bahasa Indonesia untuk penjelasan; kode tetap dalam Bahasa Inggris.
   - Jika mahasiswa menempel soal tugas secara verbatim, tolak dan arahkan
     untuk mendiskusikan pendekatan algoritmik terlebih dahulu.
   ```
3. **Aktifkan Penggunaan Berkas Instruksi**: Buka VS Code Settings (`Ctrl+,` / `Cmd+,`), cari **"GitHub > Copilot > Chat > Code Generation: Use Instruction Files"**, dan pastikan opsi tersebut aktif (centang). VS Code akan otomatis mendeteksi berkas `copilot-instructions.md` di *root* *workspace* dan menyisipkannya ke setiap permintaan Copilot Chat.
4. **Verifikasi**: Buka panel Copilot Chat (`Ctrl+Shift+I` / `Cmd+Shift+I`), lalu ajukan pertanyaan uji. Periksa apakah respons Copilot sudah sesuai dengan *role prompt* yang Anda tulis.

!!! tip "Instruksi per-Fitur"
    VS Code juga mendukung instruksi yang lebih spesifik per fitur Copilot melalui *workspace settings* (`settings.json`). Misalnya, Anda dapat menambahkan `github.copilot.chat.codeGeneration.instructions` untuk mengatur gaya *code generation*, atau `github.copilot.chat.commitMessageGeneration.instructions` untuk mengatur gaya pesan *commit*. Fitur ini berguna ketika *role prompt* umum di `copilot-instructions.md` belum cukup spesifik.

!!! info "AGENTS.md"
    VS Code juga mendukung berkas `AGENTS.md` yang berfungsi serupa dengan `copilot-instructions.md` — instruksi di dalamnya akan diterapkan ke semua permintaan Copilot di *workspace*. Berkas ini juga kompatibel dengan beberapa *autonomous coding agent* lain, sehingga berguna jika Anda menggunakan lebih dari satu *tool* AI di repositori yang sama.

#### JetBrains (IntelliJ IDEA, PyCharm, WebStorm, dll.)

1. **Buka Pengaturan Copilot**: Klik menu **File → Settings** (Windows/Linux) atau nama aplikasi pada *menu bar* → **Settings** (macOS).
2. **Navigasi ke Custom Instructions**: Pada sidebar kiri, buka **Tools → GitHub Copilot → Customizations** (atau **Edit Settings** pada beberapa versi).
3. **Pilih Lingkup Instruksi**:
   - **Workspace**: Instruksi berlaku hanya untuk proyek ini. Berkas akan disimpan sebagai `.github/copilot-instructions.md` di *root* repositori.
   - **Global**: Instruksi berlaku untuk semua proyek. Berkas disimpan di direktori konfigurasi pengguna:
     - macOS: `~/.config/github-copilot/intellij/global-copilot-instructions.md`
     - Windows: `%LOCALAPPDATA%\github-copilot\intellij\global-copilot-instructions.md`
4. **Tulis Role Prompt**: Tuliskan instruksi peran dalam format Markdown, sama seperti contoh untuk VS Code di atas.
5. **Simpan**: Klik **Apply** / **OK**. Instruksi akan otomatis disisipkan ke Copilot Chat pada IDE.

!!! warning "Periksa Versi Ekstensi"
    Fitur *custom instructions* pada JetBrains memerlukan ekstensi GitHub Copilot versi terkini. Jika opsi tidak muncul, perbarui ekstensi melalui **Settings → Plugins → GitHub Copilot → Update**.

---

## 2. Memahami Konsep Teori & Algoritma (Menggunakan Web Chat)

Ketika berhadapan dengan materi teori yang abstrak (seperti struktur data lanjutan atau konsep *multi-threading*), Anda dapat memanfaatkan antarmuka percakapan web (seperti ChatGPT atau Google Gemini) sebagai mitra diskusi.

### Langkah-langkah Praktis:
1. **Buka Antarmuka Chatbot**: Gunakan peramban web untuk mengakses layanan chatbot berbasis web.
2. **Sediakan Konteks Peran & Topik**: Tuliskan prompt yang menyertakan topik perkuliahan spesifik tanpa meminta jawaban tugas langsung.
   * *Contoh*: "Saya sedang mempelajari perbedaan algoritma pencarian BFS dan DFS pada mata kuliah SDA. Berikan penjelasan perbandingan kompleksitas ruang keduanya dengan analogi sederhana."
3. **Minta Penjelasan Bertahap**: Jika jawaban pertama terlalu umum, berikan instruksi lanjutan untuk memperdalam bagian tertentu.
4. **Verifikasi Mandiri**: Cocokkan poin penjelasan dari AI dengan slide materi perkuliahan Fasilkom UI atau buku teks resmi sebelum menggunakannya dalam pemahaman Anda.

---

## 3. Menulis & Debugging Kode di Editor (Menggunakan IDE Copilot)

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

## 4. Mengelola & Refactoring Proyek Multi-Berkas (Menggunakan Autonomous Coding Agent)

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

## 5. Menyusun Transparansi & Refleksi Penggunaan AI

Penggunaan AI dalam pengerjaan tugas di Fasilkom UI wajib disertai dengan transparansi dan refleksi proses berpikir.

### Langkah-langkah Praktis:
1. **Catat Riwayat Penggunaan**: Simpan daftar perangkat AI yang Anda gunakan serta jenis bantuan yang Anda minta selama pengerjaan tugas.
2. **Identifikasi Proses Verifikasi**: Tuliskan minimal 2-3 poin mengenai apa yang Anda periksa, kritisi, atau perbaiki dari keluaran AI tersebut secara mandiri.
3. **Lampirkan Pernyataan Refleksi**: Tambahkan bagian *Acknowledgement / Refleksi Penggunaan AI* pada berkas `README.md` repositori tugas atau laporan sesuai dengan ketentuan mata kuliah (lihat [Panduan Praktis DDP 1](panduan-praktis-ddp1.md) dan [Panduan Praktis PBP](panduan-praktis-pbp.md)).

---

## 6. Referensi Dokumen Terkait

* [Mengenal Chatbot AI](mengenal-chatbot-ai.md) — Konsep dasar LLM, antarmuka percakapan, dan penanganan halusinasi.
* [Teknik Prompting Dasar](teknik-prompting.md) — Kerangka penyusunan prompt terstruktur (T-K-F-N).
* [Panduan Praktis untuk DDP 1](panduan-praktis-ddp1.md) — Kebijakan penggunaan AI pada mata kuliah DDP 1.
* [Panduan Praktis untuk PBP](panduan-praktis-pbp.md) — Kebijakan penggunaan AI pada mata kuliah PBP.
