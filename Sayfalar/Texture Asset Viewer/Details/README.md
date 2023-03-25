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
#### [Never Stream]()
#### [Global Force Resident Mip Levels]()



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
#### [Padding Color]()
#### [sRGB]()


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
#### [Brightness Curve]()
#### [Vibrance]()
#### [Saturation]()
#### [RGBCurve]()
#### [Hue]()
#### [Min Alpha]()
#### [Max Alpha]()
#### [Chroma Key Texture]()
#### [Chroma Key Threshold]()
#### [Chroma Key Color]()




## [File Path]()
Dosyanın import edildigi yol ve tarih.

## [Compositing]()

#### [Composite Texture]()


## [Advanced]()

#### [Composite Texture Mode]()
#### [Composite Power]()

