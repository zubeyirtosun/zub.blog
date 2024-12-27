+++
title = 'Hugo ile Github Blog'
date = 2024-12-26T19:17:15+03:00
draft = true
+++

# Hugo nedir?
[Hugo](https://gohugo.io/), hızlı bir statik site oluşturucu (static site generator) yazılımıdır. Hugo, içerikleri Markdown formatında yazılmış dosyaları alır ve bunları HTML dosyalarına dönüştürerek bir web sitesi oluşturur. Genellikle bloglar, portföy siteleri, belgeler ve diğer içerik odaklı web siteleri için kullanılır.
Aynı bu okuduğunuz blog da hugo ile tasarlanıp, markdown ile yazımı yapıldı.
    
Hugo'yu, özelleştirilebilir temalar ile kurabiliyorsunuz. [Önceden hazırlanmış temalar](https://themes.gohugo.io/)ı kullanarak hızlıca bir site oluşturabilirsiniz. Tabii seçtiğiniz temaları da kendi içinde temayı yazan kişinin verdiği dokümantasyona göre düzenlemeniz gerek.

Başlangıç olarak basit bir şey seçip, deneyerek gitmeniz sizin için daha akılda kalıcı olacaktır.

Yavaştan uygulamaya geçelim:

##### Hugo kurulumu:

Kendi işletim sisteminize göre [buradan](https://gohugo.io/installation/) kurabilirsiniz. **Extended** sürüm kurmanızı öneririm çünkü güzel temalarda çalışmak isterseniz bu gerekiyor.
Ben linux kullandığımdan ona göre anlatacağım.

debian tabanlı sistemler için:
```bash
sudo apt install hugo
```
Github'ta 2 tane yeni repo açacağız. Biri Blog sitesinin altyapısını oluşturan Hugo dosyalarının tamamını depolayacağımız repo, diğeri ise sadece blog sayfamızın kodunu içerecek ve yayınlayacak repo olacak. Burada şu kısım   

