+++
title = 'Yazilim'
date = 2025-04-05T19:52:45+03:00
draft = true
+++


# 1
---
## Yazılım nedir?
Bir bilgisayarda donanıma hayat veren belirli bir işi yapması için derlenmiş komutların bütünüdür.

## İyi Bir Yazılımın Özellikleri
**Doğruluk**: Program yapması gereken işi tam ve hatasız bir şekilde yapabilmelidir.
**-Kolay Kullanım**: Programı kullanacak kişiler fazla yardım almadan, kendi başlarına kolayca kullanabilmelidir.
**-Basitlik**: Programın arayüzü mümkün olduğunca sade ve basit olmalıdır.
**-Uyumluluk**(Sistem kararlılığı/uyumluluğu):  Program çalıştığı sistemin üst versiyonlarında da çalışabilmeli, bunlara uyumlu olmalıdır.
**-Taşınabilirlik**: Programın farklı donanımlarda ve uygulamalarda kullanılmasıdır.
**-Tekrar kullanılabilirlik**: Yazılımın tamamının ya da bir kısmının farklı bir projede kullanılmasıdır.

## **Yazılım Türleri**
* **Sistem Yazılımı**: İşletim sistemleri, derleyiciler.
* **Mühendislik/Bilimsel Yazılım**: Hesaplama ve analiz için.
* **Ağ Uygulamaları**: İnternet tabanlı hizmetler.
* **Şirket Yazılımı**: Kurumsal iş süreçlerine özel.
* **Gömülü Yazılım**: Gerçek zamanlı sistemler (örn: otomobil yazılımları).
* **Yapay Zeka Yazılımları**: Makine öğrenimi, uzman sistemler.
* **Eski (Legacy) Yazılım**: Uzun süredir kullanılan sistemler.

#### **Yazılım Geliştirme Süreci**
*   **Ana Aşamalar**:
	1.  Gereksinim Analizi
	1.  Tasarım
	1.  Kodlama
	1.  Test
	1.  Bakım
*   **Destekleyici İşlemler**:
	*   Proje yönetimi, risk yönetimi, belgelendirme, teknik gözden geçirme.

## Çevik Yazılım
→ proje küçük yinemelere ayırılır ve her parça bir projeymiş gibi işlenir. Amaç ortaya hızlı proje çıkartmak

#### **Gereksinim Mühendisliği**
* **Amaç**: Müşteri ihtiyaçlarını eksiksiz ve net bir şekilde belirlemek.
*   **Süreçler**:
	*   Gereksinim toplama → Analiz → Belgeleme → Doğrulama.

**Yazılım Bakımı**; yazılım sadece yapılıp biten bir proje değildir bakımı da vardır:
* Düzeltici Bakım
* Uyarlayıcı Bakım
* İyileştirici Bakım
* Önleyici Bakım

## Kaliteli Yazılım?
1. Gereksinimleri karşılayan,
1. Amaçlanan kullanıma uygun,
1. Zamanında tamamlanmış,
1. Belirlenen bütçe sınırları içinde gerçekleştirilmiş,
1. Standartlara uyumlu,
1. Bakımı sağlanabilen yazılımdır.

## **Yazılım Test Yöntemleri**
* **Kara Kutu Testi**: Kodu bilmeden, İşlevsellik odaklı test.
* **Beyaz Kutu Testi**: Kod bilinerek test senaryoları uygulanıyor.
---

# 2
---
→ yazılımda **veri**yi **bilgi**ye dönüştürmek en önemli araçtır.

## Yazılım Yaşam Döngüsü
* Yazılımın üretim, kullanım ve bakım sürecindeki tüm aşamalar.
* **Tek yönlü değil**: Geri dönüşler ve tekrarlar mümkün.
* **Esnek**: Değişen gereksinimlere adapte olabilir.
1. **Planlama**: Üretilecek yazılımı ile ilgili olarak; personel ve donanım gereksinimlerinin çıkarıldığı, bugünden gelecekte nereye ulaşılmak istendiğinin kararlaştırılmasıdır.
1. **Analiz**: Yazılım işlevleri ile gereksinimlerin ayrıntılı olarak çıkarıldığı aşamadır.
1. **Tasarım**: Analiz aşamasından sonra belirlenen gereksinimlere karşılık verecek yazılım ya da bilgi sisteminin temel yapısının oluşturulması çalışmalarıdır.
1. **Kodlama**: Tasarımdaki veriler doğrultusunda yazılımın kodlama işlemlerinin yapıldığı aşamadır.
1. Test: Uygulama yazılımının hem belirlenen gereksinimleri sağlayıp sağlamadığı hem de gerçekleştirimin beklentilere uygun olup olmadığını kontrol edilir.
1. Bakım: hata giderme ve yeni eklentiler yapma aşamasıdır. Bu aşama, yazılımın tüm yaşamı boyunca sürer.
* Yaşam dönügüsünün temel adımları **çekirdek süreçler(core processes)** olarak da adlandırılır.
* Bu süreçleri gerçekleştirmek için;
	* **Belirtim (specification) yöntemleri** - bir çekirdek sürece ilişkin fonksiyonları
	yerine getirmek amacıyla kullanılan yöntemler
	* **Süreç (process) modelleri** - yazılım yaşam döngüsünde belirtilen süreçlerin
	geliştirme aşamasında, hangi düzen ya da sırada, nasıl uygulanacağını
	tanımlayan modeller
	kullanılır.

