---
layout: post
title: "PIC Programlama"
date: 2017-04-11 03:32:44
image: '/assets/img/'
description: 'PIC Programlamaya Giris-I'
tags:
- PIC
- microc
categories:
- PIC Programlama
twitter_text: 'I am learning PIC Programming'
---

Merhaba arkadaslar,
-------------------

PIC programlama ve uygulama örnekleri ile bir baslangıç yapmak istedim.
<!--more-->
Çalısmalarımızı 16F877A ve 18F4550 PIC’lerini kullanmayı amaçlıyorum.
Ilk olarak yol “https://www.mikroe.com/mikroc/” MikroC’nin kendi sitesinden demo versiyonunu indirerek baslayacagız. Sıfırdan baslamak isteyen arkadaslar için olabildigince ayrıntıya inecegim bu yüzden sıkıcı gelebilir kusura bakmayın lütfen.

<p><img src="{{ site.url }}/assets/img/pıc1.png" alt="{{ page.title }}"></p>
PIC olanı seçiyoruz ve;

<p><img src="{{ site.url }}/assets/img/pıc2.png" alt="{{ page.title }}"></p>

Download dedikten sonra programı kuruyoruz.

<p><img src="{{ site.url }}/assets/img/pıc3.jpg" alt="{{ page.title }}"></p>

Kurulum bittikten sonra eger elimizde PICkit varsa çıkan iki yükleme menüsüne de “yes” deyip ilerliyoruz.
PICkit yoksa brenner PIC programlayıcı kartlarından birini almanızı tavsiye ederim. Çogu yerde yapılısını anlatıyor ama bu tip konularda genelde alınmasından yanayım.

<p><img src="{{ site.url }}/assets/img/pıc6.jpg" alt="{{ page.title }}"></p>

Ben PIC K150 adı verilen sekildeki kartı kullanıyorum. Bunun içinde “https://buyhere22.com/components/k150/” linkinde “download” butonuna bastıktan sonra indirdigimiz arsivdeki “PIC Programmer Software” klasörünü içerisindeki “microbrn.exe” uygulamasını çalıstırıyoruz.

<p><img src="{{ site.url }}/assets/img/pıc4.png" alt="{{ page.title }}"></p>


<p><img src="{{ site.url }}/assets/img/pıc5.png" alt="{{ page.title }}"></p>

"microbrn.exe" uygulaması açıldıgında eger hatasını alıyorsak driver eksik demektir.

Bunun içinde “http://www.prolific.com.tw/US/ShowProduct.aspx?p_id=225&pcid=41” sitesinden “Download File: PL2303_Prolific_DriverInstaller_v1.18.0B.zip” arsivini indirip kuruyoruz ve bilgisayarımızı yeniden baslatıyoruz. su ana kadar win7 win8 win8.1 de sorunsuz çalıstıgını ancak win10 da çok ugrasmama ragmen çalısmadıgını gördüm. Driver’ı yazan adamla iletisime geçtigimde de win10 için güncelleyecegini söylemisti umarım çalısıyodur.

    Sizlere tavsiye ettigim “mikroborn.exe” uygulaması denedigim tüm PIC programlama kartlarında ise yaradıgını ve çokta stabil çalısan bi programlama uygulaması oldugunu gördüm. Tabi gönül isterki PICkit alalım ama maliyet el vermiyor.

PIC programlamanın bir avantajı da ICSP ile programlamaktır.  
Tam olarak ne oldugunu tarif edememekle birlikte PIC imizi devreden sökmeden programlama kartımızın arkasında isimleri yazan “PGC, PGD, GND, VDD ve VPP” çıkıslarını PIC imizin (16F877A ve 18F4550) sırasıyla PGC = 39. PGD = 40. GND = 12. ve 31. VDD = 11. ve 32. VPP = 1. bacaklarına baglıyoruz ve programlayıcı uygulamızla programımızı PIC imizin içine atıyoruz.

<p><img src="{{ site.url }}/assets/img/pıc7.jpg" alt="{{ page.title }}"></p>

   Mikroborn uygulaması ile PIC imize programı nasıl atacagımıza gelirsek eger öncelikle program açıldıgında ve “K150 Connected” yazısını gördügümüzde sag tarafta PIC imizi seçiyoruz. Zaten uygulama görselinde bize hangi PIC i kullanırsak kullanalım (10F ve 18F serisi içerisinde) nasıl baglanacagını gösteriyor.

    Ilk olarak “Blank” diyoruz ve oradan “Erase Chip” butonuna tıklayıp “OK” diyoruz.
    Bu islem ardından PIC imizin içi temizleniyor.
    Ardından “Load” butonuna tıklayıp MikroC ile yazıp derlendiginde bize hex çıktısının kayıtlı oldugu yeri bulup seçiyoruz.
    Ardından “Fuses” kısmına tıklıyoruz ilk gelen alert ekranında “yes” butonunu seçerek “Fuses” ayarlarını MikroC de ayarladıgımız gibi otomatik olarak algılamasını istiyoruz.
    Sonrasında çıkan ekranı kapatıp “Program” butonuna tıklıyoruz.
    Eger “Bad ve Good” içeren bi hata mesajı alırsak Fuses (sigorta) ayarlarını yanlıs ayarlamısız demektir.
    Buna ayrıntılı bi sekilde deginecegiz ileride.


Ilk kez böyle bi yazı yazdıgım için çok amatörce olabilir zamanla eksik taslar ve anlatımım yerine oturacaktır.Okudugunuz için tesekkür ederim.
