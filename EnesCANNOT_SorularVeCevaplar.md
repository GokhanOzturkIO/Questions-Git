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

