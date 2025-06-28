# 📌 Case-Based Reasoning untuk Prediksi Amar Putusan Fidusia

Repositori ini berisi **kode, dataset, dan notebook** untuk Sistem **Case-Based Reasoning (CBR)** yang digunakan untuk _retrieval_ kasus dan prediksi _amar putusan_ pada perkara jaminan fidusia.

---

## 📂 Struktur Folder

```
/data/              # Berisi dataset mentah & hasil cleaning
/notebooks/         # Berisi 5 notebook: scraping → evaluasi
README.md           # Petunjuk eksekusi
requirements.txt    # Daftar dependensi Python
```

---

## 🗂️ Deskripsi Notebook

| Notebook                       | Deskripsi                                                                           |
| ------------------------------ | ----------------------------------------------------------------------------------- |
| `01_scraping_cleaning.ipynb`   | Tahap 1 & 2: Scraping putusan dari Direktori MA, simpan PDF, cleaning teks          |
| `02_case_representation.ipynb` | Tahap 2 lanjutan: Representasi metadata, validasi teks                              |
| `03_case_retrieval.ipynb`      | Tahap 3: Vektorisasi TF-IDF & IndoBERT, retrieve top-k kasus mirip, SVM/Naive Bayes |
| `04_solution_reuse.ipynb`      | Tahap 4: Prediksi Amar Putusan pakai voting IndoBERT                                |
| `05_evaluation.ipynb`          | Tahap 5: Evaluasi retrieval & classification, simpan metrik                         |

---

## ⚙️ Requirements

- Python >= 3.8
- Disarankan jalankan di Google Colab atau lokal dengan GPU (untuk IndoBERT)

**Dependencies (requirements.txt):**

```
pandas
numpy
scikit-learn
transformers
torch
nltk
pdfminer.six
beautifulsoup4
lxml
requests
```

---

## 🚀 Cara Menjalankan

1️⃣ **Clone repo**

```bash
git clone https://github.com/alfiauliaa/PK-UAS
cd repo-fidusia-cbr
```

2️⃣ **Install dependencies**

```bash
pip install -r requirements.txt
```

3️⃣ **Buka notebook secara berurutan**

- Jalankan `01_scraping_cleaning.ipynb` → `02_case_representation.ipynb` → `03_case_retrieval.ipynb` → `04_solution_reuse.ipynb` → `05_evaluation.ipynb`.

4️⃣ Hasil evaluasi akan disimpan di `/data/eval/` sebagai file `.csv`.

---

## 📧 Kontak

**Nama:** [Nama Kamu]  
**Email:** [Email Kamu]  
**Repo:** [https://github.com/username/repo-fidusia-cbr](https://github.com/username/repo-fidusia-cbr)

---

_Silakan disesuaikan dengan kebutuhan tugas & upload ke LMS!_
