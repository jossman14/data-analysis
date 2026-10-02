# Data Analysis

Kumpulan notebook latihan analisis data dan machine learning dengan Python (EDA, clustering, uji hipotesis, analisis sentimen Twitter).

## Isi Notebook

| Notebook | Isi | Data |
|---|---|---|
| `super-market-analysis.ipynb`, `supermarketanalysis.ipynb` | EDA penjualan supermarket: penjualan per cabang/jam, lini produk, metode pembayaran, tipe pelanggan | `supermarket_sales.csv` (juga `input/supermarket_sales.csv`) |
| `customerpotential.ipynb` | Segmentasi pelanggan dengan K-Means | `supermarket_sales.csv` |
| `telcom-python.ipynb` | EDA dan uji hipotesis (t-test) pada data churn pelanggan telekomunikasi | `WA_Fn-UseC_-Telco-Customer-Churn.csv` |
| `Identify_Customer_Segments (1).ipynb` | Proyek Udacity "Identify Customer Segments": PCA + K-Means pada data demografi Bertelsmann Arvato | `Udacity_AZDIAS_Subset.csv`, `Udacity_CUSTOMERS_Subset.csv`, `AZDIAS_Feature_Summary.csv` |
| `ICSE 2019 Clustering dan Sentiment-fix.ipynb` | Pengambilan tweet (Tweepy), praproses teks Bahasa Indonesia (Sastrawi), clustering TF-IDF + K-Means, sentimen VADER/TextBlob setelah diterjemahkan (googletrans) | `politik_agama1.csv` |
| `Latent Dirichlet Allocation and Vader Sentiment Analysis.ipynb` | Pengambilan tweet (Tweepy), word cloud, dan analisis sentimen VADER pada tweet (tidak ada model LDA yang dijalankan meski disebut di judul) | `test.csv` |

## Dataset

- Disertakan di repo: `supermarket_sales.csv`, `WA_Fn-UseC_-Telco-Customer-Churn.csv`, `test.csv`, `pemerintah_13_kkNovember.csv` (kumpulan tweet November 2019).
- **Tidak disertakan** di repo: data Udacity/Arvato (`Udacity_AZDIAS_Subset.csv`, `Udacity_CUSTOMERS_Subset.csv`, `AZDIAS_Feature_Summary.csv`) dan `politik_agama1.csv`.

## Cara Menjalankan

Tidak ada `requirements.txt`. Pustaka utama: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`; untuk notebook sentimen juga `tweepy`, `nltk`, `Sastrawi`, `googletrans`, `gensim`, `textblob`, `vaderSentiment`, `wordcloud`, `pyLDAvis`, `plotly`, `pyspark`.

Buka notebook dengan Jupyter dan jalankan sel secara berurutan dari folder repo ini. Pengambilan tweet memerlukan kredensial Twitter API milik sendiri.

## Dataset & Artefak

| Dataset | File | Sumber | Di repo? |
|---|---|---|---|
| Supermarket sales | `supermarket_sales.csv` (128 KB) | sumber tidak tercatat (notebook Kaggle-style membaca `../input/supermarket_sales - Sheet1.csv`) | Ya |
| Telco Customer Churn | `WA_Fn-UseC_-Telco-Customer-Churn.csv` (0,97 MB) | sumber tidak tercatat (path di notebook: `../input/telco-customer-dataset/`) | Ya |
| Data demografi Bertelsmann Arvato (proyek Udacity *Identify Customer Segments*) | `Udacity_AZDIAS_Subset.csv`, `Udacity_CUSTOMERS_Subset.csv`, `AZDIAS_Feature_Summary.csv` | Materi proyek Udacity; URL tidak tercatat | Tidak |
| Tweet politik/agama | `politik_agama1.csv` | Diambil sendiri lewat Twitter API (Tweepy) | Tidak |
| Tweet (hasil streaming) | `test.csv` | Diambil sendiri lewat Twitter API (Tweepy) | Ya (kecil) |
| Tweet November 2019 | `pemerintah_13_kkNovember.csv` | sumber tidak tercatat (tidak dipakai notebook mana pun) | Ya (kecil) |

Tidak ada model atau artefak eksperimen yang disertakan; semua hasil (cluster, skor sentimen, grafik) dibuat ulang dengan menjalankan notebook. Data yang tidak disertakan harus disiapkan sendiri dan diletakkan di folder repo ini.
