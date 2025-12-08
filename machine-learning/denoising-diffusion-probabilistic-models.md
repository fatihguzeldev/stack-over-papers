# denoising diffusion probabilistic models

**yazar(lar):** jonathon ho, ajay jain, pieter abbeel

**yıl:** 2020

**kaynak/link:** [arXiv](https://arxiv.org/abs/2006.11239)

## özet

makale, modern diffusion modellerinin temelini atan çalışma. fikir basit: eldeki görüntüyü gaussian noise ekleyerek adım adım bozuyorsun (forward process) ve her adımda ne kadar eklediğimizi bildiğimiz için adım adım bu noise'ı kaldırmayı öğrenen bir model eğitiyorsun (reverse process). bu yaklaşım, özünde başka bir generative model olan GAN (generative adversarial network) modellerine ciddi bir alternatif, daha stabil bir eğitim süreci sağlıyor.

çalışma, score matching ve variational inference kavramlarını bir araya getirerek hem teorik olarak tutarlı hem de pratikte yüksek kaliteli örnekler üreten bir yapı kuruyor. bugün stable diffusion, dall-e gibi pek çok model bu makalenin ortaya koyduğu çerçevenin bir türevi.

## neden ilginç buldum

- modern diffusion kaynaklı tüm modellerin çıkış noktası
- teorik olarak çok temiz, anlaması kolay
- GAN modellerindeki mode collapse gibi sorunlar yaşanmıyor
- eğitim süreci daha stabil ve deterministik
- autoregressive modellere alternatif olarak yüksek çözünürlük ve kesinlik sunuyor

## notlar / ilgili kaynaklar

- iki ana adımdan oluşuyor: forward ve reverse
- reverse process'in parametreleri noise tahmini üzerinden öğreniliyor
- modelin yaptığı şey aslında sadece x_t anındaki noise'u tahmin etmek
- farklı loss fonksiyonları, genelde negative log-likelihood. mse de kullanılabilir
- bu süreci hızlandırma işini başka bir paper devralmış: denoising diffusion implicit models (song et al. 2020)
- referans: improved ddpm (nichol & dhariwal 2021)
