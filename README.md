# TUGAS-TITANIC
https://colab.research.google.com/drive/1iEZoW8QdJBuVI9hBKc2-kF90hmom7ZSK#scrollTo=yWUlquVp97Aa




# PENDAHULUAN
Dataset Titanic merupakan salah satu dataset klasik dalam dunia data science. Dataset ini berisi informasi penumpang kapal Titanic, termasuk umur, jenis kelamin, kelas tiket, tarif, dan status kelangsungan hidup (survived). Analisis ini bertujuan untuk menemukan pola dari data penumpang yang mungkin berhubungan dengan peluang bertahan hidup.

 # PENGECEKAN DATA AWAL
Dataset dimuat menggunakan fungsi sns.load_dataset("titanic"). Dari sini terlihat bahwa beberapa kolom memiliki missing values, terutama pada age, deck, dan embark_town. Ini penting dicatat karena bisa memengaruhi analisis.

# ANALISIS MISSING VALUE
Hasil visualisasi heatmap menunjukkan cukup banyak nilai kosong di kolom age dan deck. Hal ini wajar mengingat tidak semua penumpang memiliki informasi umur atau nomor dek yang tercatat.

# ANALISIS VARIABEL KATEGORIK
- Distribusi jenis kelamin (sex): Penumpang pria lebih banyak daripada wanita.
- Distribusi status kelangsungan hidup (survived): Lebih banyak penumpang yang tidak selamat dibandingkan yang selamat.

# ANALISIS VARIABEL NUMERIK
- Distribusi umur: Mayoritas penumpang berusia sekitar 20–40 tahun.
- Boxplot umur vs kelas tiket: Semakin tinggi kelas (pclass=1), cenderung penumpang lebih tua dibandingkan kelas bawah.

# KORELASI ANTAR VARIABEL
Heatmap korelasi menunjukkan:
	•	survived berkorelasi negatif dengan pclass (-0.34), artinya semakin tinggi kelas tiket, peluang selamat lebih tinggi.
	•	fare berkorelasi negatif dengan pclass (-0.55), wajar karena tiket kelas atas lebih mahal.
	•	age tidak memiliki korelasi kuat dengan survived.

# HUBUNGAN ANTAR VARIABEL
 • Survival vs Age (histogram & boxplot): Tidak ada perbedaan signifikan umur antara yang selamat dan tidak selamat.
	•	Scatter plot Age vs Fare dengan hue Survived: Terlihat bahwa banyak penumpang dengan tarif lebih tinggi (kelas atas) memiliki peluang lebih besar untuk selamat.
	•	Pairplot (age, fare, pclass): Memperlihatkan pola jelas bahwa kelas tiket dan harga sangat memengaruhi survival.

# KESIMPULAN SEMENTARA
 1. Dataset Titanic memiliki missing values signifikan pada age dan deck.
	2.	Penumpang pria lebih banyak, tetapi wanita punya peluang survival lebih tinggi.
	3.	Kelas tiket berhubungan dengan survival—kelas atas lebih aman.
	4.	Tarif tiket (fare) dan kelas (pclass) adalah faktor dominan terhadap peluang selamat.
	5.	Umur bukan faktor signifikan dalam survival.

