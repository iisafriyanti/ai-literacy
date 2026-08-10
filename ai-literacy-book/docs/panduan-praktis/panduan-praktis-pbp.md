# Panduan Praktis untuk Mahasiswa PBP (Pemrograman Berbasis Platform)

Generative AI (ChatGPT, Gemini, Claude, dll.) berkembang pesat dan menjadi bagian dari kehidupan sehari-hari. Bagi Anda sebagai mahasiswa, mungkin muncul pertanyaan: apakah saya diperbolehkan menggunakan AI untuk tugas PBP? Bagaimana dampaknya bagi proses pembelajaran?

## Cakupan Mata Kuliah PBP

PBP adalah mata kuliah pengembangan aplikasi berbasis platform — Anda akan membangun aplikasi **web (Django, HTMX, Tailwind)** dan **mobile (Flutter)**, kemudian **men-deploy**-nya ke PaaS, dan **mengintegrasikan** keduanya melalui web service. Cakupan ini berbeda dari DDP1 dan DDP2: Anda tidak hanya menulis logika, tetapi juga bekerja di atas *framework*, *package manager*, dan *lingkungan deployment*.

## Bolehkah Saya Menggunakan AI untuk Tugas?

PBP mengharapkan Anda menguasai kompetensi dasar pengembangan web & mobile **tanpa ketergantungan berlebihan** pada AI. Aturan umumnya:

| Jenis Tugas | Boleh Pakai AI? | Catatan |
|---|---|---|
| Kuis (lab maupun kelas) | Tidak | — |
| UTS / UAS | Tidak | — |
| Tugas individu (lab/tutorial) | Terbatas | Hanya untuk diskusi ide, penjelasan error, dan mencari pendekatan alternatif — bukan untuk menulis kode final. |
| Tugas kelompok (proyek awal & akhir semester) | Boleh | Wajib menulis refleksi proses dan acknowledgement. |

### Mengapa Ada Pembagian Tugas yang Boleh dan Tidak Boleh Menggunakan AI?

CS2023 (ACM/IEEE-CS/AAAI Joint Task Force, 2024) membedakan dua jenis penilaian: *secure assessment* (penilaian terjamin) dan *insecure assessment* (penilaian tidak terjamin). *Secure assessment* dilakukan dalam lingkungan terpantau — seperti kuis dan ujian yang diawasi — di mana penggunaan AI dapat dikendalikan dan hasilnya mencerminkan kompetensi mahasiswa secara langsung. *Insecure assessment* dilakukan tanpa pengawasan — seperti tugas rumah dan proyek — di mana penggunaan AI sulit dicegah dan hasilnya tidak selalu mencerminkan pemahaman mahasiswa secara mandiri. Karena itu, PBP menggunakan *secure assessment* (kuis, UTS, UAS) untuk memastikan Anda benar-benar menguasai kompetensi inti, dan *insecure assessment* (tugas lab, proyek kelompok) untuk melatih penggunaan AI secara reflektif dan kritis — dengan syarat refleksi dan *acknowledgement* yang wajib.

*(Berdasarkan: Becker et al., 2023, "Generative AI in Introductory Programming," CS2023 Curricular Practices Volume, ACM/IEEE-CS/AAAI.)*

## Klasifikasi Pelanggaran Integritas Akademik terkait AI

CS2023 (ACM/IEEE-CS/AAAI Joint Task Force, 2024) membedakan dua kategori pelanggaran integritas akademik terkait penggunaan GenAI:

**1. Pemalsuan (Falsification)**

Terjadi ketika mahasiswa menyajikan hasil kerja AI sebagai karya sendiri tanpa mengakui penggunaan AI. Ini mencakup:

- Menyalin kode utuh dari AI dan menyerahkannya sebagai hasil kerja mandiri tanpa refleksi.
- Menggunakan AI untuk menulis seluruh *view*, *serializer*, atau *widget* dan mengklaimnya sebagai karya sendiri.
- Menyajikan penjelasan atau analisis yang dihasilkan AI tanpa modifikasi atau pemahaman sendiri.

**2. Penggunaan Sumber Daya Tidak Sah (Use of Unauthorized Resources)**

