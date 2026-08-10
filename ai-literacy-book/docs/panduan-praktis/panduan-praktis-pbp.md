# Panduan Praktis untuk Mahasiswa PBP (Pemrograman Berbasis Platform)

Generative AI (ChatGPT, Gemini, Claude, dll.) berkembang pesat dan menjadi bagian dari kehidupan sehari-hari. Bagi Anda sebagai mahasiswa, mungkin muncul pertanyaan: apakah saya diperbolehkan menggunakan AI untuk tugas PBP? Bagaimana dampaknya bagi proses pembelajaran?

## Cakupan Mata Kuliah PBP

PBP adalah mata kuliah pengembangan aplikasi berbasis platform — Anda akan membangun aplikasi **web (Django, HTMX, Tailwind)** dan **mobile (Flutter)**, kemudian **men-deploy**-nya ke PaaS, dan **mengintegrasikan** keduanya melalui web service. Cakupan ini berbeda dari DDP1: Anda tidak hanya menulis logika, tetapi juga bekerja di atas *framework*, *package manager*, dan *lingkungan deployment*.

## Bolehkah Saya Menggunakan AI untuk Tugas?

PBP mengharapkan Anda menguasai kompetensi dasar pengembangan web & mobile **tanpa ketergantungan berlebihan** pada AI. Aturan umumnya:

| Jenas Tugas | Boleh Pakai AI? | Catatan |
|---|---|---|
| Kuis (lab maupun kelas) | Tidak | — |
| UTS / UAS | Tidak | — |
| Tugas individu (lab/tutorial) | Terbatas | Hanya untuk diskusi ide, penjelasan error, dan mencari pendekatan alternatif — bukan untuk menulis kode final. |
| Tugas kelompok (proyek awal & akhir semester) | Boleh | Wajib menulis refleksi proses dan acknowledgement. |

## Yang Boleh Dilakukan dengan AI

Anda dapat menganggap AI sebagai **asisten belajar** — bukan penulis kode utama. Peran yang diperbolehkan:

- Mendiskusikan rancangan arsitektur (model, view, route, widget tree).
- Meminta penjelasan *traceback* Django/Flutter.
- Membandingkan dua pendekatan (mis. Function-Based View vs Class-Based View, `setState` vs Provider, SQLite vs PostgreSQL di PaaS).
- Meminta klarifikasi terhadap penjelasan dosen/asdos atau dokumentasi framework.
- *Brainstorm* ide fitur untuk proyek kelompok.

## Yang Tidak Boleh Dilakukan

- Menyalin kode **utuh** dari AI untuk tugas individu tanpa penjelasan.
- Meminta AI menulis seluruh *view*, *serializer*, atau *widget* dan menyerahkannya sebagai hasil kerja sendiri.
- Menggunakan AI untuk **mengerjakan kuis atau ujian** — ini termasuk *academic integrity violation* dan akan ditangani sesuai aturan fakultas.
- Membagikan *API key*, *credential* PaaS, atau data pribadi ke chatbot AI publik (lihat [Bab 7 — Risiko dan Keterbatasan AI](../bab7-risiko-keterbatasan.md)).

## Tools yang Direkomendasikan untuk PBP

- **IDE & Editor**: VS Code / PyCharm dengan ekstensi seperti *GitHub Copilot*, *Continue*, atau *Cody* — gunakan sebagai *pair-programmer* inline, **bukan** untuk menghasilkan blok kode utuh.
- **AI Chat**: ChatGPT / Gemini / Claude — untuk diskusi konseptual.
- **Testing API**: Postman / Insomnia — uji endpoint Anda, jangan meminta AI menggenerasi *request* tanpa Anda pahami strukturnya.
- **Version Control**: `git` dengan commit message bermakna — supaya dosen/asdos bisa melihat **kontribusi Anda** (termasuk bagaimana Anda menggunakan AI).
- **DevTools browser** + **Flutter DevTools** — alat resmi debugging yang selalu lebih akurat daripada tebakan AI.

## Kritisi Hasil AI: Rubrik 4 Pertanyaan

Setiap kali Anda menggunakan output AI untuk tugas PBP, jawab empat pertanyaan ini (wajib ditulis di refleksi):

1. **Akurat?** — Apakah kode/perintah yang diberikan AI benar-benar berlaku untuk versi framework yang Anda pakai? (Cek dokumentasi resmi Django/Flutter.)
2. **Aman?** — Apakah ada *hardcoded secret*, *SQL injection*, atau *CORS* terbuka di output AI yang perlu diperbaiki?
3. **Sesuai konteks?** — Apakah AI paham konteks PBP (mis. Anda deploy ke PaaS, bukan localhost)? Atau AI memberikan solusi yang tidak relevan?
4. **Bisa saya jelaskan?** — Jika asdos bertanya, bisakah Anda menjelaskan **setiap baris** kode yang Anda hasilkan/gunakan? Jika tidak, itu sinyal Anda terlalu bergantung pada AI.

## Hal yang Perlu Diperhatikan dalam Penggunaan AI

