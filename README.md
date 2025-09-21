# TUGAS-TITANIC
https://colab.research.google.com/drive/1iEZoW8QdJBuVI9hBKc2-kF90hmom7ZSK#scrollTo=yWUlquVp97Aa




# PENDAHULUAN
Dataset Titanic merupakan salah satu dataset klasik dalam dunia data science. Dataset ini berisi informasi penumpang kapal Titanic, termasuk umur, jenis kelamin, kelas tiket, tarif, dan status kelangsungan hidup (survived). Analisis ini bertujuan untuk menemukan pola dari data penumpang yang mungkin berhubungan dengan peluang bertahan hidup.

 # PENGECEKAN DATA AWAL
Dataset dimuat menggunakan fungsi sns.load_dataset("titanic"). Dari sini terlihat bahwa beberapa kolom memiliki missing values, terutama pada age, deck, dan embark_town. Ini penting dicatat karena bisa memengaruhi analisis.

# ANALISIS MISSING VALUE
Hasil visualisasi heatmap menunjukkan cukup banyak nilai kosong di kolom age dan deck. Hal ini wajar mengingat tidak semua penumpang memiliki informasi umur atau nomor dek yang tercatat.
<img width="831" height="608" alt="image" src="https://github.com/user-attachments/assets/5b046b7d-5eb0-4574-8fc2-14658f6dd63b" />

# ANALISIS VARIABEL KATEGORIK
- Distribusi jenis kelamin (sex): Penumpang pria lebih banyak daripada wanita.
  <img width="695" height="547" alt="image" src="https://github.com/user-attachments/assets/69fd03d2-8031-43ac-b074-d48ed131336f" />

- Distribusi status kelangsungan hidup (survived): Lebih banyak penumpang yang tidak selamat dibandingkan yang selamat.
  <img width="695" height="547" alt="image" src="https://github.com/user-attachments/assets/a398fd27-9e22-44b7-b162-10f9dd4a25fd" />


# ANALISIS VARIABEL NUMERIK
- Distribusi umur: Mayoritas penumpang berusia sekitar 20–40 tahun.
  <img width="686" height="547" alt="image" src="https://github.com/user-attachments/assets/e84690e0-e801-4772-ad35-efe7aa069cab" />

- Boxplot umur vs kelas tiket: Semakin tinggi kelas (pclass=1), cenderung penumpang lebih tua dibandingkan kelas bawah.
  <img width="686" height="547" alt="image" src="https://github.com/user-attachments/assets/72087ee9-3e58-40fb-bbe8-de09f555458b" />


# KORELASI ANTAR VARIABEL
<img width="776" height="682" alt="image" src="https://github.com/user-attachments/assets/5c04dd99-dc2e-438d-b3c7-28a5f1370e20" />
Heatmap korelasi menunjukkan:
1. survived berkorelasi negatif dengan pclass (-0.34), artinya semakin tinggi kelas tiket, peluang selamat lebih tinggi.
2. fare berkorelasi negatif dengan pclass (-0.55), wajar karena tiket kelas atas lebih mahal.
3. age tidak memiliki korelasi kuat dengan survived.

# HUBUNGAN ANTAR VARIABEL

1. Survival vs Age (histogram & boxplot): Tidak ada perbedaan signifikan umur antara yang selamat dan tidak selamat.
<img width="609" height="470" alt="image" src="https://github.com/user-attachments/assets/a97d0279-b11b-41bd-ac03-a3444080e879" />

3. Scatter plot Age vs Fare dengan hue Survived: Terlihat bahwa banyak penumpang dengan tarif lebih tinggi (kelas atas) memiliki peluang lebih besar untuk selamat.
<img width="695" height="547" alt="image" src="https://github.com/user-attachments/assets/3c81783c-27eb-4ce6-b372-e077bb2b67e3" />

4. Embarkasi vs survival: menunjukkan bahwa tingkat kematian dan keselamatan tertinggi berasal dari pelabuhan Southampton
<img width="618" height="470" alt="image" src="https://github.com/user-attachments/assets/8b6bbdf6-0755-41ca-8d1e-070bffca4453" />


# KESIMPULAN SEMENTARA
 1. Dataset Titanic memiliki missing values signifikan pada age dan deck.
	2.	Penumpang pria lebih banyak, tetapi wanita punya peluang survival lebih tinggi.
	3.	Kelas tiket berhubungan dengan survival—kelas atas lebih aman.
	4.	Tarif tiket (fare) dan kelas (pclass) adalah faktor dominan terhadap peluang selamat.
	5.	Umur bukan faktor signifikan dalam survival.

