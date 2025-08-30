#  Database Replication

**yazar(lar):** Alex Xu

**yıl:** 2020

**kaynak/link:** [PDF](https://bytes.usc.edu/~saty/courses/docs/data/SystemDesignInterview.pdf#page=12)


## özet
Bu bölüm, database replication’ı anlatıyor. Bir veritabanı iki role ayrılıyor: master, yazma işlemlerinin yapıldığı ana veritabanı; slave ise master’dan kopya alan ve okuma işlemlerini gerçekleştiren yan veritabanları. Bu yapı yüksek erişilebilirlik ve paralel kullanıcı desteği sağlar. Senkron replikasyonda yazma tüm slave’ler güncellenmeden tamamlanmaz → tutarlılık yüksek ama performans sınırlı. Asenkron replikasyonda yazma master’da biter, slave’ler sonra güncellenir → hız yüksek ama kısa süreli tutarsızlık olabilir. Master bakımda veya çöktüğünde sistem bir slave’i yeni master olarak atar (failover).

## neden ilginç buldum
- Master-slave modelinde yazma ve okuma işlemlerinin ayrılması bence oldukça yaratıcı bir çözüm. Hem performans kazanımı hem de paralel çalışabilme fikri dikkatimi çekti.

- Senkron ve asenkron replikasyon arasındaki seçim ise aslında geliştiricinin “hız mı, kesin doğruluk mu?” sorusuna verdiği cevabı gösteriyor.

- Failover mekanizması kısmında “ya master çökse ne olacak?” sorusuna sistemin hazır bir cevabı olması güven verici. Bu noktada hata toleransının önemi çok net ortaya çıkıyor.

- Retry ve backoff stratejileri, sistemin yükü yönetmesini ve gerektiğinde biraz bekleyerek düzeni korumasını sağlıyor.
- Finansal işlemler gibi kritik alanlarda senkron ya da hibrit çözümlere yönelinmesi de gayet mantıklı görünüyor. Orada performanstan biraz ödün verilse bile güvenilirlik (reliability) her şeyin önüne geçiyor.


## notlar / ilgili kaynaklar
- Master–slave arasında önce bağlantı ve senkronizasyon kontrol edilir.

- Yazma işlemi tüm slave’lere yansımadan tamamlanmaz → tam tutarlılık ama düşük performans.

- Yazma master’da biter, slave’ler sonradan güncellenir → yüksek performans ama kısa süreli tutarsızlık.

- Master çökünce ya da bakımdayken sistem otomatik bir slave’i master yapar (failover).

- 1 master ve birden çok slave için ayrı bağlantılar tanımlanabilir.

- İşlem başarısız olursa tekrar denenir, ama sık denemek sistemi yorar.

- Denemeler arasında artan bekleme süreleri koymak yükü dengeler.