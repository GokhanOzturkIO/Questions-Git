## 1) Git Nedir?

Git dünyada en yaygın kullanılan sürüm kontrol sistemidir. Zaman içinde kodda yapılan değişiklikleri depo adı verilen özel bir veritabanına kaydeden, ücretsiz ve açık kaynaklı, dağıtılmış bir sürüm kontrol sistemidir. Git, kullanıcıların proje geçmişini takip etmesine, kimin ne zaman değişiklik yaptığını görmesine ve gerekirse projeyi daha önceki bir duruma döndürmesine olanak tanır. Hızı, ölçeklenebilirliği ve dallanma ve birleştirme işlemlerinin verimli bir şekilde gerçekleştirilmesi nedeniyle popülerdir. Git, geliştiricilerin projeler üzerinde işbirliği yapmasına olanak tanır; her ekip üyesinin, projenin geçmişiyle birlikte bir kopyası kendi makinelerinde bulunur ve merkezi sunucu çevrimdışı olsa bile proje anlık görüntülerinin yerel olarak kaydedilmesine ve diğerleriyle senkronizasyona olanak tanır.

---

## 2) "git pull" ile "git fetch" komutlarının farkı nedir?

`git fetch`, yeni verileri çalışma dosyalarınıza entegre etmeden uzak bir depodan indirir, böylece değişiklikleri yerel deponuza entegre etmeden önce gözden geçirmenize olanak tanır.

`git pull` ise yeni verileri indirir ve bunları doğrudan mevcut çalışan kopya dosyalarınıza entegre eder; bu daha hızlı olabilir ancak aynı zamanda yerel deponuzda değişikliklere ve çakışmalara neden olur.

`git fetch` yalnızca yeni verileri indirdiği için daha güvenlidir; `git pull` ise onu geçerli çalışan kopya dosyalarınıza entegre eder; bu da çakışmalara ve manuel çözümleme gerektiren değişikliklere neden olabilir.

---

## 3) Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse ve gönderdiği kodları "git pull" ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?

Takım arkadaşımız bize kodlarını gönderdiğini söylüyor ancak biz bu kodları git pull ile local olarak alamıyorsanız bunun birkaç nedeni olabilir. Kontrol edilmesi gereken bazı yaygın hatalar şunlardır:

- **Depo uzak sunucuya aktarılamama sorunu:**
Takım arkadaşımızın değişikliklerini uzak sunucuya aktardığından emin olun. Aksi takdirde bu değişiklikleri git pull ile alamayız.

- **Yanlış dal adı:**
Takım arkadaşımızın kodu için doğru dal adını kullanıldığından emin olunmalı.

- **İzin sorunu:**
Uzak sunucuda herhangi bir izin sorunu olup olmadığını kontrol etmeliyiz. Değişiklikleri almak için gerekli izinlere sahip değilsek en son değişiklikleri alamayız.

Bu yaygın hataları kontrol ederek, takım arkadaşımızın git pull ile yaptığı en son değişiklikleri almayla ilgili sorunları tanımlayabilir ve bu sorunları çözebiliriz.

---

## 4) "git fetch origin" komutundaki "origin" neye karşılık gelmektedir?

`git fetch origin` komutundaki `origin`, değişiklikleri almak istediğiniz uzak depoya atanan varsayılan adı temsil eder. Genellikle bir Git deposunu klonladığınızda orijinal depo URL'sine verilen takma addır. Bu, kısa ve akılda kalıcı bir ad kullanarak uzak depoya başvurmanıza olanak tanır.

---

## 5) "HEAD" kelimesi neyi temsil etmektedir?

"HEAD", Git deposundaki mevcut konumu işaret eden özel bir işaretçidir. Genellikle mevcut çalışma kopyasının veya dalın en son commit'ini gösterir, ancak geçici olarak farklı bir konuma da yönlendirilebilir. Bu, farklı commit'leri, etiketleri veya referansları işaretlemek için kullanılabilir.

---

## 6) "Staging Area" ya da "Index" diye isimlendirilen bölge tam olarak ne demektir?

"Staging Area" veya "Index", Git'in çalışma alanı ile depo arasında bir ara bölge olarak işlev görür. Bu bölge, değişiklikleri işlemek ve bir sonraki commit için hazırlamak için kullanılır. Değişiklikler öncelikle çalışma alanında yapılır ve daha sonra "Staging Area"e eklenir. Bu bölge, commit öncesi değişikliklerin kontrol edilmesini sağlar ve geliştiricilere değişiklikleri organize etme esnekliği sunar.

