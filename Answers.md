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

## Soru 14: "Merge conflict" ne demektir?

Farklı branch'ler üzerinde çalıştıktan sonra bu branchler amaçlarına ulaştıktan sonra birleştirilir. Birleştirme aşamasında çatışma olması durumuna "Merge conflict" denir. Aynı dosya içerisinde aynı satırlarda değişiklik yapılmışsa ya da bir tarafta dosya silinmişken diğer tarafta o dosya üzerinde değişiklik olmuşsa vb. durumlarda bu yaşanabilir. Bu durumalarda meydana gelen çatışmayı çözmek için yapılan değişikliklerin dikkatlice incelenmesi gerekir.

## Soru 15: "git log" komutu ile hangi bilgileri görebiliriz?

Bu komut ile git projesinde o anda bulunduğumuz branch'in commit geçmişini görüntüleriz.


## Soru 16: "git diff" ile kaç farklı iki durumun arasındaki değişiklikleri görebiliriz?

1- "git diff" Bu komut ile working directory ile staging area arasındaki farkları görebiliriz.

2- "git diff --cached" Bu komut ile staging area ile local repository arasındaki farkları görebiliriz.

3- "git diff HEAD" Bu komut ile local repository ile working directory arasındaki farkları görebiliriz.

4- "git diff [commit_id] [other_commit_id]" Bu komut ile iki commit arasındaki farkları görebiliriz.

5- "git diff [branch_ismi] [diger_branch_ismi]" Bu komut ile iki branch arasındaki farkları görebiliriz.

## Soru 17: Git reset ile neyi geri alıyoruz?

Sadece "git reset" komutunu kullanırsak staging area'ya alınmış olan değişiklikleri geriye alırız.

"git reset [commit_id]" ile commitlerimize geri dönebilir ve sonrasındaki commitleri ortadan kaldırabiliriz fakat bu tek başına kullanılmaz çünkü bu kodlarda olan çatışmalara nasıl karşılık vereceğimizi belirtmemiz gerekir bu yüzden de bazı parametler kullanırız. Hemen onlara göz atalım:

"git reset --soft [commit_id]" burada görmüş olduğunuz gibi soft parametresini ekledik. Bu parametre geçmiş olduğumuz commit'ten sonra yapmış olduğumuz değişiklikleri kaybetmek istemediğimiz zaman bize yardımcı oluyor.

"git reset --hard [commit_id]" burada iste hard parametresini kullandık. Bu parametre ise belirtmiş olduğumuz commit'ten sonraki değişikliklerin tamamını siler.

## Soru 18: "git commit" ile "git push" arasındaki fark nedir?  

"git commit" komutu working directory'den staging area'ya aldığımız değişiklikleri local repository'e kaydederken "git push" komutu local repository'de olan değişiklikleri remote repository'e kaydeder.

## Soru 19:Atomic commit ne demektir?

Her bir commit'in sadece belirli bir işe ayrılmasıdır. Örnek vermek gerekirse kod üzerinde bir kısmın değiştirilmesi, yeni bir kısım eklenmesi ve bir kısmında çıkarılması gerekiyorsa. Bu her bir parça ayrı ayrı yapılıp ayrı commit edilmesi ve bu commit'lerin mesajlarında anlamlı bir şekilde yapılan işi anlatması gerekmektedir.

## Soru 20: Repository ne demektir?

Kodların veya dosyaların koyulduğu ve commitlerle kayıtların yapıldığı bir saklama alanıdır.


## Soru 21: "git tag" nedir? "git branch"’ten farkı nedir?

"git tag" etiketleme işlemi yapar ve genellikle projenin sürüm numarasını ya da önemli bir noktayı işaretler.

"git branch" proje için farklı dallar oluşturur. Bu dallarda proje için farklı özellikler geliştirilebilir.

## Soru 22: Git'i görsel olarak kullanabilmek için hangi üçüncü taraf araçları ve uygulamaları kullanabiliriz?

1- [Github Desktop](https://desktop.github.com/)

2- [Git Kraken](https://www.gitkraken.com/git-client) (Ücretli)

3- [Source Tree](https://www.sourcetreeapp.com/)

## Soru 23: GitHub" ile "git" arasındaki fark nedir? GitHub benzeri diğer siteler nelerdir?

Git: Bir versiyon kontrol sistemidir ve local olarak projelerin sürümlenmesi ve depolanması için kullanılır.

GitHub: Git repolarının online olarak paylaşılmasını sağlayan ve bu şekilde farklı cihazlardan bu repolara erişim sağlanarak aynı proje üzerinde çalışmasına olanak sağlayan bir platformdur.

Github benzeri siteler: GitLab, Bitbucket, GitKraken Glo.

## Soru 24: main ya da master branch'inin diğer branchlerden farkı nedir?

main ya da master branch'i projenin geliştirildiği ana daldır. Git repository'si ilk oluşturulduğunda bu branch oluşturulur. Bu branch'te proje sorunsuz çalışır ve projenin stabil versiyonları burada oluşturulur.

## Soru 25: ".gitignore" dosyası nedir ve ne amaçla kullanılır?

Git alanı içerisinde takip edilmemesi gereken dosyaları içeren bir dosyadır. Bu uzantıdaki dosya içerisindeki dosya yollarını git otomatik olarak takip etmez fazladan bir işlem yapmamıza gerek yoktur.

## Soru 26: "git push origin --delete branch_name” nedir ve ne için kullanılır?

Buradaki komutu parça parça ele alabiliriz. 
"git push" yerel repo'daki değişiklikleri remote repo'ya göndermemiz için kullanılır.
"origin" ifadesi remote repository'nin ismidir.
"--delete [branch_name]" ise bir branch'in silinme isteğidir.
Yani verilen komut remote repository'deki bir branch'in silinmesi komutudur.
