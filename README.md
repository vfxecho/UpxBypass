# UpxBypass
                                         Tersine mühendislik upx korumasını atlatma.



Upx bilindik standart koruma yöntemidir. sıkça kullanılan bu koruma yöntemi müdahele ile kolayca çözülebilir.

Korumanın söz konusu olduğu program açılmadan bypass işlemi uygulanması imkansızdır.

Upx inject işlemi ile müdahele edilerek unpack edilebilmektedir.


her şeyden ilk olarak repoda verdiğim programları kurmanız gerekiyor.


                                                 Müdahele araçları:


https://www.kisa.link/P13e Upx Unpacker.

CrackMe Upx Koruması olan bir uygulama: https://www.reversing.be/easyfile/file.php?show=20050622213207221

                                                    Başlıyalım.

Unpackeri çıkardığımız klasore sağ tıklayıp powershell  > upx -d '.\dosyaismi.exe'

Çıkarılan deobf dosyasını

