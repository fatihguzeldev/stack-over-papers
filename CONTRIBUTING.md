# katkıda bulunma rehberi

bu rehber, yeni makale eklerken ortak bir yapı ve dil tutarlılığı sağlamayı amaçlar. aşağıdaki adımları izleyerek katkıda bulunabilirsiniz.

## genel yaklaşım

- **neden ilginç bulduğunuzu** mutlaka belirtin; kişisel bağlam ve çıkarımlar değerli.
- kaynak türü esnek: **akademik makale**, **teknik blog yazısı**, **kitap bölümü** vb. olabilir.
- içerik teknik ve kaliteli olmalı; tartışma ve keşfe katkı sunmalı.

## folder yapısı

her alt disiplin kendi folder'ında tutulur. dosya yapısı:

```
alt-disiplin-ismi/
  README.md
  makale-basligi.md
```

## isimlendirme kuralları

- folder ve dosya isimleri küçük harf ve tire `-` kullanılarak yazılmalıdır.
  - örnek folder: `distributed-systems`
  - örnek dosya: `eventual-consistency.md` veya `makale-basligi.md`
- dosyanın ismi, makalenin başlığını anlamlı bir şekilde yansıtmalıdır.

## alt disiplin `README.md` formatı

her alt disiplin folder'ındaki `README.md` şu şablonu izlemelidir:

```
`alt disiplin ismi` makaleleri:

- [makale ismi](dosya path)
...
```

- yeni eklenen her makaleyi bu listeye ekleyin. tercihen en yeni ekleme en üste gelecek şekilde sıralayın.

örnek:

```
`distributed systems` makaleleri:

- [Dynamo: Amazon's Highly Available Key-value Store](dynamo-amazon-key-value-store.md)
- [Paxos Made Simple](paxos-made-simple.md)
```


## yeni alt disiplin oluşturma (klasör yoksa)

eğer paylaşmak istediğiniz kaynak için uygun bir alt disiplin klasörü yoksa, onu siz oluşturmalısınız. Örneğin `distributed-systems`, `machine-learning`, `operating-systems` gibi.

1. yeni folder oluşturun: `alt-disiplin-ismi/`
2. içerisine bir `README.md` ekleyin ve yukarıdaki alt disiplin `README.md` şablonunu kullanarak başlatın.
3. sonrasında makale dosyanızı (`makale-basligi.md`) ekleyip aynı folderdeki `README.md` listesine bağlantısını ekleyin.

örnek folder yapısı:

```
distributed-systems/
  README.md
  dynamo-amazon-key-value-store.md
```

not: eğer alt disiplin folder'ı zaten varsa, mevcut yapıya ve liste formatına uymalısınız; farklı bir biçim kullanmayın.

## makale dosyası şablonu (`makale-basligi.md`)

aşağıdaki şablonu kullanın ve alanları doldurun:

```
# makale başlığı

**yazar(lar):**
**yıl:**
**kaynak/link:**

## özet
makalenin kısa özeti, ne hakkında, hangi problemi çözüyor veya hangi konuyu ele alıyor

## neden ilginç buldum
- bullet
- points
...

## notlar / ilgili kaynaklar
- eğer eklemek isterseniz
- makaleyle ilgili blog yazıları
- tartışmalar
- görseller ya da anlamaya yardımcı kaynaklar
- alınan kişisel notlar
```

## halihazırda eklenmiş makalelere katkı verme

halihazırda repo içinde bulunan makalelere de katkıda bulunabilirsiniz. özellikle **notlar / ilgili kaynaklar** bölümlerine kendi yorumlarınızı, ek kaynakları veya tartışma notlarınızı eklemek, makalelerin anlaşılmasını ve topluluk için faydasını artırır.

katkılarınızı eklerken mevcut format ve dil tutarlılığına uymanız yeterlidir; makaleyi tamamen değiştirmeye çalışmayın. küçük eklemeler, düzeltmeler ve ek açıklamalar da değerlidir.

## adım adım ekleme

1. uygun alt disiplini belirleyin.
   - yoksa yeni folder açın ve `README.md` dosyasını alt disiplin şablonuyla oluşturun.
   - varsa mevcut folder'ın yapısına ve formatına uyun.
2. alt disiplin folder'ında makale dosyanızı oluşturun: `makale-basligi.md` ve makale şablonunu doldurun.
3. aynı folderdeki `README.md` dosyasına, yeni makaleyi şu formatla ekleyin: `- [makale ismi](makale-basligi.md)`.
4. değişiklikleri anlamlı bir mesajla commit edin.
5. bir PR açın. PR açıklamasında kısa bir özet ve “neden ilginç” bölümü yer alsın.

## commit ve PR kuralları

- bir commit/PR mümkünse tek bir içerik eklemelidir.
- commit mesajı önerisi: `add(alt-disiplin): makale-basligi.md`.

## kalite ölçütleri ve içerik tutarlılığı

- şablonu eksiksiz doldurun; **özet** ve **neden ilginç buldum** bölümleri zorunludur.
- bağlantılar çalışır olmalı; arşiv/doi linki varsa ekleyin.
- Tartışma ve ek kaynaklar opsiyonel ama teşvik edilir.

## lisans ve atıf

- bu repo **CC BY-SA 4.0** lisansı ile paylaşılır. ayrıntı için üst düzey `README.md` ve `LICENSE` dosyasına bakın.
- üçüncü taraf içeriklerin (makale, görsel, kod parçası) lisanslarına uyun; uygun atıf verin.
