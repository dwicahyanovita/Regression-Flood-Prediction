# Flood Prediction Regression

## Deskripsi Proyek
Proyek ini bertujuan untuk membangun model regresi untuk memprediksi kemungkinan terjadinya banjir (*FloodProbability*) berdasarkan berbagai karakteristik seperti *MoonsoonIntensity*, *TopographyDrainage*, *RiverManagement*, dan fitur-fitur lainnya.

Dataset sebelum dibersihkan berisi **1.117.957 baris data dengan 22 kolom**, terdiri dari **20 fitur input** dan **1 target** (`FloodProbability`). Sedangkan setelah dibersihkan, dataset berisi **845.886 baris data**. Data ini dibagi menjadi **676.708 baris data latih** dan **169.178 baris data uji** untuk pelatihan dan pengujian model.

## Model yang Dievaluasi
Berikut ini model regresi yang dievaluasi beserta hasil metrik evaluasinya:

| Model                         | MAE        | MSE        | R²         |
|-------------------------------|------------|------------|------------|
| Lars                          | 0.806497   | 0.998246   | 0.000764   |
| Linear Regression             | 0.329142   | 0.171296   | 0.828534   |
| GradientBoostingRegressor     | 0.512672   | 0.380491   | 0.619132   |

## Analisis Hasil

- **Lars (Least Angle Regression):**  
  Lars menunjukkan performa yang buruk dengan MAE dan MSE yang tinggi serta R² mendekati nol, sehingga model ini tidak direkomendasikan untuk kasus ini.

- **Linear Regression:**  
  Linear Regression memberikan hasil terbaik dengan MAE dan MSE terendah, serta nilai R² sebesar 82,8%, yang menunjukkan model ini mampu menjelaskan sebagian besar variasi data target.

- **GradientBoostingRegressor:**  
  Model ini menunjukkan performa yang cukup baik, namun masih berada di bawah Linear Regression dalam hal akurasi prediksi.

## Kesimpulan
Model **Linear Regression** adalah pilihan terbaik dalam proyek ini berdasarkan evaluasi performa, dengan akurasi tinggi dan kesalahan prediksi yang rendah. Lars tidak disarankan untuk digunakan, sedangkan Gradient Boosting bisa menjadi alternatif cadangan.

## 💡 Kredit
Dwi Cahya Novita. Proyek ini adalah bagian dari kursus **Machine Learning untuk Pemula** yang diselenggarakan oleh **Dicoding**.

---
