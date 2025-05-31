# **Analisis Deteksi Area Terbakar di Bukit Teletubbies Taman Nasional Bromo Tengger Semeru Pasca Insiden Kebakaran September 2023**

Untuk mengidentifikasi kawasan terbakar, pendekatan yang digunakan merujuk pada Setiani et al. (2021) dalam mengidentifikasi wilayah terbakar dengan melihat perubahan nilai Normalized Burn Ratio (NBR) atau yang sering disebut sebagai Difference Normalized Burn Ratio (dNBR). Nilai yang diperoleh pada dNBR kemudian diklasifikasikan mengacu pada klasifikasi tingkat keparahan kebakaran usulan USGS. 

Tahapan analisis mencakup: (1) pra-pemrosesan data, termasuk masking awan dengan menggunakan band QA60 dan pembuatan citra komposit median bebas awan; (2) perhitungan indeks kebakaran Normalized Burn Ratio (NBR) dari kombinasi band NIR (B8) dan SWIR2 (B12); (3) penghitungan selisih NBR (dNBR) untuk mendeteksi perubahan tingkat keparahan kebakaran; serta (4) klasifikasi area berdasarkan skala keparahan kebakaran menggunakan nilai ambang (threshold) yang disesuaikan dengan standar dari USGS. Hasil akhir divisualisasikan dalam bentuk peta spasial dan histogram untuk menggambarkan distribusi dan intensitas kebakaran secara lebih jelas.

Dalam menganalisis, library geemap digunakan sebagai antarmuka Python untuk mempermudah interaksi dengan Google Earth Engine (GEE), serta mendukung visualisasi spasial secara interaktif. Geemap memungkinkan peneliti untuk memuat dan memanipulasi koleksi citra satelit, menampilkan hasil analisis langsung dalam bentuk peta dinamis, serta menyisipkan legenda dan elemen visual lainnya dengan efisien. Dalam kode yang digunakan, geemap.Map() dimanfaatkan untuk menampilkan layer-layer penting seperti batas wilayah studi (buffer), citra pra dan pasca kebakaran, indeks NBR dan dNBR, serta hasil klasifikasi tingkat keparahan kebakaran. Selain itu, geemap.chart.image_histogram digunakan untuk memvisualisasikan histogram nilai NBR sebelum dan sesudah kejadian, memberikan gambaran statistik mengenai distribusi perubahan vegetasi. Keunggulan geemap dalam menggabungkan pemrosesan data skala besar di GEE dengan kemampuan visualisasi interaktif berbasis Python menjadikannya alat yang sangat efektif dalam analisis spasial kebakaran hutan ini.

## Petunjuk
1. Ganti "geom" sesuai dengan region yang kamu ingin gunakan
2. Atur ketentuan format export apabila butuh penyesuaian

## Referensi Code
Setiani, P., Devianto, L. A., & Ramdani, F. (2021). Rapid estimation of CO2 emissions from forest fire events using cloud-based computation of google earth engine. Environmental Monitoring and Assessment, 193, 1-13.
