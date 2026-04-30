# 🧬 Meme Kanseri Teşhisi: Makine Öğrenmesi ile Sınıflandırma Analizi

Bu çalışma, sağlık teknolojilerinde yapay zeka kullanımını odak noktasına alarak, klinik veriler üzerinden tümörlerin **İyi Huylu (Benign)** veya **Kötü Huylu (Malignant)** olup olmadığını yüksek doğrulukla tahmin etmeyi amaçlar.



## 📝 Proje Vizyonu
Medikal verilerin analizinde hata payını minimize etmek, erken teşhis süreçlerini hızlandırmak için kritik bir adımdır. Bu repo içerisinde, popüler denetimli öğrenme (supervised learning) algoritmalarının performansları karşılaştırılmış ve en optimize sonuç veren model belirlenmiştir.

---

## 📊 Veri Seti İncelemesi
* **Künye:** Scikit-learn kütüphanesinde yer alan *Wisconsin Breast Cancer Dataset*.
* **Kapsam:** 569 hastaya ait tıbbi kayıt ve her kayıt için 30 farklı biyolojik özellik (hacim, doku, simetri vb.).
* **Hedef:** İkili sınıflandırma (0: Kanser Riski Yüksek, 1: Sağlıklı/İyi Huylu).
* **Not:** Veri setinde sınıflar arası sayısal bir dengesizlik (%62'ye %38) bulunmaktadır; bu durum model seçimi aşamasında titizlikle değerlendirilmiştir.

---

## 🛠️ Uygulanan Metodoloji
Analiz süreci şu teknik adımlardan oluşmaktadır:
1.  **Veri Temizleme:** Eksik değer analizi yapılarak veri bütünlüğü doğrulandı.
2.  **Ölçeklendirme:** Modellerin performansını artırmak amacıyla `StandardScaler` kullanılarak özellikler standart hale getirildi.
3.  **Model Eğitimi:** Veri kümesi %80 eğitim, %20 test olacak şekilde ayrıştırıldı.
4.  **Hata Analizi:** Sadece başarı oranına (accuracy) odaklanılmamış, aynı zamanda hassasiyet ve geri çağırma metrikleri incelenmiştir.

---

## 🤖 Algoritmalar ve Performans Karnesi

Proje kapsamında 4 farklı yaklaşım test edilmiştir:

| Algoritma | Karakteristik Özellik | Başarı Skoru |
| :--- | :--- | :--- |
| **Logistic Regression** | Lineer modeller arasında en dengeli ve başarılı sonucu verdi. | **%98.25** |
| **Random Forest** | Çoklu karar mekanizmasıyla güvenli sonuçlar üretti. | %93.86 |
| **K-Nearest Neighbors** | Veri noktalarının birbirine olan yakınlığı üzerinden sınıflandırma yaptı. | %93.86 |
| **Decision Tree** | Karmaşık kurallar setinde kaybolduğu için hafif "overfitting" eğilimi gösterdi. | %91.22 |



---

## ⚠️ Kritik Değerlendirmeler & Gelecek Planları
* **Model Lideri:** Lojistik Regresyon, veri setinin yapısı gereği en tutarlı tahminleri gerçekleştirmiştir.
* **Geliştirme Alanı:** Mevcut sonuçlar tek bir veri ayrımına dayanmaktadır. İleride **K-Fold Cross-Validation** eklenerek modellerin genelleme yeteneği artırılabilir.
* **Optimizasyon:** Random Forest modeli için hiper-parametre ayarlamaları (GridSearch) yapılarak daha üst seviye sonuçlar hedeflenebilir.

---

## 💻 Kullanım Klavuzu
Projeyi yerelinizde veya bulut ortamında denemek için:
1.  GitHub üzerinden `clone` edin veya `.ipynb` dosyasını indirin.
2.  Google Colab veya Jupyter Notebook üzerinde dosyayı açın.
3.  Aşağıdaki kütüphanelerin yüklü olduğundan emin olun:
    ```bash
    pip install scikit-learn pandas numpy matplotlib seaborn
    ```
4.  Tüm hücreleri sırasıyla çalıştırarak analiz çıktılarını gözlemleyin.

---
