# 🎬 Letterboxd Film Veriseti: EDA ve Hibrit Öneri Sistemleri
## Proje Başlığı: Letterboxd-Movies-EDA-Systems

### 📋 İçerik

1.  Proje Özeti
2.  Verisetinin Kaynağı
3.  Metodoloji ve Çalışma Adımları
4.  Temel İçgörüler (EDA Sonuçları)
5.  Oluşturulan Öneri Sistemleri
6.  Teknolojiler

---

### 1. Proje Özeti

Bu proje, Kaggle üzerinde bulunan kapsamlı Letterboxd Film Verisetini kullanarak derinlemesine bir Keşifçi Veri Analizi (EDA) gerçekleştirmeyi ve üç farklı yaklaşımla film öneri sistemleri geliştirmeyi amaçlamaktadır. Projenin ana odağı, en yüksek alaka düzeyine sahip önerileri sunan **Ağırlıklı İçerik Tabanlı Hibrit Öneri Sistemi** oluşturmaktır.

### 2. Verisetinin Kaynağı

* **Veriset Adı:** Letterboxd Movies Dataset
* **Kaynak:** Kaggle
* **Bağlantı:** [Orijinal Kaggle Veriseti Linkini Buraya Ekleyin]
* **Kayıt Sayısı:** 16,246 film kaydı
* **Özellikler:** 28 sütun (Türler, Çalışma Süresi, Ülke, Yıl, Film Süresi Kategorisi, vb.)

### 3. Metodoloji ve Çalışma Adımları

Proje, standart bir veri bilimi iş akışını takip etmiştir:

#### A. Veri Temizliği ve Ön İşleme
* `df.info()` analizi ile eksik değerler tespit edildi.
* Kategorik sütunlardaki (`primary_genre`, `country`) eksiklikler **"Bilinmiyor"** etiketiyle, sayısal sütunlardaki (`runtime`) eksiklikler ise **Medyan** ile dolduruldu.
* Tüm verilerin tutarlılığı sağlandı.

#### B. Keşifçi Veri Analizi (EDA)
* **Univariate:** En popüler film türleri (Komedi, Romantizm) ve süre dağılımı (Median Runtime: [Bulduğunuz Değeri Buraya Yazın] dk) görselleştirildi.
* **Temporal:** Yıllara göre film üretim eğilimleri ve On Yıllara göre Türlerin popülarite değişimleri (Heatmap) analiz edildi.
* **Bivariate:** Tür ve Çalışma Süresi arasındaki ilişki (Box Plot) incelendi.

#### C. Modelleme: Üç Farklı Öneri Sistemi Geliştirildi
Tüm sistemler, **Kosinüs Benzerliği (Cosine Similarity)** veya **Uzaklık Metrikleri** kullanılarak geliştirilmiştir.

### 4. Oluşturulan Öneri Sistemleri

| Sistem Tipi | Odak Noktası | Teknik | Amacı |
| :--- | :--- | :--- | :--- |
| **1. Basit Kategori Bazlı** | `primary_genre`, `decade_category` | Filtreleme & Yıla Göre Sıralama | Belirli bir kategorideki en yeni/popüler filmleri listeler. |
| **2. Tür Bazlı İçerik** | Yalnızca `genres` | TF-IDF & Kosinüs Benzerliği | Aynı tür etiketlerine sahip filmleri önerir (dar öneriler). |
| **3. Ağırlıklı Hibrit İçerik (Odak)** | `genres`, `country`, `language`, `decade_category` | **Ağırlıklı TF-IDF & Kosinüs Benzerliği** | Tür, coğrafya ve dönemi birleştirerek en alakalı, zengin önerileri sunar. |

### 5. Temel İçgörüler (Projenin En Önemli Çıktıları)

* [Bulduğunuz en yüksek korelasyonu buraya yazın.]
* [En popüler olan (Örn: Komedi) ve en az popüler olan türü yazın.]
* [Hibrit sistemin, sadece tür bazlı sisteme göre ne kadar farklı/iyi sonuç verdiğini kısaça belirtin.]

### 6. Teknolojiler

* `Python`
* `Jupyter Notebook`
* `Pandas` (Veri Manipülasyonu)
* `NumPy` (Sayısal İşlemler)
* `Matplotlib` / `Seaborn` (Görselleştirme)
* `Scikit-learn (sklearn)` (TF-IDF, Kosinüs Benzerliği)
* `WordCloud` (Opsiyonel)
