# dynamo: amazon's highly available key-value store

**yazar(lar):** Giuseppe DeCandia, Deniz Hastorun, Madan Jampani, Gunavardhan Kakulapati, Avinash Lakshman, Alex Pilchin, Swaminathan Sivasubramanian, Peter Vosshall ve Werner Vogels

**yıl:** 2007

**kaynak/link:** [PDF](https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf)

## özet

bu makale amazon’un high availability ve low latency hedefleriyle geliştirdiği dağıtık key-value store olan Dynamo’yu anlatıyor. makale, replication, consistency, partition tolerance ve node failures gibi konuları nasıl yönettiklerini detaylı şekilde açıklıyor. ayrıca eventual consistency modelini ve sistemin tasarım kararlarını net bir şekilde sunuyor.

## neden ilginç buldum

- sistemin high availability ve low latency’yi bir arada sunma şekli inanılmaz. her node failure senaryosunda bile veri kaybı olmadan devam edebilmesi etkileyici.
- replication ve partition handling konusunu aşırı pragmatik bir şekilde çözmüşler, tasarımdan zeka fışkırıyor.
- eventual consistency’i gerçek bir sistemde uygulamak, teoriden pratiğe geçişi gözler önüne seriyor.
- her node’un rolü, quorum ve read/write trade-off’ları çok net, modern distributed system’ların dna'sını görmek mümkün.
- tüm bunlar bir key-value store’da hayata geçirilmiş, sadece konsept değil, tam anlamıyla çalışan bir mühendislik şaheseri.
- consistent hashing ve virtual nodes gibi iyi bilinen teknikleri bir araya getirerek, sistemin peer-to-peer ve dağıtık yapıda büyümesini kolaylaştırmış.

## notlar / ilgili kaynaklar

- makale, SOSP '07 (Symposium on Operating Systems Principles) konferansında sunulmuş, çok saygın bir konferans.
- dynamo, amazon platformunda bir yıldan fazla kullanılmış, yoğun tatil sezonunda bile high load altında kesintisiz çalışmış, sistemin _resilience_'ı büyüleyici.
- werner vogels (amazon'un cto'su) makalenin yazarlarından, makale onun blogunda da detaylı şekilde paylaşılmış.
- dynamo’nun tasarımı, _NoSQL_ dünyasında bir dönüm noktası; özellikle _Apache Cassandra_’yı ciddi şekilde etkilemiş.
- dynamo'nun en önemli tasarım hedeflerinden biri _always-writeable_ bir sistem olmaktır. ağ bölümleri veya node arızaları gibi durumlar karşısında bile write işlemlerini asla reddetmez.
- tutarlılığı yönetmek için vector clocks kullanıyor. bu sayede bir nesnenin farklı versiyonları arasındaki nedensel ilişkiler takip edebiliyor.
- geçici node arızaları sırasında veri kopyalarının kaybolmasını önlemek için _hinted handoff_ mekanizmasını kullanıyor. bu mekanizma, bir node geçici olarak ulaşılamaz olduğunda, diğer node'ların bu node için gelen veriyi saklamasını ve node tekrar çevrimiçi olduğunda ona geri teslim etmesini sağlar.
