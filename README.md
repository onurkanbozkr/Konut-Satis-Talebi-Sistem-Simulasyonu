# Türkiye'de Konut Satış Talebinin Sistem Simülasyonu ile Analizi

Bu proje, **Sistem Modelleme ve Simülasyonu** dersi kapsamında gerçekleştirilmiştir. Çalışmada Türkiye'deki aylık toplam konut satış talebi, geçmiş dönem verileri kullanılarak olasılıksal bir sistem simülasyonu yaklaşımıyla analiz edilmiştir.

Projenin temel amacı, konut satış talebindeki değişkenliği ve belirsizliği bir olasılık dağılımı ile modelleyerek gelecek dönemlere yönelik olası talep değerleri üretmektir.

## Proje Kapsamı

Çalışma kapsamında aşağıdaki adımlar gerçekleştirilmiştir:

* TÜİK konut satış verilerinin hazırlanması ve düzenlenmesi
* Aylık toplam konut satış verilerinin analizi
* Betimsel istatistiklerin hesaplanması
* Grafiksel veri analizi ve dağılım özelliklerinin incelenmesi
* EasyFit ile teorik olasılık dağılımlarının karşılaştırılması
* Kolmogorov-Smirnov, Anderson-Darling ve Ki-Kare uygunluk testlerinin uygulanması
* Uygun dağılımın belirlenmesi
* Seçilen dağılım kullanılarak sistem simülasyonunun oluşturulması
* 12 aylık konut satış talebi için rassal değerlerin üretilmesi
* Simülasyon sonuçlarının gerçek verilerle karşılaştırılması
* Model doğrulamasının gerçekleştirilmesi

## Veri Seti

Çalışmada **Türkiye İstatistik Kurumu (TÜİK)** tarafından yayımlanan konut satış istatistiklerinden yararlanılmıştır.

Analizde **2024 Ocak – 2025 Temmuz** dönemine ait toplam 19 aylık konut satış verisi kullanılmıştır.

Modelin temel girdisi:

> Aylık toplam konut satış sayısı

olarak belirlenmiştir.

## Veri Analizi

İlk aşamada konut satış verileri düzenlenmiş ve analiz için uygun formata getirilmiştir.

Veri seti üzerinde:

* Gözlem sayısı
* Ortalama
* Standart sapma
* Minimum ve maksimum değerler
* Değişim katsayısı

gibi betimsel istatistikler incelenmiş ve konut satışlarının aylara göre değişkenliği grafiklerle değerlendirilmiştir.

## EasyFit ile Dağılım Analizi

Aylık konut satış verilerinin hangi teorik olasılık dağılımına uygun olduğunu belirlemek amacıyla **EasyFit** programı kullanılmıştır.

Dağılımların veri setine uygunluğu:

* Kolmogorov-Smirnov
* Anderson-Darling
* Ki-Kare

uygunluk testleri kullanılarak değerlendirilmiştir.

Analiz sonucunda **Genelleştirilmiş Gamma dağılımı**, simülasyon modelinde kullanılmak üzere uygun dağılım olarak belirlenmiştir.

## Simülasyon Modeli

Seçilen Genelleştirilmiş Gamma dağılımının parametreleri kullanılarak aylık konut satış talebi olasılıksal bir değişken olarak modellenmiştir.

Modelin temel yapısı:

```text
TÜİK Konut Satış Verileri
          ↓
   Veri Hazırlama
          ↓
  Betimsel İstatistik
          ↓
   EasyFit Dağılım Analizi
          ↓
  Uygunluk Testleri
          ↓
Genelleştirilmiş Gamma
          ↓
    Sistem Simülasyonu
          ↓
12 Aylık Talep Üretimi
          ↓
    Model Doğrulama
```

## Simülasyon Sonuçları

EasyFit kullanılarak oluşturulan 12 aylık simülasyon sonucunda ortalama aylık konut satış talebi:

**119.572**

olarak hesaplanmıştır.

Geçmiş verilerin ortalaması ise **121.725** olarak bulunmuştur. Simülasyon ortalaması ile geçmiş veri ortalamasının birbirine yakın olması, modelin geçmiş verideki genel eğilimi temsil edebildiğini göstermektedir.

## Model Doğrulama

Modelin gerçek verilerle uyumu değerlendirilmek amacıyla veri seti yaklaşık olarak:

* %90 eğitim verisi
* %10 doğrulama verisi

şeklinde ayrılmıştır.

2025 Haziran ve 2025 Temmuz verileri doğrulama amacıyla kullanılmış ve model ile gerçek değerler karşılaştırılmıştır.

Karşılaştırma sonucunda **ortalama yüzde hata %13,65** olarak hesaplanmıştır.

## Kullanılan Araçlar

* **Microsoft Excel**
* **EasyFit**
* **TÜİK Konut Satış Verileri**

## Proje Dosyaları

| Klasör / Dosya | Açıklama                           |
| -------------- | ---------------------------------- |
| `rapor/`       | Proje raporu                       |
| `gorseller/`   | Analiz ve simülasyon çıktıları     |

## Proje Çıktısı

Bu çalışma ile gerçek konut satış verilerinden hareketle, talepteki belirsizlik ve değişkenliği dikkate alan olasılıksal bir sistem simülasyonu modeli oluşturulmuştur.

Model, geçmiş verilerden elde edilen dağılımı kullanarak gelecek dönemlerde oluşabilecek konut satış talebi için olası değerler üretmektedir.

## Geliştirilebilecek Alanlar

Gelecek çalışmalarda modele daha uzun dönemli verilerin yanı sıra:

* Faiz oranları
* Enflasyon
* Konut kredisi hacmi
* Bölgesel konut satışları
* Ekonomik göstergeler

gibi değişkenlerin dahil edilmesiyle daha kapsamlı bir model oluşturulabilir.

## Proje Ekibi

**Onurkan Bozkır** ve proje ekip arkadaşları.

## Kaynaklar

* Türkiye İstatistik Kurumu (TÜİK) — Konut Satış İstatistikleri
* MathWave Technologies — EasyFit
* Law, A. M. — Simulation Modeling and Analysis
* Banks, J. et al. — Discrete-Event System Simulation
* Montgomery, D. C. & Runger, G. C. — Applied Statistics and Probability for Engineers
