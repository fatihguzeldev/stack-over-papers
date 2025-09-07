# Why Language Models Hallucinate

**yazar(lar):** Adam Tauman Kalai, Ofir Nachum, Santosh S. Vempala, Edwin Zhang

**yıl:** 2025

**kaynak/link:** [PDF](https://cdn.openai.com/pdf/d04913be-3f6f-4d2b-b283-ff432ef4aaa5/why-language-models-hallucinate.pdf)

## özet

makale, büyük dil modellerinin (llm) neden halüsinasyon gördüğünü, yani yanlış cevaplar ürettiğini iki ana nedene dayanarak açıklıyor: pre-training sırasındaki baskılar (belirsiz bilgileri referans alarak tahmin yürütmeyi ödüllendirmek) ve post-training sırasındaki yanlış değerlendirme yöntemleri (aynı mantık, modellere puan veriliyor -evalulation- modellerin amaçları da yüksek puan almak. generic bilgiler ürettiklerinde yüksek not aldıkları için "evaluation" başarılı kabul ediliyorlar)

içeride yoğun matematiksel analizler ve ispatlar var. anlaşılmasa dahi içeride tartışılan fikirler oldukça net.

## neden ilginç buldum

- güzel ve komik bir analoji ile başlıyor, insan öğrencilerin sınavda emin olmadıkları soruları tahmin etmelerine benzetiliyor bu halüsinasyon görme işi
- halüsinasyonların, temel bir istatistiksel prensip olan ikili sınıflandırma hatalarıyla ilişkili olduğunu matematiksel bir yaklaşımla açıklıyor
- sorunun sadece teknolojik değil, aynı zamanda mevcut değerlendirme yöntemlerinin yanlış teşvikler sunmasından kaynaklanan sosyo-teknik bir sorun olduğunu öne sürüyor

## notlar / ilgili kaynaklar

- bu makale, aynı yazarların daha önceki "Calibrated Language Models Must Hallucinate" makalesinin bir uzantısı
- RLHF (reinforcement learning from human feedback), RLAIF (reinforcement learning from ai feedback) ve DPO (direct
preference optimization) gibi post-training tekniklerinin halüsinasyonları azaltmada etkili olduğu ancak sorunu tamamen çözemediği belirtiliyor