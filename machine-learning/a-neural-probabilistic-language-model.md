# a neural probabilistic language model

**yazar(lar):** yoshua bengio, réjean ducharme, pascal vincent, christian janvin

**yıl:** 2003

**kaynak/link:** [PDF](https://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf)

## özet

bu makale, dil modellemesinde kelimeleri discrete semboller olarak ele almak yerine continuous vektörler olarak ele alan ilk ciddi çalışma. o döneme kadar dil modelleri, n-gram temelli ve istatistiksel olarak çalışıyordu. bengio ve ekibinin çalışmaları, kelimeleri sürekli bir uzaya gömmeyi (embedding) ve bu uzayda semantic olarak benzer bağlamlardaki kelimelerin birbirlerine yakın olması fikrini modele öğretmeyi sağladı.

bu çalışma modern dil modellerinin tarihsel kırılma noktalarından birisi, belki de ilki. bugün "embedding" dediğimiz şeyin doğuş anı bu makale. "latent space" konsepti burada filizleniyor:

kelimeleri dense vector olarak temsil edip, modelin istatistiksel dağılımı bu uzayda öğrenmesini sağlamak

## neden ilginç buldum

- “continuous word representation” kavramını literatüre sokan ilk makale
- “kelimeler yakın bağlamlarda geçiyorsa anlamları da yakındır” fikrini matematiksel hale getirdi
- word2vec ve GloVe gibi modeller doğrudan bu çalışmanın soyundan geliyor
- self-attention ve transformer’lar da bu temelin üzerine inşa edildi: önce anlam uzayı (embedding), sonra bağımlılık modelleme (attention)
- 2003’te yazılmış olmasına rağmen bugünkü tüm LLM’lerin altında hâlâ bu fikir çalışıyor
- “dil öğrenilebilir bir olasılık dağılımıdır” yaklaşımıyla istatistiksel dil modellemeden öğrenmeye dayalı modellere geçişin eşiği

## notlar / ilgili kaynaklar

- 2013’te mikolov’un word2vec modeli, bu fikri hesaplama açısından ölçeklenebilir hale getirdi
- representation learning kavramının doğuş noktası
- loss function: maximize log-likelihood of word sequences (language model objective)
- _training bottleneck_: büyük kelime dağarcığında softmax’in yavaşlığı; mikolov’un negative sampling yaklaşımı bu sorunu çözdü
- modern modellerdeki embedding matrix yapısı (örneğin transformer input embedding) hala aynı fikri taşıyor.
- yoshua bengio daha sonra deep learning’in üç büyük isminden biri olarak turing ödülünü aldı (godfathers of dl: lecun, hinton ile birlikte)
- bengio abi dünyanın en fazla citation'ına sahip bilgisayar bilimcisi -> 1 milyon+