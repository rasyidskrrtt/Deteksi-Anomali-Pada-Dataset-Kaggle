# 🚀 Deteksi Anomali pada Dataset Cybersecurity Logs

Proyek ini bertujuan untuk **mendeteksi aktivitas anomali** pada log keamanan sistem menggunakan algoritma **Decision Tree** dan **Random Forest**. Dataset yang digunakan adalah **Synthetic Cybersecurity Logs for Anomaly Detection** dari Kaggle.

---

## 📂 Dataset
Dataset yang digunakan berisi **10.000 baris log keamanan** dengan atribut:
- `Timestamp` → waktu request
- `IP_Address` → alamat IP pengguna
- `Request_Type` → jenis request (GET, POST, DELETE, dsb)
- `Status_Code` → kode status hasil request (200, 404, 500, dsb)
- `User_Agent` → perangkat/browser
- `Session_ID` → identitas sesi pengguna
- `Location` → lokasi pengguna
- `Anomaly_Flag` → label target (0 = normal, 1 = anomali)

📌 Sumber dataset: [Kaggle – Synthetic Cybersecurity Logs](https://www.kaggle.com/datasets/fcwebdev/synthetic-cybersecurity-logs-for-anomaly-detection)

---

## ⚙️ Preprocessing
1. **Pemeriksaan Missing Values** → memastikan tidak ada data kosong.  
2. **Encoding Variabel Kategorikal** → one-hot encoding untuk kolom `IP_Address`, `Request_Type`, `Location`, dsb.  
3. **Split Data** → 70% training, 30% testing.  

---

## 🧠 Algoritma yang Digunakan
- **Decision Tree** → sederhana, interpretatif, tetapi rawan overfitting.  
- **Random Forest** → ensemble learning, lebih stabil & akurat dibanding satu pohon keputusan.  

---

## 📊 Hasil Analisis
### 🔹 Decision Tree
- Accuracy: **0.95**  
- Precision: **0.94**  
- Recall: **0.96**  
- F1-score: **0.95**

### 🔹 Random Forest
- Accuracy: **0.98**  
- Precision: **0.98**  
- Recall: **0.98**  
- F1-score: **0.98**

📈 **Visualisasi yang dihasilkan:**
- Distribusi anomali vs normal (pie chart)  
- Distribusi Status Code & Request Type  
- Tren anomali per hari  
- Confusion Matrix (Decision Tree & Random Forest)  
- Feature Importance  

---

## 📦 Instalasi
Clone repository dan install dependencies:

```bash
git clone https://github.com/rasyidskrrtt/Deteksi-Anomali-Pada-Dataset-Kaggle.git
cd Deteksi-Anomali-Pada-Dataset-Kaggle
pip install -r requirements.txt