---

## 7) "Untracked file" ne demektir?

"Untracked file", Git'in izlemediği dosyaları ifade eder. Bu dosyalar, Git'in değişiklikleri izlemediği veya kaydetmediği dosyalardır. Yeni oluşturulan veya değiştirilen dosyalar, Git tarafından otomatik olarak izlenmez ve bu nedenle "Untracked" olarak adlandırılır. Bu dosyalar, bir sonraki commit işlemi sırasında Git tarafından görmezden gelinir. Bunları takip etmek veya değişikliklerini kaydetmek istiyorsanız, önce dosyaları "Staging Area"e eklemeniz gerekir. Bu, dosyaların Git tarafından izlenmeye başlanmasını ve sonraki commit işlemlerinde kaydedilmesini sağlar.

---

## 8) ".git" klasörünü silersek ne olur?

".git" klasörünü bir Git deposunda silmek, o depo ile ilişkilendirilmiş olan tüm sürüm kontrolü geçmişini ve ayarlarını kaldırır, yerel deposunu sürüm kontrolü geçmişi olmayan standart bir klasör haline getirir. Ancak, eğer depo bir uzak sunucuya yüklenmişse, yeniden klonlama veya indirme yoluyla tüm sürüm kontrolü geçmişi ve ayarları ile birlikte depoyu yeni bir kopyasını indirebiliriz.

---

## 9) Kendi lokalimizde her "git init" komutunu kullandığımızda otomatik olarak "ReadMe.md" dosyası oluşturulmasını istiyorsak ne yapmalıyız?

Bu tarz bir isteğin çözümü için 2 farklı yol kullanabiliriz:

- 1.1 Öncelikle herhangi bir yerde git şablonumuzu bulundurabilmek için bir klasör açıyoruz.
    ```bash
    mkdir ~/.git-templates
    ```
- 1.2 Daha sonrasında şablon içeriğimizi bir dosyaya yazdıktan sonra açtığımız git şablonları klasörüne ekliyoruz.
    ```bash
    echo "# My Project" > ~/.git-templates/ReadMe.md
    ```
- 1.3 Son olara git yapılandırmasını güncelleyerek init.templatedir özelliğini kendi özel şablon dizininize işaret edecek şekilde ayarlıyoruz.
    ```bash
    git config --global init.templatedir ~/.git-templates
    ```
--
- 2.1 Bir önceki çözüm yolunda olduğu gibi burada da bir şablonumuzun olması gerekiyor. Şablonumuzun olduğunu varsayarak diğer adıma geçiyorum.
- 2.2 Bu adımda ise şu şekilde bir şablonumuzun olduğunu git'i başlatacağımız sırada parametre olarak veriyoruz.
    ```bash
    git init --template=~/.git-template
    ```

---

## 10) Git konusunda bahsi geçen "branch" yapısı nedir? Bize ne sağlar?

Git'te "branch" (dal), projenin farklı versiyonlarını yönetmek için kullanılır. Her bir dal, farklı bir özelliğin veya değişikliğin geliştirilmesine olanak tanır. Bu, aynı anda birden fazla özellik üzerinde çalışmayı sağlar ve riskleri izole eder. Ayrıca, paralel geliştirme ve geçmişi koruma gibi faydalar sağlar.

---

## 11) Sıfırdan bir "branch" nasıl oluşturabiliriz?

Sıfırdan bir branch'i şu şekilde oluşturabiliriz:

```bash
git branch branch_name
```

ve mevcut branch'den yeni oluşturduğumuz branche geçmek için şu komutu yazarız:
```bash
git checkout branch_name
```

--

Veya kısaca yeni oluşturduğumuz branch'e şu şekilde geçiş yapabiliriz:
```bash
git checkout -b branch_name
```

---

## 12) Var olan bir "branch"e nasıl geçebiliriz?

Var olan bir branch'e şu şekilde geçiş yaparız:
```bash
git checkout branch_name
```

---

## 13) "git clone" komutunu kullanırken belirli bir spesifik branch'i sadece çekmek istiyorsak nasıl yapabiliriz?

git clone komutunu kullanırken, yalnızca belirli bir branc'i çekmek istiyorsak, klonlamak istediğimiz branch'i belirtmek için --branch veya -b seçeneği ile birlikte --single-branch seçeneğini kullanabiliriz. İşte nasıl yapılacağı:

```bash
git clone --single-branch --branch branch_name repository_url
```

