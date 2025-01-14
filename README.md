1. Judul : Penerapan Algoritma Regresi Linear Untuk Prediksi Harga Mobil Bekas
Nama : Dimas Bhagaskoro Prijambodo
NiM : A11.2022.14471
Kelompok : Data Mining A11.4507

2. Ringkasan 
Praktik bisnis jual beli mobil bekas banyak dilakukan oleh masyarakat indonesia, hal ini terdorong karena harga mobil baru yang semakin hari semakin meningkat.
Banyak faktor yang mempengaruhi harga mobil baru menjadi mahal, salah satunya adalah melemahnya nilai rupiah. 
Namun dalam jual beli mobil bekas terkadang menimbulkan masalah baru, yaitu tidak kesesuaian harga mobil dengan kondisi fisik mobil tersebut sehingga dapat merugikan bagi pembeli.

Tujuan yang akan dicapai
Pendekatan pemecahan masalah. Untuk mengatasi permasalahan tersebut, penelitian akan mengusulkan pemanfaatan metode penambangan data 
algoritma regresi linear dengan dataset data tabular untuk menentukan kelayakan harga mobil bekas. 

3. Penjelasan Dataset

Dataset berisikan 
Data columns (total 8 columns):
 #   Column        Non-Null Count   Dtype  
---  ------        --------------   -----  
 0   model         108540 non-null  object 
 1   year          108540 non-null  int64  
 2   price         108540 non-null  int64  
 3   transmission  108540 non-null  object 
 4   mileage       108540 non-null  int64  
 5   fuelType      108540 non-null  object 
 6   engineSize    108540 non-null  float64
 7   brand         108540 non-null  object 
dtypes: float64(1), int64(3), object(4)
Target: Variabel yang ingin diprediksi.
Eksplorasi Data:

Analisis distribusi fitur menggunakan histogram atau boxplot.
Pengecekan nilai yang hilang missing values: ditemukan jumlah missing values.
Korelasi antara fitur dan target:
Fitur dengan korelasi tertinggi: Nama fitur dan nilai korelasi.
Proses Feature:

Handling Missing Values: Mengisi nilai yang hilang dengan metode mean, median, mode, dll.
Encoding: Fitur kategorikal diubah menjadi numerik menggunakan one-hot encoding/label encoding.
Scaling: Data diskalakan menggunakan StandardScaler, MinMaxScaler.
Feature Selection: Dipilih jumlah fitur yang paling signifikan untuk model.

4. Proses Modelling
Dalam eksperimen ini melakukan ujicoba hanya menggunakan 1 metode yaitu metode regresi linear. 
pada proses pemodelan dataset akan dipilih yang memiliki value non non numerik/kategorikal kemudian diubah menjadi data numerik dengan menggunakan library pandas. 
data kategorikal yang dimaksud adalah model, transmission, fuel type, dan brand. kemudian data dibagi menjadi 2 bagian, sebanyak 80% digunakan untuk training model, dan 20% sisanya akan digunakan sebagai testing. 
dari hasil pemodelan tersebut akan menghasilkan score yang akan menjadi bahan pertimbangan evaluasi data dan perbaikan fitur untuk pemodelan lebih lanjut agar memberikan hasil yang terbaik dan akurasi yang maksimal.

5. Performa Model

R² Score (Train): 0.8546933979086809
R² Score (Test): 0.8448002115471912
MSE (Train): 13722886.430782957
MSE (Test): 15231855.982685601

6. Diskusi Hasil & Kesimpulan
untuk Hasil R²:

R² Score (Train): 0.8547
Model dapat menjelaskan sekitar 85.47% variabilitas data pada data latih.
Ini menunjukkan bahwa model memiliki fit yang baik pada data latih.
R² Score (Test): 0.8448
Model dapat menjelaskan sekitar 84.48% variabilitas data pada data uji.
Nilai yang sedikit lebih rendah dibandingkan dengan data latih, tetapi masih cukup baik, menunjukkan bahwa model tidak terlalu overfitting.


Kesimpulan
Eksperimen ini bertujuan untuk mempermudah pembeli yang awam dengan harga pasar mobil bekas, sehingga diharapkan dengan metode prediksi harga mobil bekas dengan algoritma regresi linear 
dapat membantu pembeli untuk mendapatkan mobil bekas dengan kondisi yang masih layak.
