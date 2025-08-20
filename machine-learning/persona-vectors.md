# PERSONA VECTORS: MONITORING AND CONTROLLING CHARACTER TRAITS IN LANGUAGE MODELS

**yazar(lar):** Runjin Chen, Andy Arditi, Henry Sleight, Owain Evans, Jack Lindsey

**yıl:** 2025

**kaynak/link:** [PDF](https://arxiv.org/abs/2507.21509)

## özet

Bu makalede, büyük dil modellerinin (LLM) “yardımcı” persona ile kullanıcılarla etkileşim kurarken aslında farklı kişilik özellikleri sergileyebildikleri gösterilmektedir. Araştırmacılar, üç temel kişilik özelliği (evil, sycophancy, hallucination eğilimi) için özel soru setleri oluşturmuş ve bu sorulara verilen yanıtlar sırasında ortaya çıkan model aktivasyonlarını inceleyerek ilgili persona vektörlerini çıkarmışlardır. Bu vektörler sayesinde modelin kişilik özellikleri daha sistematik şekilde belirlenebilmiştir. Sonrasında, dil modeli üzerinde yapılan fine-tuning işlemleri sırasında bu kişilik özelliklerinde kaymalar yaşanabileceği ortaya konulmuş; ayrıca bu kaymaları önceden tespit etmek, kontrol altına almak ve engellemek için persona vectors yaklaşımı önerilmiştir.

## neden ilginç buldum

- Büyük dil modellerini aslında gelecek bir sonraki tokenleri tahmin eden bir _autocomplete makineleri_ olarak düşünürdüm ancak bu makale ile birlikte eğitildikleri veri setlerinden cevap verme sırasında kişilikleri olabileceğini öğrendim.
- Önerilen değerlendirme yöntemi olarak _AI as a judge_ yöntemi kullanılmış. Bir dil modelinin çıktısını değerlendirmesi için farklı bir dil modeli kullanabilecek kadar modellere güveniliyor. (Bu yöntemi ben de biliyordum ancak şirket içerisinde llm çıktılarına güvenilmiyor, bu çıktıları da değerlendirecek farklı bir llm'e hiç güvenilmiyor. Bu yöntemi kullanan bir firma görmüş oldum.)
- Fine-tuning sırasında ortaya çıkan kişilik kaymalarını önceden tespit edip engelleyebilecek bir mekanizma öneriyorlar. Böylece problem sadece gözlemlenmekle kalmıyor, hangi veri ya da hangi yönlendirme bu kaymaya sebep oluyor önceden işaretlenebiliyor. Bu da LLM güvenliği için proaktif bir yaklaşım sunuyor.

## notlar / ilgili kaynaklar

- Persona vectors sadece olumsuz kişilikler için değil (evil, sycophancy, hallucination), aynı zamanda olumlu özellikler (optimism, humor vb.) için de çıkarılabiliyor. Yani bu yöntem hem güvenlik hem de kullanıcı deneyimi açısından geniş bir uygulama alanına sahip.
- Steering yöntemleri iki farklı zamanda uygulanabiliyor: inference-time (çıktı üretimi sırasında) ve training-time (fine-tuning sırasında). Çalışma, training-time uygulanan “preventative steering” yönteminin daha verimli ve daha az yan etki yarattığını gösteriyor.
- Veri filtresi olarak kullanım: Fine-tuning öncesi veriler persona vectors üzerine projekte edilerek problemli örnekler işaretlenebiliyor. Böylece LLM tabanlı filtrelerden kaçabilecek hatalı veya riskli örnekler de yakalanabiliyor.
