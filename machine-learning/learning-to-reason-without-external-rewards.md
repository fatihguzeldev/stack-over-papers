# Learning to Reason without External Rewards

**yazar(lar):** Xuandong Zhao, Zhewei Kang, Aosong Feng, Sergey Levine, Dawn Song

**yıl:** 2025

**kaynak/link:** arXiv preprint — https://arxiv.org/abs/2505.19590

## özet
Bu çalışma, etiketli veri ya da haricî bir doğrulayıcı olmadan büyük dil modellerini pekiştirmeli öğrenmeyle nasıl iyileştirebileceğimizi gösteriyor. Önerilen yaklaşım (INTUITOR), modelin kendi “öz-kesinlik” sinyalini ödül olarak kullanıyor; yani model, ürettiği her adımda ne kadar emin olduğuna bakarak kendini güncelliyor. GRPO ile birleştirilen bu düzenek, akıl yürütme ve talimat izleme görevlerinde rekabetçi sonuçlar verirken, özellikle kod üretimi gibi alan-dışı işlerde belirgin kazanımlar sağlıyor.

## neden ilginç buldum
Etiket toplama masrafını ortadan kaldırması, tek başına basit bir içsel sinyalle (öz-kesinlik) eğitim yapılabilmesi, sadece nihai cevabı değil üretim sürecini de ödüllendirerek aktarımı güçlendirmesi, küçük modellerde bile “düşün–sonra-cevapla” davranışını teşvik etmesi ve mevcut GRPO akışına zahmetsizce eklenebilmesi bu işi pratik ve uygulanabilir kılıyor; üstelik ilk adımlardan itibaren gözle görülür ilerleme elde edilmesi de cabası.

## notlar / ilgili kaynaklar
- **Ödül (öz-kesinlik):** Her adımda modelin çıktı dağılımının “tamamen rastgele” bir dağılımdan ne kadar uzak olduğuna bakılıyor; uzaklık arttıkça ödül artıyor.
- **Eğitim akışı (kısa):** Soru başına birkaç aday üret → her adayı öz-kesinlikle puanla → grup içi normalizasyonla avantajı hesapla → GRPO ile güncelle.
- **Ödül sömürüsü dersi:** Ödül sabit bir modelle **offline** hesaplanırsa, politika ödülü şişirmeyi öğrenebiliyor (gereksiz uzun, süslü cevaplar). **Online** hesaplama bu eğilimi bastırıyor.
- **KL cezası:** Özellikle aktarım (kod) görevlerinde ayarı kritik; yanlış ayar genellemeyi zayıflatabiliyor.
- **Değerlendirme:** GSM8K ve MATH’te sağlam, LiveCodeBench/CRUX gibi kod testlerinde daha büyük sıçramalar görülüyor.
- **Soru:** İçsel ödül gerçekten güvenilir mi; model kendini kandırabilir mi?  
  **Yanıt:** Tam garanti yok. Bu yüzden ödülün **online** hesaplanması, ek bir **KL cezası** ve grup içi normalizasyon kullanılıyor; ilerleme de periyodik olarak haricî test setlerinde kontrol ediliyor. Yöntem dış doğrulamayı tamamen ikame etmiyor, ama pratikte güçlü bir rehber sinyal sağlıyor.











