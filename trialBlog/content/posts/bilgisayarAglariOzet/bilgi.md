+++
title = 'Bilgi'
date = 2025-04-05T13:45:32+03:00
draft = true
+++

Burası derste işlenenlerin kendimce önemli görülen, yazmak istediğim, üşenmediği
m kısımları bulundurmaktadır. Bir başkasına göre eksiklikler görülebilir ki ben
bile görüyorum xd

tüm özetin esinlendiği ders kaynağı: https://ozalpmurat.github.io/BilgisayarAglari-Kitap/02-Topolojiler/

# nasıl kullanılmalı?
En az bir kez asıl kitabı oku, anlamadığın yer varsa buraya bir bak, farklı şekilde yazmış olabilirim ya da direkt copy paste atmış da olabilirim. Bir kez okuduktan sonra tekrar niyetine buradan göz gezdirilebilir.

---


![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B02-Topolojiler.jpg)

### Ağ Topolojileri
#### Doğrusal (Bus) Topoloji
* Herkes herkesin trafiğini görebilir kontrol yok.
* Koaksiyel (televizyon) kablosu kullanılır.
* Kablonun herhangi bir yerinde sorun olması tüm ağı etkiler.
* Aynı anda iki bilgisayar veri gönderemez.
#### Halka (Ring) Topoloji
* Doğrusal Topoloji'nin gelişmişi.
* Jeton(token) var gideceği yeri biliyor. Herkes veriye ulaşmıyor.
* Aynı anda iki bilgisayar veri gönderemez.
#### Yıldız (Star) Topoloji
* Klasik Switch özellikleri.
* Ortada bir dağıtıcı cihaz var.
* Arıza sadece bulunan bilgisayarı etkiliyor.
#### Örgü (Mesh) Topoloji
* O ona, bu buna bağlı.
* Kablosuz ağlarda da yaygın olarak kullanılır.

### OSI Modeli
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B03-OSI_ve_TCPIP.jpg)
**OSI Modeli** → Ağ elemanlarının nasıl çalıştığını ve verinin iletimi sırasında hangi işlemlerden geçtiğini kavramak için kullanılan rehberdir.

#### OSI Modeli Katmanları
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B03-OSI_Katmanlar-2.png)

##### Fiziksel Katman
* 1 ve 0'larla elektriksel sinyallerle haberleşiyor.
* Sayısal haberleşmede en küçük birim bit olduğundan bu katmanın hızı **bps, b/s (bit/saniye)** cinsindendir.
* Bakır ve fiber optik kablolar, RF (Antenler), Sinyali (işareti) elektrik olarak yükselten ve çoklayan HUB cihazları, Tekrarlayıcılar (repeater), Kablosuz iletişimde kullanılan hava.
##### Veri Bağlantı Katmanı
* Basit kontrol mekanizmaları çalışıyor.
* En çok kullanılan hata bulma algoritmaları **eşlik biti (parity check)** ve **CRC algoritmasıdır**.
> IP'yi MAC adresine dönüştürme —> **ARP**
> internet adresini IP'ye dönüştürme —> **DNS**

Verinin doğru olup olmadığına bakmaz, sadece
sağlamlığını kontrol eder. Bu katmanda üst katmandan gelen veriler
çerçeve (frame) adı verilen paketleme işlemine tabi tutulur. Kapsülleme
de denir. Birbirine doğrudan bağlı ağ cihazlarının aynı kapsülleme
yöntemini (ikinci katman protokolünü) kullanması gerekir.
> 2.katman - Çerçeve/kapsül , 3.katman - paket, 4.katman - segment
###### LAN ve WAN nedir?
> **Fark ne?**: LAN'da istediğimiz kablolama türü ve istediğimiz protokolü kullanabiliriz. Hiç bir kısıtlama olmadan ağa bağlanabiliriz. WAN'da ise servis sağlayıcının sunduğu hizmetlerden ve onun kurallarına uyarak bağlanabiliriz.

**Anahtarlama Türleri** →  Veri aktarımı, fiziksel değişiklikle yapılırsa **Devre Anahtarlama,**  her bir veri paketi için hesaplanarak, yazılımsal olarak yapılırsa **Paket Anahtarlama**dır.

