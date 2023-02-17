## Eye Adaptation
Eye adaption, yani ışıksız ortamdan ışıklı ortama girince ve ya ışıklı ortamdan ışıksız ortama girince olan göz adatasyonu. Kısaca gerçek hayatta gözlerimiz nasıl ışıga alışıyorsa, oyun içinde de Eye Adaptation budur.

## Gradient
Gradient nodları belirli şekiller veren nodlardır. Çizgi, daire, yıldız/elmas gibi.

## Offset
Offset kelimesi anlam olarak bir şey dengelemek için eklenen ek, dizgin gibi bi anlama gelir. Biz bunu genellikle konum degerlerine eklenen offset olarak görecegiz. Offset tam olarak şu işe yarar. Mesela sürekli 2000 ve 2100 arasında dönen bi deger almak istiyorsunuz, 2000 sayısını 2100e kadar arttırıp sonra tekrar 2000e düşürmek yerine, offset mantıgını kullanıp 2000 + offset degeri şeklinde yapabilirsiniz. Biz 100 artmasını istiyoruz yani offset degerimiz 0 ile 100 arasında olacak, mesela offset degeri 50 olursa 2000 + 50 = 2050 olur. İşte konum degerlerinde de bu şekilde kullanıcaz, konumun üzerine ekleme yapmak ve ya çıkarma yapmak için offset kullanılıyor. Direk konum degerini degiştirmek yerine offset degerini yani eklenecek degeri düzenliyoruz.

## Sprite Sheet
Sprite Sheet yapacagınız animasyonda olan bütün resimleri (frame) tek bir resim dosyasına tablo halinde parçalara bölüp koydugunuz teknik/yöntem dir. Bu yöntemle animasyondaki resimleri tek bir dosyada toplamış olursunuz. Sprite Sheet destekleyen yazılım resimleri bölme ve oynatma işlemini yapar. Aşagıdaki resimde bir Sprite Sheet örnegi var.

<img width="150" src="../../../Dosyalar/Sprite_Sheet.jpg">


## World Space (Uzay Boşlugu)
World Space türkçesi ile Uzay Boşlugu, kısaltma olarak WS şeklinde kullanılır. World Space yani Uzay Boşlugu degerini materyaller arasındaki (ve ya tek bir materyal de olabilir) konum degerlerini objeye göre degil de uzay boşluguna göre ayarlamak istedigimizde kullanırız. İçerisinde WS geçen nodlar World Space degerleri döndürürler.
