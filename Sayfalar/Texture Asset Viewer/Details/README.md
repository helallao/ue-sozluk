# Details
<img src="../../../Dosyalar/Texture_Asset_Viewer_Details.jpg">



# Bölümler

* [Level Of Detail](#level-of-detail)
* [Compression](#compression)
* [Interchange](#interchange)
* [Texture](#texture)
* [Adjustments](#adjustments)
* [File Path](#file-path)

## [Level Of Detail]()

#### [Mip Gen Settings]()
Buradan [MipMap](../../../Editörler/Materyal%20Editörü/Terimler%20Sözlügü#mipmap) için kullanılacak ayarı yapabilirsiniz. Size uygun olanı kullanmalısınız. Yanlarında sayı olan seçenekler, o ayarın ne kadar etkili oldugunu belirtiyor. Mesela "Blur1" ve "Blur5", "Blur1" az blur efekti, "Blur5" çok blur efekti demektir.

* ##### FromTextureGroup
Sanırım texture'un grubuna göre, Unreal Engine tarafından tanımlanan şekilde MipMap kullanıyor.

* ##### SimpleAverage
Normal MipMap.

* ##### Sharpen
Texture'u keskinleştirir. Piksel sayısı azaldıkça texture blurlu gibi ve anlaşılmaz olabilir. Texture'u keskinleştirmek, texture'u tekrar anlaşılır yapabilir.

* ##### NoMipmaps
MipMap kullanmaz.

* ##### LeaveExistingMips
Texture'un kendi MipMap ayarlarını degiştirmez ve onları kullanır.

* ##### Blur
Blur efekti verir.

* ##### Unfiltered
"SimpleAverage" e göre biraz daha blurlu, ne farkları oldugunu bilmiyorum.

* ##### Angular
Ne oldugundan emin degilim.

#### [LOD Bias]()
LOD Bias normalde 0'dır. Oluşturulan MipMap'ler 1'den başlar yani 1 ilk oluşturulan MipMap'tir ve sonra bu sayı artarak devam eder. LOD Bias orijinal texture olarak MipMap kullanmak yani maximum kaliteyi degiştirmemize yarar. Eger LOD Bias degerini 1 yaparsanız, 1 ilk oluşturulan MipMape'e denk geldigi için texture'un en yüksek kalitesi yarıya düşer, yani orijinal texture olarak ilk MipMap'i kullanmış olursunuz. Mesela elinizde 4k bir texture varsa ve siz de bunu sanki 2k texture'muş gibi kullanmak istiyorsanız LOD Bias degerini 1 yapabilirsiniz.

#### [Texture Group]()
Buradan texture'unuzun grubunu verdiginizde bir takım degişiklikler yapıyor, ne yaptıgını tam bilmiyorum ama muhtemelen %99 bu ayarı default yani "World" olarak kullanıcaksınız. Belki bi ihtimal UI için texture hazırlarken bu ayarı "UI" yapmanız gerekebilir, o da sorunlarla karşılaşırsanız.


## [Advanced]()

#### [Preserve Border]()
MipMap oluştururken texture'un köşelerini tutar yani silinmez. Eger köşelerin silinmemesi gerekiyorsa bu seçenegi açabilirsiniz.

#### [Downscale]()
Bu ayarı sadece MipMap yoksa kullanabilirsiniz. Deger 0'ken [Texture Group'dan](#texture-group) gelen scale degerine göre texture boyutlandırılır. Deger 1 iken [Texture Group'dan](#texture-group) gelen scale degerine göre texture'u boyutlandırmayı devre dışı bırakır yani boyutlandırmaz. Deger 1'i geçtikten sonra, arttıkça texture'unuz küçülür.

#### [Downscale Options]()
"Downscale" ayarını kullanırken, texture'u boyutlandırma işlemi esnasında uygulanacak efekti belirler, [Mip Gen Settings](#mip-gen-settings) gibi.

#### [Num Cinematic Mip Levels]()
bilmiyorum.

#### [Never Stream]()
Eger bu seçenek açılırsa, oyun oynanırken (runtime) texture'lar ram'den silinmezler, yani tekrar kullanılabilir diye tutulurlar.

#### [Global Force Resident Mip Levels]()
[Never Stream](#never-stream) gibi ama MipMap'ler için.



## [Compression]()

#### [Compress Without Alpha]()
Alpha kanalını texture sıkıştırmanın dışında bırakır.

#### [Editor Show Final Encode]()
#### [Editor Defer Compression]()
Bu seçenek texture sıkıştırma işlemini erteler. Normalde [Compression Settings](#compression-settings) bölümünden sıkıştırma ayarı degiştirildigi anda texture sıkıştırma işlemi gerçekleşir ama bu seçenegi açtıgınızda texture sıkıştırma işlemi siz manuel olarak (toolbar'daki [Compress](../Toolbar#compress) butonundan) sıkıştırana kadar ve ya [Save Butonuna](../Toolbar#save-butonu) basana kadar gerçekleşmez.

#### [Compression Settings]()

* ##### Default (DXT1/5, BC1/3 on DX11)
En etkili sıkıştırma yöntemlerinden biri, [6](https://www.techarthub.com/your-guide-to-texture-compression-in-unreal-engine/) - [8](https://youtu.be/h95X255NhOo?t=289) kata kadar sıkıştırma yapabiliyor. Eger Alpha kanalı yoksa DXT1, varsa DXT5 ([4](https://www.techarthub.com/your-guide-to-texture-compression-in-unreal-engine/) kata kadar sıkıştırma yapabiliyor) kullanır. Eger sisteminiz DirectX 11 üzeriyse, Alpha kanalı yoksa BC1, varsa BC3 kullanır.

* ##### Normalmap (DXT5, BC5 on DX11)
Normalmap'ler için kullanılan sıkıştırma yöntemi. Eger Normalmap kullanacaksanız en dogru seçenek budur çünkü Normalmap'ler daha farklı şekilde sıkıştırılma işleminden geçiyorlar. [4 kata kadar](https://www.techarthub.com/your-guide-to-texture-compression-in-unreal-engine/) sıkıştırma yapabiliyor. Herhangi bir Normalmap import ettiginizde Unreal Engine otomatikmen bu sıkıştırma yöntemini kullanıyor ama eger olur da kullanmazsa, o zaman manuel olarak buraya gelip kendiniz bu ayarı seçmelisiniz, Normalmap ile ilgili sorun yaşarsanız bakacagınız ilk ayar budur.

* ##### Masks (no sRGB)
Siyah-beyaz yani grayscale texture'lar için, bu grayscale texture'larda sRGB ye gerek yok çünkü içinde matematiksel bi bilgi taşıyor (bkz. [sRGB](#srgb)) ve grayscale texture'lar tek kanaldır, dolayısıyla texture'unuzda en az 3 grayscale texture var demektir, Alpha ile 4. Zaten bu yüzden ismi Mask degil de Masks. Özünde Default ile aynı sıkıştırmaları yapar yani sRGB kullanmadan Default sıkıştırmayı kullanırsanız Masks ile aynı sıkıştırma yöntemini kullanmış olursunuz.

* ##### Grayscale (G8/16, RGB8 sRGB)
Siyah-beyaz yani grayscale texture'lar için, texture'u tek bir kanala indirir, zaten adı üstünde Grayscale ve oluşturdugu bu kanalın kalitesini yüksek tutar, olabilecek en az seviyede sıkıştırır, texture'un kapladıgı alan artabilir ama tek bir kanal. Hatta belki sıkıştırma yapmıyor da olabilir. Bu sıkıştırmayı kullanırken bide [sRGB'yi](#srgb) açarsanız texture çok fena yer kaplar.

* ##### Displacementmap (G8/16)
Grayscale ile aynı diye düşünüyorum. Displacement Mapler için kullanılan sıkıştırma yöntemi.

* ##### VectorDisplacementmap (RGBA8)
Sıkıştırılmamış 32-bit RGBA, Grayscale ve ya Displacementmap gibi. Ayrıca Alpha kanalı zorunlu.

* ##### HDR (RGBA16F, no sRGB)
Hdri texturelar için. Integer yerine float tutar ve çok yüksek alan kaplayan texturelerdir. Ayrıca Alpha kanalı zorunlu.

* ##### UserInterface2D (RGBA)
Eger UI için kullanılacak bir texture hazırlıyorsanız bunu kullanmalısınız. Bu ayar UI içinde kullanılan texture'de MipMap ayarlarını devre dışı bırakır ve UI içinde görüntülenen texture'un kalitesi düşmez.

* ##### Alpha (no sRGB, BC4 on DX11)
Sanırım sadece Alpha kanalı.

* ##### DistanceFieldFont (G8)
Displacementmap ile aynı.

* ##### HDR Compressed (RGB, BC6H, DX11)
HDR ile aynı. Tek farkı "Yarım" float'lar kullanması ve böylelikle texture'un kapladıgı alanı yarıya düşürmesi.

* ##### BC7 (DX11, optional A)
Yeni çıkan bi sıkıştırma yöntemi. Bunu Default'un daha kalitesi daha yüksek ama daha fazla alan tutan versiyonu gibi düşünebilirsiniz. [4 kata kadar](https://youtu.be/h95X255NhOo?t=838) sıkıştırma yapabiliyor. Ayrıca Alpha kanalı zorunlu. Eger kullanmazsanız sistem oluşturur.

* ##### Half Float (R16F)
Siyah-beyaz tek kanallı bir texture. "Yarım" float türünden bilgi tutuyor. Ayrıca Alpha kanalı zorunlu.

* ##### Single Float (R32F)
bilmiyorum.

* ##### HDR High Precision (RGBA32F)
bilmiyorum.



## [Advanced]()

#### [Maximum Texture Size]()
Texture için maximum boyutu buraya yazabilirsiniz. "Boyutu düşürdüm ama sonuçta dosya aynı kalmayacak mı?" demeyin çünkü projenizi bitirip, oyunu paketlerken, cooking aşamasında buraya verdiginiz ayar kullanılacak yani texture'un boyutu düşmüş olacak.

#### [Lossy Compression Amount]()
#### [Oodle Texture Sdk Version]()
#### [ASTC Compression Quality]()
#### [Compression Cache ID]()




## [Interchange]()

#### [AssetlmportData]()




## [Texture]()

#### [Power Of Two Mode]()
Texture'un X ve Y eksenini 2'nin katı olacak şekilde düzenler. Bunu kullanmanın mantıksız oldugunu düşünüyorum, zaten Unreal Engine boyut degeri 2'nin katı olmayan texture'ların da MipMap'ini oluşturuyor.

#### [Padding Color]()
Power Of Two Mode kullanırken eklenen yeni kısımlara verilecek renk.

#### [sRGB]()
Bu ayar texture'un sRGB color space'inde (renk uzayı) olup olmayacagını belirler. Bu tam olarak şu anlama geliyor, eger texture visual yani görsel bir şey ise, bu seçenek aktif olmalı. Mesela texture'u material'ınızda [Base Color](../../../Editörler/Materyal%20Editörü/Graph/Main%20Material%20Node#base-color) olarak kullanacaksanız, görsel bir amaçla kullandıgınız için sRGB seçenegi açık olmalıdır. Eger texture'u görsel degil de sayısal yani texture'un içindeki bilgileri (sayıları) almak için kullanacaksanız (mesela [Normal Map](../../../Editörler/Materyal%20Editörü/Graph/Main%20Material%20Node#normal), sayısal deger tuttugu için) sRGB kapalı olmalıdır. sRGB seçenegini açtıgınızda texture'un degerlerinde degişiklikler olur ([Gamma correction](https://en.wikipedia.org/wiki/Gamma_correction)). Bu degişiklikler visual (görsel) olarak dogru sonuçlar verir ama içinde sayı degerleri tutmayı amaçlayan texture'lar için bilginin bozulması demektir.


## [Advanced]()

#### [X-axis Tiling Method]()
[TextureCoordinate](../../../Editörler/Materyal%20Editörü/Nodlar#texturecoordinatetexcoord-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F) nodunda bu texture'u kullandıgınızda ne olacagını belirler. X ekseninde tiling (tekrarlama) yaptıgınız zaman burdaki ayara göre tiling uygulanır. Wrap, bildigimiz tekrarlama. Clamp, aslında Clamp'i tam anlayamadım, sanki en çok kullanılan rengi tiling olan kısımlar için kullanıyor gibi. Mirror, aynalama yapar, yani X ekseninde ters çevirir.

#### [Y-axis Tiling Method]()
[TextureCoordinate](../../../Editörler/Materyal%20Editörü/Nodlar#texturecoordinatetexcoord-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F) nodunda bu texture'u kullandıgınızda ne olacagını belirler. Y ekseninde tiling (tekrarlama) yaptıgınız zaman burdaki ayara göre tiling uygulanır. Wrap, bildigimiz tekrarlama. Clamp, aslında Clamp'i tam anlayamadım, sanki en çok kullanılan rengi tiling olan kısımlar için kullanıyor gibi. Mirror, aynalama yapar, yani Y ekseninde ters çevirir.

#### [Do Scale Mips for Alpha Coverage]()
#### [Alpha Coverage Thresholds]()
#### [Use New Mip Filter]()
#### [Flip Green Channel]()
Bu ayar neredeyse %99.9 Normal Map'ler üzerinde kullanılıyor, Normal Map'lerde Green Channel flip edildigi zaman, içe dogru olan kısımlar dışa dogru ve ya dışa dogru olan kısımlar içe dogru dönüyor. Bu ayarı sadece, aradıgınız Normal Map kullanımına uymayan, Green Channel'ı flip edilmesi gereken textureler için kullanırsınız.

#### [Filter]()
#### [Mip Load Options]()
#### [sRGB Use Legacy Gamma]()
#### [Source Color Settings]()

* ##### Encoding Override
* ##### Color Space

#### [Asset User Data]()



## [Adjustments]()

#### [Brightness]()
Parlaklık.

#### [Brightness Curve]()
1'den az degerler parlaklıgı arttırır, 1'den büyük degerler parlaklıgı azaltır.

#### [Vibrance]()
0'dan 1'e gittikçe, doygunluk degeri düşük olan pikselleri diger pikseller gibi doygunluk derecesine getirmek için doygunluk derecesini arttırır.

#### [Saturation]()
Renklerin doygunluk degerini arttır ve ya azaltır. 0 siyah-beyaz resim demektir. 1'in üzerine gittikçe doygunluk degeri artar.

#### [RGBCurve]()
1'den az degerler parlaklıgı arttırır, 1'den büyük degerler parlaklıgı azaltır.

#### [Hue]()
[HueShift](../../../Editörler/Materyal%20Editörü/Nodlar#hueshift-%EF%B8%8F) nodunun 360 derecelik versiyonu.

#### [Min Alpha]()
Alpha degerini "Remap" etmek için "Min" degeri, Alpha degeri verilen yeni Min ve Max degerine göre şekillenecek.

#### [Max Alpha]()
Alpha degerini "Remap" etmek için "Max" degeri, Alpha degeri verilen yeni Min ve Max degerine göre şekillenecek. Bu degeri arttırarak Alpha degerinden dolayı görünmeyen kısımları daha belirgin yapabilirsiniz, sanki doygunluk degerini ve ya parlaklık degerini arttırıyormuşsunuz gibi.

#### [Chroma Key Texture]()
Texture'a Chroma Key uygular yani verilen renkteki kısımları siler.

#### [Chroma Key Threshold]()
Texture'a Chroma Key uygulama derecesini belirtir, arttırdıkça [Chroma Key Color](#chroma-key-color) rengine yakın olan kısımları siler. 0 da kullanabilirsiniz, 0 tam o renk degerine sahip olan kısımları siler.

#### [Chroma Key Color]()
Texture'a Chroma Key uygulamak için renk degeri alır.



## [File Path]()
Dosyanın import edildigi yol ve tarih.

## [Compositing]()

#### [Composite Texture]()


## [Advanced]()

#### [Composite Texture Mode]()
#### [Composite Power]()

