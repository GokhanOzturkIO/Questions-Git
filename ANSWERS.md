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

- Atomic commit ne demektir?
  - Değişiklikler düzenli, tutarlı ve yönetilebilir bir şekilde kaydetmek
  - Düzgün bir history ve anlaşılır commit mesajları

- Repository ne demektir?
  - Dosyalarının ve değişikliklerin depolandığı yer

- "git tag" nedir? "git branch"’ten farkı nedir?
  - "git tag" -> belirli bir commit'i veya projenin bir noktasını "etiketlemek" için kullaılır
  - tag işaretlemek, etiketlemek için kullanılırken ; Branch'ler, geliştirmeleri izlemek ve paralel geliştirme için.

- Git'i görsel olarak kullanabilmek için hangi üçüncü taraf araçları ve uygulamaları kullanabiliriz?
  - Fork
  - GitHub Desktop
  - GitKraken
  - SourceTree
  - GitExtensions

- "GitHub" ile "git" arasındaki fark nedir? GitHub benzeri diğer siteler nelerdir? GitHub veya diğer sitelerdeki kullanıcı adlarını yazar mısınız?
  - "git" VSC (Versiyon kontrol sistemidir)
  - GitHub bu projelerin barındırılması, işbirliği yapılması ve paylaşılması için bir platform sağlar
  - GitLab
  - Bitbucket
  - Azure DevOps
  - GitHub: musaerbay

- main ya da master branch'inin diğer branchlerden farkı nedir?
  - Ana Geliştirme branch'idir. Projenin Kalbidir :)
  - Bu branch genelde korunur. İzin olmadan değişiklik yapılamaz.
  - Diğer branchler genelde bu branchten merge alır.
