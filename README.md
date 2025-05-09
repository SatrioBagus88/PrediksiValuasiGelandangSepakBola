
# **Prediksi Valuasi Pemain Sepak Bola Posisi Gelandang Serang (CAM)**

### Disclaimer
1. *Project ini merupakan tugas pembelajaran dalam modul Machine Learning di Purwadhika Digital Technology School.*
2. *Seluruh kode ditulis menggunakan Python dan penjelasan tersedia dalam Bahasa Indonesia.*
3. *Data yang digunakan merupakan data publik dari SoFIFA dan tidak digunakan untuk keperluan komersial.*
4. *Segala nama pemain, klub, dan atribut dalam data merujuk pada data yang tersedia secara terbuka dan tidak bermaksud melanggar hak cipta.*

---

### Tentang Project

Dalam dunia sepak bola modern, valuasi pemain sangat penting dalam aktivitas transfer dan perencanaan strategi tim. Dengan banyaknya atribut performa yang tersedia, pendekatan berbasis *machine learning* menjadi solusi objektif untuk memprediksi nilai pasar pemain.

Project ini berfokus pada pemain dengan posisi **Central Attacking Midfielder (CAM)**, dengan tujuan:
- Memprediksi nilai pasar pemain berdasarkan atribut teknis, fisik, dan mental.
- Mengidentifikasi fitur paling berpengaruh dalam penentuan valuasi.
- Menghasilkan model prediktif yang dapat digunakan oleh klub atau analis sepak bola.

---

### Dataset

Data diambil dari **SoFIFA** dengan format `.csv`. Dataset mencakup:
- Informasi dasar pemain (umur, posisi, tinggi, berat).
- Atribut kemampuan seperti: passing, shooting, dribbling, pace, stamina.
- Data valuasi (nilai pasar dalam Euro) sebagai target prediksi.

---

### Fitur Utama Program
- Preprocessing dan imputasi data yang hilang.
- Feature engineering dan eliminasi multikolinearitas.
- Pemilihan model terbaik (RandomForest, XGBoost, dll) berdasarkan performa regresi.
- Evaluasi menggunakan metrik RMSE, MAE, dan MAPE.
- Interpretasi model menggunakan **SHAP** untuk mengetahui fitur paling berpengaruh.
- Penyimpanan model menggunakan `joblib`.

---

### Library yang Digunakan

- `pandas`, `numpy`: manipulasi data
- `seaborn`, `matplotlib`: visualisasi
- `scikit-learn`: preprocessing, modeling, evaluasi
- `xgboost`: boosting model
- `shap`: interpretabilitas model
- `joblib`: menyimpan dan memuat model

---

### Menyimpan dan Memuat Model

```python
# Menyimpan model
from joblib import dump, load
dump(model, 'model_cam_predictor.joblib')

# Memuat model
model = load('model_cam_predictor.joblib')
```

---

### Kekurangan dan Potensi Pengembangan

- Data hanya mencakup satu posisi pemain.
- Belum dilakukan validasi pada data musim yang berbeda.
- Belum terintegrasi dengan *real-time API* seperti Transfermarkt atau Sofascore.
- Potensi untuk membuat dashboard interaktif.

---

### Kesimpulan

Project ini membuktikan bahwa dengan pendekatan machine learning, valuasi pemain sepak bola dapat diprediksi secara lebih objektif dan berbasis data. Program ini diharapkan dapat dikembangkan lebih lanjut untuk skala yang lebih luas.

---

**Dibuat oleh Satrio Bagus Prabowo**