Anda harus sadar bahwa ada risiko dan kelemahan ketika terlalu bergantung pada AI untuk mendukung pembelajaran Anda. Ingat bahwa AI bukan manusia.

### Cognitive Offloading

Sudah banyak penelitian yang membuktikan bahwa kebergantungan pada generative AI dapat menurunkan kemampuan kognitif, metakognitif, dan berpikir kritis Anda. Jika Anda terlalu sering menggunakan AI untuk meringkas teks yang panjang, Anda akan kehilangan kemampuan berpikir kritis untuk menganalisis dokumen yang kompleks. Anda juga akhirnya tidak melatih otak Anda untuk memecahkan masalah atau mencari ide dengan kecerdasan Anda sendiri.

Pada pemrograman, ketika Anda terlalu bergantung untuk mencari solusi kode, maka Anda akan melemahkan kemampuan Anda sendiri untuk menjadi pembelajar dan menjadi ahli di bidang yang ingin Anda kuasai. Belajar dengan kerja keras dan sungguh-sungguh tentu adalah pendekatan terbaik dibandingkan mencari jalan pintas dengan bergantung pada AI.

PBP menguji **CPMK-1** (implementasi lintas platform) dan **Sub-CPMK 12** (aspek keamanan) — kedua-duanya memerlukan Anda memahami **mengapa** kode Anda bekerja, bukan hanya **apa** kode itu.

### Bias dan Halusinasi di Konteks PBP

AI generatif tahu banyak tapi tidak selalu benar. Contoh umum yang sering ditemui di PBP:

- Memberikan **API method Flutter yang sudah deprecated** (mis. `withOpacity` alih-alih `Color.withValues`).
- Mengarang **konfigurasi `pubspec.yaml` atau `requirements.txt`** yang tidak ada di versi saat ini.
- Menyarankan **middleware Django yang tidak kompatibel** dengan Django 6.x.
- Memberikan **contoh kode yang tidak aman** (mis. `mark_safe` pada input user tanpa escaping) — berbahaya untuk Sub-CPMK 12.

**Selalu verifikasi terhadap dokumentasi resmi**: [MDN](https://developer.mozilla.org), [Django Docs](https://docs.djangoproject.com/en/6.0/), [Flutter Docs](https://docs.flutter.dev), [OWASP WSTG](https://owasp.org/www-project-web-security-testing-guide/v42/), [OWASP MASTG](https://mas.owasp.org/MASTG/).

### Privasi dan Kode Akademik

Jangan menempelkan kode submission Anda ke AI publik untuk "dicek" — output dari AI dapat di-*reuse* untuk melatih model. Gunakan AI hanya untuk **cuplikan kecil** atau **konsep abstrak**, bukan seluruh artefak submission.

## Refleksi Wajib untuk Tugas PBP

Di setiap tugas individu/kelompok yang menggunakan AI, sertakan bagian refleksi singkat (3–6 kalimat) yang memuat:

- Prompt apa yang Anda gunakan.
- Output AI mana yang Anda pilih dan mengapa.
- Apa yang Anda verifikasi, kritik, atau perbaiki.
- *Acknowledgement* eksplisit: "Tugas ini menggunakan [nama tool AI] untuk [peran spesifik]."

Setiap tugas yang Anda kerjakan akan ditanyakan oleh asdos/dosen untuk menilai pemahaman dari apa yang Anda kerjakan. Dosen/asdos mungkin akan memberikan beberapa pertanyaan terkait yang Anda kerjakan, dan menanyakan kemungkinan opsi pendekatan lainnya dalam menyelesaikan tugas Anda.

## Referensi

- Connolly, R., & Hoar, R. (2022). *Fundamentals of Web Development* (3rd ed.). Pearson. <https://www.pearson.com/en-us/subject-catalog/p/fundamentals-of-web-development/P200000003214/9780136792857>
- Hoffman, A. (2024). *Web Application Security* (2nd ed.). O'Reilly Media. <https://www.amazon.com/Web-Application-Security-Exploitation-Countermeasures/dp/1098143930>
- Percival, H. *Test-Driven Development with Python: Obey the Testing Goat!* (3rd ed.). <https://www.obeythetestinggoat.com/>
- Mozilla Developer Network (MDN) Web Docs. <https://developer.mozilla.org>
- Django Documentation 6.0. <https://docs.djangoproject.com/en/6.0/>
- Flutter Documentation. <https://docs.flutter.dev>
- OWASP Web Security Testing Guide (WSTG v4.2). <https://owasp.org/www-project-web-security-testing-guide/v42/>
- OWASP Mobile Application Security Testing Guide (MASTG). <https://mas.owasp.org/MASTG/>
- University of Edinburgh. *Generative AI Guidance for Students*. <https://information-services.ed.ac.uk/computing/comms-and-collab/elm/generative-ai-guidance-for-students/using-generative-ai>

---

**Penutup:** AI adalah alat yang kuat, tetapi **pemahaman Anda yang menjadi tujuan pembelajaran PBP**. Gunakan AI secara strategis untuk mempercepat belajar — bukan untuk menghindari belajar.
