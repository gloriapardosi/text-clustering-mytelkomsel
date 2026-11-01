# Text Clustering – MyTelkomsel Reviews

## Deskripsi Project

Project ini merupakan implementasi Text Clustering pada data ulasan pengguna aplikasi MyTelkomsel.

Tujuan dari project ini adalah mengelompokkan ulasan pengguna berdasarkan kemiripan karakteristik teks, kemudian menganalisis hasil pengelompokan menggunakan beberapa metrik evaluasi.

## Dataset

Dataset yang digunakan merupakan data ulasan aplikasi MyTelkomsel yang telah melalui tahap preprocessing pada latihan sebelumnya.

Sebelum dilakukan clustering, data teks diubah menjadi representasi numerik menggunakan metode **TF-IDF (Term Frequency-Inverse Document Frequency)**.

## Metode yang Digunakan

Terdapat dua algoritma clustering yang diterapkan:

### 1. K-Means Clustering
Digunakan untuk mengelompokkan data ulasan ke dalam beberapa cluster berdasarkan kedekatan dengan titik pusat cluster (centroid).

Tahapan yang dilakukan:
- Menentukan jumlah cluster menggunakan Elbow Method.
- Membandingkan nilai Silhouette Score untuk beberapa nilai K.
- Melakukan proses clustering.
- Mengidentifikasi kata-kata yang paling representatif pada setiap cluster.
- Menganalisis hubungan cluster dengan rating ulasan.

### 2. Hierarchical Clustering
Digunakan untuk mengelompokkan data secara bertahap berdasarkan kemiripan antarulasan.

Metode yang digunakan adalah **Agglomerative Clustering** dengan Ward Linkage.

Tahapan yang dilakukan:
- Membuat visualisasi dendrogram.
- Menentukan jumlah cluster.
- Melakukan proses clustering.
- Mengidentifikasi kata-kata yang representatif pada setiap cluster.
- Menganalisis hubungan cluster dengan rating ulasan.

## Evaluasi Clustering

Hasil dari kedua algoritma dibandingkan menggunakan tiga metrik evaluasi:
- Metrik Silhouette Score -> Semakin tinggi semakin baik 
- Metrik Davies-Bouldin Index -> Semakin rendah semakin baik 
- Metrik Calinski-Harabasz Index -> Semakin tinggi semakin baik 

Selain itu, digunakan Word Cloud dan tabel hubungan cluster dengan rating untuk membantu memahami karakteristik setiap kelompok ulasan.

## Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- SciPy
- WordCloud
- Jupyter Notebook

## Cara Menjalankan Project

1. Clone repository ini atau unduh seluruh file project.
2. Pastikan dataset `review_mytelkomsel_bersih.csv` tersedia di folder yang sama dengan notebook.
3. Install library yang dibutuhkan:
   pip install pandas numpy matplotlib scikit-learn scipy wordcloud jupyter
4. Buka file notebook menggunakan Jupyter Notebook atau Google Colab.
5. Jalankan setiap cell secara berurutan.
6. Hasil clustering akan disimpan dalam file `review_mytelkomsel_clustering.csv`.

## Hasil dan Kesimpulan

Project ini membandingkan hasil pengelompokan ulasan menggunakan K-Means dan Hierarchical Clustering (Ward).

Berdasarkan hasil evaluasi pada notebook, Hierarchical Clustering (Ward) memperoleh hasil yang lebih baik dibandingkan K-Means pada ketiga metrik evaluasi yang digunakan. Namun, nilai Silhouette Score tetap perlu diperhatikan karena menunjukkan bahwa pemisahan antarcluster masih relatif lemah.

## Author
- **Nadhila Alya Azzahra** (051)
- **Gloria Jesika Oktoniar Pardosi** (148)

**Course:** Text Clustering – Exercise 7
