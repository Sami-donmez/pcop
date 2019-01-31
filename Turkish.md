# pCOP

NodeMCU ile uzaktan bilgisayarınızı açın, kapatın veya yeniden başlatın.

## Devre

  ### Gerekli Malzemeler
    * NodeMCU (ESP-12E 4M)
    * 4 adet Dişi-Erkek Jumper Kablo
    * 6 Adet Erkek-Erkek Jumper Kablo
    * 1 adet BC559 PNP Transistör
    * 1 adet 2N3904 NPN Transistör
    * 1 adet orta boy breadboard

  ### Firmware (Yazılım) Yüklenmesi
  - [ESP Flash Download Tool](https://www.espressif.com/en/support/download/other-tools) Yazılımı İndirin.
  - [Firmware(Yazılım)](https://github.com/muhep06/pcop/tree/master/firmware) Dosyalarını İndirin.
  - ESP Flash Download Tool yazılımını çalıştırın.
  - ESP8266 DownloadTool seçeneğini seçiniz.

  ### Gerekli Bilgiler
  - Yazılım yüklemesi bittikten sonra pCOp yazılımının varsayılan kullanıcı adı admin, varsayılan şifresi adminadmin şeklindedir. pCOp cihazınıza sabit IP vermediyseniz cihazın IP adresine Serial Monitor kullanarak ulaşabilirsiniz. Varsayılan port 8083'tür.

  - Modem üzerinden, NodeMCU karınızın MAC Adresine göre sabit IP atayabilirsiniz. Böylece cihazınızın IP adresi değişmez ve her zaman atadığınız sabit IP üzerinden cihazınıza ulaşabilirsiniz.
  
  - İlk kurulum sonrası 45 saniye bekleyiniz. Cihaz kurtarma moduna girecektir.(Eğer cihaz açıldıktan sonra 45 saniye içinde WiFi bağlantısı gerçekleştiremez ise) 45 saniye sonra RECOVERY_MODE adında bir WiFi ağı oluşacaktır. Bu WiFi ağına bağlanarak (http://192.168.4.1:8083/) adresinde gidiniz ve bağlanmak istediğiniz WiFi bilgilerini giriniz. Kurtarma modunda WiFi bilgilerini ayarlamak için 60 saniyeniz var. Cihaz kurtarma modunda 60 saniyede bir yeniden başlatılır. WiFi bilgileriniz doğruysa cihaz WiFi ağına bağlanacaktır. 45 saniye içinde cihaz girdiğiniz bilgilerle WiFi ağına bağlanamaz ise cihaz tekrar kurtarma moduna girecektir.

  - Cihaz girdiğiniz bilgilerle bir WiFi ağına bağlantı sağladıysa tarayıcı üzerinden Serial Monitörden öğrenebileceğiniz IP adresini kullanarak Kontrol Paneline ulaşabilirsiniz. Unutmayın cihaz 8083 portunda çalışmaktadır. ÖRN: http://192.168.1.x:8083 şeklinde olmalıdır.

  - Cihazınız bir WiFi ağına bağlıyken WiFi bağlantısını kaybederse 60 saniye boyunca kaybedilen bağlantıyı yeniden kurmaya çalışır. Eğer 60 saniye boyunca bağlantı kuramaz ise cihaz kendini yeniden başlatır. Yeniden başlatma sonrası bağlantı sağlarsa cihaz tekrar çevrimiçi olur bağlantı sağlayamaz ise cihaz kurtarma moduna girer. 60 saniye bekler ve yeniden başlar. Yeniden başlama sonrası cihaz tekrar bağlantı kurmaya çalışır, cihaz bağlantı kuramazsa tekrar kurtarma moduna girer ve bu şekilde bir kısır döngü içinde WiFi ağına bağlantıyı sağlamaya çalışır. Böylece cihazınız sürekli çevrimdışı kalmaz ve WiFi sorunu düzelince tekrar çevrimiçi olur.

  ![pCOp Şeması](https://raw.githubusercontent.com/muhep06/pcop/master/images/adim1.PNG)
  - İndirdiğiniz firmware(yazılım) dosyalarını aşağıdaki resimde olduğu gibi ESP Flash Download Tool yazılımı üzerinde seçiniz.

  ![pCOp Şeması](https://raw.githubusercontent.com/muhep06/pcop/master/images/adim2.PNG)
  
  ### Breadboard Şeması
  ![pCOp Şeması](https://raw.githubusercontent.com/muhep06/pcop/master/images/pcop-turkish_bb.png)