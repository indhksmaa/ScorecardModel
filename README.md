# Machine Learning Scorecard Model
## Overview

Repositori ini berisi implementasi machine learning scorecard model#. Model ini dirancang untuk menilai dan memprediksi kemungkinan kesulitan pembayaran berdasarkan fitur-fitur masukan. 
File README ini menyediakan informasi tentang cara menggunakan, melatih, dan mengevaluasi model tersebut.

## Table of Contents
1. Installation
2. Usage
3. Data
4. Training
5. Evaluation
6. Model Details
7. Results
8. Contributing
9. License
## Installation
To install the necessary dependencies, run the following command:
```
pip install -r requirements.txt
```

## Usage
1. Import Model
Untuk memasang dependensi yang diperlukan, jalankan perintah berikut:

```
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, roc_auc_score
from sklearn.model_selection import cross_validate
from sklearn.linear_model import LogisticRegression
from xgboost import XGBClassifier
from lightgbm import LGBMClassifier
```

2. Membuat Fungsi Evaluasi Classification
