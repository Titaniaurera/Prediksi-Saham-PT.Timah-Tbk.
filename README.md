# Prediksi Harga Saham AAPL (2019-2027)

Proyek ini bertujuan untuk memprediksi harga saham Apple (AAPL) menggunakan tiga model forecasting: **Metode Naif**, **ARIMA**, dan **LSTM**. Dataset mencakup periode 2019 hingga 2024, dengan evaluasi model berdasarkan **Root Mean Square Error (RMSE)**. Hasil analisis menunjukkan bahwa **model LSTM memberikan performa paling fit untuk prediksi harga saham AAPL** dibandingkan dengan metode lainnya. Model LSTM juga diperluas untuk memprediksi harga saham hingga tahun 2027.

## 📈 Model yang Digunakan

### 1. **Metode Naif**  
- Prediksi sederhana berdasarkan nilai terakhir yang diamati.  
- Digunakan sebagai baseline model untuk membandingkan performa.  
- **Evaluasi**: RMSE menunjukkan metode ini cocok untuk prediksi jangka pendek, namun kurang akurat untuk jangka panjang.  

### 2. **ARIMA (AutoRegressive Integrated Moving Average)**  
- Melibatkan analisis stasioneritas menggunakan uji Augmented Dickey-Fuller.  
- Differencing diterapkan untuk mengatasi data yang tidak stasioner.  
- Optimasi parameter ARIMA dilakukan dengan `auto_arima` dari pustaka `pmdarima`.  
- **Hasil**: Model memberikan prediksi yang cukup baik untuk jangka pendek, tetapi performanya menurun pada data dengan volatilitas tinggi.  

### 3. **LSTM (Long Short-Term Memory)**  
- Model jaringan saraf yang dirancang untuk data time series dengan dependensi jangka panjang.  
- Data dinormalisasi menggunakan MinMaxScaler untuk meningkatkan akurasi prediksi.  
- **Hasil Evaluasi**: LSTM menunjukkan RMSE terendah, membuktikan kemampuannya untuk memodelkan pola kompleks.  
- Prediksi diperluas hingga tahun 2027 dengan tingkat akurasi yang tetap tinggi.  

## 📊 Sorotan Visualisasi
- Perbandingan data aktual, pelatihan, pengujian, dan prediksi dari ketiga model.  
- Visualisasi prediksi jangka panjang LSTM hingga tahun 2027.  
- Plot residual dan distribusi error untuk ARIMA dan LSTM.  

## 🚀 Fitur Utama
- **Sumber Data**: Harga saham AAPL diambil dari Yahoo Finance menggunakan pustaka `yfinance`.  
- **Pra-Pemrosesan Data**: Penanganan data tidak stasioner, differencing, pembagian dataset, dan normalisasi untuk LSTM.  
- **Evaluasi**: RMSE sebagai metrik utama kinerja model.  

## 🛠️ Alat & Pustaka
- `yfinance`  
- `pandas`, `numpy`  
- `matplotlib`, `seaborn`  
- `statsmodels`  
- `pmdarima`  
- `scikit-learn`  
- `tensorflow` (untuk model LSTM)  

## 🔮 Hasil & Kesimpulan
- LSTM menghasilkan prediksi paling akurat untuk harga saham AAPL, dengan kemampuan untuk menangkap pola jangka panjang.  
- Model Naif dan ARIMA cocok untuk analisis awal atau prediksi sederhana, tetapi kurang efektif dalam skenario yang lebih kompleks.  
- Model ini dapat diperluas untuk menganalisis saham lain, mengintegrasikan faktor makroekonomi, atau menggabungkan model hybrid untuk prediksi yang lebih baik.  

## 📂 Struktur Repository
- `notebooks/`: Notebook Jupyter untuk implementasi model.  
- `models/`: Model LSTM yang disimpan dalam format `.h5` untuk penggunaan di masa depan.  
- `data/`: Dataset yang telah diproses.  
- `results/`: Grafik hasil analisis dan evaluasi model.
