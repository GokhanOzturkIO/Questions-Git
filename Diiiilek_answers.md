# 1- Git nedir?

Git, dağıtık bir versiyon kontrol sistemi olarak kullanılan,
açık kaynaklı yazılım  aracıdır. Geliştiricelere bir projenin kod tabanının
sürümlerini takip etmelerine, aynı kod tabanı üzerinde iş birliği yapmalarına ve 
değişikleri yönetmelerine yardımcı olur.


# 2- "git pull" ile "git fetch" komutlarının farkı nedir?

"git fetch" komutu uzak sunucudaki gönderilen değişikliklerden lokaldeki bilgisayarımızın 
değişiklikleri almadan, o değişikliklerden haberdar olmamızı sağlar, hangi değişiklikleri 
kabul edeceğimize karar verebiliriz.
"git pull" komutu ise uzak sunucudaki gönderilen değişikleri biz hangisini alıp hangisini 
almayacağımıza karar vermeksizin, lokaldeki bilgisayarımıza tüm değişiklikleri indirir ve 
uygular. Bu da merge işlemi sırasında istenmeyen kod çatışmalarına sebep olabilir.


# 3- Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse 
ve gönderdiği kodları "git pull" ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?

"git fetch" komutunu çalıştırmamış olabiliriz,
takım arkadaşımızın branchini takip etmiyor olabiliz,
takım arkadaşımızın çalıştığı branch main branche bağlı olmayabilir.


# 4- "git fetch origin" komutundaki "origin" neye karşılık gelmektedir?

Çalıştığımız projenin Uzak depodaki halini "origin" şeklinde adlandırırız.
Buna örnek olarak çalıştığımız projenin güncel bir içeriğini githubdan almayı örnek verebiliriz.


# 5- "HEAD" kelimesi neyi temsil etmektedir?

Aktif olan branch'de ki en son commit'i işaret etmektedir.


# 6- "Staging Area" ya da "Index" diye isimlendirilen bölge tam olarak ne demektir?

Git dosyamızda yaptığımız değişiklikleri commit'lemeden ya da push'lamadan önce 
değiştirebileceğimiz, yaptığımız değişiklikleri geçici olarak depoladığımız alandır.
Buna günlük hayattan örnek verecek olursak sanatçıların, oyuncuların sahneye çıkmadan
önce tüm hazırlıklarını gerçekleştirdiği kulis'i örnek verebiliriz.


# 7- "Untracked file" ne demektir?

Durumunu öğrenmek istediğimiz dosya'nın henüz Git tarafından haberdar olunmadığını, 
Git'in bu dosyayı takip etmediği anlamına gelmektedir.


# 8- ".git" klasörünü silersek ne olur?

Git depomuzdaki yapılan tüm değişiklikleri silmiş oluruz,
Git depomuz artık git yönetiminden çıkar.


# 9- Kendi lokalimizde her "git init" komutunu kullanıdığımızda 
otomatik olarak "ReadMe.md" dosyası oluşturulmasını istiyorsak ne yapmalıyız?

.git-templates klasörü oluşturup oluşturduğumuz bu klasöre README.md 
dosyasını kopyalamalıyız.


# 10- Git konusunda bahsi geçen "branch" yapısı nedir? Bize ne sağlar?

Branch'in Türkçe karşılığı "dal" anlamına gelmektedir. Projemizi bir ağaca benzetecek olursak
ağacın kökleri bizim projemizin değişikliğe uğramamış halidir buna main ya da master branch adını 
veririz. Ağacın dallarıda, kök proje üzerinde bir değişiklik yapmaksızın projenin klon versiyonun da 
çalışmayı, aynı anda farklı sürümleri paralel olarak geliştirmemizi,aynı proje üzerindeki farklı 
kod satırlarında aynı anda çalışmayı sağlayan yan branchleri oluşturur. Bu yan branchlere de
"git checkout <yeni_branch_ismi>" komutuyla isim verebiliriz.


# 11- Sıfırdan bir "branch" nasıl oluşturabiliriz?
"git chekout -b <branch_ismi>" komutuyla ya da "git branch <branch_ismi>" komutuyla
yeni branch oluşturabiliriz.


