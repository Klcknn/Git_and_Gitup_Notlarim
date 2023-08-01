# Git and Githup Notlarım: 
## İçindekiler

- [Git and Githup Notlarım:](#git-and-githup-notlarım)
  - [İçindekiler](#i̇çindekiler)
  - [1. Git and Githup](#1-git-and-githup)
    - [Git Nedir ?](#git-nedir-)
    - [Git Version Kontrolü](#git-version-kontrolü)
    - [Git Ayarları](#git-ayarları)
    - [Proje Oluşturulduktan sonra Sık Kullanılan Git Komutları](#proje-oluşturulduktan-sonra-sık-kullanılan-git-komutları)
  - [2. Git and Githup](#2-git-and-githup)
    - [Githup Watch || Star || Fork](#githup-watch--star--fork)
    - [Githup Issues](#githup-issues)
    - [Github Push](#github-push)
    - [Github Proje Oluşturma](#github-proje-oluşturma)
    - [Github Pull](#github-pull)
    - [Github Clone](#github-clone)
    - [.gitignore](#gitignore)

## 1. Git and Githup

### Git Nedir ? 
* Git değişiklikleri kaydeden bir version kontrol sistemidir.
* Git dağıtık bir yapıya sahiptir ve bu yapı her kullanıcının kendi yerel kopyasınn olduğu anlamına gelir.Bu şekilde çevrimdışı çalışılıp değişiklikler yerel olarak kaydedebiliriz.
* Git komut satırı üzerinde çalışılır.
* Git yapıısı ile projelerimizin farklı sürüm ve değişiklerini dallar(branch) ile yönetebiliriz.   
* 
### Git Version Kontrolü
* Git version kontrolunün yapılması
```bash

    # Git version kontrolunün yapılması
    git --version  # 1. Yöntem
    git -v         # 2. Yöntem 

```

### Git Ayarları
* Git ayarları `git config` komutu ile yapılır.
```bash
  
  # Kullanıcı adı ve E-Posta adresinin yapılandırılması için aşağıdaki komut kullanılır.
  git config --global user.name "Kenan KILIC"
  git config --global user.email "knnklc@gmail.com"

  # Renkli Çıktıları Etkinleştirmek için aşağıdaki komut kullanılır.
  git config --global color.ui true

  # Gerekli kurulumlar yapıldıktan sonra projemizin durumunu kontrol etmek için aşağıdaki  komut kullanılır. 
  git status

```
### Proje Oluşturulduktan sonra Sık Kullanılan Git Komutları

```bash
  # Git projesi oluşturmak için `git init` komutu kullanılır (git initialize).
  git init

  # Proje oluşturduktan sonra proje içindeki tüm dosyaları git deposuna eklemek için `.` işareti kullanılırız. 
  git add . 

  # Proje klasörünün içine README.md dosyası eklemek istersek aşağıdaki komutu kullanırız. 
  git add README.md

  # Proje klasörünün içine file_1.txt dosyası eklemek istersek aşağıdaki komutu kullanırız.
  git add file_1.txt

  # Proje klasörünün içine birden fazla dosya eklemek istersek aşağıdaki komutu kullanırız.
  git add file_2.txt file_3.txt 

  # Git deposuna proje dosyalarımızı ekledikten commit işlemini aşağıdaki gibi yapıyoruz. 
  git commit -m "proje dosyaları eklendi"

  # Commit geçmişini görmemizi sağlar. Son committen önceki commitlere doğru sıralı şekilde çıktı verecektir.Kısacası depoya eklenen sürümleri görmek için git log komutu kullanılır.
  git log

  # Tek satırlık bir commit geçmişini bize gösterir.
  git log --oneline

  # Projede yapılan değişiklikler sonrası yapılan tüm değişiklikleri görmek için diff komutu kullanılır.
  git diff

  # Belirli bir commit(commitID_1) ile çalışma alanındaki değişiklikleri karşılaştırma işlemi yapalım.
  git diff commitID_1 

  # İki farklı commiti karşılaştırma işlemi yapalım.
  git diff commitID_1 commitID_2 

  # Versiyonlar arası geçiş işlemi için git checkout komutu kulanılır.
  git checkout commitID_2

  # Brancler arası geçiş işlemi içinde git checkout komutu kulanılır.
  git checkout branch_name_1

  # Mevcutta bulunan tüm branch'lerimiz bir listeyelim.
  git branch

  # Yeni bir branch oluşturma işlemi
  git branch new_branch_name

  # Mevcut branch den yeni oluşturmuş olduğumuz branche geçiş yapma işlemi
  git checkout new_branch_name

  # Yeni oluşturmuş olduğumuz branch'imizi silelim.
  git branch -d new_branch_name

  # Eğer uzak sunucunuza bağlı branch’ lerimizi görmek istiyorsak aşağıdaki gibi işlem yapmamız gerekiyor.
  git branch -r

  # Yeni Branch ile Ana Branch’ imize(main) birleştirme işlei yapalım
  git checkout main
  git merge <yeni-branch-adı>

```

## 2. Git and Githup

### Githup Watch || Star || Fork 
* **Watch:** Kullanıcıların belirli bir repo veya organizasyonu takip etmek için kullandıkları bir özelliktir.
* **Star:** Kullanıcıların beğendiği veya ilgi duyduğu bir proyeji yada repoyu işaretlemek veya favlamak için kullandıkları bir özelliktir.Kısacası yakın takibe almak anlamına geliyor.
* **Fork:** Başka bir kullanıcının repo’ sunu kopyalayarak kendi GitHub hesabına taşımak ve bu kopya üzerinde bağımsız bir şekilde çalışmak için kullanılan bir işlemdir.

### Githup Issues
* Bir projede karşılaşılan sorunları, hataları veya önerileri takip etmek ve yönetmek için kullanılan bir özelliktir.
* Kullanıcılar, projenin GitHub sayfasında issues bölümünden yeni bir issue açabilir,
mevcut issue'ları takip edebilir, yorumlar ekleyebilir ve issue'ları kapatılana kadar
ilerleyişini izleyebilir.
* Bu yöntem proje ekibi ve katkıda bulunanlar arasında iletişimi kolaylaştırarak projenin
geliştirilmesine katkıda bulunur.

### Github Push
* Localdeki değişiklikleri GitHub veya başka bir uzak repo üzerine yüklemek için `git push` komutu kullanılır.Bu komut yerelde yaptığımız commit'leri uzak repo ile paylaşmamızı sağlar.

```bash 
    git push

```

### Github Proje Oluşturma
* Gitup web sitesi üzerinde oluşturmuş olduğumuz Repository'mizi local ile entegre edebiliriz.
* Aşağıdaki komutlar ile Local ile Githup Repo'muzu ilişkilendirebiliriz.

```bash 
   git init
   git add README.md
   git commit -m "first commit"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo_name>.git
   git push -u origin main

```

### Github Pull

* GitHub’ da `git pull` komutunu kullanarak, localde bulunan bir repomuz ile GitHub'da bulunan uzak repomuz arasındaki değişiklikleri senkronize etmiş oluruz.

* Bu işlem sayesinde GitHub'daki güncellemeleri lokaldeki çalışma alanımız içerisine rahatlıkla çekerek çalışmalarımıza devam ederiz.

* `Git pull` komut ile lokaldeki çalışma kopyamızı GitHub'daki uzak repo ile senkronize etmiş oluruz. Eğer uzak repomuz ile localdeki repomuz arasında farklılıklar varsa, `git pull` komutu yardımıyla bu farklılıklar birleştirilir.

```bash 
   git push

```

### Github Clone
* Uzak repoda bulunan projeleri local çalışma alanına indirmek veya eklemek için kullanılır.

```bash 
   # Kullanımı
   git clone <git_url>

   git clone https://github.com/<username>/<repo_name>.git

```


### .gitignore
* .gitignore dosyası git sürüm kontrol sisteminde kullanılan özel bir dosyadır. Git deposunda kontrol-versiyon izlemesi yaparken göz ardı edilerek dikkate alınmayacak veya git deposuna eklenmeyecek dosya, klasör ve alt klasörleri tanımlamak amaçlı kullanılır. 
* Göz ardı edeceğimiz dosyalarla ilgili olarak;
  * Belirli bir dosyayı isim olarak belirleyebiliriz.
    new.txt
  * Belirli bir dosya yolunu belirleyebiliriz.
    doc/*
  * Belirli bir dosya formatını (bulunduğu dizinde) belirleyebiliriz.
    *.txt
  * Belirli bir dosya formatını (tüm dizinde) belirleyebiliriz.
    **.txt
git.txt
git.txt görüntüleniyor.