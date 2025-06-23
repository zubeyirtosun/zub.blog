+++
title = 'Blog'
date = 2025-04-27T16:11:01+03:00
draft = false
+++


# Crowdsec'e Giriş ve Kullanım Rehberi

Bu yazıda, Crowdsec'in ne olduğunu, nasıl çalıştığını ve temel kullanım senaryolarını ele alacağım. Ayrıca bir video ödevim için bu yazıyı referans alarak Crowdsec'i tanıtacağım. Haydi başlayalım!

## Crowdsec Nedir ve Ne Yapar?

Crowdsec, açık kaynaklı bir **güvenlik çözümüdür** ve temel olarak sistemlerinizi kötü niyetli aktivitelerden korumayı amaçlar. Geleneksel bir güvenlik duvarından farklı olarak, Crowdsec **davranış analizi** yapar ve topluluk tarafından paylaşılan tehdit istihbaratını kullanarak saldırıları tespit eder ve engeller. IP adreslerini banlama, şüpheli aktiviteleri izleme ve sistemlerinizi koruma gibi işlevleri vardır. Kısacası, Crowdsec hem bireysel hem de toplu bir savunma mekanizması sunar.

## Kurulum Aşaması

Crowdsec'i kurmak oldukça basittir. Aşağıda genel bir kurulum rehberi bulabilirsiniz (Linux tabanlı bir sistem için):

1. **Depoyu ekleyin ve paketi yükleyin:**
   ```bash
   curl -s https://packagecloud.io/install/repositories/crowdsec/crowdsec/script.deb.sh | sudo bash
   sudo apt-get install crowdsec
   ```

2. **Servisi başlatın:**
   ```bash
   sudo systemctl enable crowdsec
   sudo systemctl start crowdsec
   ```

3. **Kurulumu doğrulayın:**
   ```bash
   cscli config show
   ```

Bu adımlarla Crowdsec sisteminize kurulmuş olacak. Daha fazla detay için resmi dokümantasyonu kontrol edebilirsiniz.

## Genel Crowdsec Komutları (cscli)

Crowdsec'in komut satırı aracı **cscli**, sistemi yönetmek için kullanılır. İşte bazı temel komutlar:

- **Kararları (Decisions) Görüntüleme:**
  ```bash
  cscli decisions list
  ```
  Bu komut, banlanmış IP'leri ve neden banlandıklarını gösterir.

- **Makine Durumunu Kontrol Etme (Machines):**
  ```bash
  cscli machines list
  ```
  Bağlı makineleri ve durumlarını listeler.

Bu komutlar, Crowdsec'in temel işleyişini anlamak ve yönetmek için oldukça faydalıdır.

## Crowdsec Dashboard

Crowdsec, kendi sunduğu bir **web dashboard** ile sistem durumunu görselleştirmenizi sağlar. Dashboard'a erişmek için:

1. Crowdsec'in yerel API'sini ve dashboard'u kurun:
   ```bash
   sudo cscli dashboard setup
   ```
2. Tarayıcınızda `http://localhost:3000` adresine gidin.

Bu dashboard, banlanan IP'leri, saldırı türlerini ve sistem metriklerini detaylı bir şekilde gösterir. Videoda bu ekranı da göstereceğim.

## Crowdsec'ten Banlı Olarak Gelen IP'leri Gösterme

Crowdsec, topluluk tarafından paylaşılan tehdit istihbaratını kullanarak banlı IP'leri sisteminize bildirir. Bu IP'leri görmek için aşağıdaki komutu kullanabilirsiniz:

```bash
cscli decisions list --origin crowdsec
```

Bu komut, yalnızca Crowdsec topluluğundan gelen ban kararlarını listeler. Çıktıda, banlanan IP'ler, banlanma nedenleri (örneğin "ssh-bf" yani SSH brute force) ve süreleri yer alır. Videoda bu komutu çalıştırıp gerçek zamanlı bir örnek göstermeyi planlıyorum.

## Bir IP Banlama ve Whitelist Kullanımı

Şimdi pratik bir örnek yapalım: Bir IP'yi banlayıp, ardından kendi IP'mizi whitelist'e ekleyerek banı kaldıralım.

1. **IP Banlama (örneğin SSH üzerinden):**
   ```bash
   cscli decisions add --ip 192.168.1.100 --type ban --duration 4h
   ```
   Bu komut, belirtilen IP'yi 4 saat boyunca banlar. SSH bağlantısı denenirse engellendiğini görürsünüz.

2. **Banlanan IP'nin Güvenlik Duvarında da Banlandığını Gösterme:**
   Eğer `crowdsec-firewall-bouncer` kuruluysa ve sisteminiz `nftables` kullanıyorsa, banlanan IP'nin güvenlik duvarında engellendiğini doğrulayabilirsiniz:
   ```bash
   sudo nft list ruleset | grep 192.168.1.100
   ```
   Bu komut, `nftables` kurallarında belirtilen IP'nin banlandığını gösterir. Crowdsec'in firewall bouncer'ı sayesinde bu kural otomatik olarak eklenir. Videoda bu adımı göstererek entegrasyonu açıklayacağım.

3. **Whitelist Oluşturma:**
   Kendi ağınızı (örneğin `10.x.x.x/8`) korumak için whitelist'e ekleyelim:
   ```bash
   sudo cscli decisions delete --ip 192.168.1.100
   echo "10.0.0.0/8" | sudo tee -a /etc/crowdsec/local_api/whitelist.yaml
   sudo systemctl restart crowdsec
   ```
   Artık `10.x.x.x` aralığındaki IP'ler banlanmayacak.

4. **SSH Engelleme Collection'ı:**
   SSH saldırılarını engellemek için `crowdsec/sshd` koleksiyonunu kullanabilirsiniz:
   ```bash
   cscli collections install crowdsec/sshd
   ```
   Bu, SSH loglarını analiz eder ve şüpheli girişimleri otomatik olarak engeller.

5. **Metrikleri Görüntüleme (Opsiyonel):**
   ```bash
   cscli metrics
   ```
   Bu komut, sistemin performansını ve analiz edilen olayları gösterir.

## Crowdsec Firewall Bouncer Nedir?

**Firewall Bouncer**, Crowdsec'in ban kararlarını doğrudan sistem güvenlik duvarınıza (örneğin iptables veya nftables) uygulayan bir bileşendir. Yani, Crowdsec bir IP'yi banlamaya karar verdiğinde, bouncer bu kararı otomatik olarak firewall kurallarına ekler.

Kurulumu:
```bash
sudo apt-get install crowdsec-firewall-bouncer
sudo systemctl enable crowdsec-firewall-bouncer
sudo systemctl start crowdsec-firewall-bouncer
```

Bu, Crowdsec'in tespit ettiği tehditleri anında engellemesini sağlar. Videoda bunun nasıl çalıştığını da gösterebilirim.

---

Bu blog yazısı, Crowdsec'in temel özelliklerini ve kullanımını özetliyor. Videoda bu adımları tek tek ele alarak hem kurulum hem de pratik örneklerle açıklayacağım. Sorularınız olursa yorum bırakabilirsiniz!

