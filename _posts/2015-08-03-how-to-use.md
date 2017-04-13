---
layout: post
title: "PIC Programlama"
date: 2017-04-11 03:32:44
image: '/assets/img/'
description: 'PIC Programlamaya Giriş-I'
tags:
- PIC
- microc
categories:
- PIC Programlama
twitter_text: 'How to install and use this template'
---

Merhaba arkadaşlar,
-------------------

PIC programlama ve uygulama örnekleri ile bir başlangıç yapmak istedim. Çalışmalarımızı 16F877A ve 18F4550 PIC’lerini kullanmayı amaçlıyorum.
İlk olarak yol “https://www.mikroe.com/mikroc/” MikroC’nin kendi sitesinden demo versiyonunu indirerek başlayacağız. Sıfırdan başlamak isteyen arkadaşlar için olabildiğince ayrıntıya ineceğim bu yüzden sıkıcı gelebilir kusura bakmayın lütfen.

<p><img src="{{ site.url }}/assets/img/pıc1.png" alt="{{ page.title }}"></p>
PIC olanı seçiyoruz ve;

<p><img src="{{ site.url }}/assets/img/pıc2.png" alt="{{ page.title }}"></p>

Download dedikten sonra programı kuruyoruz.

<p><img src="{{ site.url }}/assets/img/pıc3.jpg" alt="{{ page.title }}"></p>

Kurulum bittikten sonra eğer elimizde PICkit varsa çıkan iki yükleme menüsüne de “yes” deyip ilerliyoruz.
PICkit yoksa brenner PIC programlayıcı kartlarından birini almanızı tavsiye ederim. Çoğu yerde yapılışını anlatıyor ama bu tip konularda genelde alınmasından yanayım.

<p><img src="{{ site.url }}/assets/img/pıc6.jpg" alt="{{ page.title }}"></p>

Ben PIC K150 adı verilen şekildeki kartı kullanıyorum. Bunun içinde “https://buyhere22.com/components/k150/” linkinde “download” butonuna bastıktan sonra indirdiğimiz arşivdeki “PIC Programmer Software” klasörünü içerisindeki “microbrn.exe” uygulamasını çalıştırıyoruz.

<p><img src="{{ site.url }}/assets/img/pıc4.png" alt="{{ page.title }}"></p>


<p><img src="{{ site.url }}/assets/img/pıc5.png" alt="{{ page.title }}"></p>

"microbrn.exe" uygulaması açıldığında eğer hatasını alıyorsak driver eksik demektir.

Bunun içinde “http://www.prolific.com.tw/US/ShowProduct.aspx?p_id=225&pcid=41” sitesinden “Download File: PL2303_Prolific_DriverInstaller_v1.18.0B.zip” arşivini indirip kuruyoruz ve bilgisayarımızı yeniden başlatıyoruz. Şu ana kadar win7 win8 win8.1 de sorunsuz çalıştığını ancak win10 da çok uğraşmama rağmen çalışmadığını gördüm. Driver’ı yazan adamla iletişime geçtiğimde de win10 için güncelleyeceğini söylemişti umarım çalışıyodur.

    Sizlere tavsiye ettiğim “mikroborn.exe” uygulaması denediğim tüm PIC programlama kartlarında işe yaradığını ve çokta stabil çalışan bi programlama uygulaması olduğunu gördüm. Tabi gönül isterki PICkit alalım ama maliyet el vermiyor.

PIC programlamanın bir avantajı da ICSP ile programlamaktır.  
Tam olarak ne olduğunu tarif edememekle birlikte PIC imizi devreden sökmeden programlama kartımızın arkasında isimleri yazan “PGC, PGD, GND, VDD ve VPP” çıkışlarını PIC imizin (16F877A ve 18F4550) sırasıyla PGC = 39. PGD = 40. GND = 12. ve 31. VDD = 11. ve 32. VPP = 1. bacaklarına bağlıyoruz ve programlayıcı uygulamızla programımızı PIC imizin içine atıyoruz.

<p><img src="{{ site.url }}/assets/img/pıc7.jpg" alt="{{ page.title }}"></p>

   Mikroborn uygulaması ile PIC imize programı nasıl atacağımıza gelirsek eğer öncelikle program açıldığında ve “K150 Connected” yazısını gördüğümüzde sağ tarafta PIC imizi seçiyoruz. Zaten uygulama görselinde bize hangi PIC i kullanırsak kullanalım (10F ve 18F serisi içerisinde) nasıl bağlanacağını gösteriyor.

    İlk olarak “Blank” diyoruz ve oradan “Erase Chip” butonuna tıklayıp “OK” diyoruz. Bu işlem ardından PIC imizin içi temizleniyor ve ardından “Load” butonuna tıklayıp MikroC ile yazıp derlendiğinde bize hex çıktısının kayıtlı olduğu yeri bulup seçiyoruz ve ardından “Fuses” kısmına tıklıyoruz ilk gelen alert ekranında “yes” butonunu seçerek “Fuses” ayarlarını MikroC de ayarladığımız gibi otomatik olarak algılamasını istiyoruz sonrasında çıkan ekranı kapatıp “Program” butonuna tıklıyoruz. Eğer “Bad ve Good” içeren bi hata mesajı alırsak Fuses (sigorta) ayarlarını yanlış ayarlamışız demektir. Buna ayrıntılı bi şekilde değineceğiz ileride. Şimdilik bu kadar. İlk kez böyle bi yazı yazdığım için çok amatörce olabilir zamanla eksik taşlar ve anlatımım yerine oturacaktır.

Okuduğunuz için teşekkür ederim.
