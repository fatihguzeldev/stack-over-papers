# Self-supervised learning: The dark matter of intelligence

**yazar(lar):** Yan LeCun, Ishan Misra

**yıl:** 2021

**kaynak/link:** [Article](https://ai.meta.com/blog/self-supervised-learning-the-dark-matter-of-intelligence/)

---

## özet

Geleneksel yapay zeka yöntemleri devasa miktarda **etiketli veriye** ihtiyaç duysa da, insan zekası büyük ölçüde **sağduyuya (common sense)** ve önceki deneyimlere dayalıdır. İnsanlar bu sayede kısa sürede, az eğitimle yeni beceriler öğrenebilirken, örneğin araba sürmek gibi, otonom araç sistemleri milyonlarca veriyle bile bize göre basit olan bu eylemi yerine getirirken zorlanmaktadır. Bunun sebebi modelin daha öncesinde gerçek dünyaya dair bir sağduyusunun olmaması olabilir. Buna ek olarak pratikte milyarlarca verinin etiketlenmesi pek mümkün değildir. ImageNet [1] gibi görece güçük bir veri setinin bile 2.5 yıl gibi bir sürede  etiketlenmiş olduğu göz önünde bulundurulduğunda **gözetimli öğrenmenin (supervised learning)** geleceğinin pek parlak olmadığı görülmektedir. Bu durum herhangi bir modelin **öz-gözetimli öğrenme (self-supervised learning)** ile sağduyu kazandırılıp sonrasında alt-işler için (örn. sınıflandırma, tespit, segmentasyon vb.) ince ayar yapılıp **indirgenmesi (downstream)** ile çözülebilir.

---

## neden ilginç buldum

- Veri etiketlemeyi minimize ederek zaman kaybını engelliyor.
- Günümüzdeki LLM eğitimlerinin çoğunluğu bu eğitim yöntemi ile yapılıyor.
- İnsan öğreniminin makine öğrenmesine nasıl uyarlandığının örneklerle gösteriyor.
- Karanlık maddenin evrenin çoğunluğunu kaplaması gibi SSL sinyallerininde verilerimizin çoğunu kapladığından bahsediyor. 
---

## notlar / ilgili kaynaklar

- Direkt verinin kendisinden gözetim sinyalleri (supervisory signals) maskeleme yöntemi ile çıkarılabilir.
- CV (computer vision) alanında NLP (natural language processing) alanında olduğu kadar uygulanması kolay değil. Özellikle yüksek boyutsallık zorlayıcı bir unsur.
- Örneğin *“_____ savanda _____ kovalar”* cümlesini tamamlamak için modelin, aslanların veya çitaların antilop ya da sığırları kovalayabileceğini; fakat kedilerin ise mutfakta fare kovaladığını, öğrenmesi gerekir. Bu eğitimin bir sonucu olarak sistem; sözcüklerin anlamlarını, sözcüklerin dilbilgisel rollerini ve tüm metinlerin anlamını temsil etmeyi öğrenir
- SSL yöntemlerinden biri EBM eğitmektir. **EBM (energy base models)** aslında loss fonksiyonudur. Benzer değerlere düşük bir skalar değer verirken, birbirinden farklı girdilere yüksek değer verir.
- Bir EBM’yi eğitmek iki kısımdan oluşur:  

    1. Uyumlu olan **x** ve **y** örneklerini gösterip, düşük enerji üretmesi için modeli eğitmek  
    2. Belirli bir **x** için, **x** ile uyumsuz olan **y** değerlerinin, uyumlu olan **y** değerlerine kıyasla daha yüksek enerji üretmesini sağlamak  

    Zor olan kısım, modelin gerçekten yüksek enerji üretecek şekilde eğitilmesidir. Böyle bir yöntem olmadığında, iki ağ girdilerini tamamen göz ardı edip her zaman aynı çıktıyı özniteliklerden (**embeddings**) bağımsız bir şekilde üretebilir. Bu olguya **çökme (collapse)** denir.

- **Karşıtlık (contrastive)** yöntemlerinin büyük bir sorunu vardır: Eğitilmeleri çok verimsizdir.
- Gelecek **karşıt olmayan (non-contrastive)** modellerdedir (örn. *BYOL, MAE, DINO*)

[1] *J. Deng, W. Dong, R. Socher, L. -J. Li, Kai Li and Li Fei-Fei, "ImageNet: A large-scale hierarchical image database," 2009 IEEE Conference on Computer Vision and Pattern Recognition, Miami, FL, USA, 2009, pp. 248-255, doi: 10.1109/CVPR.2009.5206848.*
