## Soru 1: Git Nedir?

Git bir versiyon kontrol sistemidir. Yaptığımız çalışmalara kontrol noktaları koyabildiğimiz daha sonrasında bu kontrol noktalarını inceleyip ihtiyaç halinde geri dönebildiğimiz bir sistemdir. Her bir kontrol noktasında (commit) dosyalarımızdaki değişiklikleri gözlemlememize olanak sağlar.

## Soru 2: "git pull" ile "git fetch" komutlarının farkı nedir?

"git fetch" yaptıktan sonra local branc'lerimiz güncellemelerini alır fakat "git merge" yapmadan bu değişiklikler working directory'e işlenmez. "git pull" ise hem "git fetch" yapar hem de "git merge" yapar. Yani remote repository'den güncellemeleri local repository'e alıp bunları working directory'e işler.

## Soru 3: Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse ve gönderdiği kodları "git pull" ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?

Kod gönderilmiş olabilir ama nereye? Kodumuzun yolculuğu ilk yazmaya başladığımız andan itibaren şu şekilde oluyor: İlk başta "git add" komutu ile kodumuzu staging area'ya alıyoruz. Ardından staging area'daki kodu local repository'e eklemek için "git commit" komutunu kullanıyoruz. En sonunda local repository'de bulunan kodlarımızı remote repository'e aktarmak için "git push" komutunu kullanıyoruz. Bu aşamaların hepsi incelenip hangi aşamada eksik olduğu bulunmalıdır.


## Soru 4: "git fetch origin" komutundaki *origin* neye karşılık gelmektedir?

Origin ifadesi projemizin remote repository'sini temsil eder.

## Soru 5: "HEAD" kelimesi neyi temsil etmektedir?

HEAD git içerisinde nerede olduğumuz gösterir. Genelde son commit'i gösterir.

## Soru 6: "Staging Area" ya da "Index" diye isimlendirilen bölge tam olarak ne demektir?

"git add" komutu ile dosyalarımız eklediğimiz alandır. Dosyalarımız local repository'e commit etmeden önce incelememizi sağlar. Ayrıca hangi dosyaların eklenip hangilerinin eklenmeyeceğini de belirleyebildiğimiz bir alandır.

## Soru 7: "Untracked file" ne demektir?

git tafından takip edilmeyen dosyalardır. Bu dosyaları takibe almak için "git add" komutunu kullanabiliriz.

## Soru 8: ".git" klasörünü silersek ne olur?

git ile daha önceden kaydetmiş olduğumuz tüm işlemler (versiyonlar, oluşturulan branchler vb.) silinir, projemizin sadece son hali elimizde kalır.

## Soru 9: Kendi lokalimizde her "git init" komutunu kullanıdığımızda otomatik olarak "ReadMe.md" dosyası oluşturulmasını istiyorsak ne yapmalıyız?

Önce içerisinde "ReadMe.md" olan bir template dosyası oluşturup ardından "git init --template=[oluşturduğumuz_dosyanın_konumu]" şeklinde bir kod yazdığımız zaman bundan sonra yazdığımız tüm "git init" komutları otomatik olarak "ReadMe.md" dosyasını otomatik oluşturur.

## Soru 10: Git konusunda bahsi geçen "branch" yapısı nedir? Bize ne sağlar?

Branch yapısı aynı proje üzerinde çalışırken farklı özellikler geliştirmemizi sağlar.

## Soru 11: Sıfırdan bir "branch" nasıl oluşturabiliriz?

Bunu iki şekilde yapabiliriz:

1-  "git branch [branch_ismi]" komutu ile yeni bir branch oluşturabiliriz fakat bu şekilde oluşturduğumuzda çalıştığımız branch yeni oluşturduğumuz branch olmaz. Bu branch'e geçmek için sonrasında "git checkout [branc_ismi]" komutunu kullanmamız gerekir.

2- "git checkout -b [branch_ismi]" komutu ile yeni bir branch oluşturup direkt o branch'e geçiş yaparız.

## Soru 12: Var olan bir "branch"e nasıl geçebiliriz?

Bunu iki komut ile yapabiliriz:

1- "git checkout [branck_ismi]"
2- "git switch [branck_ismi]"

## Soru 13: "git clone" komutunu kullanırken belirli bir spesifik branch'i sadece çekmek istiyorsak nasıl yapabiliriz?

"git clone -b [branch_ismi] [url]" komutu ile belirtilen yere branch ismini ardından ise projenin url'ini yazarak sadece istediğimiz branch'i çekebiliriz.
