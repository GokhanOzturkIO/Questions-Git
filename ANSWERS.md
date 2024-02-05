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