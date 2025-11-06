# Unpacking Cloudflare Workers CPU Performance Benchmarks

**Yazar(lar):** Kenton Varda

**Yıl:** 2025

**Kaynak / Link:** [Blog](https://blog.cloudflare.com/unpacking-cloudflare-workers-cpu-performance-benchmarks)

---

## Özet

Theo Browne'nin yapmış olduğu benchmark sonrası neden cf workers'ların 3.5x'e kadar daha kötü performans gösterdiğini araştıran CF ekibinden Kenton Varda'nın ekipçe bulgularını, bu durumun kaynağını araştırıp, V8 Engine'den, OpenNext'e, v8 engine'den kendi workers'larının node.js runtime'larına kadar yaptığı değişiklikleri okuyacağınız bir yazı. CF ekibinin community'e kulak verip, bir hafta kadar kısa sürede sorunun kaynağını bulup, aldığı aksiyonları okuyabileceğiniz detaylı bir yazı.

---

## Neden İlginç Buldum

- Community'e gerçekten kulak verip hızlı aksiyon almaları
- Bulguları sadece kendilerine saklamayıp, sanki bu kötü sonucu incident gibi görüp detaylı post-mortem vari bir yaklaşım seçilmiş. Saydam bir şekilde, kötü performansın olası sebeplerini araştırarak, sadece CF'nin değil OpenNext ve v8 OSS projelere gerekli patchleri yollamışlar.
- Sadece sonuç değil, bu sonucun tutarlılığını araştırarak, özellikle günümüzde benchmark'larda en sık yapılan hatayı yani test dizaynına bir tartışma getirmiş. 

---

## Notlar / İlgili Kaynaklar

- Yazının kendisi birçok yere referans vermekte, kendinizi v8 Patch konuşmalarını okurken veya benchmark'ı daha iyi nasıl dizayn edebilirizi okurken bulabilirsiniz.