## **Yazılım Süreç Modelleri**
|**Model**||**Avantajlar**|**Dezavantajlar**|**Uygun Olduğu Projeler**||
|---|---|---|---|---|---|
|**Gelişigüzel Model**|Herhangi bir yöntem yok. Tamamen yazılımı geliştiren kişiye bağlı.|Hızlı başlangıç, basit. Herkes kullanabilir.|Plansız, riskli, belgeleme yok. Bitiş süresi belirsiz.|Küçük/kişisel projeler.||
|**Barok Modeli**|planlama, çözümleme, tasarım ve
gerçekleştirim işlevleri içermektedir.|"Belgeleme" çok önemli. Yazılım geliştikten hemen sonra belgelenmeli|aşamalar arasındaki geri dönüşlerin nasıl yapılacağının tanımlı olmamasıdır.|günümüzde kullanımı önerilmemektedir.||
|**Çağlayan (Şelale) Modeli**|yazılım yaşam döngüsü adımları baştan sona en az bir kez izlenir. Belgeleme ayrı bir adım değil, yazılımın bir ürünüdür. Adımlar arası ilişkiler vardır(yani geriye dönüş mevcut).|kullanımı basit, yönetimi kolay.iş bölümü ve iş planı projenin en başından belli.|aşamalarda yineleme olabilir, uzun teslimat süresi.gelişime ve değişime elverişsiz.adımlardan oluştuğu için son adıma kadar tamamlanmış değil. Tüm proje çöp olabilir.|İyi tanımlanmış ve yapımı az zaman gerektiren projelerdeçok iyi anlaşılmış projelerde iyi çalışır.||
|**V Modeli**|"V" yapısında bir yol izlenir. Harf şeklinin sol tarafı üretim, sağ tarafı sınama işlemleridir. **Kullanıcı**, **Mimari** ve **Gerçekleştirim** olarak 3 bölümü vardır.**Kullanıcı Modeli: ** kullanıcı ilişkisi ve sistem geneli ile alakalı plan yapılır.**Mimari Modeli:** sistem tasarımı ve sınaması ile ilişkin işlevler.**Gerçekleştirim Modeli:** yazılımın kodlanması ve sınanması.||Esnek değil, risk yönetimi zayıf.Fazlar arasında tekrarlamaları kullanmaz.Aynı zamanda gerçekleştirilebilecek olaylara kolay imkan tanımaz.Yazılım da diğer sistemler gibi zamanla evrimleşir.|Belirsizliklerin az, iş tanımlarının belirgin olduğu projeler için uygun bir modeldir.||
|**Helezonik (Spiral) Model**|risk analizi ön planda.yinelemeli artımsal yaklaşım var.süre. 4 gruba ayrılıyor:**Planlama:** ara ürün planlama,bir önceki ara ürün ile bütünleştirme sağlama.**Risk Analizi:** riski araştır ve belirle.**Üretim:** ara ürün üretilir.**Kullanıcı Değerlendirmesi:** ara ürün hakkında kullanıcının sınama ve değerlendirmeleri ele alınır. |Risk odaklı, iteratif.Yazılımı kullanacak personelin sürece erken katılması ileride oluşabilecek istenmeyen durumları engeller.proje sahibi ve yöneticiler, çalışan yazılımlarla proje boyunca karşılaştıkları için daha kolay izleme planlama yapılır.Yazılımın kodlanması ve sınanması daha erken başlar.Pek çok yazılım modelini içinde
bulundurur.Geliştirmeyi küçük parçalara böler. En riskli kısımlar önce gerçekleştirilir.|Karmaşık, yüksek maliyet.Spiral sonsuza gidebilir.Ara adımların fazlalılığı nedeniyle çok fazla dokümantasyon gerektirir.büyük ölçekteki projeler için.Öznel risk değerlendirme deneyimine dayanır.|Büyük ve riskli projeler.||
|**Hızlı Uygulama Geliştirme (RAD) Modeli**|Çok kısa süreler içinde ortaya çıkartılan kapsamı daraltılmış alt sistemlere ilişkin yazılımlardır.Gerçekleştirimin hızlı yapılabilmesi genelde hazır bileşen tabanlı olmasını gerektirir.adımları;Proje gereksinimlerini tanımlamaPrototip GeliştirmeOluşturma, test ve geri bildirimlerSon şekli verme ve |kısa geliştirme, Hızlı teslimat.Gelişmiş esneklik ve uyarlanabilirlik.Daha iyi risk yönetimi.Daha az manuel kodlama ve daha kısa test süreleri.Sürekli, güncel ve gerçek zamanlı kullanıcı geri bildirimi.|Sınırlı detay, prototip bağımlılığı.|Kısa süreli ticari uygulamalar.||
|**Prototipleme Modeli**|Amacı, ilgili alt modellerde ortaya çıkabilecek belirsizlikleri
azaltmaktır.araştırma türü bir çalışma olabileceği gibi sonradan atılacak bir yazılım parçası da olabilir.Gereksinimler hızlıca toplanarak işe başlanılır.iş adımları:Belirsizliği tanımlaÇözümleri tanımlaPrototip çalışması yapBelirsizliğin sonucunu elde et|Kullanıcı sistem gereksinimlerini
görebilir.Karmaşa ve yanlış anlaşılmaları engeller.Yeni ve beklenmeyen gereksinimler netleştirilebilir.Risk kontrolü sağlanır.|kaynak maliyeti kestirmesi zayıf. ne kadar süreceği bilinmemekte. Yönetimi zor.Belgelendirmesi olmayan hızlı ve kirli prototipler.Düzeltme aşaması atlanırsa, düşük performansa yol açar.Müşteri prototipten de son ürün gibi görünüm ve etki bekler.|Gereksinimler net olmayan projeler.||
|**Artımsal Model**|Üretilen her yazılım sürümü birbirini kapsayacak ve giderek artan sayıda işlev içerecek şekilde geliştirilir.Bir taraftan kullanım, diğer taraftan üretim yapılır.|Parçalı teslimat, risk dağılımı.Sistem için gerekli olan gereksinimler müşterilerle belirlenir.Öncelikle çalışacak ana unsur, çekirdek kısmı sunulur.İlk durumlar prototip gibi görüleceğinden gereksinimler daha iyi anlaşılır.Tüm projenin başarısız olma riskini azaltır.En önemli sistem özellikleri daha fazla test edilme imkanı bulmuş olur.|Tüm sistemin baştan tasarımı zor.Gereksinimleri doğru boyuttaki artımlara atamak bazen zor olabilir.Deneyimli personel gerektirir.Artımların kendi içlerinde tekrarlamalara izin
vermez.|Büyük ve modüler projeler.Uzun zaman alabilecek ve sistemin eksik işlevlikle çalışabileceği türdeki projeler bu modele uygun olabilir.||
|**Evrimsel Geliştirme Süreç Modeli**|İlk tam ölçekli modeldir.Her aşamada üretilen ürünler, üretildikleri alan için tam işlevselliği içermektedirler.Pilot uygulama kullan, test et, güncelle diğer birimlere taşı.Modelin başarısı ilk evrimin başarısına bağımlıdır.|Kullanıcıların kendi gereksinimlerini daha iyi anlamalarını sağlar.Sürekli değerlendirme erken
aşamalardaki geliştirme risklerini azaltır.Hatalar azalır.|Sürecin görünürlüğü azdır (düzenli teslim edilebilir
ürün yoktur).Sistemler sıklıkla iyi yapılandırılmaz (sürekli
değişiklik yazılımın yapısına zarar verir).Bakımı zordur.Yazılım gereksinimini yenilemek gerekebilir.|Coğrafik olarak geniş alana yayılmış, çok birimli organizasyonlar için önerilmektedir (banka uygulamaları). ||
|**Çevik Modeller (Agile Programming)**|İteratif geliştirme temelli bir grup yazılım geliştirme metodolojisine dayanır.Burada gereksinimler ve çözümler kendinden örgütlü olan farklı grupların ortak çalışmasıyla gerçekleştirilir.bir yazılım geliştirme yaklaşımı değil, geliştirme süreçleri topluluğudur.|Esnek, hızlı adaptasyon, müşteri odaklı.Takım oyunu.İnsanın doğal eğilimine çok yatkındır öğrenim gerektirmez adaptasyon hızlıdır.Kısa döngüler dolayısı ile takım elemanlarında motivasyon çok yüksektir. Verim artışı yaşanır.Sık çıktı üretip geri besleme aldığından kaynağı müşteri ihtiyaçlarına ve sonuca kanalize etmeye odaklanır.Değişime açıklık ve esneklik en üst düzeydedir.Proje planlama ve yürütme bir arada.Sürdürülebilir Kalite.|Kurumsal uyum zorluğu, dokümantasyon eksikliği.Sürekli değişen ihtiyaçlar dolayısı ile aşırı çalışma.Ürünün başarısı = projenin başarısı dolayısı ile kariyer riskiTakım üzerindeki hedef baskısı|Değişken gereksinimli projeler.||
