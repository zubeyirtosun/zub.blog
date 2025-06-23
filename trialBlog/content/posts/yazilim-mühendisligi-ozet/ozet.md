+++
title = 'Ozet'
date = 2025-06-23T18:23:42+03:00
draft = false
+++

# 📚 Yazılım Mühendisliği Ders Notları

## 📋 İçindekiler
1. [Yazılıma Giriş](#1-yazılıma-giriş)
2. [Yazılım Yaşam Döngüsü](#2-yazılım-yaşam-döngüsü) 
3. [Çevik Yazılım Geliştirme](#3-çevik-yazılım-geliştirme)
4. [Sistem Çözümleme ve Gereksinim Mühendisliği](#4-sistem-çözümleme-ve-gereksinim-mühendisliği)
5. [Yazılım Modelleme](#5-yazılım-modelleme)
6. [Yazılım Mimarileri](#6-yazılım-mimarileri)
7. [Yazılım Tasarımı](#7-yazılım-tasarımı)
8. [Yazılım Yapımı/Gerçekleştirimi](#8-yazılım-yapımıgerçekleştirimi)

---

## 1. 💻 Yazılıma Giriş

### 🎯 Yazılım Nedir?
Bir bilgisayarda donanıma hayat veren belirli bir işi yapması için derlenmiş komutların bütünüdür.

### ✅ İyi Bir Yazılımın Özellikleri
- **🎯 Doğruluk**: Program yapması gereken işi tam ve hatasız bir şekilde yapabilmelidir
- **👤 Kolay Kullanım**: Kullanıcılar fazla yardım almadan kolayca kullanabilmelidir
- **🎨 Basitlik**: Arayüz mümkün olduğunca sade ve basit olmalıdır
- **🔄 Uyumluluk**: Sistemin üst versiyonlarında da çalışabilmelidir
- **📦 Taşınabilirlik**: Farklı donanımlarda kullanılabilmelidir
- **♻️ Tekrar kullanılabilirlik**: Farklı projelerde kullanılabilmelidir

### 🏗️ Yazılım Türleri
- **⚙️ Sistem Yazılımı**: İşletim sistemleri, derleyiciler
- **🔬 Mühendislik/Bilimsel Yazılım**: Hesaplama ve analiz
- **🌐 Ağ Uygulamaları**: İnternet tabanlı hizmetler
- **🏢 Şirket Yazılımı**: Kurumsal iş süreçleri
- **🔧 Gömülü Yazılım**: Gerçek zamanlı sistemler
- **🤖 Yapay Zeka Yazılımları**: Makine öğrenimi, uzman sistemler
- **📚 Eski (Legacy) Yazılım**: Uzun süredir kullanılan sistemler

### 🔄 Yazılım Geliştirme Süreci

#### Ana Aşamalar:
1. **📊 Gereksinim Analizi**
2. **🎨 Tasarım**
3. **💻 Kodlama**
4. **🧪 Test**
5. **🔧 Bakım**

#### Destekleyici İşlemler:
- 📋 Proje yönetimi
- ⚠️ Risk yönetimi
- 📝 Belgelendirme
- 👥 Teknik gözden geçirme

### ⚡ Çevik Yazılım
Proje küçük yinemelere ayırılır ve her parça ayrı bir proje gibi işlenir. **Amaç**: Hızlı proje çıkartmak.

### 🔧 Yazılım Bakım Türleri
- **🩹 Düzeltici Bakım**: Hataları giderme
- **🔄 Uyarlayıcı Bakım**: Yeni ortamlara uyarlama
- **⬆️ İyileştirici Bakım**: Performans iyileştirmeleri
- **🛡️ Önleyici Bakım**: Gelecekteki sorunları önleme

### ⭐ Kaliteli Yazılım Kriterleri
1. ✅ Gereksinimleri karşılayan
2. 🎯 Amaçlanan kullanıma uygun
3. ⏰ Zamanında tamamlanmış
4. 💰 Bütçe sınırları içinde
5. 📋 Standartlara uyumlu
6. 🔧 Bakımı sağlanabilen

### 🧪 Test Yöntemleri
- **⚫ Kara Kutu Testi**: Kodu bilmeden işlevsellik testi
- **⚪ Beyaz Kutu Testi**: Kod bilinerek test

---

## 2. 🔄 Yazılım Yaşam Döngüsü

> **Temel İlke**: Yazılımda **veri**yi **bilgi**ye dönüştürmek en önemli araçtır.

### 📋 Yaşam Döngüsü Tanımı
- Yazılımın üretim, kullanım ve bakım sürecindeki tüm aşamalar
- **↔️ Tek yönlü değil**: Geri dönüşler ve tekrarlar mümkün
- **🔄 Esnek**: Değişen gereksinimlere adapte olabilir

### 🗂️ Yaşam Döngüsü Aşamaları
1. **📋 Planlama**: Kaynak ve gereksinim belirleme
2. **🔍 Analiz**: İşlev ve gereksinim detaylandırma
3. **🎨 Tasarım**: Sistem temel yapısı oluşturma
4. **💻 Kodlama**: Tasarımı koda dönüştürme
5. **🧪 Test**: Gereksinim karşılama kontrolü
6. **🔧 Bakım**: Hata giderme ve iyileştirme

### 📊 Yazılım Süreç Modelleri Karşılaştırması

| Model | Açıklama | ✅ Avantajlar | ❌ Dezavantajlar | 🎯 Uygun Projeler |
|-------|----------|-------------|----------------|------------------|
| **🎲 Gelişigüzel** | Yöntemsiz geliştirme | Hızlı başlangıç | Plansız, riskli | Küçük projeler |
| **🏛️ Barok** | Planlama odaklı | Belgeleme güçlü | Geri dönüş yok | Artık kullanılmıyor |
| **🌊 Çağlayan** | Sıralı aşamalar | Basit yönetim | Uzun teslimat | İyi tanımlanmış projeler |
| **✅ V Modeli** | V şeklinde test | Her aşamada doğrulama | Esnek değil | Belirsizliği az projeler |
| **🌀 Spiral** | Risk odaklı yinelemeli | Risk yönetimi | Karmaşık, pahalı | Büyük riskli projeler |
| **⚡ RAD** | Hızlı geliştirme | Çabuk teslimat | Sınırlı detay | Kısa süreli projeler |
| **🔬 Prototip** | Belirsizlik azaltma | Kullanıcı görür | Maliyet belirsiz | Belirsiz gereksinimler |
| **📈 Artımsal** | Kademeli büyüme | Risk dağılımı | Tasarım zorluğu | Büyük modüler projeler |
| **🧬 Evrimsel** | Tam işlevli sürümler | Sürekli değerlendirme | Görünürlük az | Geniş organizasyonlar |
| **🚀 Çevik** | İteratif metodolojiler | Esnek adaptasyon | Kurumsal uyum zor | Değişken gereksinimler |

---

## 3. 🚀 Çevik Yazılım Geliştirme

### 🎯 Çevik Yazılım Tanımı
Piyasaya çabuk ürün çıkarma, değişen isteklere hızlı yanıt verme ve kısa sürede yazılım ürününü müşteri hizmetine sunma amaçlı metodolojilerdir.

### 📜 Çevik Manifesto (2001)
Kent Beck ve 16 çevik temsilci tarafından yayınlandı.

#### 🌟 4 Temel Değer:
1. **👥 Bireyler ve etkileşimler** > Süreçler ve araçlar
2. **💻 Çalışan yazılım** > Kapsamlı dokümantasyon
3. **🤝 Müşteri ile işbirliği** > Sözleşme pazarlıkları
4. **🔄 Değişikliğe açıklık** > Plana bağlılık

#### 📋 12 Prensip:
- 😊 Müşteri memnuniyeti (hızlı ve sık teslimat)
- 🔄 Değişiklikleri her zaman kabul etme
- 📊 Çalışan yazılım = İlerleme ölçütü
- 💬 Sürekli ekip iletişimi
- 🎯 Motive olmuş ve yüz yüze iletişim
- 🎨 Basitlik ve teknik mükemmellik
- 🔄 Kendi kendini organize eden ekipler

### 🔥 Extreme Programming (XP)

#### 🌟 Temel Değerler:
- **💬 İletişim**: Yazılım ekibi ile kullanıcılar arası sıkı bağ
- **🎨 Basitlik**: Karmaşık çözümlerden kaçınma
- **🔄 Geri Bildirim**: Müşterilerle düzenli buluşmalar
- **💪 Cesaret**: Başarısızlıktan korkmama

#### 🛠️ XP Pratikleri:
- 🎯 **Artımlı planlama** (Planlama Oyunu)
- 👤 **Her zaman hazır müşteri**
- 🧪 **Test-önce geliştirme**
- 🎨 **Sade tasarım**
- 👥 **Çiftli programlama**
- 🔄 **Sürekli entegrasyon**
- 📦 **Küçük sürümler**
- 🔧 **Yeniden düzenleme**
- 🎭 **Benzetim**
- 🤝 **Ortak sahiplik**
- 📋 **Kodlama standartı**
- ⏰ **Sürdürülebilir hız** (40 saat/hafta)

### 🏃‍♂️ Scrum Metodolojisi

#### 👥 Roller:
- **📋 Ürün Sahibi**: Gereksinimleri belirler ve önceliklendirir
- **🏃‍♂️ Scrum Master**: Süreci yönetir ve engelleri kaldırır
- **👨‍💻 Geliştirme Takımı**: 3-9 kişi, kendi kendini organize eder

#### 🔄 Sprint Döngüsü:
1. **📋 Sprint Planlama**: Hedef ve görev belirleme
2. **☀️ Günlük Scrum**: 15 dakikalık toplantı
3. **👁️ Sprint Review**: Çıktıları müşteriye sunma
4. **🔄 Sprint Retrospective**: Süreç iyileştirme

---

## 4. 🔍 Sistem Çözümleme ve Gereksinim Mühendisliği

### 🎯 Sistem Çözümleme
- Üretim sürecinin başlangıcı
- Mevcut sistemin işleyişini araştırma
- **❗ Zorunluluk**: Mutlaka bir model/yöntem kullanma

### 📋 Gereksinim Tanımı
Bir sistemin veya yazılımın yerine getirmesi gereken **işlevsel ve işlevsel olmayan ihtiyaçlar**.

#### 🎯 Gereksinim Özellikleri:
1. 👨‍💻 Geliştiricilere müşteri isteklerini anlama
2. 🎨 Tasarımcılara sistem özelliklerini gösterme
3. 🧪 Test ekibine doğrulama yöntemlerini sunma

### 📊 Gereksinim Türleri

#### 👤 Kullanıcı Gereksinimleri:
- Son kullanıcı ihtiyaçları
- **Örnek**: "Sistem, kullanıcının randevu alabilmesini sağlamalıdır"

#### ⚙️ Sistem Gereksinimleri:
- Teknik detaylar ve kısıtlar
- **Örnek**: "Sistem, 1000 eşzamanlı kullanıcıyı desteklemelidir"
- **🎯 Hedef**: Yazılım geliştiriciler, sistem mimarları

#### 🔧 Fonksiyonel vs Fonksiyonel Olmayan:
- **🔧 Fonksiyonel**: Sistemin **ne yapacağını** tanımlar
- **⚡ Fonksiyonel Olmayan**: Sistemin **nasıl çalışacağını** tanımlar

### 🔄 Gereksinim Mühendisliği Süreci

#### 1. 🕵️ Gereksinimlerin Açığa Çıkarılması

**🛠️ Yöntemler**:
- 💬 Karşılıklı görüşme
- 📊 Anket uygulaması
- 👁️ Etnografya (gözlem)

**❓ Soru Tarzları**:
- **🔺 Piramit**: Özel → Genel
- **🔻 Koni**: Genel → Özel
- **💎 Elmas**: Özel → Genel → Özel

#### 2. 🔍 Gereksinimlerin Analizi
Sınıflandırma ve önceliklendirme

#### 3. 📝 Gereksinimlerin Tanımlanması
- Doğal dil tanımları
- UML kullanım durumları (Use Case)
- Form tabanlı tanımlar

#### 4. ✅ Gereksinimlerin Doğrulanması
**📋 Kontrol**: Geçerlilik, tutarlılık, eksiksizlik, uygulanabilirlik

---

## 5. 🎨 Yazılım Modelleme

### 🎯 UML (Unified Modeling Language)

#### 📖 Tanım
Yazılım sistemlerinin **görselleştirme**, **tasarlama** ve **belgeleme** için standart modelleme dili.

#### 📊 UML Diyagram Türleri

##### 🏗️ Yapısal Diyagramlar:
- **📋 Sınıf Diyagramları**: Sınıflar ve ilişkileri
- **🎯 Nesne Diyagramları**: Sınıfların örnekleri
- **🔧 Bileşen Diyagramları**: Yazılım bileşen etkileşimi
- **🌐 Dağıtım Diyagramları**: Sistemin fiziksel dağılımı

##### 🎭 Davranışsal Diyagramlar:
- **👤 Use Case**: Kullanıcı-sistem etkileşimi
- **🔄 Durum**: Nesnenin durum değişiklikleri
- **📞 Sequence**: Nesneler arası mesajlaşma
- **⚡ Etkinlik**: İş süreçleri ve adımları

#### ✅ UML Avantajları:
1. 🐛 Hata azaltma
2. ♻️ Tekrar kullanılabilirlik
3. 💬 İletişim kolaylığı
4. 📝 Dokümantasyon
5. 💰 Maliyet düşürme
6. ⭐ Kalite artırma

---

## 6. 🏗️ Yazılım Mimarileri

### 🎯 Mimari Tanımı
Tüm sistemin organizasyonu ve iskeleti. Yazılım öğelerini, ilişkilerini ve özelliklerini içerir.

### ✅ Mimari Belgeleme Avantajları:
- 💬 **Paydaş İletişimi**: İletişimi kolaylaştırır
- 🔍 **Sistem Analizi**: Fonksiyonel olmayan gereksinimleri kontrol
- ♻️ **Yeniden Kullanım**: Birden fazla sistemde kullanım

### 🏛️ Popüler Mimari Desenleri

#### 1. 🎭 Model View Controller (MVC)
- **📊 Model**: Veri ve işlem yönetimi
- **👁️ View**: Kullanıcı arayüzü
- **🎮 Controller**: Kullanıcı etkileşimi

**✅ Avantaj**: Veri-görünüm bağımsızlığı  
**❌ Dezavantaj**: Basit sistemlerde karmaşıklık

#### 2. 📚 Katmanlı Mimari
- Her katman farklı işlevsellik
- Tek yönlü etkileşim
- Üst katmana hizmet

**✅ Avantaj**: Katman bağımsızlığı  
**❌ Dezavantaj**: Temiz ayrım zorluğu

#### 3. 🗄️ Depo Mimarisi
- Merkezi veri deposu
- Bileşenler depo üzerinden etkileşim

**✅ Avantaj**: Bileşen bağımsızlığı  
**❌ Dezavantaj**: Merkezi nokta riski

#### 4. 🌐 İstemci-Sunucu
- İstemci istek yapar
- Sunucu karşılar
- Ağ üzerinde dağıtılabilir

**✅ Avantaj**: Dağıtılabilirlik  
**❌ Dezavantaj**: Ağ bağımlılığı

#### 5. 🔄 Boru & Filtre
- Sıralı işleme
- Her filtre veri işler ve aktarır

**✅ Avantaj**: Anlaşılabilirlik  
**❌ Dezavantaj**: Format kararlaştırma

---

## 7. 🎨 Yazılım Tasarımı

### 🎯 Tasarım Tanımı
Mantıksal modelin fiziksel modele dönüştürülmesi. **İlke**: Önce tasarım, sonra kod!

### 🗂️ Tasarım Aşamaları:
1. **💾 Veri Tasarımı**: Bilgileri veri yapılarına dönüştürme
2. **🏗️ Mimari Tasarım**: Yapısal parçaları tanımlama
3. **⚙️ Yordamsal Tasarım**: Yordam ve fonksiyonlara dönüştürme
4. **🖥️ Arayüz Tasarımı**: İnsan-makine etkileşimi

### 🌟 Temel İlkeler:
- **🔍 Soyutlama**: Detayları gizleyerek üst düzey bakış
- **✨ İyileştirme**: Soyutlama sonrası düzeltme ve detaylandırma

### 🖥️ Kullanıcı Arayüz Tasarımı

#### 📋 Temel İlkeler:
1. 📖 Anlaşılabilir dil
2. 🔄 Mantıksal sıralama
3. ⚡ Hızlı bilgi girişi
4. 📊 Gerekli ve yeterli bilgi
5. 🎨 Tekdüzelik
6. ⚙️ Fonksiyonellik
7. 🚫 Çelişkisizlik
8. 📚 Kılavuz desteği
9. ✅ İşlem doğrulama
10. 🎓 Kolay öğrenim

### 📊 Kalite Ölçütleri

#### 🔗 Bağlaşım (Coupling) - Az olmalı:
- **📄 Yalın Veri**: Basit veri türleri
- **📊 Karmaşık Veri**: Yapısal veri türleri
- **🎮 Denetim**: Kontrol verisi
- **🗃️ Ortak Veri**: Paylaşılan alan
- **🔗 İçerik**: İç içe modüller

#### 🧲 Yapışıklık (Cohesion) - Yüksek olmalı:
- **🎯 İşlevsel**: Tek problem çözme
- **📈 Sırasal**: Çıktı-girdi ilişkisi
- **💬 İletişimsel**: Aynı veri kullanımı
- **⚡ Yordamsal**: Denetim ilişkisi
- **⏰ Zamansal**: Zaman bağımlılığı
- **🧠 Mantıksal**: Aynı tür işlemler
- **🎲 Gelişigüzel**: İlişkisiz işlemler

---

## 8. 🔨 Yazılım Yapımı/Gerçekleştirimi

### 🎯 Yapım Tanımı
**Kodlama**, **doğrulama**, **birim test**, **entegrasyon test** ve **hata ayıklama** kombinasyonu ile yazılım oluşturma.

### 🌟 Yapımın Temelleri:
- **🎨 Karmaşıklığı Azaltma**: Basit ve okunabilir kod
- **🔮 Değişimi Öngörme**: Alt yapıyı bozmadan geliştirme
- **✅ Doğruluğu Sağlama**: Kolay hata bulma
- **♻️ Yeniden Kullanım**: İki yönlü yaklaşım
- **📋 Yapım Standartları**: Kural uyumu

### 🛠️ Pratik Hususlar

#### 1. 🎨 Yapım Tasarımı
Kodlama öncesi tasarım çalışmaları

#### 2. 💻 Yapım Dilleri
Problem çözme iletişim biçimleri

#### 3. 📝 Kodlama
- 🎨 Kod düzeni ve adlandırma
- 📋 Sınıf/değişken kullanımı
- 🔄 Kontrol yapıları
- ⚠️ Hata yönetimi
- 🔐 Güvenlik önlemleri
- 📁 Kod organizasyonu
- 📝 Belgelendirme

#### 4. 🧪 Yapım Testleri
- **🔍 Birim Testi**: Bireysel modül testleri
- **🔗 Entegrasyon Testi**: Modül etkileşim testleri

### 🛠️ Yapım Araçları
Modern IDE özellikleri:
- 🔨 Editör içi derleme
- 📂 Kaynak kod kontrolü
- 🧪 Test/hata ayıklama
- 🔄 Otomatik dönüşümler
- 🔧 Kod yeniden düzenleme

### 🌟 Temel Yazılım İlkeleri:
1. **🔍 Soyutlama**: Tekrar önleme
2. **🔒 Bilgi Gizleme**: Gerekli saklama
3. **🤖 Otomasyon**: Çalışma zamanı
4. **🛡️ Çok Düzeyli Koruma**: Seviyeli önlem
5. **🏷️ Etiketleme**: Anlam kazandırma
6. **🔍 Belirgin Arayüz**: Açık tasarım
7. **📦 Taşınabilirlik**: Donanım bağımsızlığı
8. **🔐 Güvenlik**: Veri/erişim koruma
9. **🎨 Basitlik**: Karmaşıklıktan uzak
10. **📋 Genel Yapı**: Kural uyumu
11. **🔄 Tutarlılık**: Anlamsal benzerlik
12. **♾️ Esneklik**: Sabit kısıtlamalardan kaçınma

---

## 🎯 Sonuç

Bu ders notları yazılım mühendisliğinin temel konularını kapsamlı bir şekilde ele almaktadır. Yazılım geliştirme sürecinin her aşamasında aşağıdaki faktörler kritik öneme sahiptir:

### 🔑 Anahtar Başarı Faktörleri:
- **⭐ Kalite**: Her aşamada kalite kontrol
- **⚡ Verimlilik**: Kaynakların optimal kullanımı  
- **🌱 Sürdürülebilirlik**: Uzun vadeli bakım ve geliştirme
- **🔄 Esneklik**: Değişen ihtiyaçlara adaptasyon

### 🚀 Modern Yaklaşım:
Çevik yöntemler günümüzde yaygın kullanılsa da, **proje türüne göre uygun metodoloji seçimi** kritik önem taşımaktadır. Her projenin kendine özgü gereksinimleri vardır ve bu gereksinimlere en uygun yaklaşımın seçilmesi projenin başarısını doğrudan etkiler.

---

**📝 Not**: Bu notlar temel yazılım mühendisliği konseptlerini kapsar ve sürekli güncellenen bir alandaki temel bilgileri sunar. 
