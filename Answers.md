## Soru 1: Git Nedir?

Git bir versiyon kontrol sistemidir. Yaptığımız çalışmalara kontrol noktaları koyabildiğimiz daha sonrasında bu kontrol noktalarını inceleyip ihtiyaç halinde geri dönebildiğimiz bir sistemdir. Her bir kontrol noktasında (commit) dosyalarımızdaki değişiklikleri gözlemlememize olanak sağlar.

## Soru 2: "git pull" ile "git fetch" komutlarının farkı nedir?

"git fetch" yaptıktan sonra local branc'lerimiz güncellemelerini alır fakat "git merge" yapmadan bu değişiklikler working directory'e işlenmez. "git pull" ise hem "git fetch" yapar hem de "git merge" yapar. Yani remote repository'den güncellemeleri local repository'e alıp bunları working directory'e işler 