Terjadi ketika mahasiswa menggunakan GenAI dengan cara yang dilarang oleh kebijakan mata kuliah, tugas spesifik, atau aturan ujian. Ini mencakup:

- Menggunakan AI selama kuis, UTS, atau UAS — terlepas dari apakah output disalin langsung atau dimodifikasi.
- Menggunakan AI untuk tugas individu di luar batas yang dijelaskan di bagian "Yang Boleh Dilakukan dengan AI" padahal kebijakan tugas tersebut melarangnya.

Kedua kategori di atas merupakan pelanggaran *academic integrity* dan akan ditangani sesuai aturan fakultas. Perbedaan ini penting karena membantu Anda memahami **apa yang berlebihan dan apa yang tidak** — bukan sekadar "jangan menyontoh," melainkan "kenali batas penggunaan yang sah dan akui penggunaan AI secara terbuka."

*(Berdasarkan: Becker et al., 2023, "Generative AI in Introductory Programming," CS2023 Curricular Practices Volume, ACM/IEEE-CS/AAAI.)*

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

## Teknik Prompting untuk PBP: Kerangka CLEAR

Kemampuan menyusun *prompt* yang efektif adalah keterampilan yang dapat dipelajari dan dilatih. CS2023 secara eksplisit mendorong pengajaran *prompt engineering* sebagai kompetensi praktis (Becker et al., 2023). Untuk PBP, kami mengadopsi kerangka **CLEAR** (Lo, 2023) sebagai panduan menyusun prompt yang efektif:

- **C — Concise (Ringkas)**: Gunakan bahasa yang jelas dan langsung. Hilangkan kata-kata basa seperti "tolong" atau "bisa kah Anda." Fokus pada inti instruksi.
  - *Contoh PBP*: Daripada "Tolong jelaskan cara membuat form login di Django ya," gunakan "Jelaskan langkah membuat form autentikasi di Django 6.0 menggunakan `AuthenticationForm`."

- **L — Logical (Logis)**: Susun prompt mengikuti urutan yang koheren. Pecah tugas menjadi langkah-langkah berurutan.
  - *Contoh PBP*: "Jelaskan alur request-response di Django MTV: mulai dari URL dispatcher, ke view, ke template, hingga HTTP response."

- **E — Explicit (Eksplisit)**: Tentukan format output, batasan, dan konteks secara spesifik. Sertakan versi framework yang Anda gunakan.
  - *Contoh PBP*: "Buatkan contoh Function-Based View di Django 6.0 yang mengembalikan JSON response untuk endpoint `/api/products/`. Gunakan `JsonResponse` dan sertakan penanganan error 404."

- **A — Adaptive (Adaptif)**: Jika output pertama belum sesuai, modifikasi prompt Anda. Pecah pertanyaan besar menjadi bagian-bagian kecil. Iterasi adalah bagian normal dari proses.
  - *Contoh PBP*: Jika AI memberikan kode yang menggunakan import yang sudah deprecated di Django 6.0, berikan prompt lanjutan: "Perbarui kode di atas untuk Django 6.0 — ganti `django.shortcuts.render_to_response` dengan `render`."

- **R — Reflective (Reflektif)**: Evaluasi output AI untuk akurasi, relevansi, dan kelengkapan. Gunakan evaluasi ini untuk memperbaiki prompt di masa depan.
  - *Contoh PBP*: Setelah AI memberikan solusi, tanyakan: "Apakah kode ini aman dari XSS? Apakah ada input validation yang hilang?" Jika AI mengakui kelemahan, catat itu di refleksi Anda.

**Referensi**: Lo, L. S. (2023). The CLEAR path: A framework for enhancing information literacy through prompt engineering. *Journal of Academic Librarianship*, 49(4), Article 102720. <https://doi.org/10.1016/j.acalib.2023.102720>

## Alat Bantu Belajar: Burhan (AI TA)

PBP menyediakan **Burhan**, sebuah *role prompt* yang mengubah alat AI pilihan Anda menjadi asisten Socratic. Berbeda dengan menggunakan ChatGPT atau Claude secara langsung, Burhan **tidak akan memberikan jawaban lengkap** — ia membantu Anda menemukan solusi sendiri melalui pertanyaan-pertanyaan dan rujukan ke dokumentasi resmi.

