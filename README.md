![upxshit](https://user-images.githubusercontent.com/30727573/121819411-a24bc480-cc95-11eb-8698-305928e30573.png)



Upx bilindik standart koruma yöntemidir. sıkça kullanılan bu koruma yöntemi müdahele ile kolayca çözülebilir.

Korumanın söz konusu olduğu program açılmadan bypass işlemi uygulanması imkansızdır.

Upx inject işlemi ile müdahele edilerek unpack edilebilmektedir.


her şeyden ilk olarak repoda verdiğim programları kurmanız gerekiyor.


                                                 Müdahele araçları:


https://www.kisa.link/P13e Upx Unpacker.

CrackMe Upx Koruması olan bir uygulama: https://www.reversing.be/easyfile/file.php?show=20050622213207221

                                                    Başlıyalım.

Unpackeri çıkardığımız klasore sağ tıklayıp powershell  > upx -d '.\dosyaismi.exe'

Çıkarılan deobf dosyasını dedect it easy koyup unpack olmuşmu diye bakıyoruz.

![unpacked](https://user-images.githubusercontent.com/30727573/121819495-11c1b400-cc96-11eb-8d08-fb6ab691fca3.PNG)

Görünüşe göre dosyamız unpacklendi :) bitti mi bitmedi devam edelim.

64dbg ile obfuslanmış dosyanın içerisine debug moduna alıp f9 basıyoruz.

Tail jump işlemine geçeceğiz. ama ilk olarak tailin ne olduğunu açıklayayım.

Tail jump:

Kuyruk atlamasıdır. bu kodun sonunda bulunan bir talimattır ve çok uzaktaki bir adrese bağlantı verir bu atlamayı bir dizi talimattan hemen önce bulmanız gerekmektedir.

Aksi takdirde çoğu işleme tekrar bbaşlamanız gerekir buda size zaman kaybeder.


