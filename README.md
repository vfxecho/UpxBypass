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

64dbg ile obfuslanmış dosyanın içerisine f2 ile debug moduna geçiyoruz.

Tail jump işlemine geçeceğiz. ama ilk olarak tailin ne olduğunu açıklayayım.

Tail jump:

tail jump türkçe karşılığı ile Kuyruk atlamasıdır. bir kodun sonunda bulunan bir yönergedir ve çok diğer ucundaki bir adrese bağlantı gönderir bu atlamayı  yaptığınız talimattan hemen önce bulmanız gerekmektedir.

Aksi takdirde çoğu işleme tekrar bbaşlamanız gerekir buda size zaman kaybeder.

![tail1](https://user-images.githubusercontent.com/30727573/121819666-06bb5380-cc97-11eb-9bb0-7e01f8b32321.PNG)

1. line burada

![jump2](https://user-images.githubusercontent.com/30727573/121819733-5f8aec00-cc97-11eb-8cf4-ea4bd4ea65d6.PNG)

Buda diğer ucu

Jpm'ye f9 ile breakpoint koyup f2 ile debug modundan çıkıyoruz.

Kodlar yukarıdan aşşağıyla sıralanır.

1. uçtan debugger ile programı açıp key sıralamasını deniyoruz.

eğer kod breakpointte sona ererse doğru yapmışsınızdır.

eğer kod breakpoint dışında yada içinde vermesse. yalnış bir şey yapmışsınızdır.

Breakpointin durduğu adrese sağ tık string references > strings.'e tıklıyoruz.

![breakpoints](https://user-images.githubusercontent.com/30727573/121819847-07a0b500-cc98-11eb-9fde-5d12d4f4bbe0.PNG)

Gördüğünüz üzere girilen değerler burda :)

Key hatalı ise try again, doğruysa congrulations. yazısını çıkarmakta.


                                                            Başarılı Sonuç
                                                            
Breakpointin durduğu adrese tekrar gelip debug modunda başlattıktan sonra bekliyoruz. veee

![Anahtar](https://user-images.githubusercontent.com/30727573/121819945-9a415400-cc98-11eb-9f53-e591ab55db8d.PNG)

Hop keyi aldık.

Dnspy aracı ile sourceine ulaşabilir veya geliştirebilirsiniz.

Bakalım key çalışıyormu.

![congrulations](https://user-images.githubusercontent.com/30727573/121820018-18055f80-cc99-11eb-850e-bc8f0b054232.PNG)

Evet programı tamamen kırdık.

Bu tarz tersine mühendislik eğitimlerini yakında youtube kanalımda çekmeyi düşünüyorum.

Ama şimdilik böyle desek kafidir :)

                                                                     Sonuç?
                                                          
hata ayıklayıcı aracılığıyla mevcut tüm string referanslarını kontrol ederek bu komutu yürütebilir korumayı aşarak  bu stringleri arayabilir ve editleyebiliriz, eğer rastgele bi keyi programa yazarsak muhtemelen hata verecektir.

Sonuç olarak cracklendi ve artık tamamen erişilebilir.





