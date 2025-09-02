# From Facts & Metrics to Media Machine Learning: Evolving the Data Engineering Function at Netflix

**yazar(lar):** Dao Mi, Pablo Delgado, Ryan Berti, Amanuel Kahsay, Obi-Ike Nwoke, Christopher Thrailkill, Patricio Garza

**yıl:** 2025

**kaynak/link:** [Netflix Tech Blog](https://medium.com/netflix-techblog/from-facts-metrics-to-media-machine-learning-evolving-the-data-engineering-function-at-netflix-6dcc91058d8d)

## özet

Netflix'in neden "Media ML Data Engineering" adında yeni bir Data Engineering dalı oluşturduğunu ele alıyor. Bu rol açıklandığı üzere veri kaynakları ve diğer mühendislik birimleri arasında bir köprü olarak kullanılıyor ve geleneksel veri tablolarının yerine "Media Tables" adını verdikleri yeni bir yapıyı oluşturmaya başladıkları "Media Data Lake" isimli kapsamlı bir metadata ve kaynak depolama sistemi ile entegre ediyor. Bu yeni "Media Table"lar sadece geleneksel metadata'ları tutmakla kalmıyor aynı zamanda bu metadata'lar üzerinden "Çeviri ve Ses Kalitesi", "NSFW Çarpanı" gibi birçok yenilikçi uygulamaya öncü oluyor. Başlangıçtan itibaren ilk hedefleri "Data Pond" adını verdikleri daha küçük kapsamlı bir "Media Data Lake" ile bu süreci yönetmek ve sunmak iken uzun vadedeki hedefleri arasında bu rol ve sistemleri kullanarak standardize edilmiş ve yüksek kaliteli media data ile eğitilmiş ML modelleri oluşturmak ve bu modeller ile kendi içerikleri ve iş akışları hakkında daha derinlemesine bilgiler toplamak gibi amaçlar var.

## neden ilginç buldum

- "Media Tables" kavramının geleneksel veri tablolarının ötesine geçmesi ve medya içeriğinin doğasına özel daha kapsamlı yapılar oluşturulması ve bunu Machine Learning kullnarak yapıyor olmaları
- Oluşturdukları mimarinin "UI Components", "Data API" gibi diğer alanları da kapsaması ve bu alanlara destek olması
- Media Data Lake gibi büyük bir havuz oluşturmaları ve bunu belirli bir scale ile kullanmaya başlamaları
- Veri kaynakları ile mühendislik birimleri arasında köprü görevi gören yeni bir rol tanımlamaları
...

## notlar / ilgili kaynaklar

- Netflix'in zaten kişiselleştirme üzerine ne kadar efor sarf ettiğini biliyoruz, bunun üzerine bu tarz bir media data yönetim sistemine geçiş yapmaları uzun vadede kişiselleştirmenin çok daha otomatize ve kapsamlı olacağını düşündürtüyor.
- ML Media Data Engineering'i bir köprü gibi kullanarak veri ve diğer mühendislikleri bağlamaları çok gerekli ve kolaylaştırıcı bir hiyerarşi sağlıyor ve veriye erişimi kolaylaştırıyor.
- Tüm olay aslında Media Table'lar etradında dönüyor, blog'da da bahsedildiği üzere bu sistemdeki en "core" yapı Media Table'lar