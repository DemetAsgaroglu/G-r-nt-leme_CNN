# Goruntuısleme_CNN

**Görüntü Manipülasyonu ve Model Değerlendirmesi**
Bu proje, bir derin öğrenme modelinin görüntü sınıflandırma görevinde kullanılması üzerine odaklanmaktadır. Model, görüntüler üzerinde yapılan manipülasyonlar ve renk düzeltmeleri ile değerlendirilmiştir. Amacımız, manipüle edilmiş görüntülerin ve renk düzeltmesi yapılan görüntülerin modelin doğruluğu üzerindeki etkisini anlamaktır.

**Proje Hakkında**
Bu proje, görüntü sınıflandırma ve model değerlendirmesi konularında çalışmaktadır. Farklı veri setleri ve görüntü manipülasyonları ile modelin doğruluğu karşılaştırılmaktadır. Modelin eğitimi sırasında, aşağıdaki üç test seti kullanılmıştır:

* Orijinal Test Seti: Değişiklik yapılmamış orijinal görüntüler.
* Manipüle Edilmiş Test Seti: Görüntülerde parlaklık, kontrast gibi manipülasyonlar yapılmış test seti.
* Düzeltilmiş Test Seti: Görüntülerin renk düzeltmesi uygulanmış hali.

**Veri Seti ve Ön İşleme**
Bu projede, görüntü sınıflandırma için uygun bir veri seti kullanılmıştır. Veri seti, etiketli görüntülerden oluşur ve iki ana bölümden oluşmaktadır:

* Eğitim Seti: Modelin eğitilmesi için kullanılan veri seti.
* Test Seti: Modelin doğruluğunu değerlendirmek için kullanılan veri seti.

Veri setine yönelik ön işleme adımları:

* Görüntü Augmentasyonu: Eğitim sırasında veri genişletme teknikleri kullanılır (örneğin, rastgele kırpma, döndürme vb.).
* Normalizasyon: Görüntüler, modelin daha iyi öğrenebilmesi için normalize edilir. 

**Modelin Eğitilmesi ve Değerlendirilmesi**
* Model, derin bir evrişimsel sinir ağı (CNN) mimarisi kullanılarak tasarlanmıştır. Aşağıda modelin ana katmanları bulunmaktadır:
Evrişim Katmanları (Convolutional Layers): Görüntülerin özelliklerini çıkarmak için kullanılır.
Max-Pooling Katmanları: Görüntü boyutlarını küçültmek için kullanılır.
Tam Bağlı Katmanlar (Fully Connected Layers): Özellikler çıkarıldıktan sonra sınıflandırma yapılır. 

* Eğitim Süreci
Kayıp Fonksiyonu (Loss Function): CrossEntropyLoss
Optimizasyon Yöntemi (Optimizer): Adam
Öğrenme Oranı Azaltma: StepLR (Öğrenme oranı 10 adımda bir yarıya düşürülür)
Modelin eğitilmesi sırasında doğruluk (accuracy) ve kayıp (loss) izlenir.

* Model Değerlendirmesi
Model, aşağıdaki üç test setinde değerlendirilmiştir:

Orijinal Test Seti: Modelin orijinal, manipülasyona uğramamış veri seti üzerindeki doğruluğu.
Manipüle Edilmiş Test Seti: Görüntülerdeki renk manipülasyonlarının model doğruluğuna etkisi.
Düzeltilmiş Test Seti: Renk düzeltmesi yapılan görüntüler üzerinde model doğruluğu.

**Görüntü Manipülasyonu ve Düzeltme**
* Manipülasyon
Test görüntüleri üzerinde yapılan manipülasyonlar, parlaklık artırma gibi basit işlemleri içerir. Manipülasyon işleminden sonra, modelin doğruluğu gözlemlenir.

* Renk Düzeltme
Görüntülerdeki renk bozulmalarını düzeltmek için kullanılan teknikler, genellikle renk dengeleme yöntemlerini içerir. Bu düzeltme işlemi sonrası modelin doğruluğu tekrar hesaplanır.

**Sonuçlar ve Görselleştirme**
Modelin doğruluk oranları, aşağıdaki test setlerinde karşılaştırılmaktadır:

Orijinal Test Seti: Doğal ve manipülasyona uğramamış görüntülerle test edilmiş doğruluk.
Manipüle Edilmiş Test Seti: Görüntülerdeki manipülasyonlara karşı modelin doğruluğu.
Düzeltilmiş Test Seti: Renk düzeltme işleminden sonra elde edilen doğruluk. 

Kaggle linki: 
https://www.kaggle.com/code/demetasgaroglu/cnn-g-r-nt-leme

