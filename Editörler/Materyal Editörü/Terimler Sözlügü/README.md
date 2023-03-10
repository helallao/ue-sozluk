## Eye Adaptation
Eye adaption, yani ışıksız ortamdan ışıklı ortama girince ve ya ışıklı ortamdan ışıksız ortama girince olan göz adatasyonu. Kısaca gerçek hayatta gözlerimiz nasıl ışıga alışıyorsa, oyun içinde de Eye Adaptation budur.

## Gradient
Gradient nodları belirli şekiller veren nodlardır. Çizgi, daire, yıldız/elmas gibi. 1den 0a ve ya 0dan 1e dogru degerler verirler (hepsi degil). Bunları yani bu şekilleri kullanıp texture eklemeye gerek kalmadan işlemlerimizi yapabiliriz.

## Material Attributes
["Main Material Node"](../Graph/Main%20Material%20Node) da olan attribute lerin aynılarına sahiptir. Kodların çok karışacagı ve ya birden fazla materyalle ugraştıgınız durumlarda "Material Attributes" kullanmak kolaylık saglar. "Material Attributes" sadece "Main Material" nodunun kopyasını verir, yani sonuç olarak hala tek bir tane gerçek "Main Material Node" vardır. "Material Attributes" ları kullanmak için gerçek olan "Main Material" nodunun "Use Material Attributes" seçenegini aktifleştirin.

## Material Parameter Collection
Material Parameter Collection oluşturmak için Content Drawer'da [Add butonunu](../../../Sayfalar/Content%20Drawer/Toolbar#add-butonu) kullanarak ve ya boş bir yere sag tıklayarak, "Materials" bölümünden oluşturabilirsiniz. Material Parameter Collection şu işe yarar, materyallere vermek istediginiz bütün parametreleri burada toplarsınız, database gibi. Sonra [CollectionParameters](../Nodlar#collectionparameters-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F) nodunu kullanarak bu parametreleri databaseden çekersiniz ve materyalinizde kullanırsınız. Material Parameter Collection dosya olarak kaydedildigi için istediginiz kadar materyalde kullanabilirsiniz, ayrıca blueprint nodları ile de database üzerinde degişiklikler yapabilirsiniz.

## Offset
Offset kelimesi anlam olarak bir şey dengelemek için eklenen ek, dizgin gibi bi anlama gelir. Biz bunu genellikle konum degerlerine eklenen offset olarak görecegiz. Offset tam olarak şu işe yarar. Mesela sürekli 2000 ve 2100 arasında dönen bi deger almak istiyorsunuz, 2000 sayısını 2100e kadar arttırıp sonra tekrar 2000e düşürmek yerine, offset mantıgını kullanıp 2000 + offset degeri şeklinde yapabilirsiniz. Biz 100 artmasını istiyoruz yani offset degerimiz 0 ile 100 arasında olacak, mesela offset degeri 50 olursa 2000 + 50 = 2050 olur. İşte konum degerlerinde de bu şekilde kullanıcaz, konumun üzerine ekleme yapmak ve ya çıkarma yapmak için offset kullanılıyor. Direk konum degerini degiştirmek yerine offset degerini yani eklenecek degeri düzenliyoruz.

## Sprite Sheet
Sprite Sheet yapacagınız animasyonda olan bütün resimleri (frame) tek bir resim dosyasına tablo halinde parçalara bölüp koydugunuz teknik/yöntem dir. Bu yöntemle animasyondaki resimleri tek bir dosyada toplamış olursunuz. Sprite Sheet destekleyen yazılım resimleri bölme ve oynatma işlemini yapar. Aşagıdaki resim bir Sprite Sheet örnegi.

<img width="150" src="../../../Dosyalar/Sprite_Sheet.jpg">

## Vertex
Vertex ingilizcede tepe, zirve anlamına gelir. Biz vertex kelimesini, XYZ eksenlerine ve bunların tam tersine bakan noktalar için kulanıcaz. Yani mesela X eksenine bakan nokta vertex ve ya X ekseninin tam zıttına (-1) bakan nokta da vertex. XYZ olarak 3 tane vertex ve bunların eksili hali yani -XYZ olarak da 3 tane vertex, toplamda 6 vertex vardır. Bunu bir küpün 6 yüzeyi olarak düşenebilirsiniz. Bu 6 yön vertex'dir.

## World Space (Uzay Boşlugu)
World Space türkçesi ile Uzay Boşlugu, kısaltma olarak WS şeklinde kullanılır. World Space yani Uzay Boşlugu degerini materyaller arasındaki (ve ya tek bir materyal de olabilir) konum degerlerini objeye göre degil de uzay boşluguna göre ayarlamak istedigimizde kullanırız. İçerisinde WS geçen nodlar World Space degerleri döndürürler.
