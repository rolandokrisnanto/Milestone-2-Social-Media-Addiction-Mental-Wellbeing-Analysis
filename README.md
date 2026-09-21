# Milestone 2 — Social Media Addiction & Mental Wellbeing Analysis

Analisis statistik dan dashboard visualisasi untuk mengetahui hubungan antara perilaku penggunaan media sosial dengan kondisi kesejahteraan mental pengguna.

**Nama:** Rolando Krisnanto — **Batch:** CODA-RMT-021

**Dashboard:** [Tableau Public — M2 Dashboard](https://public.tableau.com/app/profile/rolando.krisnanto5616/viz/M2_P1_Dashboard_RolandoKrisnanto/Dashboard1?publish=yes)

## Latar Belakang & Problem Statement

Penggunaan media sosial yang berlebihan berpotensi memicu kecanduan, kecemasan, dan gangguan tidur. Analisis ini dilakukan untuk melihat hubungan antara faktor-faktor perilaku penggunaan media sosial dengan kondisi kesehatan mental penggunanya, berdasarkan data lebih dari 1.000 pengguna.

## Dataset

- **Sumber:** [Kaggle — Social Media Addiction & Mental Wellbeing Dataset](https://www.kaggle.com/datasets/harpartapsingh13/social-media-addiction-and-mental-wellbeing-dataset/data)
- **Cakupan:** ±1.500 baris data pengguna, meliputi demografi (usia, gender), perilaku platform (platform utama, durasi pemakaian harian), dan skor kesehatan mental (anxiety, depression, loneliness, sleep quality, mental wellbeing, addiction level)

## Metodologi

1. **Data Cleaning** — drop kolom yang tidak relevan, isi missing value (interpolasi untuk kolom numerik, modus untuk kolom kategorikal), buat kolom turunan untuk kebutuhan analisis
2. **Statistik Deskriptif** — central tendency, distribusi, dan deteksi outlier per kelompok
3. **Statistik Inferensial** — uji normalitas (Shapiro-Wilk), korelasi Spearman, dan uji Kruskal-Wallis
4. **Visualisasi** — Matplotlib & Seaborn di notebook, serta dashboard interaktif di Tableau

## Key Findings

1. Tingkat kecanduan tertinggi ada pada pria usia 26–35 tahun
2. Instagram merupakan platform dengan jumlah pengguna kecanduan berat terbanyak
3. Korelasi Spearman signifikan (p < 0.05) tapi lemah antara durasi penggunaan harian dan tingkat kecanduan
4. Anxiety score berkorelasi negatif lemah dan signifikan dengan wellbeing score; depression score tidak signifikan
5. Durasi tidur tidak menunjukkan hubungan linear yang kuat dengan wellbeing score
6. Semakin tinggi tingkat kesepian (loneliness), semakin rendah wellbeing score-nya
7. Uji Kruskal-Wallis mengonfirmasi wellbeing score menurun signifikan seiring naiknya tingkat kecanduan (rata-rata 7.90 pada Low → 4.59 pada Severe)

**Kesimpulan:** semakin tinggi tingkat kecanduan media sosial, semakin rendah kesejahteraan mental penggunanya.

## Tech Stack

Python · Pandas · NumPy · SciPy · Matplotlib · Seaborn · Tableau

## Struktur File

```
├── P1M2_rolando_krisnanto.ipynb                          # Notebook: cleaning, analisis statistik, visualisasi
├── social_media_addiction_mental_wellbeing_raw.csv        # Data mentah
├── social_media_addiction_mental_wellbeing_clean.csv      # Data setelah dibersihkan (untuk Tableau)
└── README.md
```
