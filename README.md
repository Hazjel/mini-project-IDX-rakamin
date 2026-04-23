# Analisis Potensi Investasi Deposito Nasabah 🏦📊

[cite_start]Proyek *Exploratory Data Analysis* (EDA) ini bertujuan untuk mengidentifikasi nasabah *existing* yang memiliki potensi tertinggi untuk berinvestasi pada produk simpanan jangka panjang (deposito)[cite: 4]. [cite_start]Analisis ini dilakukan untuk mendukung strategi bisnis bank dalam meningkatkan *Customer Lifetime Value* (CLV)[cite: 3].

## 🎯 Objektif Proyek
1. [cite_start]Melakukan eksplorasi data untuk melihat hubungan antara profil nasabah dan keputusan berlangganan deposito (`subscription`)[cite: 6].
2. [cite_start]Menganalisis pola perilaku nasabah berdasarkan usia, saldo bulanan rata-rata, dan status pinjaman[cite: 7].
3. [cite_start]Merumuskan tipe nasabah (segmentasi) yang paling potensial untuk ditargetkan oleh *Relationship Manager* (RM)[cite: 8].

## 📂 Informasi Dataset
[cite_start]Dataset yang digunakan berisi 30 baris data nasabah dengan 15 kolom atribut[cite: 28]. [cite_start]Data terindikasi bersih tanpa adanya *missing values* (0 total *missing*)[cite: 86].

**Fitur Utama:**
* [cite_start]**Demografi:** `age`, `job`, `marital`, `education`[cite: 30].
* [cite_start]**Finansial & Produk:** `avg_monthly_balance`, `total_products_owned`, `years_as_customer`[cite: 30].
* [cite_start]**Pinjaman & Investasi:** `housing_loan`, `personal_loan`, `credit_card`, `investment_experience`[cite: 30].
* [cite_start]**Interaksi Bisnis:** `contact_channel`, `relationship_manager_contact`[cite: 30].
* [cite_start]**Target Variabel:** `subscription` (yes/no)[cite: 30].

## 🛠️ Alat & Teknologi (Tech Stack)
Proyek ini dikembangkan menggunakan Python dengan beberapa pustaka utama untuk manipulasi dan visualisasi data:
* [cite_start]`pandas` [cite: 9]
* [cite_start]`numpy` [cite: 10]
* [cite_start]`matplotlib` [cite: 11]
* [cite_start]`seaborn` [cite: 12]

## 💡 Temuan Utama (Key Insights)
[cite_start]Berdasarkan analisis yang telah dilakukan, nasabah yang berlangganan (Subscriber) memiliki perbedaan profil yang sangat kontras dibandingkan dengan yang tidak berlangganan (Non-Subscriber)[cite: 690]:
* [cite_start]**Faktor Usia & Saldo:** *Subscriber* umumnya adalah nasabah senior dengan usia rata-rata 50.5 tahun (batas bawah ~40 tahun) dan memiliki saldo rata-rata Rp 24.5 Juta (5.3x lebih tinggi dari *non-subscriber*)[cite: 690].
* [cite_start]**Loyalitas:** *Subscriber* memiliki *engagement* yang jauh lebih tinggi, rata-rata sudah menjadi nasabah selama 15.3 tahun dan memiliki 4.2 produk bank[cite: 690].
* [cite_start]**Hambatan Utama (Barrier):** Kepemilikan cicilan rumah/KPR (*housing loan*) sangat menurunkan rasio *subscription* hingga hanya 11.4%[cite: 310]. [cite_start]Sebaliknya, nasabah tanpa KPR memiliki *success rate* sebesar 66.7%[cite: 309].
* [cite_start]**Faktor Penentu Mutlak (Perfect Predictors):** Variabel `investment_experience` (pengalaman investasi) dan `relationship_manager_contact` (kontak dari RM) memisahkan target secara sempurna dengan akurasi 100%[cite: 521, 522].

## 🎯 Profil Target Ideal
[cite_start]Nasabah paling potensial untuk ditargetkan oleh *Relationship Manager* memiliki karakteristik berikut[cite: 692]:
* [cite_start]Usia $\ge$ 41 tahun[cite: 693].
* [cite_start]Saldo bulanan rata-rata $\ge$ Rp 15 juta[cite: 694].
* [cite_start]Lama menjadi nasabah $\ge$ 9 tahun[cite: 695].
* [cite_start]Memiliki $\ge$ 3 produk bank[cite: 697].
* [cite_start]Tidak memiliki *housing loan* aktif[cite: 696].
* [cite_start]Pekerjaan: *management*, *retired*, *self-employed*, atau *entrepreneur*[cite: 698].
* [cite_start]Pendidikan: *tertiary* atau *primary (senior)*[cite: 699].

## 🚀 Rekomendasi Bisnis
1. [cite_start]**Prioritaskan Kontak Personal:** RM harus lebih proaktif menghubungi nasabah secara personal, mengingat variabel ini memiliki korelasi 100% terhadap konversi[cite: 701, 702, 703].
2. [cite_start]**Edukasi Investasi Dasar:** Gunakan program literasi keuangan sebagai langkah awal untuk membangun `investment_experience` sebelum menawarkan produk deposito *high-ticket*[cite: 704, 705].
3. [cite_start]**Fokus Segmen High-Value:** Optimalkan sumber daya pada nasabah berusia $\ge$ 40 tahun dengan saldo $\ge$ Rp 15 Juta[cite: 706, 707].
4. [cite_start]**Efisiensi Targeting:** Hindari penawaran investasi jangka panjang pada nasabah dengan beban *housing loan* aktif[cite: 708, 709].

---
[cite_start]*Dibuat berdasarkan Pre-Challenge 2b - Data Science Track* [cite: 1]