---

## 14) "Merge conflict" ne demektir?

Merge Conflict, Git'in birleştirme işlemi sırasında değişiklik setlerini otomatik olarak birleştirememesi durumunda ortaya çıkar. Bu durum, genellikle farklı yazılımcıların aynı dosyalarda aynı satırları değiştirmesi veya farklı dallarda yapılan değişikliklerin çakışması sonucunda meydana gelir. Merge conflictler, yazılımcılara çakışmanın olduğu dosyalarda değişiklikleri inceleyip çözümlemeleri için fırsat sunar.

---

## 15) "git log" komutu ile hangi bilgileri görebiliriz?

Bu komut, en son işlemden başlayarak geçerli branchin commit geçmişini görüntüler. Çıktı, commit hash code'unu, yazarı, tarihi ve commit mesajını içerir.

Örneğin;
```
commit 24be20e2f27315d165ede25784f1d04bb4214553
Author: Enes CAN <enesscann98@gmail.com>
Date:   Tue Feb 6 21:13:34 2024 +0300

    ""Merge conflict" ne demektir?" sorusunun cevabı eklendi.
```

---

## 16) "git diff" ile kaç farklı iki durumun arasındaki değişiklikleri görebiliriz?

"git diff" komutu ile Git depomuzun iki farklı durumu arasındaki farkları görebiliriz. Bu komutu kullanmanın birkaç yolu var, ancak en yaygın kullanımı; çalışma dizinimizin mevcut durumunu en son commitle karşılaştırmaktır. Bu bize son committen bu yana yaptığımız değişiklikleri gösterecektir.

İşte "git diff" komutunu nasıl kullanabileceğimize dair bir örnek:
```
git diff HEAD
```
Bu komut bize en son commit ile çalışma dizinimizin mevcut durumu arasındaki farkları gösterecektir.
</br>
Eğer iki spesifik commit’i karşılaştırmak istiyorsak aşağıdaki komutu kullanabiliriz:
```
git diff commit1 commit2
```
Bu bize belirtilen iki commit arasındaki farkları gösterecektir.
</br>
Belirli bir işlemi çalışma dizinimizin mevcut durumuyla karşılaştırmak istiyorsak aşağıdaki komutu kullanabiliriz:
```
git diff commit
```
Bu bize belirtilen commit ile çalışma dizinimizin mevcut durumu arasındaki farkları gösterecektir.
</br>
Belirli iki branchi karşılaştırmak istiyorsak aşağıdaki komutu kullanabiliriz:
```
git diff branch1 branch2
```
Bu bize belirtilen iki branch arasındaki farkları gösterecektir.
</br>
Belirli bir branchi çalışma dizinimizin mevcut durumuyla karşılaştırmak istiyorsak aşağıdaki komutu kullanabiliriz:
```
git diff branch
```
Bu bize belirtilen dal ile çalışma dizinimizin mevcut durumu arasındaki farkları gösterecektir.
</br>
Tüm bu durumlarda, çıktı bize eklenen, değiştirilen veya silinen dosyalar da dahil olmak üzere iki durum arasındaki farkları gösterecektir.

---

## 17) Git reset ile neyi geri alıyoruz?

git reset komutu, Git deposundaki değişiklikleri geri almak için kullanılır. --soft, --mixed ve --hard gibi seçeneklerle kullanılarak değişikliklerin geri alınma şekli belirlenir.

`git reset --soft:` Bu seçenek, son commit'i geri alır, ancak değişiklikleri çalışma dizininde ve dizin endeksinde (staging area) bırakır.
```
git reset --soft HEAD
```

`git reset --mixed:` Bu seçenek, son commit'i geri alır ve değişiklikleri çalışma dizininde tutar, ancak dizin endeksini (staging area) geri alır.
```
git reset --mixed HEAD
```

`git reset --hard:` Bu seçenek, son commit'i ve yapılan değişiklikleri tamamen geri alır.
```
git reset --hard HEAD
```

---

## 18) "git commit" ile "git push" arasındaki fark nedir?

"git commit" komutu, yerel Git deposunda yapılan değişiklikleri bir commit olarak kaydeder ve bu değişiklikler sadece yerelde saklanır. "git push" komutu ise yerelde yapılan commit'leri uzak bir depoya gönderir ve diğer kullanıcılarla paylaşılmasını sağlar. Bu komutlar birlikte kullanılarak, yerelde yapılan değişikliklerin paylaşılması ve işbirliği yapılması sağlanır.

--