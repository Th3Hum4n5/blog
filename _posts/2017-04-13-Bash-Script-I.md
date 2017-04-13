---
layout: post
title: "Bash Script"
date: 2017-04-13 03:32:44
image: '/assets/img/'
description: 'Bash Script-I'
tags:
- Bash
- Script
categories:
- Bash Script
twitter_text: 'I am learning Bash Script Language'
---
Bash Script Nedir?
------------------

Bash programlama, terminal üzerinde yazdığımız komutların, bir dosya içerisine kaydedip toplu bir şekilde çalıştırılmasını sağlar.Yazdığımız bu scriptler derlenerek çalıştırılmaz yani yazdığımız komutlar yorumlanarak çalıştırılır.Yazdığımız komutları .sh olarak kaydediyoruz.

Bash Script Nasıl Çalıştırılır?
-------------------------------


Bash dosyasını çalıştırmak oldukça basittir.Ancak dosyayı çalıştırmadan önce izin verilmesi gerekir.Eğer izin vermeden çalıştırmaya çalışırsak hata verecektir.

> 755 komutu scriptler için sıklıkla kullanılan,scriptlere yazma ve
> değiştirme izni veren bir komuttur.

{% highlight bash %}
./script.sh
{% endhighlight %}

İlk Uygulama
------------
**Script.sh**

{% highlight bash %}
#!/bin/bash
#Ekrana hello world yazdıran script

echo "Hello World!"
{% endhighlight %}


**Satır 1:** Bu komutta linux da bulunan bash’in yolunu gösterir.
**Satır 2:** ‘#’ işareti yorum satırı oluşturur.Bundan sonra yazdığımız komutlar çıktı olarak gözükmez.
**Satır 3:** Echo komutu ekrana yazı yazdırmamızı sağlar.Terminal de denediğimiz zaman yine aynı çıktıyı alırız.

**Neden ./ **

Terminal de ls veya echo gibi komutları çalıştırırken adını yazdığımızda direk olarak çalışır.Ama biz scriptleri çalıştıracağımız zaman başına ./ ekleriz.Bunun nedeni bash bir komutu çalıştıracağı zaman $PATH yolunda arar.Eğer orada yoksa çalıştırmaz.Biz bu yolları terminal echo yazarak görebiliriz.

<p><img src="{{ site.url }}/assets/img/path.png" alt="{{ page.title }}"></p>

Gördüğünüz gibi echo komutuyla yollarımızı görmüş olduk.Bu yollar birbirinden “:” ile ayrılır.Peki biz scriptimizi ./ kullanmadan nasıl çalıştırabiliriz.

<p><img src="{{ site.url }}/assets/img/usr.png" alt="{{ page.title }}"></p>

Scriptimizi $PATH içinde bulunan klasörlerden birine attığımız zaman ./ kullanmadan scriptimizi çalıştırmış olduk.

Okuduğunuz için teşekkürler.
