## 1) Git Nedir?

Git dünyada en yaygın kullanılan sürüm kontrol sistemidir. Zaman içinde kodda yapılan değişiklikleri depo adı verilen özel bir veritabanına kaydeden, ücretsiz ve açık kaynaklı, dağıtılmış bir sürüm kontrol sistemidir. Git, kullanıcıların proje geçmişini takip etmesine, kimin ne zaman değişiklik yaptığını görmesine ve gerekirse projeyi daha önceki bir duruma döndürmesine olanak tanır. Hızı, ölçeklenebilirliği ve dallanma ve birleştirme işlemlerinin verimli bir şekilde gerçekleştirilmesi nedeniyle popülerdir. Git, geliştiricilerin projeler üzerinde işbirliği yapmasına olanak tanır; her ekip üyesinin, projenin geçmişiyle birlikte bir kopyası kendi makinelerinde bulunur ve merkezi sunucu çevrimdışı olsa bile proje anlık görüntülerinin yerel olarak kaydedilmesine ve diğerleriyle senkronizasyona olanak tanır.

---

## 2) "git pull" ile "git fetch" komutlarının farkı nedir?

`git fetch`, yeni verileri çalışma dosyalarınıza entegre etmeden uzak bir depodan indirir, böylece değişiklikleri yerel deponuza entegre etmeden önce gözden geçirmenize olanak tanır.

`git pull` ise yeni verileri indirir ve bunları doğrudan mevcut çalışan kopya dosyalarınıza entegre eder; bu daha hızlı olabilir ancak aynı zamanda yerel deponuzda değişikliklere ve çakışmalara neden olur.

`git fetch` yalnızca yeni verileri indirdiği için daha güvenlidir; `git pull` ise onu geçerli çalışan kopya dosyalarınıza entegre eder; bu da çakışmalara ve manuel çözümleme gerektiren değişikliklere neden olabilir.

---

