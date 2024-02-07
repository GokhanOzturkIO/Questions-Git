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
