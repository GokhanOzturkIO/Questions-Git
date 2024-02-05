## Soru 1: Git Nedir?

Git, Linux kurucusu Linus Torvalds tarafından geliştirilen bir versiyon kontrol sistemidir. 
Bu sistem bir proje üzerinde birden fazla kişinin çalışmasına, projede yapılan değişikliklerin daha kolay bir şekilde bu projede çalışan kişilere iletebilmeyi sağlayan, projede yaptığımız değişiklikleri takip edebildiğimiz, yapılan değişiklik kim tarafından yapıldığını gösteren bir versiyon kontrol sistemidir.

## Soru 2: `git pull` ile `git fetch` komutlarının farkı nedir?

- `git fetch` komutu, remote sunucudaki repoda veri değişikliği oldu ise o verileri çekmeyi amaçlar, ancak yerel çalışma dizinindeki dosyaları güncellemez.

- `git pull` komutu, **remote sunucudan veri çekmeyi ve otomatik olarak mevcut çalışma(local repository) dizinindeki dosyaları güncellemeyi amaçlar**.
Bu komut, `git fetch` ve ardından `git merge` işlemlerini birleştirerek kullanır. Yani, uzak depodan verileri çeker ve daha sonra otomatik olarak yerel çalışma dizinindeki dosyaları günceller.

## Soru 3: Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse ve gönderdiği kodları `git pull` ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?

Eğer gönderilen değişiklikleri `git pull` ile lokalimize alamıyorsak, arkadaşımız yazdığı kodları remote sunucuda bulunan repoya göndermemiştir. Yani `git push` komutunu kullanmamıştır.

Yani arkadaşımız değişiklikleri yaptıktan sonra `git commit -m ""` yaptıktan sonra yaptığı değişikliklerin uzak sunucuya gönderildiğini sanmış ama `git push` komutunu kullanarak herhangi bir şekilde işlem yapmadığı için değişiklikler uzak sunucuya gönderilmemiş ve bizde bu değişikleri `git pull` ile local çalışma alanımıza dahil edemedik.

## Soru 4: `git fetch origin` komutundaki *origin* neye karşılık gelmektedir?

`git fetch origin` komutundaki *origin* ifadesi remote repositoryi temsil eden bir isimdir. 

**origin terimi**, varsayılan olarak birçok Git deposunda kullanılan yaygın bir isimdir, ancak projenizin yapılandırmasına bağlı olarak farklı bir isim de kullanılabilir. Eğer Git'e remote bağlantı eklerken farklı bir isim kullanmış olsa idik onu kullanmamız gerekirdi.

#### Peki Bunun Yapılandırmasını Nasıl Yapıyorduk?

`git remote add istediğimizBirİsim url` komutunu kullanarak ayarlamasını yapıyorduk. :)