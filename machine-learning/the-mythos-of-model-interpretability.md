# The Mythos of Model Interpretability

**yazar(lar):** Zachary C. Lipton  
**yıl:** 2016 (ICML Workshop on Human Interpretability in Machine Learning)  
**kaynak/link:** [PDF](https://arxiv.org/abs/1606.03490)

---

## özet

Makalede “interpretability” (yorumlanabilirlik) kavramının aslında belirsiz ve çoğu zaman içi doldurulmadan kullanıldığı tartışılıyor.  
Lipton, farklı motivasyonları (güven, nedensellik, adalet, bilgilendiricilik) birbirinden ayırıyor ve bu motivasyonların bazen birbiriyle çeliştiğini gösteriyor. Ayrıca, yorumlanabilirliğin iki farklı anlamını öne çıkarıyor:  

- **şeffaflık (transparency):** modelin nasıl çalıştığını doğrudan görebilmek (simulatability, decomposability, algoritmik açıklık)  
- **post-hoc açıklamalar:** modelin iç işleyişini açıklamasa da faydalı bilgi sunan yorumlar (ör. saliency map, örnekle açıklama, text açıklaması)

Sonuç: “yorumlanabilirlik” tek bir şey değil; çoklu kavramlardan oluşuyor ve hangi amaç için istendiği net belirtilmeden kullanılması bilimsellikten uzaklaşıyor.

---

## neden ilginç buldum

- İnsanların sürekli “linear modeller yorumlanabilir, deep learning kara kutu” demesi aslında temelsiz: yüksek boyutlu lineer modeller de gayet şeffaflıktan uzak olabilir; bazı durumlarda DNN’ler post-hoc açıklamalarla daha fazla şey verebiliyor.  
- Makale, “neden yorumlanabilirlik istiyoruz?” sorusunu net soruyor: güven mi, nedensellik mi, etik mi, yoksa bilgilendiricilik mi? Her biri farklı beklenti doğuruyor.  
- Post-hoc açıklamalar bazen yanıltıcı olabilir, yani “güzel görünüyor” diye aslında yanlış güven yaratabilir. Bu uyarı bence günümüzde hâlâ çok geçerli.

---

## notlar / ilgili kaynaklar

- Yorumlanabilirlik ihtiyacı genelde **model hedefi ile gerçek hayat hedefi arasındaki uyumsuzluktan** doğuyor. (ör. pneumonia risk modelinde asthma örneği)  
- Avrupa Birliği’nin “right to explanation” (açıklama hakkı) düzenlemesi bu tartışmaya erken dönemde bağlanmış.  
- Makale, literatürde kavramın bulanıklığını ve sahte kesinlik (“quasi-scientific”) havasını eleştiriyor.  
- Kritik takeaway: “Interpretability” lafı geçiyorsa, mutlaka **hangi yorumlanabilirlik türü** kastediliyor, sorulmalı.
