# 📧 Eterna Teknoloji - E-Posta Spam Tespit Sistemi

## 🚀 Proje Mimarisi (Component Yapısı)

Proje, yazılım mimarisi disiplinlerine uygun olarak 5 temel bileşen (component) üzerinden modüler bir şekilde inşa edilmiştir:

1. **Data Pipeline Component:** Verinin dış kaynaktan (GitHub) çekilmesi, yapılandırılması ve Train/Test olarak ayrılması.
2. **Text Preprocessing Component:** NLTK kütüphanesi kullanılarak metinlerin gürültüden arındırılması (Lowercase, Punctuation Removal, Stopwords, Lemmatization, Tokenization).
3. **Feature Engineering Component:** Temizlenmiş metinlerin `TfidfVectorizer` ile matematiksel matrislere (3000 Feature) dönüştürülmesi ve yoğunluk analizi.
4. **Model & Evaluation Component:** Naive Bayes ve Support Vector Machine (SVM) algoritmalarının eğitilmesi, Accuracy, Precision, Recall, F1 metriklerinin hesaplanması ve Confusion Matrix görselleştirmeleri.
5. **Inference Component:** Modelin daha önce hiç görmediği yeni e-postalar üzerinde test edilmesi ve anlık tahmin (Prediction) yapması.

## 📊 Öne Çıkan Sonuçlar

* **Veri Seti:** 5572 E-posta (%86.59 Normal, %13.41 Spam)
* **Model Performansı:** SVM Modeli **%98.2 Doğruluk (Accuracy)** ve **%92.9 F1 Skor** ile en yüksek genel performansı göstermiştir.
* **Tercih Stratejisi:** False Positive maliyetinin çok yüksek olduğu kurumsal senaryolar için Precision değeri 1.000 olan Naive Bayes modeli de değerlendirmeye sunulmuştur.

## 🛠️ Kullanılan Teknolojiler
* **Dil:** Python
* **Veri İşleme & NLP:** Pandas, NumPy, NLTK, Scikit-learn
* **Görselleştirme:** Matplotlib, Seaborn