### Cara Menggunakan Burhan

1. Unduh *template repository* tugas/tutorial PBP dari GitHub — *role prompt* Burhan tersedia di `.github/agents/burhan-ta.agent.md`.
2. Salin (copy-paste) isi *role prompt* tersebut ke dalam alat AI pilihan Anda (ChatGPT, Gemini, Claude, dll.) sebagai *custom prompt*, *system prompt*, atau pesan pertama.
3. Mulai bertanya. Burhan akan membantu Anda secara Socratic — menunjukkan ke dokumentasi, menjelaskan konsep, dan mengarahkan Anda ke solusi sendiri.

Burhan bekerja dengan **alat AI apa pun** yang Anda gunakan — gratis maupun berbayar. Kami merekomendasikan untuk selalu menggunakan Burhan ketika meminta bantuan AI untuk tugas PBP, karena:

- Ia melatih Anda untuk berpikir, bukan menyalin.
- Ia mengarahkan Anda ke dokumentasi resmi (Django, Flutter, MDN, OWASP).
- Ia tidak akan menyelesaikan tugas *untuk* Anda — tetapi ia akan menemani Anda *mengerjakan* tugas.

**Tips:** Jika Anda menggunakan VS Code dengan GitHub Copilot atau Cursor IDE, Burhan akan otomatis dimuat dari *template repository* — Anda tidak perlu *copy-paste* manual. Untuk pengguna ChatGPT/Gemini/Claude versi web, muat Burhan secara manual sebagai pesan pertama sebelum bertanya.

**Catatan:** Burhan adalah *prompt*, bukan platform. Ia bergantung pada Anda untuk memuatnya ke alat AI Anda. Jika Anda meminta bantuan AI tanpa memuat Burhan terlebih dahulu, Anda kehilangan panduan Socratic tersebut — dan cenderung menerima jawaban lengkap yang tidak Anda pahami.

## Tools yang Direkomendasikan untuk PBP

- **IDE & Editor**: VS Code / PyCharm dengan ekstensi seperti *GitHub Copilot*, *Continue*, atau *Cody* — gunakan sebagai *pair-programmer* inline, **bukan** untuk menghasilkan blok kode utuh.
- **AI Chat**: ChatGPT / Gemini / Claude — untuk diskusi konseptual (jangan lupa muat Burhan terlebih dahulu).
- **Testing API**: Postman / Insomnia — uji endpoint Anda, jangan meminta AI menggenerasi *request* tanpa Anda pahami strukturnya.
- **Version Control**: `git` dengan commit message bermakna — supaya dosen/asdos bisa melihat **kontribusi Anda** (termasuk bagaimana Anda menggunakan AI).
- **DevTools browser** + **Flutter DevTools** — alat resmi debugging yang selalu lebih akurat daripada tebakan AI.

## Kritisi Hasil AI: Rubrik 4 Pertanyaan

Setiap kali Anda menggunakan output AI untuk tugas PBP, jawab empat pertanyaan ini (wajib ditulis di refleksi):

1. **Akurat?** — Apakah kode/perintah yang diberikan AI benar-benar berlaku untuk versi framework yang Anda pakai? (Cek dokumentasi resmi Django/Flutter.)
2. **Aman?** — Apakah ada *hardcoded secret*, *SQL injection*, atau *CORS* terbuka di output AI yang perlu diperbaiki?
3. **Sesuai konteks?** — Apakah AI paham konteks PBP (mis. Anda deploy ke PaaS, bukan localhost)? Atau AI memberikan solusi yang tidak relevan?
4. **Bisa saya jelaskan?** — Jika asdos bertanya, bisakah Anda menjelaskan **setiap baris** kode yang Anda hasilkan/gunakan? Jika tidak, itu sinyal Anda terlalu bergantung pada AI.

## Verifikasi Pemahaman: Model Bertingkat

Untuk memastikan mahasiswa memahami kode yang mereka kerjakan — terutama ketika AI terlibat — PBP menerapkan verifikasi pemahaman dalam tiga tingkat:

