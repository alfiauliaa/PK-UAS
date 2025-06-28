📌 Case-Based Reasoning untuk Prediksi Amar Putusan Fidusia
Repositori ini berisi kode, dataset, dan notebook untuk Sistem Case-Based Reasoning (CBR) yang digunakan untuk retrieval kasus dan prediksi amar putusan pada perkara jaminan fidusia.

📂 Struktur Folder
bash
Salin
Edit
/data/                # Folder berisi dataset mentah & hasil cleaning
/notebooks/           # Folder berisi 5 notebook: scraping → evaluasi
README.md             # Petunjuk eksekusi
requirements.txt      # Library dependencies
✅ Isi Notebook
Notebook	Deskripsi
01_scraping_cleaning.ipynb	Tahap 1 & 2: Scraping putusan dari Direktori MA, simpan PDF, cleaning teks
02_case_representation.ipynb	Tahap 2 lanjutan: Representasi metadata, validasi teks, simpan hasil
03_case_retrieval.ipynb	Tahap 3: Vectorisasi TF-IDF & IndoBERT, retrieve top-k kasus mirip, SVM/Naive Bayes
04_solution_reuse.ipynb	Tahap 4: Prediksi Amar Putusan pakai voting IndoBERT
05_evaluation.ipynb	Tahap 5: Evaluasi retrieval & classification, simpan metrik

⚙️ Persyaratan
Python:
Python ≥ 3.8

Jalankan di Google Colab atau lokal dengan GPU untuk IndoBERT

Libraries:
Buat file requirements.txt seperti:

nginx
Salin
Edit
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
🚀 Cara Menjalankan
1️⃣ Clone repo

bash
Salin
Edit
git clone https://github.com/username/repo-fidusia-cbr.git
cd repo-fidusia-cbr
2️⃣ Instal dependency

bash
Salin
Edit
pip install -r requirements.txt
Atau buka notebook di Google Colab, lalu jalankan cell instalasi di setiap notebook jika perlu.

3️⃣ Eksekusi pipeline

Mulai dari 01_scraping_cleaning.ipynb

Lanjutkan hingga 05_evaluation.ipynb

Setiap tahap akan menghasilkan file output di /data/

💡 Contoh Eksekusi
Scraper otomatis akan mendownload PDF dan menyimpan CSV.

03_case_retrieval.ipynb akan menampilkan top-5 hasil kemiripan.

05_evaluation.ipynb menyimpan metrik evaluasi di /data/eval/.

📚 Catatan
Dataset putusan diambil dari putusan3.mahkamahagung.go.id

Model IndoBERT dari indobenchmark/indobert-base-p1

