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
- Sıfırdan bir "branch" nasıl oluşturabiliriz?
- Var olan bir "branch"e nasıl geçebiliriz?
- "git clone" komutunu kullanırken belirli bir spesifik branch'i sadece çekmek istiyorsak nasıl yapabiliriz?
- "Merge conflict" ne demektir?
- "git log" komutu ile hangi bilgileri görebiliriz?
- "git diff" ile kaç farklı iki durumun arasındaki değişiklikleri görebiliriz?
- Git reset ile neyi geri alıyoruz?
- "git commit" ile "git push" arasındaki fark nedir?
    * git commit ile yaptığımız değişiklikleri local repositorye yazarız.
    * git push ile localdeki değişiklikleri remote repositorye göndeririz.

- Atomic commit ne demektir?
- Repository ne demektir?
- "git tag" nedir? "git branch"’ten farkı nedir?
- Git'i görsel olarak kullanabilmek için hangi üçüncü taraf araçları ve uygulamaları kullanabiliriz?
- "GitHub" ile "git" arasındaki fark nedir? GitHub benzeri diğer siteler nelerdir? GitHub veya diğer sitelerdeki kullanıcı adlarını yazar mısınız?
- main ya da master branch'inin diğer branchlerden farkı nedir?
