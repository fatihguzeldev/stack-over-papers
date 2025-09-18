# Writing a C Compiler

**yazar(lar)**: Nora Sandler

**yıl**: 2017

**kaynak/link**: [Blog](https://norasandler.com/2017/11/29/Write-a-Compiler.html)

## özet

nora sandler bu blog serisinde sıfırdan, adım adım bir c compiler yazma sürecini anlatıyor. c normalde de self-hosted, yani compiler'ı kendi dilinde. c dilinin tamamını değil, küçük ama çalışan bir kısmını derleyebilecek bir compiler hedefliyor. süper bir öğretici yolculuk, production-ready bir compiler değil hedeflenen şey. öğrenmek için küçük ama gerçek bir derleyici.

## neden ilginç buldum

- genelde compiler anlatıları teorik olur ya da küçük dillerini icat ediyorlar. burada c üzerinden öğreniyorsun, c biliyorsunuz değil mi?

- ilk derleyici çok basit bir ifadeyi (ör 2+3\*4) çalıştırabiliyor. sonra her bölüm yeni bir feature ekleniyor. böylece "küçük zaferleri" bize net bir şekilde gösteriyor.

## notlar / ilgili kaynaklar

- nora ablamız sonradan bu blog serisini kitaba döküyor, aha da link: [Writing a C Compiler: Build a Real Programming Language from Scratch](https://www.amazon.com/Writing-Compiler-Programming-Language-Scratch/dp/1718500424)

- her şeyi elle yaparak "core" mantığı çok güzel öğretiyor

- bütün temel compiler kavramları var: lexer, parser, ast, codegen

- flow control yapıları da var: if, while...

- en sonda da assembler geliyor...