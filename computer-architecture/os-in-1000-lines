# Operating System in 1000 Lines

**yazar**: Seiya Nuta

**yıl**: 2023

**kaynak/link**: [Makale](https://1000os.seiya.me/en/)

## özet

İşletim sistemleri, birçok soyutlamayı barındıran ve çeşitli uygulamaların çalışmasına ortam sağlayan; kısacası donanım ile kullanıcı arasında köprü görevi gören yazılımlardır. Bu yazıda RISC-V mimarisi kullanılarak temel I/O işlemlerinden scheduling (zamanlama) uygulamasına, sayfalamadan diske yazma işlemlerine kadar pek çok kavram pratikte gösteriliyor. Projenin hedefi, bu konuları 1000 satırın altında, anlaşılır bir örnek çerçevesinde sunmaktır.

## neden ilginç buldum

- Herkesin üzerinde uygulama koşturduğu ve/ya çalıştığı en az bir işletim sistemi vardır. Böyleyken en azından sürece dair salt teorik bilginin ötesinde bilgilenmemiz gerekiyor diye düşünüyorum.

- Kernel’in boot sürecinden sonra nasıl yüklendiğini ve temel mekanizmaların — örneğin context switch işleminin — RISC-V bağlamında nasıl uygulandığını görmek isteyenler için mükemmel bir kaynak. Çoğu kaynakta context switch yalnızca teorik düzeyde anlatılır veya PCB’ye (Process Control Block) kaydedilen context bilgisinin nasıl geri yüklendiği parça parça gösterilir; bu yazıda ise bu süreç, kernel entry içinde bütünlüklü bir örnek üzerinden doğrudan uygulanarak açıklanıyor.

- xv6 gibi öğrenme amaçlı işletim sistemleri genelde x86 odaklıyken, RISC-V ile hazırlanmış ve pratik odaklı bir giriş olması cezbedici.

- Yazı, klasik işletim sistemi kitaplarına (ör. Understanding the Linux Kernel, Operating Systems: Three Easy Pieces) kıyasla ne yalnızca teoriye sıkışıyor ne de kavramları parça parça verip bütünlüğü kaybediyor; adım adım ilerliyor.

## Notlar / İlgli Kaynaklar

- OS: Three Easy Pieces kitabı kavramları oturtmak için yararlı olabilir. Ayriyeten riscV özelinde deneme/okuma yapmak da gerekebilir. Onun dışında yazı içerisinde kavramlara da değinerek implementasyonu gerçekleştirdiğinden anlamak için yeterli olacağını düşünüyorum
