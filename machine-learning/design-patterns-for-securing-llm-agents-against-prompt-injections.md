# Design Patterns for Securing LLM Agents against Prompt Injections

**Yazar(lar):** Luca Beurer-Kellner, Beat Buesser, Ana-Maria Cretu, Edoarda Debenedetti, Daniel Dobos, Daniel Fabian, Marc Fischer, David Froelicher, Kathrin Grosse, Daniel Naeff, Ezinwanne Ozoani, Andrew Paverdi, Florian Tramer, Vaclav Volhejn

**Yıl:** 2025

**Kaynak/Link:** [PDF](https://arxiv.org/abs/2506.08837)

---

## Özet

Günümüzde yaşanan _Agentic AI_ dönüşümünde karşılaşılabilecek güvenlik risklerine odaklanıyor. Özellikle yetkilerin kontrolsüzce verildiği agent yapılarına dikkat çekiliyor. Böyle durumlarda faydadan çok zarar ortaya çıkabileceği belirtiliyor. Bunun önüne geçmek için altı farklı design pattern öneriliyor ve bu patternlerin avantajları, dezavantajları, kullanım senaryoları gibi alanlarda tartışılıyor.

---

## Neden İlginç Buldum

- Pek çok firma _Agentic AI_ dönüşümüne odaklanmış durumda, fakat LLM’lerin deterministik olmaması ve özellikle **function-calling** gibi özelliklerin yeni güvenlik açıklarını beraberinde getirmesi ciddi bir problem yaratıyor.
- Makale, production seviyesinde agent kullanımında kritik öneme sahip olan **altı farklı güvenlik patternini** örnek senaryolarla inceliyor.
- Şu an geldiğimiz noktada hâlâ **prompt injection** sorunu çözülebilmiş değil. Agentic AI ekosisteminde bu alanda büyük bir boşluk var (belki buradan bir startup fikri çıkabilir).

---

## Notlar / İlgili Kaynaklar

- Önerilen patternler çoğunlukla LLM’e **dışarıdan verilen external data** kaynaklı riskleri azaltmaya odaklanıyor. Okurken bu noktaya dikkat edin.
- Okurken dikkat edilmesi gereken nokta şu: bazı örneklerde “Ben bunu prompt ile inject etsem yine sızmaz mıyım?” sorusu akla gelebiliyor. Yazarlar da bu duruma dikkat çekmiş. Yani önerilen yöntemler tamamen çözüm değil, kısmi önlemler.
- Genel olarak fikirlerin kökeni **Simon Willison**’un blog yazılarında bulunuyor. Makalede de bu bloga atıf yapılıyor. Merak edenler için: [Simon Willison's Weblog](https://simonwillison.net/).
