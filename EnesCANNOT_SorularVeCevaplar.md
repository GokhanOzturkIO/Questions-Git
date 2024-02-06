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

