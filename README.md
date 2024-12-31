# 🔍 **Analisis Hubungan Angka Harapan Hidup**

Proyek ini bertujuan untuk menganalisis faktor-faktor yang memengaruhi angka harapan hidup di berbagai negara. Dengan menggunakan data statistik dan algoritma machine learning, kami mengevaluasi hubungan antara variabel ekonomi, kesehatan, dan sosial terhadap angka harapan hidup.

---

## 📂 **Dataset**

Sumber Data: `life_expectancy_data.csv`

Dataset ini mencakup:

- **Ekonomi**:
  - Consumer Price Index (CPI): Ukuran inflasi dan daya beli.
  - GDP: Gross Domestic Product, total nilai barang dan jasa yang diproduksi di negara tersebut.
  - Minimum Wage: Tingkat upah minimum dalam mata uang lokal.
  - Unemployment Rate: Persentase angkatan kerja yang menganggur.
- **Kesehatan**:
  - Fertility Rate: Jumlah rata-rata anak yang dilahirkan oleh seorang wanita selama masa hidupnya.
  - Infant Mortality: Jumlah kematian per 1.000 kelahiran hidup sebelum mencapai usia satu tahun.
  - Maternal Mortality Ratio: Jumlah kematian ibu per 100.000 kelahiran hidup.
  - Out of Pocket Health Expenditure (%): Persentase total pengeluaran kesehatan yang dibayar langsung oleh individu.
  - Physicians per Thousand: Jumlah dokter per seribu orang.
- **Sosial**:
  - Population: Total populasi negara.
- **Target**: Kolom `Life Expectancy` (angka harapan hidup dalam tahun).


**Langkah Persiapan Data**:
- Menangani nilai yang hilang (missing values) dengan metode imputasi.
- Melakukan normalisasi variabel numerik untuk memastikan konsistensi dalam analisis.
- Menangani duplikasi dan outlier.

---

## 🛠️ **Pemodelan dan Evaluasi**
Kami menggunakan beberapa algoritma machine learning untuk memahami faktor-faktor yang memengaruhi angka harapan hidup:
1. **GradientBoostingRegressor**
2. **Support Vector Regressor (SVR)**
3. **RandomForestRegressor**
4. **LinearRegression**
5. **ExtraTreesRegressor**
6. **AdaBoostRegressor**
7. **DecisionTreeRegressor** 
8. **XGBRegressor** 
9. **XGBRFRegressor**

**Metrik Evaluasi**:
-  Mean Absolute Percentage ErrorN (MAPE)
- Coefficient of Determination (R²)


**Langkah-Langkah**:

1. **Eksplorasi Data**: Meninjau pola dan distribusi variabel melalui visualisasi.
2. **Feature Selection**: Memilih variabel yang paling berkontribusi terhadap prediksi angka harapan hidup.
3. **Pelatihan Model**: Melatih model dengan data training menggunakan algoritma yang disebutkan.
4. **Evaluasi Model**: Membandingkan performa model dengan metrik yang telah ditentukan.

---

## 🏆 **Hasil**

### **Feature Importance**

| No | Fitur                                 | Pentingnya |
|----|---------------------------------------|------------|
| 1  | Maternal Mortality Ratio              | 0.441403   |
| 2  | Infant Mortality                      | 0.328048   |
| 3  | Fertility Rate                        | 0.128563   |
| 4  | Physicians per Thousand               | 0.027848   |
| 5  | Minimum Wage                          | 0.018913   |
| 6  | CPI Change (%)                        | 0.015701   |
| 7  | Out of Pocket Health Expenditure (%)  | 0.015142   |
| 8  | GDP                                   | 0.014825   |
| 9  | Population                            | 0.009556   |

### **Model Terbaik**
- **Model**: XGBRFRegressor
  - **R²**: 90.531463
  - **MAPE**: 2.607853
  - **Interpretasi Fitur**: Variabel seperti Maternal Mortality Ratio, Infant Mortality, dan Fertility Rate memiliki pengaruh signifikan terhadap angka harapan hidup.

---

## 💻 **Teknologi yang Digunakan**

- **Python**: Untuk pengolahan data dan pemodelan.
- **Scikit-learn**: Digunakan untuk membangun dan mengevaluasi model machine learning.
- **Pandas**: Manipulasi dan analisis data.
- **Matplotlib & Seaborn**: Visualisasi data dan hasil analisis.

---

## 📈 **Visualisasi**

Kami menyediakan grafik interaktif untuk:

- Distribusi angka harapan hidup berdasarkan wilayah.
- Korelasi antara variabel ekonomi dan angka harapan hidup.
- Pentingnya fitur dalam model prediksi.



