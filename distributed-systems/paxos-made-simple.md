# paxos made simple

**yazar(lar)**: leslie lamport

**yıl:** 2001

**kaynak/link:** [PDF](https://lamport.azurewebsites.net/pubs/paxos-simple.pdf)

## özet

bu makale, dağıtık sistemlerde "birden fazla node'un tek bir karara _güvenilir_ şekilde" nasıl varabileceği problemini çözmek için geliştirilen paxos algoritmasını (normalde okuması ve anlaması çok karmaşık, kompleks) basitleştirerek anlatıyor. lamport amcamız karmaşık akademik dilden ve karman çorman definition'lardan uzak durmuş. sadece algoritmanın genel fikirlerini ve özünü çok yalın bir dille aktarmış, ele aldığı konu da "bir kararı herkese nasıl kabul ettiririz?".

## neden ilginç buldum

-  paxos, modern consensus algoritmalarının tamamının temeli (multi-paxos, raft, zab...)
- lamport amcanın akademik mizahı eğlenceli, "paxos aslında yunan kasabası..."
- 20 yıl önce yazılmasına, çizilip konuşulmasına rağmen hala günümüzdeki her şeyin temeli
- lamport amca bilgisayar biliminin kemiklerinden birisi: time, order, causality, tla+, paxos... hepsi lamport amcanın imzası

## notlar / ilgili kaynaklar

- leslie lamport, 2013 turing ödülü sahibi (bilgisayar biliminin nobel ödülü)
- bu makale (paxos made simple) aslında 1990'larda yazdığı ama kimsenin anlamadığı "the part-time parliament" makalesinin sadeleştirilmiş hali
- raft (2014) bu makaleye tepki olarak, "paxos çok soyut ve karmaşık, biz daha güzel ve basitini yapalım" diyerek yazıldı (geliştirildi)
- dağıtık sistemler tarihine baktığında paxos, “consensus” kelimesinin matematiksel tanımını getiren ilk çalışma