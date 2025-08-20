# the byzantine generals problem

**yazar(lar):** Leslie Lamport, Robert Shostak, Marshall Pease

**yıl:** 1982

**kaynak/link:** [PDF](https://lamport.azurewebsites.net/pubs/byz.pdf)

## özet

bu makale, dağıtık sistemlerde güvenilmez aktörler (hatalı veya kötü niyetli) varken nasıl karar alınabileceğini inceliyor. temel problem, generallerin bir saldırı planını koordine etmek istemesi ama bazılarının ihanet edebileceği bir ortamda doğru ve tutarlı kararlar almanın yollarını araştırmak. konsept bugün fault-tolerant sistemler ve consensus algoritmalarının temelini oluşturuyor.

## neden ilginç buldum

- _distributed systems_ ve _fault tolerance_ konularının temelini oluşturuyor, anlayışı kökten değiştirdi
- _consensus_ problemini formalize eden ilk çalışmalar arasında
- klasik "impossible problem" olarak biliniyor, ama çözümü matematiksel ve elegant
- bugün _blockchain_ ve _replicated state machine_'lerin altyapısına direkt ilham verdi

## notlar / ilgili kaynaklar

- paxos ve raft makaleleri bu çalışmanın devamı niteliğinde
- paxos: konsept olarak müthiş ama implementasyonu zor, Lamport'un matematiği epey sağlam
- raft: paxos'a göre daha anlaşılır, log replication ve lider seçimi net
- pratikte etcd, consul gibi sistemlerde raft kullanılıyor, paxos genelde akademik veya core altyapılarda
- paxos'un toy implementation'ını yapmıştım, kafa açıcıydı :D
- consensus mantığını anlamak, fault-tolerant sistem tasarımı için zorunlu bir checkpoint
