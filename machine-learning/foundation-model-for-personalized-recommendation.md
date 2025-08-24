# Foundation Model for Personalized Recommendation

**yazar(lar):** Netflix Technology Blog

**yıl:** 2025

**kaynak/link:** [Blog](https://netflixtechblog.com/foundation-model-for-personalized-recommendation-1a0bd8e02d39)

## özet

Netflix, kullanıcı etkileşimlerini (izleme, durdurma, atlama, beğenme vb.) token’lara dönüştürerek bunları bir dil gibi ele alıyor. Bu etkileşim dizileri üzerinden eğitilen foundation model, her kullanıcının izleme davranışlarını anlayıp kişiselleştirilmiş öneriler üretebiliyor. Böylece klasik collaborative filtering yöntemlerinin ötesine geçen, ölçeklenebilir ve daha doğru çalışan bir öneri sistemi kurulmuş oluyor. Model, yüz milyonlarca kullanıcının günlük etkileşimlerinden oluşan devasa bir veri setiyle besleniyor.

## neden ilginç buldum

- Kullanıcı davranışlarını bir “dil” olarak modelleme fikri çok farklı. Şuanki modellerde genel olarak doğal dil cümleleri tokenize edilirken, Netflix kullanıcı etkileşimlerini tokenize etmeye başlamış.
- Cold start problemine karşı dayanıklı bir çözüm sunuyor; yeni kullanıcılar için bile önerilerin kalitesi hızla artabiliyor.  
- Ölçek çok büyük: milyarlarca etkileşimden öğrenen bir foundation model, içerik keşfini tamamen farklı bir boyuta taşıyor.  

## notlar / ilgili kaynaklar

- Bu yaklaşım “user interaction as language” konseptiyle NLP ve recommender systems alanlarını birleştiriyor. Yakın gelecekte yeni tip recommender sistemlere ön ayak olabilir.
- Token tabanlı modelleme, gelecekte oyun, müzik veya e-ticaret gibi diğer alanlara da uygulanabilir.  
