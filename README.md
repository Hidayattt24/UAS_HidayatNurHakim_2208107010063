---

# 📝 Intelligent Email Writer for Students

Aplikasi web yang membantu mahasiswa menulis email secara otomatis, profesional, dan efisien dengan dukungan **Large Language Model (LLM)** dari **Gemini API**.

---

## 📦 Fitur Utama

* ✅ Pilihan kategori email: Akademik, Skripsi, Magang, dan lainnya.
* ✅ Penyesuaian nada penulisan: Formal, Netral, atau Santai.
* ✅ Mendukung dua bahasa: Indonesia dan Inggris.
* ✅ Input poin-poin utama yang ingin disampaikan.
* ✅ Output email yang profesional, ringkas, dan sesuai konteks.

---

## 📁 Struktur Proyek

```
intelligent_email_writer/
├── .env                   # Berisi API Key Gemini (jangan dibagikan)
├── .env.example           # Template konfigurasi untuk publik
├── app.py                 # Frontend berbasis Streamlit
├── backend/
│   └── main.py            # Backend API menggunakan FastAPI
├── requirements.txt       # Dependensi backend
├── requirements_frontend.txt # Dependensi frontend (opsional)
```

---

## ⚙️ Cara Instalasi & Menjalankan Proyek

### 1. Kloning Repository

```bash
git clone https://github.com/username/intelligent_email_writer.git
cd intelligent_email_writer
```

### 2. Menyiapkan Environment & Backend (FastAPI)

```bash
# Buat dan aktifkan virtual environment
python -m venv env
# Aktifkan:
# - Windows
env\Scripts\activate
# - Linux/macOS
source env/bin/activate

# Instal dependensi backend
pip install -r requirements.txt

# Jalankan server FastAPI
uvicorn backend.main:app --reload --host 0.0.0.0 --port 8000
```

### 3. Menjalankan Frontend (Streamlit)

Buka terminal baru (jangan lupa aktifkan environment jika belum):

```bash
streamlit run app.py
```

---

## 🔐 Konfigurasi API Key Gemini

1. Kunjungi: [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Klik **Create API Key**.
3. Simpan API key ke dalam file `.env` di root proyek:

```env
GEMINI_API_KEY=your_api_key_here
```

> **Catatan:** Jangan pernah commit file `.env` ke GitHub. Gunakan `.env.example` sebagai panduan umum.

---

## 📄 Membuat File .env dari Template

Untuk memulai, salin file template:

```bash
cp .env.example .env
```

Lalu isi dengan konfigurasi sesuai kebutuhan (misalnya API key).

---

## 📬 Contoh Penggunaan Aplikasi

1. Pilih kategori dan gaya bahasa email.
2. Masukkan informasi penerima, subjek, dan poin-poin penting.
3. Klik **"Buat Email"**.
4. Hasil generate akan tampil di halaman utama.

---

