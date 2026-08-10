# Teknik Prompting Dasar

## Apa Itu Prompt?

**Prompt** adalah instruksi, pertanyaan, atau permintaan yang Anda berikan kepada AI. Kualitas prompt sangat memengaruhi kualitas jawaban yang dihasilkan — inilah sebabnya kemampuan menyusun prompt yang baik menjadi keterampilan penting dalam literasi AI praktis.

## Prinsip Dasar Prompt yang Baik

### 1. Jelas dan Spesifik

Semakin jelas instruksi Anda, semakin relevan hasilnya.

| Prompt Kurang Baik | Prompt Lebih Baik |
|---|---|
| "Buatkan tulisan tentang kucing" | "Buatkan artikel 300 kata tentang cara merawat kucing anggora untuk pemula, dengan gaya bahasa santai" |
| "Bantu saya belajar Excel" | "Jelaskan cara menggunakan rumus VLOOKUP di Excel dengan contoh data sederhana, untuk pemula" |

### 2. Berikan Konteks

Sertakan informasi latar belakang yang relevan agar AI memahami situasi Anda.

> Contoh: "Saya seorang guru SD yang ingin membuat kuis matematika sederhana untuk siswa kelas 3. Buatkan 5 soal penjumlahan dengan angka di bawah 100."

### 3. Tentukan Format Output

Jika Anda menginginkan hasil dalam bentuk tertentu, sebutkan secara eksplisit.

> Contoh: "Buat dalam bentuk tabel dengan kolom: Nama, Fungsi, Contoh Penggunaan."

### 4. Berikan Contoh (Few-shot Prompting)

Memberikan satu atau dua contoh format yang diinginkan dapat membantu AI menghasilkan output yang lebih sesuai harapan.

### 5. Minta AI Berpikir Bertahap

Untuk pertanyaan yang kompleks atau membutuhkan penalaran, minta AI menjelaskan langkah-langkahnya.

> Contoh: "Jelaskan langkah demi langkah cara menghitung persentase keuntungan dari data penjualan berikut..."

### 6. Iterasi dan Perbaiki

Jangan berhenti di jawaban pertama. Berikan umpan balik untuk memperbaiki hasil.

> Contoh lanjutan: "Ini bagus, tapi tolong buat lebih singkat dan gunakan bahasa yang lebih formal."

## Kerangka Prompt Sederhana: T-K-F-N

Kerangka ini dapat membantu Anda menyusun prompt secara terstruktur:

- **T — Tugas**: Apa yang Anda ingin AI lakukan?
- **K — Konteks**: Informasi latar belakang apa yang relevan?
- **F — Format**: Bagaimana bentuk output yang diinginkan?
- **N — Nada/Gaya**: Gaya bahasa atau nada seperti apa yang diinginkan?

**Contoh penerapan:**

> "**Tugas**: Buatkan draf email permintaan cuti. **Konteks**: Saya karyawan yang ingin cuti 3 hari untuk urusan keluarga, mulai Senin depan. **Format**: Email formal dengan salam pembuka dan penutup. **Nada**: Sopan dan profesional."

## Kesalahan Umum dalam Prompting

- Terlalu singkat dan ambigu sehingga AI harus menebak maksud Anda
- Meminta terlalu banyak hal sekaligus dalam satu prompt
- Tidak memberikan contoh saat format output penting
- Langsung menerima jawaban pertama tanpa verifikasi atau iterasi

!!! tip "Latihan Praktis"
    Coba tulis ulang prompt "Bantu saya buat rencana bisnis" menjadi prompt yang lebih spesifik menggunakan kerangka T-K-F-N di atas.

---

**Lanjut ke:** [AI untuk Produktivitas](ai-untuk-produktivitas.md)