##### Ağ Katmanı (IP)
> Port 4  —> Segment
IP          —> Paket
MAC     —> Çerçeve (frame), kapsül
IP   —> Apartman Port   —> kapı numarası benzetmeleri yapılabilir.
* IP yönlendirilebilir bir protokol olduğundan her türlü veri ağı üzerinden
haberleşmeye olanak sağlar. Bu katman en önemli görevi yönlendirme
işlemidir. Yönlendirme işlemi birden fazla ağ arayüzüne (network
interface) sahip olan yönlendirici(router) adı verilen cihazlar
tarafından yapılır.
> 3. katmanda aktarılan verinin en küçük anlamlı birimine `paket` denir.
* IP internetin temel protokolüdür.
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B03-AglarArasiBaglanti.png)

##### Taşıma Katmanı
* IP üzerinde kullanılan bu katmanda 2 tane protokol vardır. Bunlar `TCP` ve `UDP`'dir. 
* **TCP**: Bağlantı temelli bir protokoldür. Trafik başlamadan önce karşıdaki uca müsait olup olmadığı sorulur. Bu yönüyle telefon görüşmesine benzer.
* **UDP**: Bağlantı temelli değildir. Trafik doğrudan başlatıldığı için paketlerin iletimi garanti edilmez. SMS gönderimine benzetilebilir. Özellikle gerçek zamanlı görüntü ve ses taşıma uygulamalarında elverişlidir. TCP’ye göre daha hızlıdır.
> TCP kontrol sistemi vardır. UDP'de yoktur; veri gitti mi, başarılı mı bilinmez!
> Dördüncü katmanın bir başka görevi de üst katmanlardan gelen veriyi
bölümleyerek daha küçük parçalara ayırmaktır. Bu parçalara `segment`
denir.
Örneğin; HTTP üzerinden 1GB'lık program indireceksek ve 80 segment halinde karşıya gönderilecekse, `1/80, 2/80, ..., 80/80` şeklinde parçalanarak ve her bir segmente numara eklenerek karşıya iletilir.

##### Uygulama Seviyesi Katmanları
```Bash
nslookup obs.bilecik.edu.tr 192.168.120.3
# just checking dns address of obs.bilecik.edu.tr
```
> ICMP —> Ping
* **ping** (hping): Karşı uç ile aramızda 3. katmanda 
bağlantı var mı? Paketler kaç milisaniyede gidip geliyor? Büyük paketler
 ve küçük paketler ağdan aynı şekilde gidebiliyor mu?
* **traceroute (tracert)**: Uzaktaki bir sisteme IP üserinden hangi rotadan gittiğimizi gösterir. ICMP kapalı olan sistemlerde `TCP Trace` denenebilir.
* **Telnet**: Ağlarda yönetim ve kontrol amaçlı kullanılır. Ağ cihazlarının genellikle tamamı telnet ile yönetimi destekler. Bunun dışında, 2 cihaz arasında 4. katmanda bağlantı (erişebilirlik) kontrolü yapmak için de kullanılır. Örneğin SMTP veya HTTP gibi protokoller, Telnet ile çalıştırılabilir.
* **netstat**: kullanılan bilgisayarda hangi portların,hizmetlerin açık olduğu görülebilir.
* **nmap**: herhangi bir ip üzerinde(ağ üzerinde) açık olan portları,hizmetleri görüntüler.
* **wireshark**: bakılan bilgisayardan gelen ve giden ağ trafiği gözlemlenir. (ekstra bilgi: ethernet kartını okuyarak çalışır.)
* **TCPView(Microsoft)**

> hedef ip 255.255.255.255 olduğunda **broadcast**(ağdaki herkese) yayın yapar.

# Temel Kavramlar
**MTU (**_Maximum Transmission Unit)_** **—> Bir seferde gönderilebilecek maksimum veri miktarını belirler. Ethernet ağlarında MTU değeri varsayılan olarak **1500 bayt/kapsül**
**RTT** (_Round Trip Time)_ —> Paketlerin karşı tarafa gidip geri gelmesi için geçen süre.
**TTL** (_Time to Live) __—_> Paketlerin ağda sonsuza kadar dolaşmaması için kullanılan **yaşam süresi**dir. Bir paket, **hop noktaları** arasında her aktarıldığında **TTL değeri 1 azalır**.

