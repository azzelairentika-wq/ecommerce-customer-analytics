# E-Commerce Customer Analytics: Identifying Potential Customers using EDA in Python

Mini-project Exploratory Data Analysis (EDA) untuk membantu tim marketing e-commerce mengidentifikasi profil pelanggan potensial dan menganalisis distribusi demografi serta pendapatan, sebagai bagian dari tugas mata kuliah Sains Data.

## 🎯 Studi Kasus

Sebuah platform e-commerce ingin mengidentifikasi segmen pelanggan potensial berdasarkan total belanja dan domisili, serta memastikan kualitas data pelanggan dengan menangani *missing values* dan duplikasi, agar strategi pemasaran dan promosi dapat lebih tepat sasaran.

## 🗂️ Dataset

`mhs1_ecommerce_analytics.csv` — Data pelanggan e-commerce dengan kolom:

| Kolom | Deskripsi |
|---|---|
| ID_Pelanggan | Kode unik pelanggan |
| Umur | Usia pelanggan (terdapat nilai kosong) |
| Kota | Kota domisili pelanggan |
| Total_Belanja | Total nominal belanja pelanggan (Rupiah) |
| Kategori_Produk | Kategori produk yang paling sering dibeli |
| Membeli_Lagi | Status pelanggan apakah melakukan pembelian ulang (Ya/Tidak) |

## 🔧 Tahapan Analisis

1. **Pemeriksaan struktur data** - `.info()` dan pengecekan *shape* dataset awal.
2. **Statistik deskriptif & distribusi awal** - `.describe()`, perhitungan mean vs median untuk Umur dan Total_Belanja, serta visualisasi histogram sebelum *cleaning*.
3. **Data cleaning** - Imputasi nilai kosong pada kolom `Umur` menggunakan median, dan penghapusan data duplikat berdasarkan `ID_Pelanggan`.
4. **Feature engineering & filtering** - Membuat kolom `Kategori_Status` (Pelanggan Potensial vs Biasa) dan memfilter pelanggan dengan total belanja > Rp 5.000.000 yang berdomisili di Jakarta dan Surabaya.
5. **Visualisasi & storytelling** - Diagram batang total pendapatan per kota, dilengkapi dengan analisis distribusi data sebelum dan sesudah *cleaning*.
6. **Export hasil cleaning** - Menyimpan data duplikat dan data final ke dalam file Excel terpisah untuk dokumentasi.

## 📊 Temuan Utama

- Terdapat *missing values* pada kolom `Umur` dan duplikasi pada `ID_Pelanggan` yang berhasil ditangani tanpa menghapus informasi penting.
- Distribusi `Umur` dan `Total_Belanja` menunjukkan perubahan pada nilai mean dan median setelah proses imputasi dan penghapusan duplikat, mengindikasikan data yang lebih representatif.
- Segmen **Pelanggan Potensial** (belanja > Rp 5.000.000) banyak terkonsentrasi di kota besar seperti Jakarta dan Surabaya.
- Visualisasi pendapatan menunjukkan adanya ketimpangan kontribusi antar kota, di mana kota-kota tertentu mendominasi total *revenue*.

## 💡 Rekomendasi Bisnis

Toko dapat meningkatkan promosi, memberikan penawaran khusus, atau membuat program loyalitas pada wilayah yang memiliki transaksi tinggi. 
Pelanggan dengan total belanja di atas Rp5.000.000 dapat diberikan perlakuan khusus berupa pemberian voucher, program membership, promo eksklusif, serta rekomendasi produk yang disesuaikan dengan riwayat pembelian mereka. Selain itu, kota dengan nilai transaksi yang lebih kecil perlu dianalisis lebih lanjut untuk mengetahui faktor penyebab rendahnya tingkat pembelian, seperti kurang optimalnya strategi promosi, perbedaan preferensi produk, atau jumlah pelanggan yang masih terbatas. Hasil evaluasi tersebut dapat menjadi dasar dalam menyusun strategi pemasaran yang lebih tepat untuk meningkatkan transaksi di wilayah tersebut.

## 🛠️ Tools

Python, Pandas, NumPy, Matplotlib, openpyxl (Jupyter Notebook)

## 📁 Struktur Repository

```text
├── ecommerce_analytics.ipynb               # Notebook analisis utama
├── mhs1_ecommerce_analytics_fixed.xlsx     # Dataset mentah
├── Data_Duplikat_dan_Data_Kosong_Diperbaiki.xlsx # Dokumentasi hasil cleaning
├── charts/                                 # Hasil visualisasi (PNG)
│   ├── pendapatan_per_kota.png
│   ├── distribusi_awal_sebelum_cleaning.png
│   └── distribusi_setelah_cleaning.png
└── README.md

## Author
Tengku Azzella Irantika - - 41525110015 - Program Studi Teknik Informatika 2026
