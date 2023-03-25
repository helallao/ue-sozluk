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
Buradan [MipMap](../../../Editörler/Materyal%20Editörü/Terimler%20Sözlügü#mipmap) için kullanılacak ayarı yapabilirsiniz. Size uygun olanı kullanmalısınız. Yanlarında sayı olan seçenekler, o ayarın ne kadar etkili oldugunu belirtiyor. Mesela "Blur1" ve "Blur5", Blur1 az blur efekti, Blur5 çok blur efekti demektir.

* ##### FromTextureGroup
Sanırım texture'nin grubuna göre, Unreal Engine tarafından tanımlanan şekilde MipMap kullanıyor.

* ##### SimpleAverage
Normal MipMap.

* ##### Sharpen
Texture'yi keskinleştirir. Piksel sayısı azaldıkça texture blurlu gibi ve anlaşılmaz olabilir. Texture'yi keskinleştirmek, texture'yi tekrar anlaşılır yapabilir.

* ##### NoMipmaps
MipMap kullanmaz.

* ##### LeaveExistingMips
Texture'nin kendi MipMap ayarlarını degiştirmez ve onları kullanır.

* ##### Blur
Blur efekti verir.

* ##### Unfiltered
SimpleAverage'e göre biraz daha blurlu, ne farkları oldugunu bilmiyorum.

* ##### Angular
Ne oldugundan emin degilim.

#### [LOD Bias]()
LOD Bias normalde 0'dır. Oluşturulan MipMap'ler 1'den başlar yani 1 ilk oluşturulan MipMap'tir ve sonra bu sayı artarak devam eder. LOD Bias orijinal texture olarak MipMap kullanmak yani maximum kaliteyi degiştirmemize yarar. Eger LOD Bias degerini 1 yaparsanız, 1 ilk oluşturulan MipMape'e denk geldigi için texture'nin en yüksek kalitesi yarıya düşer, yani orijinal texture olarak ilk MipMap'i kullanmış olursunuz. Mesela elinizde 4k bir texture varsa ve siz de bunu sanki 2k texture'muş gibi kullanmak istiyorsanız LOD Bias degerini 1 yapabilirsiniz.

#### [Texture Group]()
Buradan texture'nizin grubunu verdiginizde bir takım degişiklikler yapıyor, ne yaptıgını tam bilmiyorum.


## [Advanced]()

#### [Preserve Border]()
MipMap oluştururken texture'nin köşelerini tutar yani silinmez. Eger köşelerin silinmemesi gerekiyorsa bu seçenegi açabilirsiniz.

#### [Downscale]()
Bu ayarı sadece MipMap yoksa kullanabilirsiniz. Deger 0'ken [Texture Group'dan](#texture-group) gelen scale degerine göre texture boyutlandırılır. Deger 1'ken [Texture Group'dan](#texture-group) gelen scale degerine göre texture'yi boyutlandırmayı devre dışı bırakır yani boyutlandırmaz. Deger 1'i geçtikten sonra, arttıkça texture'niz küçülür.

#### [Downscale Options]()
"Downscale" ayarını kullanırken, texture'yi boyutlandırma işlemi esnasında uygulanacak efekti belirler, [Mip Gen Settings](#mip-gen-settings) gibi.

#### [Num Cinematic Mip Levels]()
Ne işe yaradıgını bilmiyorum.

#### [Never Stream]()
Eger bu seçenek açılırsa, oyun oynanırken (runtime) texture'lar ram'den silinmezler, yani tutulurlar.

#### [Global Force Resident Mip Levels]()
[Never Stream](#never-stream) gibi ama MipMap'ler için.



## [Compression]()

#### [Compress Without Alpha]()
#### [Editor Show Final Encode]()
#### [Editor Defer Compression]()
#### [Compression Settings]()


## [Advanced]()

#### [Maximum Texture Size]()
#### [Lossy Compression Amount]()
#### [Oodle Texture Sdk Version]()
#### [ASTC Compression Quality]()
#### [Compression Cache ID]()




## [Interchange]()

#### [AssetlmportData]()




## [Texture]()

#### [Power Of Two Mode]()
Texture'nin X ve Y eksenini 2'nin katı olacak şekilde düzenler. Bunu kullanmanın mantıksız oldugunu düşünüyorum, zaten Unreal Engine 2'nin katı olmayan texture'ların da MipMap'ini oluşturuyor.

#### [Padding Color]()
Power Of Two Mode kullanırken eklenen yeni kısımlara verilecek renk.

#### [sRGB]()
Bu ayar texture'nin sRGB color space'inde (renk uzayı) olup olmayacagını belirler. Bu tam olarak şu anlama geliyor, eger texture visual yani görsel bir şey ise, bu seçenek aktif olmalı. Mesela texture'yi materyalinizde [Base Color](../../../Editörler/Materyal%20Editörü/Graph/Main%20Material%20Node#base-color) olarak kullanacaksanız, görsel bir amaçla kullandıgınız için sRGB seçenegi açık olmalıdır. Eger texture'yi görsel degil de sayısal yani texture'nin içindeki bilgileri (sayıları) almak için kullanacaksanız (mesela [Normal Map](../../../Editörler/Materyal%20Editörü/Graph/Main%20Material%20Node#normal), sayısal deger tuttugu için) sRGB kapalı olmalıdır. sRGB seçenegini açtıgınızda texture'nin degerlerinde degişiklikler olur ([Gamma correction](https://en.wikipedia.org/wiki/Gamma_correction)). Bu degişiklikler visual (görsel) olarak dogru sonuçlar verir ama içinde sayı degerleri tutmayı amaçlayan textureler için bilginin bozulması demektir.


## [Advanced]()

#### [X-axis Tiling Method]()
#### [Y-axis Tiling Method]()
#### [Do Scale Mips for Alpha Coverage]()
#### [Alpha Coverage Thresholds]()
#### [Use New Mip Filter]()
#### [Flip Green Channel]()
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
Texture'ye Chroma Key uygular yani verilen renkteki kısımları siler.

#### [Chroma Key Threshold]()
Texture'ye Chroma Key uygulama derecesini belirtir, arttırdıkça [Chroma Key Color](#chroma-key-color) rengine yakın olan kısımları siler. 0 da kullanabilirsiniz, 0 tam o renk degerine sahip olan kısımları siler.

#### [Chroma Key Color]()
Texture'ye Chroma Key uygulamak için renk degeri alır.



## [File Path]()
Dosyanın import edildigi yol ve tarih.

## [Compositing]()

#### [Composite Texture]()


## [Advanced]()

#### [Composite Texture Mode]()
#### [Composite Power]()

