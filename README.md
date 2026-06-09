# 🛡️ CISA Advisories Semantic Topic Modeling
**Penerapan Semantic Topic Modeling untuk Klasterisasi Topik Laporan Keamanan Teknologi Operasional Siber berdasarkan Data CISA Advisories**

Repositori ini berisi keseluruhan *source code*, *dataset* hasil ekstraksi, dan metodologi eksperimen untuk penelitian Skripsi Strata-1 (S1) Sistem Informasi di Universitas Airlangga.

## 📖 Tentang Proyek Ini
Laporan kerentanan sistem kendali industri (*Industrial Control Systems* / ICS) dan Teknologi Operasional (OT) sangat krusial bagi intelijen ancaman siber (*Cyber Threat Intelligence*). Proyek ini bertujuan mengotomatisasi ekstraksi dan klasterisasi informasi ancaman siber dari **3.461 laporan CISA Advisories** menggunakan arsitektur *Machine Learning* tanpa pengawasan (*unsupervised learning*). 

Penelitian ini mengkomparasikan dua skenario *embedding model* di dalam kerangka kerja **BERTopic**:
- **Skenario A:** Menggunakan *General-purpose embedding* (`all-MiniLM-L6-v2`).
- **Skenario B:** Menggunakan *Domain-specific embedding* (`CyBERT`).

## 🛠️ Tech Stack & Metodologi
- **Bahasa Pemrograman:** Python
- **Natural Language Processing (NLP):** `BERTopic`, `HuggingFace Transformers`, `CyBERT`, `NLTK`, `Spacy`
- **Dimensionality Reduction & Clustering:** `UMAP`, `HDBSCAN`
- **Data Wrangling:** `Pandas`, `JSON`

## 📊 Hasil Penelitian (Ringkasan)
1. **Peningkatan Semantik:** Penggunaan CyBERT berhasil menurunkan *noise* (outlier dokumen) secara drastis dari 35,5% menjadi 16,5% dan meningkatkan kepadatan Koherensi Semantik (Cv).
2. **Identifikasi Vektor Serangan:** Model spesifik-domain mampu memetakan klaster teknis menjadi taktik operasional yang spesifik, seperti *Patch Management*, *Security Awareness* (Social Engineering/Email), dan Kerentanan Vendor Industri.
3. **Validasi Pakar (Blind Review):** Representasi topik divalidasi langsung oleh praktisi *Security Operations Center* (SOC) melalui metode pengujian buta (skor koherensi pakar mencapai 4.5/5 untuk klaster operasional).

## 🔗 Referensi Data & Model
- **Raw Data (JSON):** [CISA CSAF Repository](https://github.com/cisagov/CSAF/tree/develop)
- **CISA ICS Advisories:** [Official Publication](https://www.cisa.gov/news-events/ics-advisories)
- **CyBERT Model:** Model embedding spesifik keamanan siber yang digunakan merujuk pada Repositori [CyBERT (Ranade et al., 2021)](https://github.com/priyankaranade1/CyBERT).

## 👨‍💻 Peneliti
**Javier Ihsan Adhipratama** S-1 Sistem Informasi | Universitas Airlangga  
