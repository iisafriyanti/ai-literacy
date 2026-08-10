# Artificial Intelligence

## Apa Itu Kecerdasan Buatan (AI)?
Artificial Intelligence atau kecerdasan buatan mungkin sulit didefinisikan oleh sebagian orang, bahkan bagi seorang ahli pun demikian. Kamus Cambridge mendefinisikan bahwa AI adalah sistem komputer atau mesin yang kemampuannya seperti otak manusia, seperti kemampuan menjawab pertanyaan, menggambar, memecahkan masalah, atau yang lainnya. Namun, terminologi ini sebenarnya terus berkembang, tergantung kapan dan siapa kita mengenalnya. Namun, secara sederhana AI bukanlah manusia, namun suatu program komputer yang dilatih untuk mengenali pola dari data yang sangat besar. Dari data tersebut, program komputer akan membuat prediksi atau menghasilkan output yang sesuai dengan probabilitas dari data yang pernah sistem terima.

## Bagaimana AI "Belajar"?

Sebagian besar AI modern menggunakan pendekatan yang disebut **machine learning (pembelajaran mesin)**. Alih-alih diprogram dengan aturan tetap ("jika X maka Y"), sistem ini "belajar" dari data:

1. **Data pelatihan** — sistem diberi contoh dalam jumlah sangat besar (misalnya jutaan gambar kucing dan bukan kucing).
2. **Proses pelatihan** — sistem menyesuaikan parameter internalnya berulang kali untuk semakin akurat mengenali pola.
3. **Model** — hasil akhir dari proses ini adalah "model" yang dapat digunakan untuk memproses data baru.

## Jenis-Jenis AI
Ada berbagai macam jenis AI dengan cara pengoperasian yang berbeda-beda tergantung bagaimana ia dikembangkan, tujuannya untuk apa, dan bagaimana mendeploynya. Namun, setidaknya terdapat dua jenis AI yang cukup berkembang: (1) Generative AI dan (2) Predictive Ai

### AI Generatif (Generative AI - GenAI)
**AI generatif (generative AI)** adalah jenis AI yang mampu *menghasilkan* konten baru — teks, gambar, audio, video, atau kode — berdasarkan data yang dimiliki atau dilatih. Contoh populer termasuk chatbot berbasis **Large Language Model (LLM)** seperti Claude, serta alat pembuat gambar AI. Sistem AI ini mampu menghasilkan output yang seperti original asli, padahal output yang dihasilkan berdasarkan data latih yang dimiliki AI. Hal ini yang menjadi pertanyaan bagi kita bagaimana keaslian, copyright, dan kepemilikikan dari luaran AI?

Beberapa istilah kunci yang sering muncul:

- **Large Language Model (LLM)**: model AI yang dilatih pada teks dalam jumlah sangat besar untuk memahami dan menghasilkan bahasa manusia.
- **Prompt**: instruksi atau pertanyaan yang diberikan pengguna kepada AI.
- **Token**: satuan unit teks (kurang lebih sepotong kata) yang diproses oleh model bahasa.
- **Halusinasi (hallucination)**: kondisi ketika AI menghasilkan informasi yang terdengar meyakinkan tetapi sebenarnya salah atau tidak berdasar fakta.

## Apa yang AI Bisa dan Tidak Bisa Lakukan

=== "Yang Bisa Dilakukan AI"
    - Merangkum teks panjang dengan cepat
    - Menjawab pertanyaan umum berdasarkan pola dari data pelatihan
    - Membantu menulis draf, kode, atau ide kreatif
    - Menerjemahkan bahasa
    - Mengenali pola dalam gambar, suara, atau data

=== "Batasan AI"
    - Tidak benar-benar "memahami" makna seperti manusia — ia memproses pola statistik
    - Dapat menghasilkan informasi salah dengan percaya diri (halusinasi)
    - Pengetahuannya terbatas pada data yang digunakan saat pelatihan (ada *cutoff* waktu)
    - Tidak memiliki kesadaran, emosi, atau niat
    - Dapat mewarisi bias dari data yang digunakan untuk melatihnya

!!! warning "Poin Penting"
    AI generatif memprediksi kata atau elemen berikutnya yang paling mungkin berdasarkan pola statistik, bukan mengambil dari basis data fakta yang selalu benar. Inilah sebabnya verifikasi hasil AI tetap penting.

## GenAI Prompt Guide
Prompt adalah pesan atau instruksi yang kita sampaikan kepada GenAI

- Berikan prompt berupa pertanyaan atau instruksi yang jelas. Sebagai contoh, jika Anda ingin GenAI menuliskan cerita singkat, maka berikan prompt "Tuliskan cerita singkat tentang ...". Berikan prompt yang deskriptif dan rinci untuk memperbaiki output GenAI
- Berikan instruksi untuk output yang diinginkan, seperti format yang diberikan apakah .json, .txt, apakah berupa paragraf atau esai panjang, tulis juga jika memiliki word count. Misal, jika Anda menginginkan GenAI menulis esai tentang Pulau Seribu dibatasi 1000 kata, maka berikan prompt "Buatkan esai tentang Pulau Seribu yang dibatasi hanya 1000kata"
- Klarifikasi untuk target pembaca dari output yang dihasilkan GenAI
- 

---

**Lanjut ke:** [Bab 3 — Sejarah Singkat AI](bab3-sejarah-ai.md)
