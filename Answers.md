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

## Soru 5: "HEAD" kelimesi neyi temsil etmektedir?

**HEAD** kavramını bir gösterge veya işaretci olarak düşünebiliriz.     
Anlık olarak çalışmış olduğumuz ortam hakkında bilgi verir. 
- Bu en son atılmış commit
- Yada üzerinde çalışma yapmış olduğumuz branch
- Veya geçmişde var olan bir commit'i incelemek istedim ve o commite geçtim, bunu bir örnek ile anlatayım. Örneğin 1,2,3,4 adında commitlerimiz var. Şu anda **HEAD** kavramı 4'ü(en son commit) işaret eder. Ben bir ihtiyaç doğrultusunda 2. commit'te geçip sadece o commit sırasında yapılmış olan değişiklikleri incelemek istedim ve 2. commit'e geçiş yaptım. Bu durumda **HEAD** 2. commit'i temsil eder.

## Soru 6: "Staging Area" ya da "Index" diye isimlendirilen bölge tam olarak ne demektir?

![](data:image/png;base64,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)


**Staging Area** veya **Index**, Git'in commit yapmadan önce değişiklikleri hazırlamanızı sağlayan bir ara bölgedir. Bu bölge, projenizdeki dosyalarda yaptığınız değişiklikleri seçip, bir sonraki commit'e dahil etmek üzere belirlemenizi sağlar. Bu ara bölge sayesinde, projenizdeki birden fazla değişikliği gruplamak, sadece belirli dosyaları commit'e dahil etmek veya commit yapmadan önce değişiklikleri kontrol etmek gibi avantajlar elde edersiniz. 

`git add` komutunu kullanarak dosyalarımı **Staging Area** kısmına ekleme işlemini yaparız.

## Soru 7: "Untracked file" ne demektir?

*Untracked file* kelime anlamından da anlayabileceğimiz gibi, Git tarafından takip edilmeyen dosyalardır. Bu dosyalar, projenizde bulunabilir, ancak Git bu dosyaların değişikliklerini veya durumunu izlemez.

Örneğin bu dosyamıza resim adında bir görüntü ekledim. Şimdi `git status` ile güncel durumumuza bir bakalım.

![](/screenshots/1.png)

resim.png dosyasını ben daha önceden `git add` kullanarak ekleme yapmadığım için Untracked kısmında duruyor ve Git tarafından takip edilmediği anlamına geliyor.

## Soru 8: ".git" klasörünü silersek ne olur?

Eğer ".git" klasörünü silersek, projemizin Git ile yönetilen tüm geçmişi, branch bilgileri, commit bilgileri gibi Git ile ilişkilendirilmiş tüm veriler kaybolur.

## Soru 9: Kendi lokalimizde her `git init` komutunu kullanıdığımızda otomatik olarak "ReadMe.md" dosyası oluşturulmasını istiyorsak ne yapmalıyız?

Öncelikle içerisinde Readme.md olan bir şablon dosya hazırlayacağız. Ardından yeni bir repo oluşturmak istediğimizde `git init -- template [şablonDosyası konumu]` komutunu kullanarak oluşturabiliriz.

## Soru 10: Git konusunda bahsi geçen "branch" yapısı nedir? Bize ne sağlar?

Bir proje üzerinde birden fazla geliştirici çalışıyor olabilir, bu durumda geliştiriciler birbirlerini etkilemeden kendi işlerinde çalışabilmelerini ve aynı anda birçok özelliği veya geliştirme yapabilmeyi sağlar.

Her bir branch farklı geliştirmeleri, değişiklikleri veya özellikleri içerebilir.

## Soru 11: Sıfırdan bir "branch" nasıl oluşturabiliriz?

Branch oluşturmak için temel olarak yapabileceğimiz iki yöntem var.

 1 - `git branch branch_ismi` komutunu kullanarak yeni bir branch oluşturabiliriz. Ardından `git checkout branch_ismi` komutunu kullanarak da oluşturduğumuz yeni branch'e geçiş yapabiliriz.

 2 - Yeni bir branch oluşturma ve daha sonra o branch'e geçme işlemini tek bir komut ile de yapabiliriz. İşte o komut:
 `git checkout -b branch_ismi`

 ## Soru 12: Var olan bir "branch"e nasıl geçebiliriz?

Branchler arası geçişin nasıl yapıldığını söylemeden önce hangi branch üzerinde olduğumuzu nasıl öğrenebiliriz ona bakalım.

Bu bilgiyi öğrenebilmek için `git branch` komutunu kullanabiliriz. Mevcut yani şu anda çalışmış olduğumuz branch yıldız(*) ile işaretlenmiş olan branchdir.

![](/screenshots/2.png)

Branch değiştirmek için kullanabildiğimiz komutlar.
- `git checkout branch_ismi`
- `git switch branch_ismi` 

## Soru 13: "git clone" komutunu kullanırken belirli bir spesifik branch'i sadece çekmek istiyorsak nasıl yapabiliriz?

Remote sunucudan sadece belirli bir branch'i çekmek istiyorsak;
`git clone -b branch_ismi url` komutunu kullanabiliriz.
 Örneğin **ödev** adında bir branchimiz olsun ve remote sunucudan sadece bu branchi çekmek istiyorsak;
 
  `git clone -b ödev url`