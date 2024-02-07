1. Git nedir?
  
  Git, yazılım geliştirme süreçlerinde kullanılan, hız odaklı, dağıtık çalışan bir sürüm kontrol ve kaynak kod yönetim sistemidir.
==========================

2. "Git pull" ile "Git fetch" komutlarının farkı nedir?

  Git Fetch ve Git Pull arasındaki temel fark, git fetch’in kaynaktan en yeni meta veri bilgilerini geri yüklemek için yerel git’inizi gösteren komut olmasıdır. Herhangi bir dosya aktarmaz. Daha çok değişikliklerin mevcut olup olmadığını bulmak için verileri incelemek gibidir, oysa git pull tüm değişiklikleri deponuza çekmekle birlikte aynı şeyi yapar
==========================

3. Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse ve gönderdiği kodları "git pull" ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?

  Commitlediği dosyaları pushlamayı unutmuş olabilir. Yanlış branche göndermiş olabilir.
==========================

4."Git fetch origin" komutundaki "origin" neye karşılık gelmektedir?

  "Git fetch origin" komutundaki "origin", genellikle yerel depoya bağlı olan bir uzak depoyu ifade eder.
==========================

5. "HEAD" kelimesi neyi temsil etmektedir?
 
  "HEAD", Git deposunda şu anki çalışma konumunu (pozisyonunu) ifade eden bir gösterge veya referanstır. Git'in içerisinde bulunduğunuz branch veya commit'in adını veya kimliğini temsil eder. HEAD göstergesi, Git deposundaki anlık konumunuzu belirtir ve hangi commit'in veya branch'in üzerinde çalıştığınızı belirlemenize yardımcı olur. Bu, Git'in iş akışı ve durumu hakkında önemli bilgiler sağlar.
==========================

6. "Staging Area" ya da "Index" diye isimlendirilen bölge tam olarak ne demektir?

  "Staging Area" veya "Index", Git'in çalışma prensibinde önemli bir konsepttir. Bu bölge, değişikliklerinizi geçici olarak sakladığınız ve bir sonraki commit'e dahil etmek istediğiniz dosyaları belirttiğiniz yerdir.
==========================

7. "Untracked file" ne demektir?

  "Untracked file" (İzlenmeyen dosya), Git'in çalışma dizininde bulunan ve Git tarafından takip edilmeyen bir dosyayı ifade eder. Yani, bu dosya Git'in sürüm kontrolü altında değildir ve Git tarafından izlenmez veya yönetilmez.
==========================

8. ".git" klasörünü silersek ne olur?

  .git klasörü, bir Git deposunun kalbidir ve sürüm kontrolü ile ilgili tüm bilgileri içerir. Bu klasörü silerseniz, Git deposunun tüm geçmişi, commit'leri, branch'leri ve diğer tüm bilgileri kaybolur. Bu durumda, Git deposu kullanılamaz hale gelir ve o projenin Git tarihçesi tamamen kaybolur.
==========================

9. - Kendi lokalimizde her "git init" komutunu kullanıdığımızda otomatik olarak "ReadMe.md" dosyası oluşturulmasını istiyorsak ne yapmalıyız?
  
  Her git init komutu kullanıldığında otomatik olarak bir ReadMe.md dosyası oluşturulmasını istiyorsanız, bir çözüm olarak aşağıdaki adımları izleyebilirsiniz:

Yeni bir ReadMe.md dosyası oluşturun ve içeriğini istediğiniz şekilde düzenleyin. Örneğin, # My Project gibi bir başlık ekleyebilir veya proje hakkında kısa bir açıklama yazabilirsiniz.

Bu ReadMe.md dosyasını herhangi bir yeni Git deposunun kök dizinine (yani .git klasörünün olduğu yer) kopyalayın.

Ardından, herhangi bir dizinde git init komutunu kullanarak yeni bir Git deposu oluşturduğunuzda, ReadMe.md dosyası otomatik olarak bu depoya dahil olacaktır.

Bu yöntemle, her yeni Git deposu oluşturulduğunda otomatik olarak bir ReadMe.md dosyası ekleyebilirsiniz. Ancak, bu dosyanın içeriği her projeye göre değişebilir, bu nedenle içeriği her defasında düzenlemek isteyebilirsiniz.
==========================

10. Git konusunda bahsi geçen "branch" yapısı nedir? Bize ne sağlar?

  Git'te "branch" (dal), projenin farklı çalışma alanlarını temsil eden bir yapıdır. Her branch, projenin farklı bir versiyonunu veya farklı bir iş özelliğini temsil eder. Branch'ler, projenin geliştirilmesi sırasında paralel çalışma yapmayı sağlar ve birçok avantaj sunar. Bu avantajları şu şekilde sıralayabiliriz; paralel geliştirme, risk izolasyonu, geneme ve inceleme, geri dönüşüm ve paralel yayınlama gibi avantajlar sağlar.
==========================
