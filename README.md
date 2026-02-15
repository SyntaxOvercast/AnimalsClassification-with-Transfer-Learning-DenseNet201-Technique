# 🐾 Animal Image Classification using Transfer Learning (DenseNet201)

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://www.tensorflow.org/)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-green.svg)](https://www.kaggle.com/datasets/antobenedetti/animals)

## 📖 Deskripsi Proyek
Proyek ini bertujuan untuk mengklasifikasikan gambar hewan ke dalam 5 kategori berbeda menggunakan teknik *Deep Learning*. Dengan memanfaatkan **Transfer Learning** menggunakan arsitektur **DenseNet201**, model ini mampu mengenali pola visual yang kompleks dengan akurasi tinggi.

---

## 📊 Dataset
Dataset yang digunakan berasal dari **Kaggle: antobenedetti/animals**. Data telah melalui proses *filtering* untuk memastikan kualitas dan keseimbangan kelas.

| Kelas Hewan | Jumlah Gambar |
| :--- | :--- |
| Cat | 3,037 |
| Elephant | 2,992 |
| Lion | 2,936 |
| Dog | 2,927 |
| Horse | 2,754 |
| **Total** | **14,646** |

---

## 🏗️ Arsitektur Model
Kami menggunakan pendekatan *Transfer Learning*. DenseNet201 digunakan sebagai *feature extractor* (pre-trained weight dari ImageNet), yang kemudian diikuti oleh *custom classifier* untuk menyesuaikan dengan dataset spesifik ini.

**Detail Struktur:**
1.  **Base Model:** DenseNet201 (Frozen)
2.  **Custom Layers:**
    * Conv2D
    * BatchNormalization
    * LeakyReLU
    * GlobalAveragePooling2D
    * Dense (Hidden)
    * Dropout (Regularization)
    * Dense (Output - Softmax)

---

## 📈 Evaluasi Model
Model menunjukkan performa yang sangat baik dengan tingkat *overfitting* yang minimal.

### Metrik Performa

| Metrik | Nilai |
| :--- | :--- |
| **Accuracy** | 96.96% |
| **Precision** | 97.02% |
| **Recall** | 96.96% |
| **F1-Score** | 96.96% |

### Log Pelatihan
* **Training Loss:** 0.4858 | **Accuracy:** 96.94%
* **Validation Loss:** 0.4725 | **Accuracy:** 96.65%
* **Testing Loss:** 0.4741 | **Accuracy:** 96.96%

---