**Tingkat 1 — Verifikasi Asdos (Lab Routine)**

Pada setiap sesi lab, asdos secara acak memilih 2–3 mahasiswa untuk menjelaskan satu bagian kode yang mereka kerjakan minggu itu. Ini bukan penilaian formal — cukup 3–5 menit per mahasiswa — tetapi menciptakan budaya "siap menjelaskan" dan memberi sinyal dini untuk mahasiswa yang kesulitan.

**Tingkat 2 — Code Review Berstruktur (Proyek Kelompok)**

Pada proyek awal dan akhir semester, setiap kelompok wajib melakukan *code review session* dengan asdos. Setiap anggota kelompok menunjukkan minimal satu kontribusi *commit* dan menjelaskan logikanya. Asdos mencatat skor pemahaman per anggota menggunakan rubrik sederhana (memahami / memahami sebagian / tidak memahami). Skor ini memengaruhi nilai individu proyek (CPMK-3, Sub-CPMK 15).

**Tingkat 3 — Oral Defense Terbatas (UTS & UAS)**

Pada periode UTS dan UAS, dosen melakukan oral defense untuk **sampel mahasiswa** — bukan seluruh 300. Mekanisme pemilihan:

- Mahasiswa dengan skor proyek individu di ambang batas (borderline) wajib diundang.
- Mahasiswa yang dicurigai menggunakan AI secara berlebihan (berdasarkan pola commit, refleksi yang terlalu generik, atau laporan asdos).
- Sampel acak ~10% untuk menjaga validitas statistik.

Dengan 300 mahasiswa, ini berarti sekitar 30–50 oral defense per periode ujian — atau 6–10 per dosen — yang realistis dalam jangka waktu 2 minggu.

**Catatan tentang peran asdos**: Verifikasi Tingkat 1 dan 2 dilakukan oleh asdos dengan rubrik yang distandardisasi. Untuk mengatasi kekhawatiran tentang objektivitas asdos, rubrik dirancang berbasis *checklist* konkret ("apakah mahasiswa dapat menjelaskan fungsi parameter `request`?") alih-alih penilaian subjektif. Asdos juga tidak berwenang memberikan skor final — mereka hanya merekomendasikan, dan dosen melakukan konfirmasi.

## Akses yang Adil terhadap Alat AI (Keadilan dan Inklusi)

PBP di Universitas Indonesia menyadari bahwa mahasiswa kami berasal dari latar belakang ekonomi dan sosial yang beragam. Tidak semua mahasiswa memiliki kemampuan finansial untuk berlangganan alat AI berbayar (Claude Pro/Max, GitHub Copilot, GPT-4 Plus, dll.), dan tidak semua mahasiswa memiliki pengalaman sebelumnya dalam menggunakan alat AI untuk pemrograman. Kami berkomitmen memastikan bahwa **nilai akhir mata kuliah ini tidak ditentukan oleh kemampuan finansial untuk mengakses alat AI**.

### Kebijakan Akses yang Adil

**1. Secure assessment tidak bergantung pada AI**

Kuis, UTS, dan UAS — yang merupakan komponen utama penilaian individu — **tidak menggunakan AI**. Ini berarti semua mahasiswa dinilai atas dasar kompetensi mereka sendiri, bukan atas kualitas alat AI yang mereka mampu beli. Mahasiswa dengan AI gratis dan mahasiswa dengan Claude Max memiliki kesempatan yang persis sama di komponen penilaian yang paling berdampak.

**2. Burhan: panduan Socratic untuk semua alat AI**

PBP menyediakan *role prompt* Burhan yang dapat dipasang pada alat AI apa pun — ChatGPT gratis, Gemini, Claude, maupun alat berbayar lainnya. Burhan memastikan bahwa di mana pun mahasiswa meminta bantuan AI, mereka mendapatkan **bimbingan Socratic, bukan jawaban lengkap**. Mahasiswa dengan AI gratis dan mahasiswa dengan AI berbayar sama-sama mendapatkan pengalaman bimbingan yang berfokus pada pembelajaran, bukan pada penyelesaian tugas secara otomatis.

**3. Refleksi dinilai, bukan output AI**