# 12- Var olan bir "branch"e nasıl geçebiliriz?

Var olan branch e geçmek için "git checkout <var_olan_branch_ismi>" komutuyla geçebiliriz.


# 13- "git clone" komutunu kullanırken belirli bir spesifik branch'i sadece çekmek istiyorsak nasıl yapabiliriz?

"git clone --single-branch" <spesifik_branch_url> <branch_adı> komutunu konsola girerek 
istediğimiz branch'i çekebilriz.


# 14- "Merge conflict" ne demektir?

birden fazla branch'i birleştirirken, Git'in aynı dosya üzerindeki aynı satırdaki kodların farklılığından,
kod satırının silinmiş olmasından ya da yeni bir kod satırı eklenmesinden kaynaklı ortaya çıkan bir durumdur.


# 15- "git log" komutu ile hangi bilgileri görebiliriz?

repository'e atılan geçmiş commit'leri, bu commit'leri atan kişinin ismini, e-mail'ini,
commit'in atıldığı tarihi ve saati ve yapılan değişikliklerin kısa bir özetini görebiliriz.


# 16- "git diff" ile kaç farklı iki durumun arasındaki değişiklikleri görebiliriz?

Dört farklı iki durumun arasındaki değişiklikleri gösterir. Bunlar:
İki commit arasındaki değişiklikler,
Mevcut durum ile son commit arasındaki değişiklikler,
Staging area ile son atılan commit arasındaki değişiklikler,
İki farklı branch arasındaki değişiklikler.


# 17- Git reset ile neyi geri alıyoruz?

Staging area'ya gönderdiğimiz değişiklikleri geri alırız.


# 18- "git commit" ile "git push" arasındaki fark nedir?

"git commit" komutu ile lokal projemiz de yaptığımız değişiklikleri kayıt eder 
ve takip ederiz.
"git push" komutuyla ise lokal bilgisayarımızdaki projede yaptığımız değişiklikleri 
uzak sunucudaki depoya (repository) göndeririz.


# 19- Atomic commit ne demektir?

Benzer kategorideki birden fazla değişikliğe ayrı ayrı commit uygulamak yerine 
tek bir commit uyguladığımız mantıksal bir yaklaşımdır.


# 20- Repository ne demektir?

Repository, versiyon kontrol sistemi tarafından yönetilen bir projenin kaynak 
kodlarını ve diğer ilgili dosyaları depolayan ve projenin geçmişteki tüm sürümlerini 
takip etmeyi sağlayan bir alandır.


# 21- "git tag" nedir? "git branch"’ten farkı nedir?

"git tag" komutu önemli commit'leri işaretlemek veya sürümleri numaralandırmak 
için kullanılır ve yalnızca commit geçmişini etkiler.
"git branch" 'ten farkı ise "git branch" komutu, farklı geliştirme yollarını ve projenin 
farklı paralel geliştirme süreçlerini yönetmek için kullanılır.


# 22- Git'i görsel olarak kullanabilmek için hangi üçüncü taraf araçları ve uygulamaları kullanabiliriz?

SourceTree, Gitkraken, Githistory, Gource, Learning Git Branching, Git-School, Onlywei


# 23- "GitHub" ile "git" arasındaki fark nedir? GitHub benzeri diğer siteler nelerdir? 
GitHub veya diğer sitelerdeki kullanıcı adlarını yazar mısınız?

"Git" dosyalardaki değişiklikleri takip etmeyi sağlayan bir versiyon kontrol sistemir.
Komut satırı aracılığıyla kullanılır, ücretsiz ve açık kaynak kodludur.
"Github" ise Git'i web tabanlı bir arayüzle kullanan bir hosting hizmetidir.
Depolama, iş birliği ve kod incelemesi gibi ek özellikler sunar, ücretsiz ve ücretli planları
mevcuttur.
GitHub benzeri diğer sitelere örnek olarak, GitLab, Bitbucket, Gitea, SourceForge gibi siteleri 
verebiliriz.









