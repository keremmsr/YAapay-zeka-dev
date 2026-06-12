# Yapay Zeka Dersi - Ödev 2: Word2Vec Metin Benzerliği Hesaplama

Bu proje, daha önceden ön işlemesi tamamlanmış (Lemmatized ve Stemmed) yemek tarifi veri setleri üzerinde Word2Vec modelleri eğitmeyi ve bu modeller aracılığıyla metinler arası kosinüs benzerliği (Cosine Similarity) ile anlamsal değerlendirme yapmayı amaçlamaktadır. Toplamda 16 farklı konfigürasyonla (CBOW/SkipGram, Window 2/4, Vektör 100/300) model eğitilmiştir.

## İçerik ve Klasör Yapısı
- `Yapay_Zeka_Odev_2.ipynb`: Modellerin eğitilmesi, kosinüs benzerliğinin hesaplanması, Jaccard benzerliği (Heatmap) ve genel değerlendirme kodlarının tümünü içeren Jupyter Notebook dosyası.
- `model/`: Eğitilen 16 adet Word2Vec modelinin kaydedildiği klasördür.
- `benzerlik_sonuclari.txt`: 16 modelin her biri için belirlenen örnek giriş metnine ("Sodalı Köfte") en çok benzeyen 5 tarifin ve bu tariflerin kosinüs benzerliği skorlarının dökümü.
- `jaccard_heatmap.png`: Modellerin sıralama tutarlılığını (Ranking Agreement) gösteren 16x16'lık Jaccard ısı haritası.
- `*Veri_Seti.csv`: Model eğitiminde kullanılan Lemmatized ve Stemmed veriler.

## Kurulum ve Çalıştırma Talimatları
Bu projeyi kendi ortamınızda çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

1. **Gereksinimleri Yükleyin:**
   Bilgisayarınızda Python yüklü olmalıdır. Projenin bağımlılıklarını kurmak için terminal (veya cmd/powershell) üzerinden şu komutu çalıştırın:
   ```bash
   pip install pandas gensim scikit-learn numpy seaborn matplotlib jupyter
   ```

2. **Jupyter Notebook'u Başlatın:**
   Terminalde proje klasörünün içindeyken Jupyter Notebook'u başlatın:
   ```bash
   jupyter notebook
   ```

3. **Kodları Çalıştırın:**
   Tarayıcınızda açılan arayüzden `Yapay_Zeka_Odev_2.ipynb` dosyasını açın. Dosya içerisinde 3 ana görev hücresi bulunmaktadır:
   - **Görev-1 Hücresi:** Modelleri eğitir ve `model/` klasörüne kaydeder.
   - **Görev-2 Hücresi:** Belirlenen girdi metni için 16 modelde benzerlikleri hesaplar.
   - **Görev-3 Hücresi:** Heatmap (Isı haritası) oluşturur ve değerlendirme metriklerini üretir.
   
   Yukarıdan "Run All" (Tümünü Çalıştır) seçeneğine tıklayarak veya hücreleri sırasıyla (Shift+Enter) çalıştırarak tüm süreçleri baştan sona yürütebilirsiniz.

## Modeller Hakkında
Boyutları nedeniyle modeller GitHub'a yüklenememiş ise, rapor içerisinde yer alan Google Drive bağlantısı üzerinden erişebilirsiniz. (Eğer GitHub'a sığdıysa doğrudan `model` klasöründen ulaşılabilir.)