Pada tugas kelompok yang memperbolehkan AI, penilaian tidak didasarkan pada kelengkapan kode hasil AI, melainkan pada **refleksi proses**: bagaimana mahasiswa menggunakan AI (alat apa pun itu), apa yang diverifikasi, apa yang diperbaiki, dan bagaimana kontribusi setiap anggota dijelaskan. Mahasiswa yang menggunakan AI gratis tetapi menulis refleksi yang mendalam akan dinilai lebih tinggi daripada mahasiswa yang menggunakan AI berbayar tetapi tidak dapat menjelaskan kodenya.

**4. Tidak ada keharusan menggunakan alat AI berbayar**

Tugas-tugas di PBP dirancang untuk dapat diselesaikan **tanpa alat AI berbayar**. Dokumentasi resmi (Django Docs, Flutter Docs, MDN) dan Burhan sudah cukup. Mahasiswa **tidak diwajibkan** membeli langganan AI apa pun. Jika Anda merasa tertekan untuk membeli langganan AI agar bisa bersaing, beri tahu dosen — itu **bukan** ekspektasi mata kuliah ini.

**5. Sumber daya gratis yang direkomendasikan**

- [Google AI Studio](https://aistudio.google.com) — akses gratis ke model Gemini (termasuk untuk pemrograman)
- [GitHub Copilot Free](https://github.com/features/copilot) — tier gratis dengan batasan bulanan
- [Cursor IDE Free Tier](https://cursor.com) — editor dengan integrasi AI, tier gratis tersedia
- [ChatGPT Free](https://chat.openai.com) — model GPT dengan batasan harian
- [Claude Free](https://claude.ai) — model Claude dengan batasan harian
- Burhan (PBP AI TA) — asisten Socratic khusus PBP, gratis untuk mahasiswa

### Mengapa Ini Penting

CS2023 (Becker et al., 2023) memperingatkan tentang **"Matthew Effect"**: mahasiswa dengan pengalaman dan sumber daya lebih akan mendapat manfaat lebih besar dari AI, sementara mahasiswa dengan sumber daya lebih sedikit dapat tertinggal lebih jauh. PBP secara aktif bekerja melawan efek ini dengan memastikan bahwa:

- Penilaian inti (kuis, ujian) tidak bergantung pada akses AI
- Bantuan AI (Burhan) tersedia gratis untuk semua
- Refleksi dan pemahaman dinilai, bukan kualitas keluaran AI
- Tidak ada mahasiswa yang harus mengeluarkan biaya untuk bersaing secara adil

Jika Anda mengalami kesulitan akses atau merasa dirugikan oleh perbedaan sumber daya, silakan menghubungi dosen. Diskusi ini akan dijaga kerahasiaannya.

*(Berdasarkan: Becker et al., 2023, "Generative AI in Introductory Programming," CS2023 Curricular Practices Volume; Eaton & Epstein, 2024, "AI in CS2023: Rationale and Challenges," AAAI-24.)*

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

- Becker, B. A., Craig, M., Denny, P., Keuning, H., Kiesler, N., Leinonen, J., Luxton-Reilly, A., Malmi, L., Prather, J., & Quille, K. (2023). Generative AI in Introductory Programming. In *Computer Science Curricula 2023, Curricular Practices Volume*. ACM/IEEE-CS/AAAI. <https://csed.acm.org>
- ACM/IEEE-CS/AAAI Joint Task Force. (2024). *Computer Science Curricula 2023 (CS2023)*. ACM, IEEE Computer Society, AAAI. <https://doi.org/10.1145/3664191>
- Eaton, E., & Epstein, S. L. (2024). Artificial Intelligence in the CS2023 Undergraduate Computer Science Curriculum: Rationale and Challenges. In *Proceedings of the Thirty-Eighth AAAI Conference on Artificial Intelligence (AAAI-24)*. <https://ojs.aaai.org/index.php/AAAI/article/view/30352>
- Lo, L. S. (2023). The CLEAR path: A framework for enhancing information literacy through prompt engineering. *Journal of Academic Librarianship*, 49(4), Article 102720. <https://doi.org/10.1016/j.acalib.2023.102720>
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
