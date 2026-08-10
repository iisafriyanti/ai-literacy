# Panduan Praktis untuk Dosen Pemrograman

Generative AI, seperti ChatGPT, Gemini, dan Claude, berkembang sangat cepat dan menjadi bagian dari proses pendidikan. Bagi Anda sebagai dosen atau asisten dosen, panduan ini membantu Anda merancang kebijakan penggunaan AI yang seimbang — tidak melarang sepenuhnya, tetapi juga tidak membiarkan mahasiswa ketergantungan.

## Kebijakan Penggunaan AI dalam Mata Kuliah Pemrograman

Setiap mata kuliah memiliki kebijakannya sendiri dalam pemanfaatan AI. Berikut adalah kerangka umum yang dapat disesuaikan:

### Untuk Mata Kuliah Pemrograman Berbasis Platform (PBP)
Mata kuliah PBP adalah mata kuliah pemrograman web dan mobile pertama yang dipelajari mahasiswa di Fasilkom UI. Mahasiswa diharapkan menguasai kompetensi dasar pemrograman berbasis web dan mobile tanpa bergantung berlebihan pada AI. Dengan demikian, kuis dan ujian tengah maupun akhir semester tidak diperkenankan menggunakan AI. Namun, mahasiswa dapat melatih proses berpikir kritis dalam pemanfaatan AI selama proses pembelajaran di lab. Selain itu, mahasiswa dapat memanfaatkan AI untuk pengerjaan proyek awal dan akhir semester bersama teman satu kelompok serta merefleksikan proses pengerjaannya.

### Untuk Mata Kuliah Dasar-Dasar Pemrograman 1 (DDP 1)
Mata kuliah DDP 1 adalah mata kuliah pemrograman pertama yang dipelajari mahasiswa. Mahasiswa diharapkan menguasai kompetensi dasar pemrograman tanpa bergantung pada AI. Tutorial, kuis, dan ujian tidak diperkenankan menggunakan AI. Namun, ada tugas akhir yang memberikan kesempatan untuk bereksplorasi dengan bantuan AI.

Setidaknya mahasiswa dapat memanfaatkan AI untuk mengerjakan tugas individu dan tugas kelompok, namun mereka harus:
- Menuliskan refleksi bagaimana proses mereka memanfaatkan AI dalam mengerjakan tugas
- Apa saja yang mereka verifikasi, kritik, atau perbaiki dari keluaran AI
- Menuliskan pengakuan atau acknowledgement terhadap penggunaan AI seperti apa saja yang mereka manfaatkan dari AI

Setiap tugas yang mahasiswa kerjakan akan ditanyakan oleh asdos/dosen untuk menilai pemahaman dari apa yang mereka kerjakan. Dosen/asdos mungkin akan memberikan beberapa pertanyaan terkait yang mereka kerjakan, dan menanyakan kemungkinan opsi pendekatan lainnya dalam menyelesaikan tugas.

## Strategi Pembelajaran dengan AI
Anda dapat mendorong mahasiswa memanfaatkan AI untuk proses pembelajaran di luar kuliah tatap muka. Mahasiswa dapat menganggap AI sebagai teman untuk mendukung perkuliahan, dengan melakukan:
- Mendiskusikan ide
- Meminta penjelasan error pada kode yang mereka buat
- Meminta bantuan untuk memberikan pendekatan alternatif lainnya
- Meminta penjelasan lebih terhadap penjelasan dosen/asdos atau informasi yang mereka temukan

### Tools AI untuk pemrograman yang cocok untuk mahasiswa
- Google Colab (untuk DDP 1)
- VS Code + Copilot/Continue/Cody (untuk PBP)
- Postman / Insomnia (untuk pengujian API di PBP)

### Mendorong Kritisi Hasil dari AI
Anda dapat meminta mahasiswa secara berkelompok mengkritisi hasil keluaran AI:
- Apakah kode yang diberikan AI akurat dan sesuai versi framework yang dipakai?
- Apakah ada masalah keamanan (hardcoded secret, SQL injection, CORS terbuka)?
- Apakah AI memberikan solusi yang relevan dengan konteks mata kuliah?
- Bisakah mahasiswa menjelaskan setiap baris kode yang dihasilkan AI?

## Hal-hal yang perlu diperhatikan dalam penggunaan AI
Anda harus sadar bahwa ada risiko dan kelemahan ketika terlalu bergantung pada AI untuk mendukung pembelajaran Anda. Ingat bahwa AI bukan manusia.

### Cognitive Offloading
Sudah banyak penelitian yang membuktikan bahwa kebergantungan pada generative AI dapat menurunkan kognitif Anda, menurunkan metakognitif, dan berpikir kritis. Jika Anda terlalu sering menggunakan AI untuk meringkas teks yang panjang, Anda akan kehilangan kemampuan berpikir kritis untuk menganalisis dokumen yang kompleks. Anda juga akhirnya tidak melatih otak Anda untuk memecahkan masalah atau mencari ide dengan kecerdasan Anda sendiri. Pada pemrograman, ketika Anda terlalu bergantung untuk mencari solusi kode, maka Anda akan melemahkan kemampuan Anda sendiri untuk menjadi pembelajar dan menjadi ahli di bidang yang ingin Anda kuasai. Belajar dengan kerja keras dan sungguh-sungguh tentu adalah pendekatan terbaik dibandingkan mencari jalan pintas dengan bergantung pada AI. 

Penelitian tentang AI yang dapat menurunkan kemampuan kognitif dan metakognitif mahasiswa terus berkembang. Sebagai dosen, penting untuk merancang tugas yang mendorong mahasiswa menggunakan AI secara reflektif, bukan sekadar konsumtif.

### Bias dan Halusinasi

AI dapat menghasilkan informasi yang terdengar meyakinkan tetapi sebenarnya salah (halusinasi). Dalam konteks pemrograman, AI dapat memberikan kode yang terlihat benar tetapi mengandung bug halus, menggunakan API yang sudah deprecated, atau menyarankan library yang tidak ada. Mahasiswa perlu dilatih untuk mengenali dan mengkritisi hal ini.

AI juga dapat mewarisi bias dari data pelatihannya. Diskusikan dengan mahasiswa bagaimana bias ini dapat muncul dalam contoh kode, saran desain, atau penjelasan konsep yang diberikan AI.

## Referensi

- University of Edinburgh. *Generative AI Guidance for Students*. <https://information-services.ed.ac.uk/computing/comms-and-collab/elm/generative-ai-guidance-for-students/using-generative-ai>