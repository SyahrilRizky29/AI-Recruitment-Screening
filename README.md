# 🤖 AI-Recruitment-Screening

Sistem otomasi screening CV pelamar kerja menggunakan **n8n** dan **AI (Gemini/Groq)**. Workflow ini mengubah dokumen PDF yang tidak terstruktur menjadi data penilaian kandidat yang terstruktur secara otomatis.

---

## 🚀 Fitur Utama
*   **PDF Ingestion**: Menerima unggahan CV format PDF melalui n8n Form Trigger.
*   **Binary Processing**: Konversi file ke Base64 dan pemberian timestamp otomatis (Luxon).
*   **Automated Extraction**: Ekstraksi teks mentah dari dokumen PDF secara sistemik.
*   **AI Analysis**: Penilaian profil, skill, dan pemberian skor (0-100) menggunakan LLM.
*   **JSON Validation**: Pembersihan output AI menggunakan logika JavaScript (try-catch) agar data valid.
*   **Telegram Notification**: Pengiriman hasil ringkasan screening langsung ke Telegram HRD.

---

## 🛠️ Alur Kerja (Workflow)
1.  **Form Input**: Kandidat mengisi data dan mengunggah CV PDF.
2.  **Code Node (Base64)**: Memproses file biner dan mencatat waktu pendaftaran.
3.  **Extract Node**: Mengubah isi PDF menjadi teks yang bisa dibaca AI.
4.  **LLM Chain**: AI menganalisis kecocokan kandidat berdasarkan teks CV.
5.  **Data Cleaning**: Node JavaScript memastikan output AI bersih dari format Markdown.
6.  **Output**: Notifikasi dikirimkan ke Telegram bot.

---

## ⚙️ Persiapan
*   **Kredensial**: API Key AI (Gemini/Groq) dan Bot Token Telegram.
*   **n8n**: Import file `.json` workflow ke dalam instance n8n Anda.
*   **Spreadsheet**: (Opsional) Tambahkan node Google Sheets jika ingin mengarsipkan data.

---
