## Detail Texturing
Detail Texturing, kullanıdıgınız Base Color ve Normal Map üzerine, yeni Base Color ve Normal Map eklemek (bazen, sadece Normal Map de yeterli olur) ve texture üzerinde, texture'a çok yaklaşsak bile görülebilecek detaylar oluşturmaktır. Detail Texturing yapmadıgımız materyallerde, eger texture'a çok yakından bakarsanız üzerindeki detayların çok olmadıgını görebilirsiniz (aslında bu kullanılan texture'a göre). Böyle durumlarda texture üzerine, ikincil Normal Map ekleriz ve bu Normal Map'in tiling (tekrarlama) ayarını yükseltiriz. Bu da bize çok küçük küçük detaylar verir ve texture daha gerçekçi olur. Tabi Detail Texturing sadece yakından görülecek texture'lar için gereken bi durum. Daha fazla bilgi için [buraya](https://docs.unrealengine.com/5.1/en-US/adding-detail-textures-to-unreal-engine-materials/) bakın.

## Eye Adaptation
Eye adaption, yani ışıksız ortamdan ışıklı ortama girince ve ya ışıklı ortamdan ışıksız ortama girince olan göz adatasyonu. Kısaca gerçek hayatta gözlerimiz nasıl ışıga alışıyorsa, oyun içinde de Eye Adaptation budur.

## Gradient
Gradient nodları belirli şekiller veren nodlardır. Çizgi, daire, yıldız/elmas gibi. 1'den 0'a ve ya 0'dan 1'e dogru degerler verirler (hepsi degil), yani grayscale. Bunları yani bu şekilleri kullanıp texture eklemeye gerek kalmadan işlemlerimizi yapabiliriz.

## Material Attributes
["Main Material Node"](../Graph/Main%20Material%20Node) da olan attribute'lerin aynılarına sahiptir. Kodların çok karışacagı ve ya birden fazla materyalle ugraştıgınız durumlarda "Material Attributes" kullanmak kolaylık saglar. "Material Attributes" sadece "Main Material" nodunun kopyasını verir, yani sonuç olarak hala tek bir tane gerçek "Main Material Node" vardır. "Material Attributes" ları kullanmak için Main Material nodunun ["Use Material Attributes"](../Graph/Main%20Material%20Node#use-material-attributes) seçenegini aktifleştirin.

## Master Material Fonksiyonları
"MF_" prefixi (Prefix = ön ek) ile başlayan nodlardır. Normalde "MF_" prefixi Unreal Engine'de kullanıcılar tarafından oluşturulmuş materyal fonksiyonları için bir belirteçtir ama Materyal Editöründe kullanıcı tarafından oluşturulmamış, motorla birlikte gelen "MF_" prefixi ile başlayan nodlar var. Aslında bunlar aynı işleve yarayan bir grup nodlar ama Unreal Engine geliştiricileri bu nodlara isim koymak için yanlış bi seçim yapmış. Zaten Materyal Editöründe bir sürü fonksiyon vardı, hiçbirinde "MF_" prefixi kullanılmadı, sadece bu nodlarda kullanmaları çok mantıksız. Neyse, bu nodlar kullanıcılar tarafından yazılmış "MF_" ile başlayan fonksiyonlar ile karışabilir (idare etcez artık). Bu nodların işlevine gelirsek, bu nodlar Materyal Instance oluşturdugumuzda kullanabilelim diye bize otomatik parametre oluşturan fonksiyonlardır. Konuya göre dagılmışlardır ve bu fonksiyonları kullanıp materyale bir sürü parametre ekleyebilirsiniz ama kullanılmayacak parametreler de eklemek materyali daha karmaşık yapar. Master Materyaller parametreler aracılıgıyla yönetilen materyaller oldugu için Master Material Fonksiyonları çok kullanılır.

## MipMap
[MipMap](https://en.wikipedia.org/wiki/Mipmap), oluşturdugumuz bir texture'nin daha küçük boyutlarda versiyonlarını da oluşturmaktır. Her MipMap bir öncekinin yarısı kadar piksel sayısına sahiptir yani her MipMap oluşturmada texture kalitesi yarılanır. Orijinal kaliteden 1x1 (ya da 2x2 emin degilim) kalitesine kadar zincirleme bir MipMap oluşturma işlemi gerçekleşir. Bu işlem sadece MipMap oluşturuldugu anda olur yani siz projenizi hazırlarken. MipMap'ler şu işe yarar, mesela oyun içinde bir obje size çok uzakta ve bu obje için kullandıgınız texture'yi en son kalitede render ederek performans düşürmeye gerek yok, bunun yerine objeden uzaklaşıldıgında kalitesinin düşürülmesi performans açısından daha iyi ama bu taktik render (performans) açısından iyi olsa da, alan açısından kötüdür (yani kötü demiyelim de, projenize göre). Projenizdeki her bir texture [%33](https://en.wikipedia.org/wiki/1/4_%2B_1/16_%2B_1/64_%2B_1/256_%2B_%E2%8B%AF) daha fazla alan kaplar. Ayrıca bu teknik kaliteyi de arttırır ([aliasing](https://en.wikipedia.org/wiki/Aliasing) bakımından).

<img src="../../../Dosyalar/Mipmap_Aliasing_Comparison.png">

## Named Reroute Declaration Node
[Add Named Reroute Declaration Node...](../Nodlar#add-named-reroute-declaration-node-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F) nodu ile oluşturulur. İsimlendirilmiş düzenleme nodunu kullanarak nodların birbirine girip spagetti oluşturmasını engelleyebilirsiniz. İsimlendirilmiş düzenleme nodlarının bir girişi ve sınırsınız çıkışı vardır. [Add Named Reroute Declaration Node...](../Nodlar#add-named-reroute-declaration-node-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F) nodunu kullandıgınızda girişi oluşturmuş olursunuz. Sonrasında oluşturdugunuz isimlendirilmiş düzenleme nodunun çıkışını istedigini kadar kullanabilirsiniz, çıkış [Named Reroutes](../Nodlar#named-reroutes) kategorisinde görünür. Yani kısacası çıkıştan gelen kodlar girişe giren kodlardan gelen içeriktir, ışınlama işlemi gibi düşünebilirsiniz.

## Normal Map - Displacement Map - Bump Map - Height Map
Normal Map içerisinde yön degerlerini (açıları) tutar ve bize bazı kısımları yüksek bazı kısımları alçak gösterir, yani 3d gibi. Bütün açılar için ışıgın yansıma (ve ya başka bişe emin degilim) bilgisini tutar. Aslında hiçbir yükseklik bilgisi tutmaz ama tuttugu yön (açı) degerleri, motora yükseklik degerlerini simule edebilmesi için gerekli bilgiyi sunar, yani fake bir yükseklik görüntüsü oluşturur. Diger Mapler (Displacement, Bump ve Height) de aynı şeyi yaparlar yani fake bir yükseklik görüntüsü oluştururlar ama hiçbiri Normal Map gibi her yönün, açının degerini tutmadıgı için Normal Map kadar kaliteli - kapsamlı degillerdir. Şimdi gelelim diger Maplere Displacement Map, Bump Map ve Height Map, bunlar hakkında uzun yazılar okusam bile görünüşe göre herşeyleri aynı sadece kullanılış alanları farklı ama kullanılış alanları farklı olsa bile aynı bilgileri tutan aynı şeyler oldukları için birbirleri yerine kullanılabiliyorlar ve aynı bilgileri tutan şeyler oldukları için isimleri de sürekli birbiri yerine kullanılıyor. Dolayısı ile hepsini aynı şeymiş gibi düşünüp anlatıcam (zaten teknik açıdan aynılar). Displacement Map, Bump Map ve Height Map, Normal Mapin eski hali gibi düşünülebilir. Bu maplerin hepsi grayscale (tek kanal) ve sadece yükseklik bilgisi tutarlar. Daha fazla bilgi için [bu kaynaga](https://www.cgdirector.com/normal-vs-displacement-vs-bump-maps/) bakabilirsiniz.

## Offset
Offset kelimesi anlam olarak bir şey dengelemek için eklenen ek, dizgin gibi bi anlama gelir. Offset bize boşluk verme, ya da orijinal degerin üzerine ekleme yapma olanagı saglar. Mesela konum degerlerinde offset şu işe yarar, diyelim ki sürekli 2000 ve 2100 arasında dönen bi deger almak istiyorsunuz, 2000 sayısını 2100'e kadar arttırıp sonra tekrar 2000'e düşürmek yerine, offset mantıgını kullanıp 2000 + offset degeri şeklinde yapabilirsiniz. Biz 100 artmasını istiyoruz yani offset degerimiz 0 ile 100 arasında olacak, mesela offset degeri 50 olursa 2000 + 50 = 2050 olur. İşte konum degerlerinde de bu şekilde kullanıcaz, konumun üzerine ekleme yapmak ve ya çıkarma yapmak için offset kullanılıyor. Offset sadece konum degerlerinde degil, bir sürü başka şeyde de kullanacaksınız. Sonuç olarak offset, belirli bi degeri ileri/geri alma anlamına geliyor.

## Packed Map
[Main Material Node'un Attribute'lerine](../Graph/Main%20Material%20Node#attributes) bagladıgımız Maplerin hepsi RGB yani 3 kanala ihtiyacı duymaz. Tek kanal olanlar da vardır (grayscale) ve bu Mapler için tek tek texture oluşturup hem düzensizlik hem de performans düşüşü yapmaya gerek yok, bu tek kanallı Mapleri tek bir texturenin R,G ve B kanallarına ayrı ayrı koyabiliriz. Buna "Packed Map" denir. Texturenin ismine bu Maplerin sırasına göre baş harfleri konulur. Packed Map olabilecek Attributeler ve alabilecegi isimler aşagıda, mesela Unreal Engine Quixel Bridge'den alının materyaller için "ORDp" adında bir texture kullanır. O -> Ambient Occlusion, R -> Roughness, Dp -> Displacement Mapini temsil eder. Sırayla RGB kanallarına konulmuşlardır.

Map | Kısa İsim
:---: | :---:
Base Color | Color, Diffuse, Albedo, D, C, BC
Metallic | M
Specular | S, Reflection
Roughness | R, G, GL
Emissive Color | E, Emmission, Glow
Normal | Normal, N, Nor_GL, Nor_DX
Ambient Occlusion | AO, O
Displacement | D, DP

## Niagara Nodları
Materyaller içerisinide parçacık sistemi (niagara) ile ilgili nodlar vardır. Bu nodlar parçacıkları yönetebilmemiz içindir. Eger materyalimizi niagara sisteminde kullanacaksak materyal içerisindeki niagara nodlarını kullanmamız gerekir.

## Sprite Sheet
Sprite Sheet yapacagınız animasyonda olan bütün resimleri (frame) tek bir resim dosyasına tablo halinde parçalara bölüp koydugunuz teknik/yöntem dir. Bu yöntemle animasyondaki resimleri tek bir dosyada toplamış olursunuz. Sprite Sheet destekleyen yazılım resimleri bölme ve oynatma işlemini yapar. Aşagıdaki resim bir Sprite Sheet örnegi.

<img width="150" src="../../../Dosyalar/Sprite_Sheet.jpg">

## Vertex
Vertex ingilizcede tepe, zirve anlamına gelir. Biz vertex kelimesini, XYZ eksenlerine ve bunların tam tersine bakan noktalar için kulanıcaz. Yani mesela X eksenine bakan nokta vertex ve ya X ekseninin tam zıttına (-1) bakan nokta da vertex. XYZ olarak 3 tane vertex ve bunların eksili hali yani -XYZ olarak da 3 tane vertex, toplamda 6 vertex vardır. Bunu bir küpün 6 yüzeyi olarak düşenebilirsiniz. Bu 6 yön vertex'dir.

## Vertex Shader ve Pixel Shader
Bu ikisi hakkında bir sürü video izledim ama hala tam anladıgımı söyleyemem. İlk olarak burda bahsedilen "Vertex" ile "Vertice" (yani meshleri oluşturan her geometri, her parça, her triangle) aynı şey. Pixel Shader ekrandaki her pikseli işlerken, Vertex Shader her vertexi (vertice) işler. Mesela diyelim ki ekranınıza ufak bi küp meshi koydunuz, toplam 8 vertice (vertex) den oluşuyor ve siz bu küpün scale degerini çok büyüttünüz, o kadar büyük ki küpe yakından bakarken ekranınızın yarısını kaplıyor, bu durumda hesaplamaları Pixel Shader yaparsa mesela 1000x1000 pikseli hesaplaması gerekecek ama hesaplamaları Vertex Shader yaparsa sadece 8 vertice (vertex) için hesaplama yapması gerekecek. Dolayısıyla vertice (vertex) sayısı düşük olan meshler için Vertex Shader kullanmak performans açısından çok kar saglar. Peki eger vertice (vertex) sayısı çok fazla olan bir meshimiz varsa, mesela diş fırçası, bu durumda Vertex Shader yerine Pixel Shader kullanmalıyız. Diş fırçası meshi ekranımızda en fazla 100x100 piksel falan yer kaplar çünkü küçük. Eger Vertex Shader kullanıp her vertice (vertex) için hesaplama yaparsak performans kaybı yaşarız, hesaplamaları Pixel Shader kullanıp yaparsak performans açısından çok kar saglarız. Tabi bunlar çok özel durumlar, genel olarak (nerdeyse hep) Vertex Shader kullanmak Pixel Shader kullanmaktan daha performanslıdır ama yine de işler yukarda yazdıgım gibi işliyor.

<img width="400" src="../../../Dosyalar/Vertex_and_Pixel_Shader.jpg">

## World Space (Uzay Boşlugu)
World Space türkçesi ile Uzay Boşlugu, kısaltma olarak WS şeklinde kullanılır. World Space yani Uzay Boşlugu degerini materyaller arasındaki (ve ya tek bir materyal de olabilir) konum degerlerini objeye göre degil de uzay boşluguna göre ayarlamak istedigimizde kullanırız. İçerisinde WS geçen nodlar World Space degerleri döndürürler.
