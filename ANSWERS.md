# Answers - Git

- Git Nedir?
  - Linus Torvalds deyişi ile "Stupid Content tracker" (Aptal içerik takip sistemi) veya "Global Information Tracker" (Küresel Bilgi Sistemi)
  - Dosyalar üzerinde versiyonlama, Log takibi yapma
  - Bir doysa üzerinde bir den fazla kişi değişiklik yapacaksa birlikte çalışmak için kullanma

- "git pull" ile "git fetch" komutlarının farkı nedir?
  -	"git fetch"  ->  kendi localimin remotedan haberdar olması için , değişiklikleri getirir ama güncellemez.
  - "git pull"  ->  fetch ile alınan değişiklerle Local güncellenir.

- Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse ve gönderdiği kodları "git pull" ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?
  - Göndermiş ama nereye ?
  - Değişiklikler "git add" ile staging area atılır
  - "git commit" komutu ve commit mesajı ile kalıcı olarak kaydedilir
  - "git push" local repository'deki commitleri uzak repoya gönderir
  - Bu işlemlerden hepsi yapılmalı. Genelde "git push" unutulur :)

- "git fetch origin" komutundaki "origin" neye karşılık gelmektedir?
  - Uzak sunucu
  - Reponuzun uzak sunucudaki halini çekebilirsiniz.

- "HEAD" kelimesi neyi temsil etmektedir?
  - Mevcut konumunuzu gösterir
  - Genellikle son commit'i işaret eder.

- "git log" komutu ile hangi bilgileri görebiliriz?
  - Commit Tarihçesi :
    - Commit Hash (SHA-1)
    - Yazar
    - Tarih
    - Commit Açıklaması

- "git diff" ile kaç farklı iki durumun arasındaki değişiklikleri görebiliriz?
  - git diff -> Dizinizdeki değişiklikler vs "staging area"
  - git diff --cached  ->  "Staging area" vs son commit
  - git diff <commit1> <commit2>  ->  İki commit arasındaki farklar
  - git diff <branch1> <branch2>  ->  İki branch arasındaki farklar

- Git reset ile neyi geri alıyoruz?
  -  Remota gitmeyen Commitlerinizi geri alır.
  - soft , mixed , hard

- "git commit" ile "git push" arasındaki fark nedir?
  - "git commit"  ->  Local repoya kayıt
  - "git push"  ->  Remote repoya kayıt