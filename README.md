# Model Machine Learning Score Card

## Tujuan

Model ini bertujuan untuk memprediksi apakah seorang nasabah akan mengalami kesulitan pembayaran pinjaman (default) atau tidak.

## Data

Data yang digunakan adalah data nasabah Home Credit Indonesia. Data tersebut ialah  : <br>

**application_{train|test}.csv**: File utama yang berisi informasi tentang setiap aplikasi pinjaman. <br>
**bureau.csv:** Menyimpan informasi tentang semua pinjaman sebelumnya yang dimiliki klien dari lembaga keuangan lain yang dilaporkan ke Biro Kredit. <br>
**credit_card_balance.csv:** Menyimpan snapshot saldo bulanan kartu kredit sebelumnya yang dimiliki pemohon dengan Home Credit. <br>
**previous_application.csv:** Menyimpan semua pengajuan pinjaman Home Credit sebelumnya dari klien yang memiliki pinjaman <br>
klik [tautan ini](https://drive.google.com/drive/folders/1BdF6LSNWzir1KEpHY6bx7ZZFawpxTimK?usp=sharing) untuk mengunduh dataset

## Fitur

Fitur-fitur yang digunakan adalah sebagai berikut:

- Lamanya bekerja
- Perubahan nomor telepon
- Sumber informasi kredit
- Besarnya angsuran bulanan 
- Usia
- Lamanya memiliki kartu identitas
- Pendapatan total

Target dari model ini adalah apakah nasabah akan mengalami kesulitan pembayaran pinjaman (default) atau tidak. Target diubah menjadi biner, yaitu 1 untuk default dan 0 untuk tidak default.

## Model

Model yang digunakan adalah LightGBM. Model ini dipilih karena performanya yang baik untuk data imbalanced.

## Evaluasi

Model dievaluasi menggunakan ROC AUC. ROC AUC adalah metrik yang mengukur kemampuan model untuk membedakan antara kelas positif dan kelas negatif.

## Hasil

Hasil evaluasi menunjukkan bahwa model memiliki ROC AUC sebesar 0,97. Hal ini menunjukkan bahwa model dapat memprediksi apakah nasabah akan mengalami kesulitan pembayaran pinjaman dengan akurasi yang cukup baik.

Penggunaan

Model ini dapat digunakan untuk memprediksi apakah seorang nasabah akan mengalami kesulitan pembayaran pinjaman. Model ini dapat digunakan oleh lembaga keuangan untuk menentukan apakah nasabah layak untuk diberikan pinjaman.

Pustaka yang digunakan

````python
import pandas as pd
import scipy
import numpy as np
from sklearn.preprocessing import MinMaxScaler
import seaborn as sns
import matplotlib.pyplot as plt
import math
from sklearn.ensemble import RandomForestClassifier
from lightgbm import LGBMClassifier
from sklearn.metrics import roc_auc_score
from sklearn.metrics import confusion_matrix
````

Untuk menjalankan model, buka file Data_Preprocessing.ipynb dan Modelling.ipynb File tersebut berisi kode untuk mempersiapkan data, melatih model, dan mengevaluasi model.

Kesimpulan

Model machine learning score card ini dapat digunakan untuk memprediksi apakah seorang nasabah akan mengalami kesulitan pembayaran pinjaman. Model ini memiliki akurasi yang cukup baik, yaitu 0,97.
