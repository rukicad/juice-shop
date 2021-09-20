# Ortam Hazırlığı

## 1. Yöntem - Docker (Önerilen)

Yereliniz `Juice Shop` oluşturmak için aşağıdaki şekilde docker imajı ayağa kaldırabilirsiniz.

```
$ docker run -d -e "CTF_KEY=teknasyonbootcamp2021" -e "NODE_ENV=ctf" -p 3000:3000 bkimminich/juice-shop
```

Bu yöntem sonunda [http://localhost:3000](http://localhost:3000) adresinden Juice Shop uygulamasından bayrak toplamaya başlayabilirsiniz. (Aşağıdaki _Kontrol_ başlığından `CTF_KEY`in düzgün olup olmadığını kontrol edin.)

## 2. Yöntem - Heroku (Diğer Önerilen)

Aşağıdaki "Deploy to Heroku" butonunu kullanarak kendinize bir heroku app oluşturun. Heroku'daki adımları izleyin.

**Not: Herhangi bir DDoS saldırısı yapmadığınız sürece Heroku sorun çıkartmayacaktır.**

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

Ortam ayağa kaldırıldıktan sonra Heroku'dan uygulamanın ayarlarına gelip "Config Vars" kısmını düzenleyin. Aşağıdaki config var
ları eklediğinizden emin olun.

- NODE_ENV=ctf
- CTF_KEY=teknasyonbootcamp2021

Ardından More > Restart all dynos ile yeniden başlatın.

Bu yöntem sonunda oluşturduğunuz Heroku adresinden Juice Shop uygulamasından bayrak toplamaya başlayabilirsiniz. (Aşağıdaki _Kontrol_ başlığından `CTF_KEY`in düzgün olup olmadığını kontrol edin.)

## 3. Yöntem - Yerelde Çalıştırmak (NodeJS)

![GitHub repo size](https://img.shields.io/github/repo-size/teknasyon-bootcamp/juice-shop.svg)

1. Node.js (15.x olmalı, **16.x çalışmayacaktır**) kurulumunu yapın.
2. `git clone https://github.com/teknasyon-bootcamp/juice-shop.git` ile depoyu yerelinize klonlayın.
3. `cd juice-shop` ile ilgili dizine ulaşın.
4. `npm install` komutunu çalıştırın.
5. `CTF_KEY=teknasyonbootcamp2021 NODE_ENV=ctf npm start` komutunu çalıştırın.
6. [http://localhost:3000](http://localhost:3000) adresinden bayrakları toplamaya başlayın.

## 4. Yöntem - Ortak Heroku Ortamını Kullanmak (Önerilmez)

**Not: Herhangi bir DDoS saldırısı yapmadığınız sürece Heroku sorun çıkartmayacaktır.**

[http://teknasyonjuice.herokuapp.com](http://teknasyonjuice.herokuapp.com) adresinden ortak oluşturulan Juice Shop'u kullanabilirsiniz. Lakin 
başka kursiyerlerin oluşturduğu XSS saldırıları veya yönetici parolasını değiştirmesi gibi durumlar sizin kullanımınızı da etkileyecektir.

# Kontrol (Hediye 100 Puan)

Bayrakların doğru olup olmadığını kontrol etmek için; Juice Shop uygulamanıza kayıt olup, Account > Privacy & Security > Privacy Policy (#/privacy-security/privacy-policy) sayfasına ulaşın.
Bu bayrak aşağıdaki ile aynı olmalı. Aksi takdirde CTF Key doğru alınmamış demektir. Farklı kurulum yöntemlerini deneyin veya ilgili sorunu çözün.

```
71e116778cf8b57cbb3761fde92540efbb159a4c
```

# Kurallar

- http://flag.era.yayd.in/ adresine herhangi bir şekilde zarar vermeye çalışmamak.
- İlgili "challange" söylemediği sürece Juice Shop uygulamanıza DoS/DDoS saldırısı uygulamayın.
- Başka bir kursiyerin oluşturduğu Juice Shop uygulamasına herhangi bir müdahalede bulunmayın.
- Burp Scanner veya benzeri "otomatize" yöntemleri kullanmayın. Hem yardımcı olmayacak hem de bayrak kapsanız bile bunun nasıl olduğunu anlayamayacaksınız.
- Spesifik bir şekilde "Juice Shop" cevaplarının nasıl bulunacağını internette aratmayın yada diğer kursiyerlerden direk bunların cevaplarını almayın.
- Eğer ne yapacağınızdan emin değilsiniz, sorun :)