### Bant Genişliği (Bandwidth)
* Analog sinyallerde birimi **Hertz (hz)** iken, dijital sistemlerde **bps (b/s)** şeklindedir.  
> "Bant genişliği" kavramını otoban yolda şerit sayısı gibi 
düşünebiliriz. Trafik ne kadar fazla olursa olsun, şerit sayısı arttıkça
 trafik sorunsuz ilerleyebilir. Bu kavram doğrudan iletimin hızını ifade
 etmemekte ama dolaylı olarak iletim süresinin kısalmasını 
sağlamaktadır.  
* Bir haberleşme sistemi, gönderici, alıcı ve iletim ortamından oluşur.
**İletim kapasitesi en küçük olan, bütün sistemin bant genişliği belirler.**
1. Latency (gecikme süresi): Verinin ağ üzerinde aktarımı sırasında geçen süre.
1. Response time (cevap süresi): Bilgisayarların performansı da dahil edilerek cevap almak için geçen toplam süre.
1. Throughput (işlem hacmi): Bant genişliği teorik bir kavram iken, 
işlem hacmi uygulamada görülen gerçek kapasiteyi ifade eder. Anahtar 
(switch) cihazlarının da işlem kapasitesi bu kavram ile ifade edilir. (şey gibi düşün kutuda 16 megabit yazıyor sana 10 geliyor, 10 görüyorsun.)
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B04-BantGenisligi02.png)

240 MB (megabayt) —> 240*8 Mb (megabit)
16 Megabit internetim var diyelim -> saniyede 16/8 yani 2 megabayt saniyede.

**Jitter** —> giden paketlerin arasında sabit bir gecikme olmama durumu. 
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B04-Jitter.png)




**QoS** (quality of service) —> bant genişliğini duruma göre öncelik vermek üzere yapılandırma.
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B04-QoS.png)


---

Bu haftayı kaçırdım (malum minibüs olayı)

---

## Yerel Ağlar (LAN/VLAN)
ethernet protokolü **802.3** standardını kullanılır.

> vlan atamaları **802.1q** ethernet standardı ile geldi. **Dot1q** olarak da bilinir. 

> 802.11 -> ev ve işyerlerinde en çok kullanılan, bilgisayar, yazıcı gibi cihazların birbirleri ile kablosuz olarak haberleşme standardı(wifi standardı).

##### ARP 
* IP adresini MAC adresine çevirir.
* ARP tablosu ağdaki cihazların MAC adresini tutar.

##### Yayın Adresi (Broadcast Address)
* tüm yerel ağı temsil eder. Ağdaki tüm cihazlara aynı anda veri yollanmış olur.
* Hedef MAC burada full 1 yani FF:FF:FF:FF:FF:FF olur.

###### Yayın Alanı
* LAN gibi düşünülebilir. Kendi network alanı (sadece mac ile pc'ler haberleşebiliyor.)
* Başka bir ağa ulaşmak için "gateaway" ağ geçidinden geçmesi lazım.

soru-1
1- yönlendirici
1.2- hub →3pc
1.3- anahtar →3pc
1.3.1- hub → 3pc
1.3.2- hub → 3pc

soru-2
1- anahtar → F pc
1.1- hub → A pc & B pc
1.2- hub → C pc & D pc & E pc

> Yayın mesajını(tüm ağa gönderilen mesajı) router durdurur, keser.

> uplink portu: Anahtar üzerinde pc’lerin haricinde dış dünya ile iletişim kurmak için bağlantı yapılan porta "uplink" portu denir.

##### Ağ Geçidi (Gateway)
Ağ geçidi, bir ağın dışarı açılan kapısıdır.
İnternete çıkılan kapı.

##### Alt Ağa Bölme Yöntemleri
**klasik yöntem**de fiziksel olarak bir cihaz koyup kablo çekerek bölme,
**VLAN yapısı**nda ise fizikselden ziyada uzaktan sanal olarak bölme durumu söz konusudur.

##### Ağları bölmenin faydaları
* işletme kolaylığı
* PC sayısını azaltmak
* Güvenlik


##### VLAN Anahtarlar
her anahtarda sanal ağlar tanımlanmaz.  Tanımlananlara yönetilebilir anahtar, tanımlanamayanlara yönetilemeyen anahtar denir.
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B06-VLAN_Anahtar.png)
> Aynı VLAN numarasına sahip portlar aynı sanal ağa aittir.

