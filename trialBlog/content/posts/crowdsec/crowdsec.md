+++
title = 'CrowdSec Makineler Arasında Güvenli Bağlantı ve Firewall Yapılandırması'
date = 2025-01-27T02:48:59+03:00
draft = false
+++

# CrowdSec Makineler Arasında Güvenli Bağlantı ve Firewall Yapılandırması


## CrowdSec İki Makine Arasında Kurulum ve Yapılandırma

### Çocuk Makine Yapılandırması

1. **LAPI (Local-API) Bağlantısı Kaydı:**

   - Çocuk makinede aşağıdaki komutu çalıştırın:

     ```bash
     $ cscli lapi register -u http://<Merkez-Makine-Adresi>
     ```

   - Eğer başarısız olursa, port numarasını ekleyerek tekrar deneyin:

     ```bash
     $ cscli lapi register -u http://<Merkez-Makine-Adresi>:8080
     ```

   - Başarılı bir kayıt işlemi sonrasında aşağıdaki çıktıyı görmelisiniz:

     ```
     INFO Successfully registered to Local API (LAPI)
     INFO Local API credentials written to '/etc/crowdsec/local_api_credentials.yaml'
     WARN Run 'sudo systemctl reload crowdsec' for the new configuration to be effective.
     ```

     ![çıktı örneği-1](/crowdsec-images/lapiRegister2.png)

2. **Ana Makinede Kayıt Onayı:**

   - Ana makinede aşağıdaki komutu çalıştırarak yeni kayıt için gelen makineyi görüntüleyin:

     ```bash
     $ cscli machines list
     ```

   - Makineyi onaylamak için:

     ```bash
     $ cscli machines validate <makine-ismi>
     ```

    ![aktif makine liste örneği](/crowdsec-images/machinesList.png)

### Firewall Bağlantısı

3. **Bouncer Oluşturma ve API Key Paylaşımı:**

   - Ana makinede bir bouncer oluşturun:

     ```bash
     $ cscli bouncers add <bouncer-adı>
     ```

        ![oluşmuş API key örneği](/crowdsec-images/bouncerAdd.png)

   - Oluşturulan API key’i çocuk makinesindeki `/etc/crowdsec/bouncers/crowdsec-firewall-bouncer.yaml` dosyasına ekleyin:

     ```yaml
     api_url: http://<merkez-makine-adresi>:8080/
     api_key: <eklenen-bouncer-API'si>
     ```

   - Servisleri yeniden başlatın.

### PF (Packet Filter) Yapılandırması ve Opnsense Eklentisi Üzerindeki Ayar Gösterimi

4. **Banlamaların PF’te Gözükmesi:**

   - `/usr/local/etc/crowdsec/bouncers/crowdsec-firewall-bouncer.yaml` dosyasında aşağıdaki değişikliği yapın:

     ```yaml
     mode: pf
     ```

   - Diğer seçenekleri yorum satırına alın veya silin.
   - Opnsense üzerinde Crowdsec kısmı ayarları uygun şekilde yapılandırılmalıdır:

        ![opnsense crowdsec plugin ayarı örneği](/crowdsec-images/opnsenseCrowdsec.png)

### Crowdsec’in Kendi Panelinin Kullanımı

Herhangi crowdsec kurulu bir makineyi Crowdsec’in kendi sunduğu web arayüzünde detaylı görüntüleyebilirsiniz. Ayrıca bu birkaç avantaj da sağlıyor, sırayla açıklayacağım:

5. **Aradaki Bağlantıyı Sağlamak:**

   - Öncelikle [Crowdsec Security Engines](https://app.crowdsec.net/security-engines) üzerinde, Crowdsec kurulu makinede aşağıdaki komut ile bağlantıyı sağlayın:

     ```bash
     cscli console enroll --name <instance_name> --tags <tag_1> --tags <tag_2> <ENROLL-KEY>
     ```

     Buradaki `ENROLL-KEY`, `enroll command` kısmından alınır. Örneğin:

     ![crowdsec sec engine örnek foto](/crowdsec-images/crowdsecSecurityEngine.png)
     ![içe aktarma anahtar örneği](/crowdsec-images/crowdsecEnrollCommand.png)

     ```bash
     cscli console enroll --name mintMakinesi --tags denemeTagi cm6ibltpg000nttgmf5saniq9
     ```

   - Şimdi bunu panelden onaylamanız gerekmektedir. Bu işlemler sonunda artık makinenizi görebilmelisiniz.

    ![onaylama örneği](/crowdsec-images/acceptingEnroll.png)

### Uyarılar ve Ekstra Bilgiler

6. **Karar Tipleri:**

    - `cscli decisions add -t ban -d 2m -i <your_ip_address>` komutunda `-t "ban"` kısmı kesinlikle “ban” olmalıdır. Aksi takdirde PF’te gözükmez. Farklı isimde banlamaların gözükmesi için `/etc/crowdsec/bouncers/crowdsec-firewall-bouncer.yaml` dosyasında `supported_decisions_types` kısmına ekleme yapılması gerekmektedir.

---

Bu adımları takip ederek, Crowdsec kurulu iki makine arasında CrowdSec’i başarıyla yapılandırabilir ve güvenli bir ağ ortamı oluşturabilirsiniz.




