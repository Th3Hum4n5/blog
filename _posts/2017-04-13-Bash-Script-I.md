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

Bash programlama, terminal üzerinde yazdıgımız komutların, bir dosya içerisine kaydedip toplu bir sekilde çalıstırılmasını saglar.Yazdıgımız bu scriptler derlenerek çalıstırılmaz yani yazdıgımız komutlar yorumlanarak çalıstırılır.Yazdıgımız komutları .sh olarak kaydediyoruz.

Bash Script Nasıl Çalıstırılır?
-------------------------------


Bash dosyasını çalıstırmak oldukça basittir.Ancak dosyayı çalıstırmadan önce izin verilmesi gerekir.Eger izin vermeden çalıstırmaya çalısırsak hata verecektir.

> 755 komutu scriptler için sıklıkla kullanılan,scriptlere yazma ve
> degistirme izni veren bir komuttur.

{% highlight bash %}
./script.sh
{% endhighlight %}

Ilk Uygulama
------------
**Script.sh**

{% highlight bash %}
#!/bin/bash
#Ekrana hello world yazdıran script

echo "Hello World!"
{% endhighlight %}


**Satır 1:** Bu komutta linux da bulunan bash’in yolunu gösterir.
**Satır 2:** ‘#’ isareti yorum satırı olusturur.Bundan sonra yazdıgımız komutlar çıktı olarak gözükmez.
**Satır 3:** Echo komutu ekrana yazı yazdırmamızı saglar.Terminal de denedigimiz zaman yine aynı çıktıyı alırız.

**Neden ./ **

Terminal de ls veya echo gibi komutları çalıstırırken adını yazdıgımızda direk olarak çalısır.Ama biz scriptleri çalıstıracagımız zaman basına ./ ekleriz.Bunun nedeni bash bir komutu çalıstıracagı zaman $PATH yolunda arar.Eger orada yoksa çalıstırmaz.Biz bu yolları terminal echo yazarak görebiliriz.

<p><img src="{{ site.url }}/assets/img/path.png" alt="{{ page.title }}"></p>

Gördügünüz gibi echo komutuyla yollarımızı görmüs olduk.Bu yollar birbirinden “:” ile ayrılır.Peki biz scriptimizi ./ kullanmadan nasıl çalıstırabiliriz.

<p><img src="{{ site.url }}/assets/img/usr.png" alt="{{ page.title }}"></p>

Scriptimizi $PATH içinde bulunan klasörlerden birine attıgımız zaman ./ kullanmadan scriptimizi çalıstırmıs olduk.

Okudugunuz için tesekkürler.