**trunk (tagged) port**: bir switch'teki bağlantıyı başka bir switch'e bağlantı verirken kullanılır. Genelde bilgisayarın bağlanması için kullanılmaz.

**access (untagged) port**: Bilgisayarın bağlanması, internete sahip olması için açılan portlar.

ünide kullanım şekli: eğer bir switch'ten başka switch'e internet aktaracaksak trunk port ayarlarız, eğer ünide lab'taki bir pc kullanacaksa access port ayarlarız.

> layer(katman) 3 switch, yönlendirebilen switch'tir.
layer 2 switch, yönlendiremeyen switch'tir.


#### Anahtar Kullanım Mimarisi
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B06-AnahtarMimarisi.png)
1. Omurga (core):
en çok ağır yüke giren switch, trafiğe maruz kalan katman
1. Dağıtım (distrubution) Katmanı:
chill takılan rahat trafiği bulunan omurga ile binalar arası iletişimi veren katman
1. Kenar  (access):
son kullanıcıyla etkileşime girip trafiğe sahip olan katman

önemli bir foto:
![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B06-InterVLAN_Routing.png)
açıklamak gerekirse: C'de layer 3 switch var yani yönlendirebilen. Diğerleri yönlendirilemeyen layer 2 switch.
A'da nasıl switch direkt yönlendiremese de router'da belirli ayarlar yaparak yönlendirme işlemi yapılabiliyor.

## IP

