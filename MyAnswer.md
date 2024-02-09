### Git Nedir?
- Git, kısaca yapacağımız işlerin (bireysel proje geliştirmeleri veya ekip içerisindeki projelerin geliştirilmesinde) takibini, yönetilebilirliğini ve bir sorun olması durumunda versiyonlar arası geçiş yaparak kontrol edilmesini sağlayan bir versiyon yönetim aracıdır.

### "git pull" ile "git fetch" komutlarının farkı nedir?
- Aslında her ikiside genel olarak bakıldığında uzak sunucuda var olan güncellemeleri (değişiklikleri) kendi yerel sunucunuza indirir fakat aralarında birkaç farklı yöntem mevcuttur.

- Git fetch, çalışma alanınıza herhangi bir etkide bulunmadan uzak sunucudaki değişiklikleri indirir ve sizin yerel çalışma alanınıza herhangi bir müdahalede bulunmaz.

- Git pull, hem uzak sunucudaki değişiklikleri bilgisayarınıza indirir hem de yerel sunucunuzdaki verileri onlar ile günceller.

### Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse ve gönderdiği kodları "git pull" ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?

- Arkadaşımızın kesin olarak bu kodları sunucuya doğru bir şekilde gönderebildiğini göz önüne alarak aşağıdaki işlemleri kontrol ederim.

- Bizim öncesinde açmış olduğumuz branchin eskide kalması sonucu branchini göremiyor olabiliriz. Böyle bir durumda kişinin branchine geçiş yapmamız gerekecektir.

- Conflict yemiş olabiliriz. Bu durum genelde localimize çekmeye çalıştığımız kodlar ile var olan kodlarımız arasında bir çakışma sonucu veyahut hali hazırda çalışıyor olduğumuz bir kod mevcutsa ve oradaki değişiklikleri stashlememiş veya geri almadan pull işlemi yapmaya çalıştıysak sorun çıkıyor olacaktır. Böyle bir durumu ise conflict aldığımız kodların problemlerini çözüp olması gerektiği hal ile güncelleyerek çözüme ulaşacağızdır.

### "git fetch origin" komutundaki "origin" neye karşılık gelmektedir?

- Origin, Türkçe'ye köken, orjinal gibi anlamlarla çevrilmiştir. Buradan bile yola çıkarak aslında local sunucumuzun işaret ettiğin ana projeyi temsil etmektedir. Mesela bir projeyi klonladık. Yapacağımız fetch işlemi veya pull işlemi doğrudan tanımlı projeye gider ve oradaki değişiklikleri kendi local sunucumuza getirir.

- Github, Gitlab... gibi ortamlara bir şeyleri pushladığımız zaman aslında git sistemine orayı referans almasını söylüyoruz. Hal böyleyken origin kullanıldığında sunucumuzun işaret ettiği yere göre yeni işlemler yapacaktır.

### "HEAD" kelimesi neyi temsil etmektedir?

- Head, kullanmış olduğumuz branchteki son commiti temsil eder.

### "Staging Area" ya da "Index" diye isimlendirilen bölge tam olarak ne demektir?

- Staging Area, bir tür geçici depolama alanıdır. Takibe aldığımız
değişikliklerimizi tuttuğumuz alandır. Burada değişiklikleri commite dahil etmeden önce inceleyip düzenleyebileceğiniz işlemleri yaparsınız.

### "Untracked file" ne demektir?

- Git tarafından takibe alınmayan dosyalardır. Gerektiği durumda git add komutunu kullanarak stage area tarafına aktararak takibe alınmasını sağlayabiliriz.

### ".git" klasörünü silersek ne olur?

- Git'e dair yapmış olduğumuz tüm değişiklikler ve kayıt altına aldığınız her şey geri dönülmez bir şekilde silinmiş olur.

### Kendi lokalimizde her "git init" komutunu kullanıdığımızda otomatik olarak "ReadMe.md" dosyası oluşturulmasını istiyorsak ne yapmalıyız?

- Ardından, Git'in şablon dizinini belirleyin ve bu dosyaları içine kopyalayın. Örneğin, ~/.git_template gibi bir dizin oluşturabilirsiniz.

- Son olarak, Git'in bu dizini kullanmasını sağlamak için git config komutunu kullanarak bu dizini belirtin

- git config --global init.templateDir ~/.git_template

### Git konusunda bahsi geçen "branch" yapısı nedir? Bize ne sağlar?

- Branchler bizler için main branchi kopyalayan ayrı bir dal oluşturur.

- Bir nevi yol gibi düşünün bu da o yola ek sapa başka bir yol oluşturur fakat her ikiside birbirinin kopyasıdır. 

- Amacımız genelde main branchtekileri değiştirmeden aynı branchi kopyalayarak tüm değişiklikleri orada yapmamızı sağlarız. Ardından her şey yolundaysa bu branchleri birbiri ile birleştiririz.

### Sıfırdan bir "branch" nasıl oluşturabiliriz?

- git checkout -b branch_adı

### Var olan bir "branch"e nasıl geçebiliriz?

- git checkout branch_adı