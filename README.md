# Aldo_2457201002355_SVM_kelulusan
# Prediksi Kelulusan Mahasiswa SVM

## 1. Judul Proyek
**Prediksi Kelulusan Mahasiswa Menggunakan Support Vector Machine (SVM)**

---

## 2. Deskripsi Dataset
Dataset ini berisi atribut mahasiswa, termasuk Indeks Prestasi (IPS/IPK) dan data demografis, yang digunakan untuk memprediksi status kelulusan.
- **File Data:** `datakelulusanmahasiswa.csv`
- **Target Variabel:** STATUS KELULUSAN (TEPAT atau TERLAMBAT)

---

## 3. Tahapan Pengerjaan

Proyek ini diselesaikan melalui tahapan berikut:
1.  **Preprocessing:** Feature Scaling menggunakan `StandardScaler` (Wajib untuk SVM), dan One-Hot Encoding untuk variabel kategorikal.
2.  **Model Training:** Pelatihan model SVM dengan Hyperparameter Tuning menggunakan `GridSearchCV` untuk mencari kombinasi terbaik antara kernel (`linear`, `rbf`) dan parameter `C`, `gamma`.
3.  **Evaluasi:** Menggunakan Confusion Matrix dan Classification Report (Accuracy, Precision, Recall, F1-Score).
4.  **Deployment Sederhana:** Pembuatan fungsi Python untuk prediksi input data baru.

---

## 4. Hasil Utama Pemodelan (Bagian D & E)

### 4.1 Parameter Terbaik SVM
| Metrik | Nilai Terbaik |
| :--- | :--- |
| **Kernel Terbaik** | **linear** |
| **Nilai C Terbaik** | **10** |
| **Nilai Gamma Terbaik** | **scale** |

### 4.2 Metrik Kinerja (Test Set)
| Metrik | Nilai |
| :--- | :--- |
| **Akurasi Model** | **91%** |
| **Precision (Kelas TEPAT)** | 0.95 |
| **F1-Score (Kelas TEPAT)** | 0.91 |

### 4.3 Analisis Kunci (Interpretasi Model)
1.  **Dominasi Fitur:** Fitur **IPK** dan **IPS** menunjukkan korelasi terkuat dengan status kelulusan. Semakin tinggi IPK, semakin besar probabilitas prediksi **TEPAT** waktu.
2.  **Keputusan Model:** Kernel **Linear** terpilih. Hal ini menyimpulkan bahwa data mahasiswa **dapat dipisahkan secara linear** (atau hampir linear) di ruang fitur yang ada, sehingga *hyperplane* garis lurus sudah cukup untuk melakukan klasifikasi dengan akurasi optimal.
2.  **Keputusan Model:** Kernel **[RBF/Linear]** terpilih, yang menyimpulkan bahwa data **tidak** linearly separable, sehingga memerlukan *trick* kernel / **dapat** dipisahkan secara linear di ruang fitur.

---

## 5. Cara Menjalankan Proyek
Proyek ini sepenuhnya dijalankan menggunakan Google Colab, dengan asumsi Google Drive sudah terhubung (Mounted).
1. Struktur Repositori: Pastikan file data (`datakelulusanmahasiswa.csv`) berada di dalam folder /data pada repositori yang di-clone.
2.  Akses Notebook: Buka file Notebook (`Aldo_2457201002355_SVM_kelulusan.ipynb`) melalui Google Colab.
3.  Eksekusi Kode: Jalankan semua cell kode secara berurutan, dimulai dari Bagian A (Setup & Loading Data).
4.  Sistem akan secara otomatis meminta otorisasi untuk Mount Google Drive di awal.
5.  Verifikasi Hasil: Hasil analisis model, Confusion Matrix, dan Classification Report akan tercetak langsung di bawah cell Bagian D.
6.  Jalankan Cell berurutan.

---

## 6. Identitas Mahasiswa

- **Nama Mahasiswa:** ALDO
- **NIM:** 2457201002355
- **Prodi:** Sistem Informasi 3A 