![](https://ozalpmurat.github.io/BilgisayarAglari-Kitap/images/B07-IP_Sinif1.png)

ilk üç sınıfı (A,B,C) aralığını ezberle! (first octet decimal range)


##### Özel ve genel IP Adresleri
10.0.0.0/8

172.16.0.0/12

192.168.0.0/16

NAT(Network Address Translation) içerisinde kullanılan IP adresleri

> NAT : kendi içerisinde ağın aldığı IP. Dışarıya çıktığında herkes tek veya birden fazla(nasıl ayarlanmışsa) IP kullanabilir.

> 168.254.0.0/16  —> IP aralığı, Windows'ta eğer bilgisayar IP alamazsa bunu otomatik olarak alıyor. Yani IP alamadığının göstergesi.

##### Diğer ayrılmış IP adres aralıkları
0.0.0.0/8

127.0.0.0/8

169.254.0.0/16


---

Cuma derse katılmadım. (diş kontrolüne gidildi.)

---

> IP sayısı ve host sayısı;
	Host tanımlayıcısı kısmındaki bit sayısı ile elde edilebilecek adres sayısı, o ağda kullanılabilecek IP adresi sayısıdır. Her ağın ilk IP  adresi `ağ adresi` ve son IP adresi de `yayın adresi` olarak kullanıldığından, **her ağda kullanılabilecek host sayısı IP sayısından 2 eksiktir**.


> Ağ maskesi herhangi bir IP adresi ile ikilik sistemde çarpılırsa (mantıksal `VE` işlemi) çıkan sonuç **ağın adresi**ni verir. Bu sayede, ağın nerede başladığı bulunmuş olur.


her ağ için;

ilk ip: ağ adresi

son ip: yayın adresi


	> ip adresinin bölündükten sonrasını 0 yaparsak ağ adresini, 1 yaparsak yayın adresini buluruz.
	ağ: 10.0.0.0
	yayın: 10.0.255.255


	soru: 10.0.1.123/24   ağ maskesini, ağ adresini ve yayın adresini bulun.

		maske: 255.255.255.0
		ağ adresi: 10.0.1.0
		yayın adresi: 10.0.1.255


	soru: 10.0.1.123/25  ağ maskesini, ağ adresini ve yayın adresini bulun.
		10.0.1.123 —> 10.0.1.{01111011} —> 0/1111011
			maske: 255.255.255.128
			ağ adresi: 10.0.1.0
			yayın adresi: 10.0.1.127


	soru: 10.0.1.133/25  ağ maskesini, ağ adresini ve yayın adresini bulun.
		10.0.1.133 —> 10.0.1.{10000101} —> 1/0000101
			maske: 255.255.255.128
			ağ adresi: 10.0.1.128  —> 1/0000000
			yayın adresi: 10.0.1.255 —> 1/1111111

	soru: 10.0.1.133/26  ağ maskesini, ağ adresini ve yayın adresini bulun.
		10.0.1.133 —> 10.0.1.{10000101} —> 10/000101
			maske: 255.255.255.192
			ağ adresi: 10.0.1.128  —> 10/000000
			yayın adresi: 10.0.1.191 —> 10/111111

	> how can we do this all:
	örnek: 10.0.1.123/16     ağ maskesini, ağ adresini ve yayın adresini bulun.

	maske: 255.255.0.0
		       11111111.11111111.00000000.00000000

	ağ adresi: 2'lik sayı sisteminde ip adresi ile ağ maskesinin çarpımıdır.
		10.0.1.123 x 255.255.0.0 = 10.0.0.0 = ağ adresi




---
# IP Hesaplarında Formüller ve Özet
## IPv4 Adresleri
* IP (v4) adresleri **32 bitten** oluşur.
* Bu bitler sekizer gruplu (**oktet**) olarak yazılır ve okunur.**Örnek:** `10.170.265.44`⚠️ Ancak **hiçbir oktet 255'ten büyük olamaz**, bu nedenle bu örnek **geçersiz bir IP adresidir.**
## Ağ ve Host Tanımı
* IP adresindeki ilk **N bit** (soldan itibaren) **ağı** tanımlar.
* Geri kalan **(32 - N) bit** ise **hostları** (cihazları) tanımlar.
Bu iki bileşeni birbirinden ayırmanın iki yolu vardır:
### 1. CIDR Gösterimi
* Bölü işareti (`/`) ile ifade edilir.**Örnek:** `10.5.0.100/16`
### 2. Alt Ağ Maskesi Gösterimi
* M tane 1, N tane 0 olacak şekilde bitler yazılır.
* Sonra bu bitler 10’luk sisteme çevrilir.**Örnek:** `10.5.0.100 - 255.255.0.0`
---
## IP Sayısı Hesaplama
Bir ağda kaç IP olduğunu bulmak için, `/` işaretinden sonraki **host bit sayısına** bakılır:
* Eğer `X` tane **host biti** varsa:🔢 **Toplam IP sayısı = 2^X**
⚠️ Kullanılabilir IP sayısı = `2^X - 2`
(Neden? Çünkü ilk IP adresi **ağ adresi**, son IP adresi **yayın (broadcast) adresidir**)
---
## Alt Ağ (Subnet) Hesaplamaları
Ağları alt ağlara bölmeye başlamadan önce mutlaka mevcut ağı tanımla:
* Nerede başlar?
* Nerede biter?
* Maskesi nedir?
* CIDR gösterimi nedir?
* Bu ağda kaç IP vardır?
---
## Ağ Adresi Nasıl Bulunur?
* IP adresinde `/`’den **sonraki tüm bitler sıfırlanır**.
* Sonra ikilik sistemden onluk sisteme çevrilir.
---
## Yayın (Broadcast) Adresi Nasıl Bulunur?
* IP adresinde `/`’den **sonraki tüm bitler bire çevrilir**.
* Sonra onluk sisteme çevrilir.
---
## Alt Ağ Maskesi Nasıl Bulunur?
* IP adresinde, `/`’den **önceki tüm bitler 1 yapılır**.
* `/`’den **sonraki tüm bitler 0 yapılır**.
* Sonra 10’luk sisteme çevrilir.
---



