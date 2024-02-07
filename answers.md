- Git Nedir?
    * Git, bir versiyon kontrol sistemidir. 
    * Git'in temel amacı, bir proje dosyalarının farklı versiyonlarını ve bu versiyonlar arasındaki değişiklikleri kaydetmek ve izlemektir.

- "git pull" ile "git fetch" komutlarının farkı nedir?
    * git fetch ile remote repositorydeki tüm değişiklikleri local repositorye indirir, ancak bu değişiklikleri doğrudan mevcut çalışma dalına uygulamaz.
    * git pull ise uzak depodaki değişiklikleri alır ve doğrudan mevcut çalışma dalına entegre eder.
    * Yani temel fark, git fetch'in uzak depodaki güncellemeleri sadece yerel depoya indirmesi ve bunları mevcut çalışma dalına entegre etmemesi, git pull'un ise güncellemeleri alıp doğrudan mevcut çalışma dalına entegre etmesidir.

- Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse ve gönderdiği kodları "git pull" ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?
    * yanlış branche atmış olabilir
    * yaptığı değişiklikleri pushlamamış olabilir
    * git fetch komutunu çalıştırmamış olabiliriz.

- "git fetch origin" komutundaki "origin" neye karşılık gelmektedir?
    * origin uzak sunucuya karşılık gelir.

- "HEAD" kelimesi neyi temsil etmektedir?
    * mevcutta çalıştığımız branchin son commitini işaret eder.
    
- "Staging Area" ya da "Index" diye isimlendirilen bölge tam olarak ne demektir?
- "Untracked file" ne demektir?
- ".git" klasörünü silersek ne olur?
- Kendi lokalimizde her "git init" komutunu kullanıdığımızda otomatik olarak "ReadMe.md" dosyası oluşturulmasını istiyorsak ne yapmalıyız?
- Git konusunda bahsi geçen "branch" yapısı nedir? Bize ne sağlar?
    * Branch, projenin farklı çalışma kopyalarını oluşturur ve bize bağımsız olarak geliştirme yapılmasını sağlar.
    * Yeni feature geliştirme veya var olan bir bug fix yapmak için yeni branchler açıp bunlarla remote branchi etkilemeden çalışabiliriz.

- Sıfırdan bir "branch" nasıl oluşturabiliriz?
    * git branch <branchadi> komutuyla oluşturabiliriz.

- Var olan bir "branch"e nasıl geçebiliriz?
    * geçmek istediğimiz branche git checkout <branchadi> ile geçiş yapabiliriz.

- "git clone" komutunu kullanırken belirli bir spesifik branch'i sadece çekmek istiyorsak nasıl yapabiliriz?
    *  git clone -b <branchadi> <repo_url> komutunu kullanabiliriz.

- "Merge conflict" ne demektir?
    * versiyon kontrol sistemi kullanılırken iki veya daha fazla farklı kaynaktan gelen değişikliklerin uygun bir şekilde birleştirilemediği durumu ifade eder. 

- "git log" komutu ile hangi bilgileri görebiliriz?
    * commit geçmişini gösterir. commit id - tarih - yazar - commit mesajı bilgilerini içerir.

- "git diff" ile kaç farklı iki durumun arasındaki değişiklikleri görebiliriz?
    * git diff, iki durum arasındaki farkları gösterir.

- Git reset ile neyi geri alıyoruz?
    * gitmeyen commitleri geri alır.

- "git commit" ile "git push" arasındaki fark nedir?
    * git commit ile yaptığımız değişiklikleri local repositorye yazarız.
    * git push ile localdeki değişiklikleri remote repositorye göndeririz.

- Atomic commit ne demektir?
    * düzgün anlaşılır yapılan işle ilgili bilgileri özetleyebilen commit mesajı 

- Repository ne demektir?
    * Bir repository, bir projenin tüm dosyalarının, geçmiş versiyonlarının ve yapılandırma bilgilerinin depolandığı bir yerdir. 

- "git tag" nedir? "git branch"’ten farkı nedir?
    * git tag belirli bir commiti etiketlemek için kullanılır.
    * branchler geliştirme yapılmak için kullanılır.

- Git'i görsel olarak kullanabilmek için hangi üçüncü taraf araçları ve uygulamaları kullanabiliriz?
    * Fork,Github Desktop, Sourcetree 

- "GitHub" ile "git" arasındaki fark nedir? GitHub benzeri diğer siteler nelerdir? GitHub veya diğer sitelerdeki kullanıcı adlarını yazar mısınız?
- main ya da master branch'inin diğer branchlerden farkı nedir?
