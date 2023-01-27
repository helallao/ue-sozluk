# Açıklamalar
Puanlama sistemi hakkında, her node kullanılırlıgına göre puana sahiptir, puanlar kalp sayısına göre belirlenir. Puanlar 1 - 5 arasıdır, 1 ve 2 çok kullanışsız ve (muhtemelen) kullanılmayan nodlardır ve beyaz kalp ile gösterilirler, 3 ve 5 arası kullanışlı ve kullanılan nodlardır ve renkli kalp ile gösterilirler.
<br>
<br>
Bunlardan hariç temel ve spesifik nodlar var. Temel nodlar 6 tane yanan kalp ile gösterilirler ve puanlama sisteminden muaftırlar, bu nodlar işlemler yapmamıza yarayan nodlardır yani bir yazılım dilini oluşturan ana dili gibi. Spesifik nodlar kurdeleli kalp ile gösterilirler ve puanlama sisteminden muaftırlar, bu nodlar bazı (kendine has) durumlarda kullanılan nodlardır.
<br>
<br>
<br>
1-2 Puanlar = 🤍🤍
<br>
3-5 Puanlar = ❤️💛💚💙💜
<br>
Temel Node = ❤️‍🔥❤️‍🔥❤️‍🔥❤️‍🔥❤️‍🔥❤️‍🔥
<br>
Spesifik Node = 💝
<br>
<br>


## Atomsphere

* #### [AtomsphereFogColor](https://docs.unrealengine.com/5.1/en-US/atmosphere-material-expressions-in-unreal-engine/#atmosphericfogcolor) 🤍
Kullanılmıyor. Sis ve atmosferik level efektlerini etkileyen şeyler var. Ama dedigim gibi, kullanılmıyor o yüzden ben de bilmiyorum.


## Blend

* #### [Blend_ColorBurn](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_colorburn) ❤️💛💙
Blend_ColorBurn textureyi verdigimiz blend texturesi ile yogunlaştırır ve ya birleştirir. Sonuç daha renkli ve blend rengi ile birleşmiş bir texture olur. Eger blend olarak verdigimiz texture beyaz ise bi etki olmaz çünkü Blend_ColorBurn textureyi daha koyu (yogun) yapmak içindir.

* #### [Blend_ColorDodge](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_colordodge) 💜💚❤️
Blendi 1 den çıkarıp ([1-x](#oneminus1-x)), base olarak verdigimiz textureyi blende bölüyor. Sonuç olarak daha parlak bir texture döndürür. Çok denemeler yapsam da mantıgını anlayamadım, internette de kaynak yok.

* #### [Blend_Darken](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_darken) 💚💛💙
Verdigimiz iki texturenin her pikselini karşılaştırır ve koyu (yogun) olanı seçer. (zıttı [Blend_Lighten](#blend_lighten))

* #### [Blend_Difference](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_difference) 💚💜❤️
Base textureyi blendden çıkarıp sonucun mutlak degerini alarak, sanki daldırma gibi bi efekt uygular, karıştırmak gibi ama tam degil.

* #### [Blend_Exclusion](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_exclusion) 💛💚❤️
Base ve blendi yarı saydam yapıp birbiri üzerine koyar, yani iki texture üst üste gelir.

* #### [Blend_HardLight](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_hardlight) 💚💜💙
[Blend_Overlay](#blend_overlay) ile aynıdır ama daha sert (ve ya yogun) bir sonuç verir. [Blend_LinearLight](#blend_linearlight) kadar olmasa da, bi düşük seviyesidir diyebiliriz.

* #### [Blend_Lighten](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_lighten) 💛💜❤️
Verdigimiz iki texturenin her pikselini karşılaştırır ve açık olanı seçer. (zıttı [Blend_Darken](#blend_darken))

* #### [Blend_LinearBurn](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_linearburn) 💚❤️💙
Baseyi blende ekler (toplar) ve sonuçtan bir çıkarır ([1-x](#oneminus1-x)). Ne oldugunu bilmiyorum.

* #### [Blend_LinearDodge](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_lineardodge) 💚💛❤️
Baseyi blende ekler (toplar).

* #### [Blend_LinearLight](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_linearlight) 💛❤️💙
[Blend_Overlay](#blend_overlay) ile aynıdır ama daha sert (ve ya yogun) bir sonuç verir.

* #### [Blend_Overlay](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_overlay) ❤️💚💙
Blendin her pikselini kontrol eder, eger piksel 50% griden daha açıksa Base ve Blend birleştirilir (ya da toplanıyor da olabilir). Eger piksel 50% griden daha koyuysa Base ve Blend çarpılır.

* #### [Blend_PinLight](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_pinlight) 💚💛💙
[Blend_Overlay](#blend_overlay) ile aynıdır ama kontrast degeri düşürüldügü için daha yumuşak bir sonuç verir.

* #### [Blend_Screen](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_screen) ❤️💛💙
Base ve Blend olarak verdigimiz texturelerin ikisini de [1-x](#oneminus1-x) nodundan geçirir ve sonuçları birbiriyle çarpar. Çıkan sonucu tekrar [1-x](#oneminus1-x) den geçirir ve output olarak verir. Ne oldugundan emin degilim.

* #### [Blend_SoftLight](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_softlight) ❤️💙💛
Linkteki açıklamaya göre [Blend_PinLight](#blend_pinlight) ile aynı.

* #### [Lerp_ScratchGrime](https://forums.unrealengine.com/t/lerp-scratch-grime/685309/2) 🤍🤍
Scratch/grime türkçeye çevirirsek çizik/kir demektir. Aslında bu node bir texturenin üzerine çizik ve ya kir efekti uygulamamıza yarar. Ama aslında bu çok anlamsız, yani lerp nodu ile aynı şeyi yapıyor. Tek farkları iki input alması, yani çift lerp nodu diyebiliriz.

* #### [Lerp_ScratchGrime2](https://forums.unrealengine.com/t/lerp-scratch-grime/685309/2) ❤️💚💛
[Lerp_ScratchGrime](#lerp_scratchgrime) ile aynı sayılır ama bu node, scratch olarak verdiginiz texturenin base texture ile toplanmış halini, base ile lerp eder. Yani scratch ile base lerp olmadan önce, scratch kendisine base textureyi de ekler. Grime ise, kendini texture ile çarpar. Yani scratch/grime olarak verdigimiz textureler direkmen base textureye konulmak yerine toplanarak ve çarpılarak eklenir.


## Chromakeying

* #### [DiffColorKeyerErodeSinglePass](https://youtu.be/CEUGMFLjc4Y) 🤍
Kullanışsız, renkleri silmede kullanılıyor.

* #### [MF_Chromakeyer](https://youtu.be/CEUGMFLjc4Y) 🤍
Kullanışsız, renkleri silmede kullanılıyor.


## Color

* #### [Desaturation](https://youtu.be/0pPyCZvZ05A)
0 dan bire yaklaştıkça texturenin renkleri solmaya başlar ve 1 olunca siyah beyaz olur. Aynı şekilde -1 e yaklaştıkça da texturenin renkleri daha da artar ve -1 de iki katı renkli olur. Bunu texturenizin renklerini arttırmak ve azaltmak için kullanabilirsiniz.

* #### [LinearTosRGB]()
Verilen texturenin kontrast derecesini arttırır. Mesela ateş resmi düşünün, ateşin oldugu nokta çok parlak ama uç noktalar ise daha az parlaktır. LinearTosRGB kullanırsanız az parlak noktalar daha parlak olur ve ateş daha da büyür (zıttı [sRGBToLinear](#srgbtolinear)).

* #### [Luminance]()
Verilen inputun (3 boyutlu olmalı) rengine göre parlaklık degeri döndürür. Yani insan gözüne ne kadar parlak göründügünü. Luminance Factors bölümünde hangi renklerin daha parlak oldugunu görebilirsiniz, burdaki orana göre parlaklık hesaplanıyor. Luminance Mode kısmında farklı renk uzaylarına (color space) göre ayarlanan Luminance Factors degerleri vardır. Zaten burdaki renk uzaylarının hepsinin degerleri birbirine çok yakın. Normalde parlaklık Yeşil > Kırmızı > Mavi şeklinde hesaplanıyor. Tabi isterseniz Luminance Factors bölümünden kendi istediginiz oranları verebilirsiniz, böylelikle "Custom" Luminance Mode kullanmış olursunuz. Bu nodu farklı şeylerde de kullanabilirsiniz.

* #### [sRGBToLinear]()
Verilen texturenin kontrast derecesini azaltır. Mesela ateş resmi düşünün, ateşin oldugu nokta çok parlak ama uç noktalar ise daha az parlaktır. sRGBToLinear kullanırsanız az parlak noktalar neredeyse yok olur, ateşin çok parlak oldugu kısımlar daha az parlak ve ateş daha da küçük olur (zıttı [LinearTosRGB](#lineartosrgb)).


## Constants

* #### [Constant]()
Tek bir degere sahip (1 boyutlu) degişken. İçerisinde sayı tutar. Bazı yerlerde (S) diye geçer yani skaler (scalar).

* #### [Constant2Vector]()
Constantın 2 boyutlu hali, içerisinde iki sayı tutar. Bazı yerlerde UV diye geçer.

* #### [Constant3Vector]()
Constantın 3 boyutlu hali, bu üç boyut RGB ye denk gelir. İçerisinde renk ve ya vektör tutar. Renk tutuyorsa RGB vektör tutuyorsa XYZ denir.

* #### [Constant4Vector]()
Constantın 4 boyutlu hali, bu dört boyut rgba ye denk gelir. RGB den farklı olarak içerisinde alpha (opaklık/saydamlık) degeri tutar. İsim olarak RGBA diye geçer.

* #### [ConstantDouble]()
Normal constanta göre daha dogru, daha detaylı. internete difference between float and double yazın.

* #### [DeltaTime]()
İki fps arasındaki süreyi gösterir, her fpsde deger döndürür.

* #### [DistanceCullFade](https://www.youtube.com/watch?v=E0A9JHxHNCI)
Bunu kullanabilmeniz için ilk baş dünyanıza [CullDistanceVolume](https://docs.unrealengine.com/5.1/en-US/cull-distance-volumes-in-unreal-engine/) eklemelisiniz. Ardından bu volume içinde sizin oluşturdugunuz materyale sahip meshler olacak. Ne zaman ki bir oyuncu bu volume içine girerse DistanceCullFade nodu deger döndürür ve bu degeri kullanarak oyuncu bu volume içine girdiginde yapmak istediginiz basit efektleri uygulayabilirsiniz. Mesela opaklıga DistanceCullFade baglayın ve volume içerisine giridiginiz anda içerdeki mesh görünmez iken yavaşça görünür hale gelicek.

* #### [IsOrthographic]()


* #### [ParticleColor]()


* #### [ParticleDirection]()


* #### [ParticleMotionBlurFade]()


* #### [ParticleRadius]()


* #### [ParticleRandom]()


* #### [ParticleRelativeTime]()


* #### [ParticleSize]()


* #### [ParticleSpeed]()


* #### [PerInstanceFadeAmount]()


* #### [PerInstanceRandom](https://youtu.be/_Pxwi2CAQBI)
Her instance oluşturdugunuzda bu node 0 ve 1 arasında random deger döndürür.

* #### [PrecomputedAOMask]()


* #### [Time](https://youtu.be/SMQI9_MEfRM)
Oyun başladıgı andan itibaren geçen süreyi verir. Eger editördeyseniz editörde geçen süreyi verir. Degeri görüntülemek için DebugScalarValues nodunu kullanabilirsiniz. Period parametresi ile kaç saniyede bir sıfılanacagı, daha dogrusu kaça kadar sayacagını belirleyebilirisiniz.

* #### [TwoSidedSign]()
Eger materyalinizin iki yüzlü ve iki yüzünde ayrı textureler olmasını istiyorsanız bunu kullanabilirisiniz. [Lerp (LinearInterpolate)](#linearinterpolatelerp) noduna alpha degeri olarak TwoSidedSign nodunu baglayın.

* #### [VertexColor](https://docs.unrealengine.com/5.1/en-US/constant-material-expressions-in-unreal-engine/#vertexcolor)


* #### [View Property](https://docs.unrealengine.com/5.1/en-US/constant-material-expressions-in-unreal-engine/#viewproperty)
Materyalleri sürekli degiştirebilmeniz/güncelleyebilmeniz ve işlemler yapabilmeniz için, dünya ve oyuncular hakkında bilgiler verir. Parametreleri,
<br>
<br>
<br>
Render Target Size = Ekran boyutu
<br>
<br>
Field of View = Görüş alanı
<br>
<br>
View Size = Ekran boyutu
<br>
<br>
View Position (Absolute World Space) = Konumumuzu verir (3 boyutlu vektör)
<br>
<br>
Camera Position (Absolute World Space) = Kameramızın konumunu verir (3 boyutlu vektör)
<br>
<br>
Pre-Exposure = Eye adaption, yani ışıksız ortamdan ışıklı ortama girince ve ya ışıklı ortamdan ışıksız ortama girince olan göz adatasyonu. Kısaca gerçek hayatta gözlerimiz nasıl ışıga alışıyorsa, oyun içinde de eye adaption degerini bunun sayesinde alabiliyoruz.


## Coordinates

* #### [1Dto2DIndex]()

* #### [1Dto3DIndex]()

* #### [2Dto1DIndex]()

* #### [3Dto1DIndex]()

* #### [ActorPositionWS](https://youtu.be/Kn3ZQ8TxZoE)
Aktörün pozisyonunu dünyaya göre 3d (vektör) olarak verir.

* #### [BlurSampleOffsets]()
Kullanışsız, verilen inputu 2 boyutlu vektörler ile çarpıyor.

* #### [BoundingBoxBased_0-1_UVW]()

* #### [CameraPositionWS](https://youtu.be/MRbjCXf1hmg)
Kameranın pozisyonunu dünyaya göre 3d (vektör) olarak verir.

* #### [CameraVectorToLatLongUV]()


* #### [LightmapUVs]()
Lightmap UV için texture coordinatelerini verir. X ve Y için iki boyutlu bir vektör verir. Eger Lightmap UV açık degilse 0 verir.

* #### [LocalPosition]()

* #### [LongLatToUV]()

* #### [MapARPassThroughCameraUV]()

* #### [ObjectAlignedVirtualPlaneCoordinates]()

* #### [ObjectOrientation](https://youtu.be/eDlSIm0BL6g)
Bu materyale sahip olan objenin yön bilgisini verir (3d vektör). Mesela eger X eksenine dönükse (1, 0, 0), Y eksenine dönükse (0, 1, 0), Z eksenine dönükse (0, 0, 1) verir. Bu deger aralarda da olabilir, obejenin yönüne göre.

* #### [ObjectPositionWS](https://youtu.be/P530OKEXCJo)
Bu materyale sahip olan objenin konum bilgisini verir (3d vektör).

* #### [ObjectRadius](https://youtu.be/Om3k66NY7Jc)
Bu materyale sahip olan objenin kapladıgı alanın yarıçapını verir.

* #### [Panner](https://youtu.be/24mfLY7aQFQ)
Texturelara hareket vermenize yarar.

* #### [PanTextureCoordinateChannelfrom-1ton+1]()


* #### [PanTextureCoordinateFrom-1toN+1]()


* #### [ParticlePositionWS]()


* #### [ParticleSubUVProperties]()


* #### [PixelNormalWS](https://youtu.be/gTK2EHj6ycg)
Her pikselin baktıgı yönü vektör olarak döndürür. Mesela eger bu materyale sahip meshinizin sadece yukarı bakan tarafının istediginiz renge sahip olmasını istiyorsanız bunu kullanabilirsiniz. Eger normal map kullanırsanız, egimli noktalardaki pikseller hatalara yol açabilir, bunun olmasını istemiyorsanız [VertexNormalWS](#vertexnormalws) kullanın. Linkteki videoya bakın görseller ile anlamak daha kolay.

* #### [Rotator](https://youtu.be/0wFUoN63F6I)
Textureye dönme efekti kazandırır. UV texture kordinatı döndürür (Texturelerdeki UV bölümüne baglıyorsunuz). Coordinate olarak TextureCoordinate verebilirsiniz, böylelikle tiling (tekrarlama) ayarlayabilirsiniz. Center X ve Center Y şu anlama geliyor, default olarak 0.5, 0.5 geliyor yani dönme efekti texturenin tam ortasına geliyor, ama eger (0,0) vermiş olsaydık sol üst köşeyi dönme efektinin tam orta noktası olarak alırdı. Yani Center X ve Center Y, eksenlerin kordinatını temsil ediyor, 0 derseniz o eksenin başlangıcı, 1 derseniz o eksenin sonu, dönme efekti sizin ayarladıgınız kordinatı dönme efektinin orta noktası olarak alır. Bunu en iyi deneyerek anlayabilirsiniz.

* #### [SampleSceneDepth]()


* #### [SceneTexelSize]()
The SceneTexelSize expression allows you to offset by texel sizes, as you would when using the SceneColor and SceneDepth expressions. This is useful for edge detection in multi-resolution systems, as without this calculation you would be forced to use a small static value, resulting in inconsistent results at lower resolutions.

* #### [ScreenPosition](https://youtu.be/OKIJlsOxNPI)
ScreenPosition, verdiginiz materyale sahip olan meshin, sizin ekranınızda tam olarak hangi pikseller üzerinde durdugunu verir (2 boyutlu vektör). Bunu anlatması çok zor o yüzden linkteki videoya kesin bakın. Diyelim ki bir meshe bu materyali verdiniz, ekranınızı yavaşça başka bir tarafa döndürün, ScreenPosition degeri sürekli degişecektir. X ve Y olarak iki deger verir, eger mesh ekranınızın sol kenarında ve neredeyse kaybolacaksa, Y degeri sıfıra çok yakın demektir, eger mesh ekranınızın üst kenarında ve neredeyse kaybolacaksa, X degeri sıfıra çok yakın demektir. ScreenPosition iki output döndürür ama ikisi aynı anlama gelir, ViewportUV bu degeri 0 ve 1 arasında verirken, PixelPosition bu degeri gerçek piksel sayısına göre verir.

* #### [TextureCoordinate(TexCoord)](https://youtu.be/_thf1Z3j73s)
Textureların UV (tekrarlama) degerini ayarlamamıza yarar. Tiling (tekrarlama) aynı materyali farklı boyutlardaki meshlerde de kullanacagımız zaman materyale meshin boyutuna göre bi oran vermemizi saglar. parametreleri,
<br>
<br>
<br>
UTiling = x ekseninde (yatay) takrarlama sayısı
<br>
<br>
VTiling = y ekseninde (dikey) takrarlama sayısı

* #### [UVBrickPatterns]()


* #### [UVRemap_0-1_ToRange]()


* #### [UVToLongLat]()


* #### [VertexNormalWS](https://youtu.be/sGuJxr4Bfxw)
Her kenarın baktıgı yönü vektör olarak döndürür (1 ile -1 arası, mesela x eksenine bakıyorsa 1, x ekseninin zıttına bakıyorsa -1). Mesela eger bu materyale sahip meshinizin sadece yukarı bakan tarafının istediginiz renge sahip olmasını istiyorsanız bunu kullanabilirsiniz. [PixelNormalWS](#pixelnormalws) nin aksine bu node pixel yerine vertex kullanıldıgı için normal map kullanırken hatalar oluşmaz. Linkteki videoya bakın görseller ile anlamak daha kolay.

* #### [VertexTangentWS]()


* #### [ViewSize](https://youtu.be/CLW73n19N_U)
Ekran boyutunu piksel olarak verir. 2 boyutlu vektör döndürür. Eger ekranınızı küçültürseniz bu deger de degişir.

* #### [VirtualPlaneCoordinates]()


* #### [WorldPosition](https://youtu.be/8aYe54XrZYI)
Pixellerin uzay/zaman da konumunu döndürür. Eger materyallerinizin texture kordinatlarının aynı olmasını istiyorsanız, yani aynı datayı kullanmaları, aynı konumları kullanmaları için, bunu kullanabilirsiniz. Ya da texturelerin konumlarının kameraya göre görünmesini istiyorsanız da bunu kullanabilirsiniz. Bu dediklerim anlamsız gelebilir, linkteki videoyu izleyin. Parametreleri,
<br>
<br>
<br>
Absolute World Position = Dünyaya göre konumu (materyalin) verir (3 boyutlu vektör)
<br>
<br>
Camera Relative World Position = Kameraya göre konumu (materyalin) verir (3 boyutlu vektör)

* #### [WorldSpaceAlignedScreenCoordinates]()


## Cubemaps

* #### [InteriorCubemap]()


* #### [LongLatToUV]()


* #### [UVToLongLat]()



## Custom

* #### [Custom]()
HLSL dili (High-Level Shader Language) ile yazılan kodları çalıştırmanıza yarar.

* #### [PerInstanceCustomData]()

* #### [PerInstanceCustomData3Vector]()

* #### [TangentOutput]()



## Debug

* #### [DebugBinaryValues-Float]()
Verilen constant (1 boyutlu) sayıları, [floatdan](http://www.binaryconvert.com/convert_float.html) binarye çevirilmiş halini döndürür.

* #### [DebugBinaryValues-Int]()
Verilen constant (1 boyutlu) sayıları, [integerdan](http://www.binaryconvert.com/convert_signed_int.html) binarye çevirilmiş halini döndürür.

* #### [DebugFloat2Values]()
Verilen 2 boyutlu vektörü gösteren bi texture döndürür. Eger iç içe girmiş sayılar görüyorsanız bilin ki, verilen input sadece 2 ögeden degil daha fazla ögeden, yani listeden ve ya pikseller de olabilir, daha çok ögeden oluşan bir input.

* #### [DebugFloat3Values]()
Verilen 3 boyutlu vektörü gösteren bi texture döndürür. Eger iç içe girmiş sayılar görüyorsanız bilin ki, verilen input sadece 3 ögeden degil daha fazla ögeden, yani listeden ve ya pikseller de olabilir, daha çok ögeden oluşan bir input.

* #### [DebugFloat4Values]()
Verilen 4 boyutlu vektörü gösteren bi texture döndürür. Eger iç içe girmiş sayılar görüyorsanız bilin ki, verilen input sadece 4 ögeden degil daha fazla ögeden, yani listeden ve ya pikseller de olabilir, daha çok ögeden oluşan bir input.

* #### [DebugOnOff]()
1 saniye içerisinde, 1 saniyenin yarısı 0 yarısı 1 olacak şekilde, sürekli 1 ve 0 arasında output döndürür. Kullanmayın bile.


* #### [DebugScalarValues]()
Verilen sayıyı (constant) gösteren bi texture döndürür. Eger iç içe girmiş sayılar görüyorsanız bilin ki, verilen input sadece 1 ögeden degil daha fazla ögeden, yani listeden ve ya pikseller de olabilir, daha çok ögeden oluşan bir input.

* #### [DebugTimeSine]()
Sürekli 0 ve 1 arasında döner. 1 ve 0 civarında iken birazcık yavaşlar, smooth (yumuşak) bi geçiş olur, o da sinüs degeri alındıgından dolayı (fonksiyonda).


## Decals

* #### [ApplyDBuffer]()


* #### [DBufferTexture]()


* #### [StaticMeshDecal_Function]()



## Density

* #### [BeersLaw]()


* #### [RayMarchHeightMap]()



## Depth

* #### [DepthFade](https://youtu.be/2BxrGjPcirk)
Saydam meshler opak olanlar ile kesiştiginde ne olacagını ayarlayabilirsiniz. Parametreleri,
<br>
<br>
<br>
Opacity = Opaklık, sıfırdan (saydam) başlar, arttırdıkça opak olur.
<br>
<br>
FadeDistance = Saydamlık efektinin ne kadar uzaga kadar etkili olacagı, bunu 0 yapmayın çünkü 0 yapınca hareket ederken renkler sürekli birbirine giriyor. En az 0.1 yapın.

* #### [DepthFromWorldPosition]()
(Bu materyali kullanırken, output degerini 2000 gibi bi sayıya falan bölün yoksa döndürdügü deger yüksek oldugu için işlem yapamayız) [PixelDepth](#pixeldepth) nodu ile aynı işlevi görür ama bu node size PixelDepth degerini istediginiz konumdan verir. Mesela siz PixelDepth degeri üzerinde oynamak istiyorsunuz, diyelim ki konumunuzun x ekseninde -100 azalmasını istiyorsunuz, o zaman [WorldPosition](#worldposition) kullanıp konumunuzu aldıktan sonra bunu [subtract](#subtract) nodundan geçirip istediginiz konum degerini aldıktan sonra, bu konum degerine göre PixelDepth degerini DepthFromWorldPosition kullanarak elde edebilirsiniz.

* #### [PixelDepth](https://youtu.be/AHOidP7olg0)
(Bu materyali kullanırken, output degerini 2000 gibi bi sayıya falan bölün yoksa döndürdügü deger yüksek oldugu için işlem yapamayız) Bu materyale sahip meshin, ekranınızın ortasına olan uzaklıgı ve cameranızın meshe olan uzaklıgını verir. Yanlış anlaşılmasın iki output vermiyor, bu ikisine baglı olarak ekranınızda görünen piksellerin size ve ekranınızın ortasına olan uzaklıgını veriyor. Ben baya denemeler yaptım ve çıkardıgım sonuca göre şu şekilde düşünmeniz yeterli; bu node tam olarak piksellerin ekranınızda ne kadar yer kapladıgı (yakındayken büyük uzaktayken küçük) ve ya bu piksellerin ne kadar kaliteli oldugunu veriyor ve bunu yaparken de sizin meshe olan uzaklıgınız ve kamera açınızı baz alıyor. Bu node sadece materyalin yüzeyine etki eder, yani arka tarafı göstermez. Arka tarafı gösteren node [SceneDepthe](#scenedepth) de bakabilirsiniz. Daha iyi anlamak için linkteki videoya bakın.

* #### [SceneDepth](https://youtu.be/ABv7abxTMoM)
(Bu materyali kullanırken, output degerini 2000 gibi bi sayıya falan bölün yoksa döndürdügü deger yüksek oldugu için işlem yapamayız) [PixelDepthin](#pixeldepth) aksine sadece yüzeyi degil, arka tarafları da gösterir. Sadece saydam materyallerde işe yarar. Bu materyale sahip meshe yaklaştıkça arka taraftaki objeler görünür olmaya başlar ve arka tarafta kalan objeler uzaklıgına göre deger döndürür. Bu degerleri kullanarak işlemler yapabiliriz. Linkteki videoya bakın. Ayrıca son olarak, SceneDepth kullanırken bölme sayısını (en başta yazan) kendinize göre ayarlayın, 2000 istediginiz detayları tam vermeyebilir, bazen 1000, bazen 2000 iyi olabilir, test edip istediginiz degeri bulabilirsiniz.


## Distance Fields

* #### [DistanceField_Capsule]()


* #### [DistanceField_Cylinder]()


* #### [DistanceField_Intersection]()


* #### [DistanceField_Sphere]()


* #### [DistanceField_Subtract]()


* #### [DistanceField_Union]()


* #### [RayTraceSphereFalloff]()


## Distance Fields Rendering

* #### [DistanceFieldsRenderingSwitch]()


## Foliage

* #### [PixelDepthOffset_Foliage]()



## Font

* #### [FontSample]()
The FontSample expression allows you to sample the texture pages out of a font resource as regular 2D textures. The alpha channel of the font will contain the font outline value. Only valid font pages are allowed to be specified.

* #### [FontSampleParameter]()
The FontSampleParameter expression provides a way to expose a font-based parameter in a material instance constant, making it easy to use different fonts in different instances. The alpha channel of the font will contain the font outline value. Only valid font pages are allowed to be specified.


## Functions

* #### [FunctionInput]()
(Bu node sadece materyal fonksiyonlarında kullanılabilir)

* #### [FunctionOutput]()
(Bu node sadece materyal fonksiyonlarında kullanılabilir)

* #### [MaterialFunctionCall]()
Bu node ile kendi yazdıgınız materyal fonksiyonlarını çagırabilirsiniz. Materyal fonksiyonlarına iki kere tıklarsanız o fonksiyonun içerigini yeni sayfada açar. Materyal fonksiyonları ile ilgili bilmeniz gereken diger nodlar: [FunctionInput](#functioninput), [FunctionOutput](#functionoutput)

* #### [PreviousFrameSwitch]()


* #### [StaticBool]()
True ve ya False degeri tutar. [StaticSwitch](#staticswitch) kullanarak aynı [if](#if) gibi koşul koyabilirsiniz. Bu node parametreye çevrilemiyor, çevirmek isterseniz [StaticBoolParameter](#staticboolparameter) kullanmalısınız.

* #### [StaticSwitch]()
[If](#if) ile aynı işlevi görür ama input olarak [bool](#staticbool) degeri alır.

* #### [TextureObject]()
The TextureObject expression is used to provide a default texture for a texture function input within a function. This node does not actually sample the texture, so it must be used in conjunction with a TextureSample node.


## Get Post Process Setting

* #### [GetAmbientCuvemapIntensity]()


* #### [GetAmbientCuvemapTint]()



## Gradient

* #### [DiamondGradient](https://youtu.be/TzeOSKSsVVA)
Yıldız şeklinde bi texture döndürüyor, büyüklügünü falan ayarlıyorsunuz. Kullanmayın bile.

* #### [GetGradientMapRow]()


* #### [GradientMap_Multi]()


* #### [GradientMap_Multi_TexObjSamplerType]()


* #### [LinearGradient](https://youtu.be/g7UreR23luA)
İnput olarak texturecoordinate verin. Verdiginiz deger sıfıra yaklaştıkça U kanalı (X) için soldan saga, V kanalı (Y) için yukarıdan aşagıya siyah efekt uygular, yani kenarlarda siyah bölümler oluşturur. Output olarak gelen U ve V kanallarını kullanıp, mesela bi textureden gelen rgb degerini U degeriyle çarparak, resminizin kenarlarına siyahlık ekleyebilirsiniz. Ayrıca linkteki videoya bakın, görseller ile anlamak daha kolay.

* #### [RadialGradientExponential](https://youtu.be/0xNFriRv-Bc)
LinearGradient gibi ama bu daire şeklinde beyazlık oluşturuyor. İnput olarak texturecoordinate verin. UVs degerini degiştirmek bu node için tekrarlama degil küçültme anlamına geliyor, yani [şurdaki](https://youtu.be/0xNFriRv-Bc?t=355) gibi. Center Position şu anlama geliyor, default olarak 0.5, 0.5 geliyor dairenin orta noktası texturenin tam ortasına geliyor, ama eger (0,0) vermiş olsaydık sol üst köşeyi orta noktası olarak alırdı. Yani Center X ve Center Y, eksenlerin kordinatını temsil ediyor, 0 derseniz o eksenin başlangıcı, 1 derseniz o eksenin sonu, daire sizin ayarladıgınız kordinatı orta noktası olarak alır. Radius dairenin çapı, büyüklügü yani. Density beyazlık şiddeti. İnvert density, açık degilken density degeri beyazlıgın şiddetinin temsil eder ve ortadan dışarıya dogrudur, açıkken density degeri beyazlıgın degil beyazlıgın çevresindeki siyahlıgın şiddetinin temsil eder ve dışarıdan ortaya dogrudur. Linkteki videoyu izleyin, görseller ile anlamak daha kolay.

* #### [SmoothCurve]()
The SmoothCurve function takes in an existing texture channel or gradient and uses a procedural curve to control the transition from dark to light. The user can adjust the tangents of this curve to change the result.

* #### [ValueStep](https://youtu.be/ovelaLbCNjw)
The ValueStep function takes in an existing texture channel or gradient and outputs a pure black and white image based on inputs from the user. The result is a mask that represents what portion of the gradient equals the value of the inputs.


## Hair Attributes

* #### [Hair Attributes]()



## Hair Color

* #### [Hair Color]()



## Image Adjustment

* #### [3ColorBlend]()
The 3ColorBlend function blends between 3 input colors based on a grayscale alpha, in the following manner:

* #### [3PointLevels]()
The 3PointLevels function takes in an image and remaps the values of each channel across 3 points (white, black, middle). This is similar to applying a Levels adjustment in Photoshop. However, unlike the CheapContrast functions, this function provides full control in that it gives the user ability to adjust interpolation of lights, darks, and grays (gamma). By default, the three remapping points are interpolated linearly. However, you may input your own custom interpolation curve if you wish.

* #### [CheapContrast]()
The CheapContrast function boosts the contrast of an input by remapping the high end of the histogram to a lower value, and the low end of the histogram to a higher one. This is similar to applying a Levels adjustment in Photoshop, and pulling the black and white flags in a bit. The user may control the degree to which the contrast is boosted.

* #### [CheapContrast_RGB]()
The CheapConstrast_RGB function boosts the contrast of an input by remapping the high end of the histogram to a lower value, and the low end of the histogram to a higher one. This is similar to applying a Levels adjustment in Photoshop, and pulling the black and white flags in a bit. The user may control the degree to which the contrast is boosted.Unlike the regular CheapContrast function, this function can take in a Vector3 as the input, allowing it to perform contrast operations on a color image.

* #### [Contrast_Preserve_Color]()


* #### [DeriveHDRfromLDR]()


* #### [HighPassFunction]()


* #### [HighPassTexture]()


* #### [HsvToRgb]()


* #### [HueShift]()
Bu node Texture inputuna verilen texture ve ya renk degerini Percentage inputuna verilen degere göre renk paletinde saat yönünde ileri alır. Percentage degeri 0 ve 1 arasında olmalı çünkü 1 tam bir tur demektir. Mesela 0.5 verirseniz rengimiz renk paletinde karşı tarafa geçer, yarım tur atar. Mesela rengimiz aşagıdaki gibi ise 0.5 HueShift uyguladıgımızda rengimiz açık mavi olan kısma gelecektir.

<img width="150" src="../../Dosyalar/HueShift_Palet.jpg">


* #### [Luminosity_And_Color]()


* #### [RaiseBlackLevelsByPercentage]()


* #### [SCurve]()
The SCurve function boosts contrast of an image by interpolating the values of each channel values of an image along an S-curve. This is similar to applying a Curves adjustment in Photoshop and setting the RGB curve to an S-curve or using the Increase Contrast (RGB) preset.

* #### [RgbToHsv]()


* #### [SCurve]()


* #### [SmoothThreshold]()
The SmoothThreshold function takes in a gradient, an interpolation rate, and a threshold value (Cutoff Value). It then applies a smooth contrast to the gradient, based on the inputs. Here is a breakdown of what each input does:

* #### [UnSharpMaskFunction]()


* #### [UnSharpMaskTexture]()



## Landscape

* #### [Landscape_Manual_UVW]()


* #### [LandscapeGrassOutput]()


* #### [LandscapeLayerBlend]()
Although any random Material can be used with a Landscape Actor, the Material system inside Unreal Engine 4 (UE4) provides some Landscape-specific material nodes that can help improve the textures for your Landscape. In this document, we explain how these material nodes function, and how you can use them in your Landscape materials.

* #### [LandscapeLayerCoords]()
Although any random Material can be used with a Landscape Actor, the Material system inside Unreal Engine 4 (UE4) provides some Landscape-specific material nodes that can help improve the textures for your Landscape. In this document, we explain how these material nodes function, and how you can use them in your Landscape materials.

* #### [LandscapeLayerSample]()


* #### [LandscapeLayerSwitch]()
Although any random Material can be used with a Landscape Actor, the Material system inside Unreal Engine 4 (UE4) provides some Landscape-specific material nodes that can help improve the textures for your Landscape. In this document, we explain how these material nodes function, and how you can use them in your Landscape materials.

* #### [LandscapeLayerWeight]()
Although any random Material can be used with a Landscape Actor, the Material system inside Unreal Engine 4 (UE4) provides some Landscape-specific material nodes that can help improve the textures for your Landscape. In this document, we explain how these material nodes function, and how you can use them in your Landscape materials.

* #### [LandscapePhysicalMaterialOut]()


* #### [LandscapeVisibilityMask]()
Although any random Material can be used with a Landscape Actor, the Material system inside Unreal Engine 4 (UE4) provides some Landscape-specific material nodes that can help improve the textures for your Landscape. In this document, we explain how these material nodes function, and how you can use them in your Landscape materials.

* #### [Landscape_Manual_UVW]()



## Lighting

* #### [GGXSpecular]()


* #### [PixelDepthOffset_Foliage]()


## Masks

* #### [ThresholdWithRange]()


## Material Attributes

* #### [BlendMaterialAttributes]()


* #### [BreakMaterialAttributes]()
The Break Material Attributes expression is ideal when using a Layered Material - a feature of the Material Functions system. When using a Material Layer Function within a Material, you may want to use only one aspect of the layer. For example, you may have a Material Layer that defines a nice looking generic Material, such as steel. You may want to use only the Roughness and Base Color attributes from that layer in your final Material, rather than using the whole thing. In such cases, you can use a Break Material Attributes node to split up all of the incoming attributes of the Material Layer, and then just plug in the ones you want. This also allows for complex blending of various Material Attributes.

* #### [GetMaterialAttributes]()


* #### [MakeMaterialAttributes]()
The Make Material Attributes node does exactly the opposite of the Break Material Attributes node. Instead of splitting attributes apart, this brings them together. This is useful when creating your own Material Layer functions, as you will have access to all of the standard attributes for your output. This can also be used for complex Material setups in which you want to define more than one type of Material and blend them together, all within one Material.

* #### [MaterialAttributeLayers]()


* #### [SetMaterialAttributes]()



## MaterialLayerBlend

* #### [MaterialLayerBlend_AddWorldPositionOffset]()


* #### [MaterialLayerBlend_AO]()


* #### [MaterialLayerBlend_BakedNormal]()


* #### [MaterialLayerBlend_BakedNormal_SimpleAdd]()


* #### [MaterialLayerBlend_BlendAngleCorrectedNormals]()


* #### [MaterialLayerBlend_BreakBaseColor]()


* #### [MaterialLayerBlend_BreakNormal]()


* #### [MaterialLayerBlend_Decal]()


* #### [MaterialLayerBlend_Decal_UV3]()


* #### [MaterialLayerBlend_Emissive]()


* #### [MaterialLayerBlend_LightmassReplace]()


* #### [MaterialLayerBlend_ModulateRoughness]()


* #### [MaterialLayerBlend_ModulateSpecular]()


* #### [MaterialLayerBlend_Multiply]()


* #### [MaterialLayerBlend_MultiplyBaseColor]()


* #### [MaterialLayerBlend_NormalBlend]()


* #### [MaterialLayerBlend_NormalFlattern]()


* #### [MaterialLayerBlend_OverrideBaseColor]()


* #### [MaterialLayerBlend_OverrideDisplacement]()


* #### [MaterialLayerBlend_OverrideMetalness]()


* #### [MaterialLayerBlend_OverrideOpacity]()


* #### [MaterialLayerBlend_OverrideOpacityMask]()


* #### [MaterialLayerBlend_OverrideSubSurface]()


* #### [MaterialLayerBlend_OverrideWorldPositionOffset]()


* #### [MaterialLayerBlend_ReplaceNormals]()


* #### [MaterialLayerBlend_RoughnessOverride]()


* #### [MaterialLayerBlend_SeparateNormalandColorClamps]()


* #### [MaterialLayerBlend_Simple]()


* #### [MaterialLayerBlend_Stain]()


* #### [MaterialLayerBlend_Standard]()


* #### [MaterialLayerBlend_StandardWithDisplacement]()


* #### [MaterialLayerBlend_StandardWithMaskEdgeTint]()


* #### [MaterialLayerBlend_TenLayerBlend]()


* #### [MaterialLayerBlend_Tint]()


* #### [MaterialLayerBlend_TintAllChannels]()


* #### [MaterialLayerBlend_TopNormal]()



## Math

* #### [2dArrayLookupByIndex]()


* #### [Abs](https://youtu.be/yh59nFJrxKM)
Mutlak deger.

* #### [Add](https://youtu.be/gvlPC1nH3Mo)
Toplama.

* #### [AddComponents]()
Verdiginiz vektörden (2, 3, 4) her boyutundaki sayıları toplar. mesela (30, 50, 200) şeklinde 3 boyutlu bi vektör verdiniz, sonuç olarak 30 + 50 + 200 = 280 alırsınız.

* #### [AngleBetweenVectors]()


* #### [Append3Vector]()
AppendVector(Append) için geçerli olan kurallar bunda da geçerlidir. Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür.

* #### [Append4Vector]()
AppendVector(Append) için geçerli olan kurallar bunda da geçerlidir. Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür.

* #### [AppendVector(Append)](https://youtu.be/pFkth9GKci4)
Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür. En fazla 4 boyutlu vektör yapılabilir, eger 3 + 2 gibi bir işlem yaparsanız hata verecektir, ama 3 + 1 yaparsanız sanki birinci inputa alpha degeri ekliyormuşsunuz gibi toplar ve 4 boyutlu vektör döndürür.

* #### [Arccosine]()
The Arccosine expression outputs the inverse cosine function.

* #### [ArccosineFast]()
The ArccosineFast expression outputs an approximation of the inverse cosine function that is faster to calculate than the more accurate Arccosine expression. Input must be between -1 and 1.

* #### [Arcsine]()
The Arcsine expression outputs the inverse sine function.

* #### [ArcsineFast]()
The ArcsineFast expression outputs an approximation of the inverse sine function that is faster to calculate than the more accurate Arcsine expression. Input must be between -1 and 1.

* #### [Arctangent]()
The Arctangent expression outputs the inverse tangent function.

* #### [Arctangent2]()
The Arctangent2 expression outputs the inverse tangent of x / y where input signs are used to determine quadrant.

* #### [Arctangent2Fast]()
The Arctangent2Fast expression outputs an approximation of the inverse tangent of X / Y where input signs are used to determine quadrant. It is faster to calculate but less accurate than the Arctangent2 expression.

* #### [ArctangentFast]()
The ArctangentFast expression outputs an approximation of the inverse tangent function that is faster to calculate than the more accurate Arctangent expression.

* #### [ArrangePointsEvenlyAroundABox]()


* #### [Ceil](https://youtu.be/UIXOPWJVHDE)
Verdiginiz sayıyı en yakın küçük tamsayıya yuvarlar (zıttı Floor). örnegin 
9.9 -> 9
9.1 -> 9

* #### [Clamp](https://youtu.be/KqMpPxVjGWY)
Verdigimiz inputu min ve max degerine göre düzenler. Eger input min degerinden küçükse min degerine, input max degerinden büyükse max degerine taşınır. Modları,
<br>
<br>
<br>
Clamp = min ve max çalışır.
<br>
<br>
Clamp Min = sadece min çalışır, input max degerinden büyük olsa bile max çalışmaz.
<br>
<br>
Clamp Max = sadece max çalışır, input min degerinden küçük olsa bile min çalışmaz.

* #### [ComponentMask(Mask)]()
İnput olarak verdigimiz vektörden (1 boyuttan fazla), istedigimiz kanalı alabilmemizi saglar.

* #### [Cosine](https://youtu.be/gn5Zbsq8eFs)
Cosine yani kosinüs, sürekli 1 ve 0 arasında dönen bi dalga. Kendini tekrar eder, çogu durumda kullanışlıdır. İnput olarak time nodunu baglayabilirsiniz, böylelikle sürekli tekrarlayan bi deger döndürür. Linkteki videoda görseller ile anlatılmış kesin izleyin. (Bkz. Sine)

* #### [CreateThirdOrthogonalVector]()


* #### [CrossProduct](https://youtu.be/KWtRiKbNS24)
The CrossProduct expression computes the cross product of two three-channel vector value inputs and outputs the resulting three-channel vector value. Given two vectors in space, the cross product is a vector that is perpendicular to both of the inputs.

* #### [CylinderIntersection]()


* #### [DegreesToRadians]()


* #### [DeriveNormalZ_Function]()


* #### [Divide](https://youtu.be/ibGKUNCM8e8)
Bölme.

* #### [DotProduct](https://youtu.be/sf3jT12pN6o)
The DotProduct expression computes the dot product, which can be described as the length of one vector projected onto the other, or as the cosine between the two vectors multiplied by their magnitudes. This calculation is used by many techniques for computing falloff. DotProduct requires both vector inputs to have the same number of channels.

* #### [Exponential]()


* #### [FindSaturation]()


* #### [Floor](https://youtu.be/UIXOPWJVHDE)
Verdiginiz sayıyı en yakın büyük tamsayıya yuvarlar (zıttı Ceil). örnegin 
9.9 -> 10
9.1 -> 10

* #### [Fmod](https://youtu.be/J57rNg3YwaA)
Verilen A sayısını (constant) B sayısına (constant) böler ve kalanı verir. örn,
<br>
<br>
30 / 20 = 10
<br>
7 / 3 = 1

* #### [Frac](https://youtu.be/PQnXWXsUWTg)
Verilen inputun kesirli yani . (nokta) dan sonraki kısmını verir. örnegin,
<br>
<br>
1.5 = 0.5
<br>
2.0 = 0
<br>
0.99 = 0.99

* #### [If](https://youtu.be/iRACLJlm9UQ)
Duruma/koşula göre yapılacak işlemi seçmemize yarar. İki input alıyor A ve B. Üç seçenek sunuyor,
<br>
<br>
A > B
<br>
A == B
<br>
A < B
<br>
<br>
Diyelim ki A = 100 ve B = 10. A B den büyük oldugu için sonuç A > B seçenegine verdigimiz şey olacaktır. Eger A ve B birbirine eşit olsa A == B seçenegine verdigimiz şey sonuç olarak döndürülecekti. Eger A B den küçük olsa A < B seçenegine verdigimiz şey sonuç olarak döndürülecekti. Yani verdigimiz koşula göre hangi işlemin yapılması gerektigini belirliyoruz.

* #### [InverseLinearInterpolate]()


* #### [InverseTransformMatrix]()


* #### [LinearInterpolate(Lerp)](https://youtu.be/fckeT6GyvPc)
Verilen alpha degerine göre iki inputu (resim ve ya renk) birbirine karıştırır. İstedigimiz boyutta constant verebiliriz, hem alpha hem de inputlarımız için. Örnegin bir boyutlu constant yani sayı kullanalım, A ve B için iki sayı girin mesela 10 ve 0. Eger alpha degerine 0 verirseniz A, 1 verirseniz B degeri döndürülür. Eger alpha degerine 0.5 verirseniz sayımız da A ve B nin ortası yani 5 olur. Yani 0 a yaklaştıkça A, 1 e yaklaştıkça B. Ayrıca dedigim gibi, istediginiz boyutta input ve alpha verebilirsiniz. Mesela A ve B için iki tane renk (rgb yani 3 boyutlu) verelim. Alpha degeri olarak da 3 boyutlu bi vektör verelim. Alphanın içindeki her kanalı degiştirdiginizde A ve B için de geçerli olan alpha degeri degişir. Mesela r (red) degiştirirseniz A ve B nin r kanalı için alpha degerini belirlemiş olursunuz ama sadece r kanalı için, diger iki kanalı da yine Alphanın içindeki kanallardan degiştirmeniz gerek.

* #### [LinearSine]()
The LinearSine function takes in a scalar value and outputs the linear sine (or rounded linear sine) of that value, running between 0 and 1. If you connect a Time expression to the value input and use the Linear Sine, you can see animation in the output that coincides with a linear sine wave.

* #### [LineIntervalIntersection]()


* #### [Logarithm]()


* #### [Logarithm10]()
The Logarithm10 node returns the base-10 logarithm, also called the common logarithm, of the input value. That is, if you take a base value of 10 and raise it to the power of the number returned by this expression, you would get the input value.

* #### [Logarithm2]()
The Logarithm2 node returns the base-2 logarithm of the input value. That is, if you take a base value of 2 and raise it to the power of the number returned by this expression, you would get the input value.

* #### [MakeVectorsOrthogonal]()


* #### [Max](https://youtu.be/g0C_kXxiwSU)
Verilen iki inputtan büyük olanı döndürür. Vektör verirseniz her boyutun, texture verirseniz her pikselin büyük olanını döndürür.

* #### [Min](https://youtu.be/g0C_kXxiwSU)
Verilen iki inputtan küçük olanı döndürür. Vektör verirseniz her boyutun, texture verirseniz her pikselin büyük olanını döndürür.

* #### [Multiply](https://youtu.be/Ge96lim4t8A)
Çarpma.

* #### [MultiplyAdd]()


* #### [Normalize]()
The Normalize expression calculates and outputs the normalized value of its input. Normalized vectors (also called "unit vectors") have an overall length of 1.0. This means each component of the input is divided by the total magnitude (length) of the vector.

* #### [OneMinus(1-x)](https://youtu.be/bS6WWlAVj9o)
Verilen inputun 1 den çıkarılmış halini döndürür. Aslında bu node 0 ve 1 arasındaki herşeyi karşıya geçirir, yani flip yapar. Mesela aşagıdaki örneklerde 0a yakın olan degerler artık 1e, 1e yakın olan degerler artık 0a yakın. Bakın,
<br>
<br>
1 için 1 - 1 = 0, yani 1 olan deger 0 oldu
<br>
0 için 1 - 0 = 1, yani 0 olan deger 1 oldu
<br>
0.3 için 1 - 0.3 = 0.7, yani 0.3 olan deger 0.7 oldu

* #### [Pi]()
Pi.

* #### [Power](https://youtu.be/zR7ZjwpNV5c)
Verilen inputun (sayı) kuvvetini alır.

* #### [ProjectVectorOntoPlane]()


* #### [QuadraticFormula]()


* #### [RadiansToDegrees]()


* #### [RayTracedSphere]()


* #### [Remap]()
Verdigimiz inputtaki belirli bir aralıgı (range) başka bi aralıga almamızı saglar (acaba :D). İnput Low ve High arasındaki sayıların hepsi Target Low ve High arasına taşınır ama DİKKAT bu işlem random degil yani bi orana göre gidiyor, mesela verdiginiz İnput, İnput Low ve High ın tam ortasında ise o zaman output da Target Low ve High ın da tam ortasında olacaktır. Ayrıca verdiginiz İnput, İnput Low ve High dışında olsa bile bu node herşeyi orana göre degiştirecektir. Yani mesela İnputunuz İnput High dan daha yüksek, verdiginiz İnput orana göre düzenlenecek ve output yine bu orana göre olacaktır. Eger İnput Low ve High arasında bi remap yapmak istiyorsanız if kullanıp düzenleme yaparak küçük ve büyük degerleri remap dışına alabilirsiniz.


* #### [RemapValueRange](https://youtu.be/V0by6a5Xesk)
Verdigimiz inputtaki belirli bir aralıgı (range) başka bi aralıga almamızı saglar (acaba :D). İnput Low ve High arasındaki sayıların hepsi Target Low ve High arasına taşınır ama DİKKAT bu işlem random degil yani bi orana göre gidiyor, mesela verdiginiz İnput, İnput Low ve High ın tam ortasında ise o zaman output da Target Low ve High ın da tam ortasında olacaktır. Ayrıca verdiginiz İnput, İnput Low ve High dışında olsa bile bu node herşeyi orana göre degiştirecektir. Yani mesela İnputunuz İnput High dan daha yüksek, verdiginiz İnput orana göre düzenlenecek ve output yine bu orana göre olacaktır. Ayrıca bu node fonksiyon oldugu için inputlara illaki bişeler baglamanız gerekiyo, node üzerinden veremiyorsunuz, bu da kodları çok karıştırıyo. Bu yüzden "Remap" isimli diger nodu kullanın, o da bununla aynı işi yapıyor. Ayrıca son bi tavsiye, eger İnput Low ve High arasında bi remap yapmak istiyorsanız if kullanıp düzenleme yaparak küçük ve büyük degerleri remap dışına alabilirsiniz.


* #### [RemapValueRangeNormalized]()
Sıfır ve bir arasında clamp yapar. Clamp(0, 1) ile eşit yani. Kullanmayın bile.


* #### [RGBtoHSV]()


* #### [Round]()
Verilen inputu (sayı) yuvarlar.


* #### [Round]()
Evet enayi unreal engine aynı nodun fonksiyon halini de yapmışlar.


* #### [SafeNormalize]()


* #### [Saturate]()
Sıfır ve bir arasında clamp yapar. Clamp(0, 1) ile eşit yani. Kullanmayın bile.

* #### [Sign]()
The Sign node indicates whether a numeric input is negative, positive, or exactly 0.

* #### [Sine](https://youtu.be/gn5Zbsq8eFs)
Sine yani sinüs, sürekli 1 ve 0 arasında dönen bi dalga. Kendini tekrar eder, çogu durumda kullanışlıdır. İnput olarak time nodunu baglayabilirsiniz, böylelikle sürekli tekrarlayan bi deger döndürür. Linkteki videoda görseller ile anlatılmış kesin izleyin. (Bkz. Cosine)

* #### [Sine_Remapped]()


* #### [SmoothCeil]()


* #### [SmoothStep]()


* #### [SquareRoot(sqrt)](https://youtu.be/HnQZ9acKWiI)
Verilen inputun karekökünü döndürür. Eger vektör verirseniz her degerinin karekökü ayrı ayrı alınır.

* #### [Step]()


* #### [Subtract](https://youtu.be/zvNvjzupOn8)
Çıkarma.

* #### [SumOfAConsecutiveNumberSequence]()


* #### [Tangent]()
The Tangent node outputs the tangent of the specified value.

* #### [Transform3x3Matrix]()


* #### [TransformToClipSpace]()


* #### [Truncate]()
The Truncate node truncates a value by discarding the fractional part while leaving the whole number untouched.

* #### [UnpackNormalFromFloat]()


* #### [VectorToRadialValue](https://youtu.be/pVhnvs_lScE)
The VectorToRadialValue function transforms the vector of a Vector2 into an angle, or transforms UV coordinate data into radial coordinates. In the case of a vector, the angle will output in one channel and the length of the vector in the other.


## MAXScripts

* #### [MS_MultiNormal_UVnormals]()


* #### [MS_MultiNormal_VertexColorNormals]()


* #### [MS_SequencePainter_Sequence]()


* #### [MS_SequencePainter_SequenceFlipbook]()


* #### [MS_VertexAnimationTools_MorphTargets]()


* #### [ms_StaticMeshSkeletalAnimation]()


* #### [ms_StaticMeshSkeletalAnimationHighQuality]()



## Misc

* #### [3ColorBlend]()


* #### [3dParticleOpacity]()


* #### [3DSandMayaUVCoordinates]()


* #### [3PointLevels]()


* #### [AbberatedBlur-Texture]()


* #### [AddComponents]()


* #### [AlignFacingParticlesByVelocity-2D]()


* #### [AlignMeshToTheCamera]()


* #### [AlphaOffset]()


* #### [AppendMany]()


* #### [AttachMeshToTheCamera]()


* #### [BakedDisplacement]()


* #### [BellCurve]()


* #### [BitMask]()


* #### [Blend_ColorBurn](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_colorburn)
Blend_ColorBurn textureyi verdigimiz blend texturesi ile yogunlaştırır ve ya birleştirir. Sonuç daha renkli ve blend rengi ile birleşmiş bir texture olur. Eger blend olarak verdigimiz texture beyaz ise bi etki olmaz çünkü Blend_ColorBurn textureyi daha koyu (yogun) yapmak içindir.

* #### [Blend_ColorDodge](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_colordodge)
Blendi 1 den çıkarıp ([1-x](#oneminus1-x)), base olarak verdigimiz textureyi blende bölüyor. Sonuç olarak daha parlak bir texture döndürür. Çok denemeler yapsam da mantıgını anlayamadım, internette de kaynak yok.

* #### [Blend_Darken](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_darken)
Verdigimiz iki texturenin her pikselini karşılaştırır ve koyu (yogun) olanı seçer. (zıttı [Blend_Lighten](#blend_lighten))

* #### [Blend_Difference](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_difference)
Base textureyi blendden çıkarıp sonucun mutlak degerini alarak, sanki daldırma gibi bi efekt uygular, karıştırmak gibi ama tam degil.

* #### [Blend_Exclusion](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_exclusion)
Base ve blendi yarı saydam yapıp birbiri üzerine koyar, yani iki texture üst üste gelir.

* #### [Blend_HardLight](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_hardlight)
[Blend_Overlay](#blend_overlay) ile aynıdır ama daha sert (ve ya yogun) bir sonuç verir. [Blend_LinearLight](#blend_linearlight) kadar olmasa da, bi düşük seviyesidir diyebiliriz.

* #### [Blend_Lighten](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_lighten)
Verdigimiz iki texturenin her pikselini karşılaştırır ve açık olanı seçer. (zıttı [Blend_Darken](#blend_darken))

* #### [Blend_LinearBurn](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_linearburn)
Baseyi blende ekler (toplar) ve sonuçtan bir çıkarır ([1-x](#oneminus1-x)). Ne oldugunu bilmiyorum.

* #### [Blend_LinearDodge](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_lineardodge)
Baseyi blende ekler (toplar).

* #### [Blend_LinearLight](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_linearlight)
[Blend_Overlay](#blend_overlay) ile aynıdır ama daha sert (ve ya yogun) bir sonuç verir.

* #### [Blend_Overlay](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_overlay)
Blendin her pikselini kontrol eder, eger piksel 50% griden daha açıksa Base ve Blend birleştirilir (ya da toplanıyor da olabilir). Eger piksel 50% griden daha koyuysa Base ve Blend çarpılır.

* #### [Blend_PinLight](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_pinlight)
[Blend_Overlay](#blend_overlay) ile aynıdır ama kontrast degeri düşürüldügü için daha yumuşak bir sonuç verir.

* #### [Blend_Screen](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_screen)
Base ve Blend olarak verdigimiz texturelerin ikisini de [1-x](#oneminus1-x) nodundan geçirir ve sonuçları birbiriyle çarpar. Çıkan sonucu tekrar [1-x](#oneminus1-x) den geçirir ve output olarak verir. Ne oldugundan emin degilim.

* #### [Blend_SoftLight](https://docs.unrealengine.com/5.1/en-US/blend-material-functions-in-unreal-engine/#blend_softlight)
Linkteki açıklamaya göre [Blend_PinLight](#blend_pinlight) ile aynı.

* #### [BlendAngleCorrectedNormals]()


* #### [BlurSampleOffsets]()
Kullanışsız, verilen inputu 2 boyutlu vektörler ile çarpıyor.


* #### [BoundingBoxBased_0-1_UVW]()


* #### [BoxIntersection]()


* #### [BoxMask-2D]()


* #### [BoxMask-3D]()


* #### [BreakOutFloat2Components]()


* #### [BreakOutFloat3Components]()


* #### [BreakOutFloat4Components]()


* #### [BumpOffset_advanced]()


* #### [CalcLightsourceAngle]()


* #### [CameraDepthFade]()


* #### [CameraDirectionVector]()


* #### [CameraOffset]()


* #### [CameraVectorWithWPOOptions]()


* #### [CameraWorldBlend]()


* #### [CanopyCreator_Branches]()


* #### [CellularFlakes]()


* #### [CenterPivotAroundVector]()


* #### [CheapContrast]()


* #### [CheapContrast_RGB]()


* #### [CheckerPattern]()


* #### [ComponentBasis_Vectors]()


* #### [ComponentPivotLocation]()


* #### [ComponentWise_SphereMask]()


* #### [Compute3DDeriv]()


* #### [ComputeFilterWidth]()


* #### [ComputeMipLevel]()


* #### [ConstantScalebyDistance]()


* #### [CreateThirdOrthogonalVector]()


* #### [CurlFrom3DDeriv]()


* #### [CustomReflectionVector]()


* #### [CustomRotator]()


* #### [CylindricalUVs]()


* #### [DebugFloat2Values]()


* #### [DebugFloat3Values]()


* #### [DebugFloat4Values]()


* #### [DebugOnOff]()


* #### [DebugScalarValues]()


* #### [DebugTimeSine]()


* #### [DepthFromWorldPosition]()
(Bu materyali kullanırken, output degerini 2000 gibi bi sayıya falan bölün yoksa döndürdügü deger yüksek oldugu için işlem yapamayız) [PixelDepth](#pixeldepth) nodu ile aynı işlevi görür ama bu node size PixelDepth degerini istediginiz konumdan verir. Mesela siz PixelDepth degeri üzerinde oynamak istiyorsunuz, diyelim ki konumunuzun x ekseninde -100 azalmasını istiyorsunuz, o zaman [WorldPosition](#worldposition) kullanıp konumunuzu aldıktan sonra bunu [subtract](#subtract) nodundan geçirip istediginiz konum degerini aldıktan sonra, bu konum degerine göre PixelDepth degerini DepthFromWorldPosition kullanarak elde edebilirsiniz.


* #### [DeriveHDRfromLDR]()


* #### [DeriveNormalZ_Function]()


* #### [DeriveTangentBasis]()


* #### [DetailTexturing]()


* #### [DiamondGradient]()


* #### [Distance_Blend]()


* #### [DitherTemporalAA](https://www.youtube.com/watch?v=kvHh0Jd-D3Q)
Bu nodun tam olarak yaptıgı işlem Alpha Threshold inputuna verilen degere göre belirli bir sayı aralıgından rastgele (ve ya degil) sayı döndürmesidir. Mesela en yaygın kullanışlarından biri olan görünmezlik efektini örnek alalım, materyalinizi Masked moduna alın ve DitherTemporalAA nodunu opacity maske baglayın. Alpha Threshold degerini düşürdükçe materyaliniz de görünmez olmaya başlar, çünkü DitherTemporalAA nodu bazı output degerlerini sıfırdan düşük döndürdügü için materyalimizdeki bazı pikseller görünmez olacak. DitherTemporalAA nodundan gelen output degerini çeşit çeşit şeylerde kullanabilirsiniz. Random inputuna da 0 vererek rastgele sayıları kapatabilirsiniz. Böylelikle output olarak gelen sayılar bir düzene göre gelir, materyalde bir desen olur. Yukarıda yazdıgım görünmezlik efektini yapıp Random kapalıyken Alpha Threshold degeriyle oynarsanız, materyalinizdeki görünmezlik efektinin bir desen oluşturdugunu görebilirsiniz.


* #### [DrawLine-2D]()


* #### [DrawLine-3D]()


* #### [DynamicBranch]()


* #### [DynamicNormalFromDistanceField]()


* #### [Ellipsoid-ConeShadow-Texture]()


* #### [ExponentialDensity]()


* #### [FixRotateAboutAxisNormals]()


* #### [FlattenNormal]()


* #### [FlipBook]()


* #### [FlipBook_MotionVectors]()


* #### [FlipbookWind]()


* #### [FlowMaps]()


* #### [FlowMaps_Simple]()


* #### [FlowMaps_UV1]()


* #### [FoliageScaleFactor]()


* #### [FoliageZRotation]()


* #### [FOV]()


* #### [Fresnel_Function]()


* #### [FuzzyShading]()


* #### [FuzzyShadingGrass]()


* #### [GenerateASpline]()


* #### [GeneratedBand]()


* #### [GeneratedOffsetBands]()


* #### [GeneratedRoundRect]()


* #### [GetAmbientCubemapIntensity]()


* #### [GetAmbientCubemapTint]()


* #### [GetGradientMapRow]()


* #### [GetUserInterfaceUV]()


* #### [GradFrom3DDeriv]()


* #### [GradientMap_Multi]()


* #### [GradientMap_Multi_TexObjSamplerType]()


* #### [HeightLerp]()


* #### [HeightLerpWithTwoHeightMaps]()


* #### [HighPrecisionWorldPosTextureSampling]()


* #### [HueShift]()
Bu node Texture inputuna verilen texture ve ya renk degerini Percentage inputuna verilen degere göre renk paletinde saat yönünde ileri alır. Percentage degeri 0 ve 1 arasında olmalı çünkü 1 tam bir tur demektir. Mesela 0.5 verirseniz rengimiz renk paletinde karşı tarafa geçer, yarım tur atar. Mesela rengimiz aşagıdaki gibi ise 0.5 HueShift uyguladıgımızda rengimiz açık mavi olan kısma gelecektir.

<img width="150" src="../../Dosyalar/HueShift_Palet.jpg">


* #### [Imposter_MotionVectors]()


* #### [ImposterUVs]()


* #### [InverseTransformMatrix]()


* #### [IsFloatValid]()


* #### [Lerp_3Color]()


* #### [Lerp_Multiple_Float]()


* #### [Lerp_Multiple_Float2]()


* #### [Lerp_Multiple_Float3]()


* #### [Lerp_Multiple_Float4]()


* #### [Lerp_ScratchGrime](https://forums.unrealengine.com/t/lerp-scratch-grime/685309/2)
Scratch/grime türkçeye çevirirsek çizik/kir demektir. Aslında bu node bir texturenin üzerine çizik ve ya kir efekti uygulamamıza yarar. Ama aslında bu çok anlamsız, yani lerp nodu ile aynı şeyi yapıyor. Tek farkları iki input alması, yani çift lerp nodu diyebiliriz.


* #### [Lerp_ScratchGrime2](https://forums.unrealengine.com/t/lerp-scratch-grime/685309/2)
[Lerp_ScratchGrime](#lerp_scratchgrime) ile aynı sayılır ama bu node, scratch olarak verdiginiz texturenin base texture ile toplanmış halini, base ile lerp eder. Yani scratch ile base lerp olmadan önce, scratch kendisine base textureyi de ekler. Grime ise, kendini texture ile çarpar. Yani scratch/grime olarak verdigimiz textureler direkmen base textureye konulmak yerine toplanarak ve çarpılarak eklenir.


* #### [LinearGradient](https://youtu.be/g7UreR23luA)
İnput olarak texturecoordinate verin. Verdiginiz deger sıfıra yaklaştıkça U kanalı (X) için soldan saga, V kanalı (Y) için yukarıdan aşagıya siyah efekt uygular, yani kenarlarda siyah bölümler oluşturur. Output olarak gelen U ve V kanallarını kullanıp, mesela bi textureden gelen rgb degerini U degeriyle çarparak, resminizin kenarlarına siyahlık ekleyebilirsiniz. Ayrıca linkteki videoya bakın, görseller ile anlamak daha kolay.


* #### [LinearSine]()


* #### [LineIntervalIntersection]()


* #### [LocalAlignedTexture]()


* #### [LocalAlignedTexture_TransformedWorldSpac]()


* #### [LocalPosition]()


* #### [LongLatToUV]()


* #### [LumensFromLightSource]()


* #### [MakeFloat2]()


* #### [MakeFloat3]()


* #### [MakeFloat4]()


* #### [MakeVectorsOrthogonal]()


* #### [MatLayerBlend_AddWorldPositionOffset]()


* #### [MatLayerBlend_AO]()


* #### [MatLayerBlend_BakedNormal]()


* #### [MatLayerBlend_BakedNormal_SimpleAdd]()


* #### [MatLayerBlend_BlendAngleCorrectedNormals]()


* #### [MatLayerBlend_BreakBaseColor]()


* #### [MatLayerBlend_BreakNormal]()


* #### [MatLayerBlend_BreakOpacity]()


* #### [MatLayerBlend_Decal]()


* #### [MatLayerBlend_Decal_UV3]()


* #### [MatLayerBlend_Emissive]()


* #### [MatLayerBlend_LightmassReplace]()


* #### [MatLayerBlend_ModulateRoughness]()


* #### [MatLayerBlend_ModulateSpecular]()


* #### [MatLayerBlend_Multiply]()


* #### [MatLayerBlend_MultiplyBaseColor]()


* #### [MatLayerBlend_NormalBlend]()


* #### [MatLayerBlend_NormalFlatten]()


* #### [MatLayerBlend_OverrideBaseColor]()


* #### [MatLayerBlend_OverrideDisplacement]()


* #### [MatLayerBlend_OverrideMetalness]()


* #### [MatLayerBlend_OverrideOpacity]()


* #### [MatLayerBlend_OverrideOpacityMask]()


* #### [MatLayerBlend_OverrideSubSurface]()


* #### [MatLayerBlend_OverrideWorldPositionOffset]()


* #### [MatLayerBlend_ReplaceNormals]()


* #### [MatLayerBlend_RoughnessOverride]()


* #### [MatLayerBlend_SeparateNormalandColorClamps]()


* #### [MatLayerBlend_Simple]()


* #### [MatLayerBlend_Stain]()


* #### [MatLayerBlend_Standard]()


* #### [MatLayerBlendStandardWithDisplacement]()


* #### [MatLayerBlendStandardWithMaskEdgeTint]()


* #### [MatLayerBlend_TenLayerBlend]()


* #### [MatLayerBlend_Tint]()


* #### [MatLayerBlendTintAllChannels]()


* #### [MatLayerBlend_TopNormal]()


* #### [MetallicShading]()


* #### [MF_BaseLayerTessellation]()


* #### [MF_BaseLayerTextures]()


* #### [MF_DetailNormalTiling]()


* #### [MF_DetailNormalTiling]()


* #### [MF_Displacement]()


* #### [MF_Displacement]()


* #### [MF_Displacement]()


* #### [MF_Displacement]()


* #### [MF_Displacement]()


* #### [MF_DisplacementBlend]()


* #### [MF_FlipBook]()


* #### [MF_FrameBlend]()


* #### [MF_FrameTextures]()


* #### [MF_Fuzz]()


* #### [MF_Fuzz]()


* #### [MF_Fuzz]()


* #### [MF_Fuzz]()


* #### [MF_Imperfection]()


* #### [MF_Iridescence]()


* #### [MF_MapAdjustments]()


* #### [MF_MapAdjustments]()


* #### [MF_MapAdjustments]()


* #### [MF_MapAdjustments]()


* #### [MF_MaterialBlend]()


* #### [MF_MiddleLayerTessellation]()


* #### [MF_MiddleLayerTextures]()


* #### [MF_NormalStrength_WS]()


* #### [MF_ObjAdjustments]()


* #### [MF_ObjAdjustments]()


* #### [MF_ObjAdjustments]()


* #### [MF_ObjAdjustments]()


* #### [MF_OrenNayerView]()


* #### [MF_PerceivedBrightness]()


* #### [MF_PuddleLayer]()


* #### [MF_QuixelDecalPOM]()


* #### [MF_QuixelDecalPOM]()


* #### [MF_Refraction]()


* #### [MF_RotateVector_90]()


* #### [MF_SchlickApprox]()


* #### [MF_SpecGlossToMetalRoughness]()


* #### [MF_SSSObjAdjustments]()


* #### [MF_SSSObjAdjustments]()


* #### [MF_Temporal_Blur]()


* #### [MF_Tiling]()


* #### [MF_Tiling]()


* #### [MF_Tiling]()


* #### [MF_Tiling]()


* #### [MF_Tiling]()


* #### [MF_Tiling]()


* #### [MF_TopLayerTextures]()


* #### [MF_Translucency]()


* #### [MF_Translucency]()


* #### [MF_TranslucencyEmission]()


* #### [MF_TranslucencyMetallic]()


* #### [MF_Transmission]()


* #### [MF_Transmission]()


* #### [MF_Transmission]()


* #### [MF_Transmission]()


* #### [MF_WindowImperfection]()


* #### [MF_WindowNormalStrength]()


* #### [MotionBlur-Texture]()


* #### [MS_CanopyCreatorMeshExpansion]()


* #### [MS_MultiNormal_UVnormals]()


* #### [MS_MultiNormal_VertexColorNormals]()


* #### [MS_SequencePainter_Sequence]()


* #### [MS_SequencePainter_SequenceFlipbook]()


* #### [MulM4V4]()


* #### [MultiplyAdd]()


* #### [MultiplyVectorWithQuaternion]()


* #### [MX_StandardSurface]()


* #### [MX_Transmission]()


* #### [NormalFromFunction]()


* #### [NormalFromHeightmap]()


* #### [NormalFromHeightmapChaos]()


* #### [ObjectLocalBounds]()


* #### [ObjectPivotPoint]()


* #### [ObjectScale]()


* #### [ObjectSpaceFalloff]()


* #### [OffsetAndScaleTol]()


* #### [OrthoFOV]()


* #### [PackedDistanceField]()


* #### [PackTwoNormalizedFloats]()


* #### [PanTextureCoordinateChannelfrom-1ton+1]()


* #### [PanTextureCoordinateFrom-1toN+1]()


* #### [ParallaxOcclusionMapping]()


* #### [ParticleDOF]()


* #### [PassThrough]()


* #### [PerceivedBrightness]()


* #### [PerturbNormalHQ]()


* #### [Pi]()


* #### [PivotAxis]()


* #### [PixelDepthOffset_Foliage]()


* #### [PixellnWorldUnits]()


* #### [PlotFunctionOnGraph]()


* #### [PlotFunctionOnGraph_Derivative]()


* #### [PlotFunctionOnGraph_Setup_Input]()


* #### [PointSampledUVs]()


* #### [Prepare3DDeriv]()


* #### [PreparePerturbNormalHQ]()


* #### [RadialGradientExponential](https://youtu.be/0xNFriRv-Bc)
LinearGradient gibi ama bu daire şeklinde beyazlık oluşturuyor. İnput olarak texturecoordinate verin. UVs degerini degiştirmek bu node için tekrarlama degil küçültme anlamına geliyor, yani [şurdaki](https://youtu.be/0xNFriRv-Bc?t=355) gibi. Center Position şu anlama geliyor, default olarak 0.5, 0.5 geliyor dairenin orta noktası texturenin tam ortasına geliyor, ama eger (0,0) vermiş olsaydık sol üst köşeyi orta noktası olarak alırdı. Yani Center X ve Center Y, eksenlerin kordinatını temsil ediyor, 0 derseniz o eksenin başlangıcı, 1 derseniz o eksenin sonu, daire sizin ayarladıgınız kordinatı orta noktası olarak alır. Radius dairenin çapı, büyüklügü yani. Density beyazlık şiddeti. İnvert density, açık degilken density degeri beyazlıgın şiddetinin temsil eder ve ortadan dışarıya dogrudur, açıkken density degeri beyazlıgın degil beyazlıgın çevresindeki siyahlıgın şiddetinin temsil eder ve dışarıdan ortaya dogrudur. Linkteki videoyu izleyin, görseller ile anlamak daha kolay.


* #### [RaiseBlackLevelsByPercentage]()


* #### [RayTracedSphere]()


* #### [Refract]()


* #### [RemapDistribution]()


* #### [RGBtoHSV]()


* #### [RGBtoHSV]()


* #### [RotateAboutWorldAxis_cheap]()


* #### [RotateVector]()


* #### [Round]()


* #### [SafeNormalize]()


* #### [SampleSceneDepth]()


* #### [ScaleUVsAroundPoint]()


* #### [ScaleUVsByCenter]()


* #### [SceneTextureAverage]()


* #### [SchlickPhase]()


* #### [ScreenAlignedPixelToPixelUVs]()


* #### [ScreenAlignedUVs]()


* #### [ScreenResolution]()


* #### [SCurve]()


* #### [SimpleGrassWind]()


* #### [SimplifiedFlakes]()


* #### [Sine_Remapped]()


* #### [SkyAtmospherelmage]()


* #### [SkyboxImage]()


* #### [SlopeMask]()


* #### [SmoothCurve]()


* #### [SmoothStep]()


* #### [SmoothThreshold]()


* #### [SoftOpacity]()


* #### [SpecGlossToMetalRoughness]()


* #### [SpeedTreeColorVariation]()


* #### [Sphere_AO]()


* #### [Sphere-ConeShadow-Texture]()


* #### [SphereGradient-2D]()


* #### [SphereGradient-3D]()


* #### [Spherical-Cap-Intersection]()


* #### [SpiralBlur-SceneTexture]()


* #### [SpiralBlur-SceneTexture]()


* #### [SpiralBlur-Texture]()


* #### [SpiralBlur-Texture]()


* #### [SplineBasedModelDeformation]()


* #### [SplineThicken]()


* #### [SplitComponents]()


* #### [Sprite]()


* #### [StaticMeshMorphTargets]()


* #### [StencilMaskCompare]()


* #### [SteppingPannerTime]()


* #### [SubUV_Function]()


* #### [SubUV_Function_MipDerivative]()


* #### [SumOfAConsecutiveNumberSequence]()


* #### [Swizzle]()


* #### [TangentBasis]()


* #### [TextureCropping]()


* #### [TimeWithSpeedVariable]()


* #### [Transform3x3Matrix]()


* #### [TransformImposterNormals]()


* #### [TransformNormals_Tangent_to_Vertex]()


* #### [TransformToClipSpace]()


* #### [TransformToZVector]()


* #### [Triplanar]()


* #### [CameraVector]()


* #### [TwoSidedTexturing]()


* #### [UnpackNormalFromFloat]()


* #### [UnpackTwoNormalizedFloats]()


* #### [UnwrapUVsForRender]()


* #### [UVBrickPatterns]()


* #### [UVLayoutToWorldSpacePosition]()


* #### [UVRemap_0-1_ToRange]()


* #### [UVToLongLat]()


* #### [ValueStep]()


* #### [VectorDisplacement]()


* #### [VectorLength]()


* #### [VectorToRadialValue]()


* #### [ViewAlignedReflection]()


* #### [VirtualPlaneCoordinates]()


* #### [Wind]()


* #### [WithinRange]()


* #### [WithinRangeFloat2]()


* #### [WithinRangeFloat3]()


* #### [WithinRangeFloat4]()


* #### [WorldAlignedBlend]()


* #### [WorldAlignedNormal]()
[WorldAlignedTexture](#worldalignedtexture) nodunun normal mapler için olan versiyonu, özünde aynı denebilir ama farklılıklar var.

* #### [WorldAlignedReflection]()


* #### [WorldAlignedTexture](https://www.youtube.com/watch?v=MfJ_1LWe2Q4)
Verilen texture objesinin her yüzeyini [World Position](#worldposition) nodu kullanarak yerleştirir. İki materyali iç içe koysanız bile, eger iki materyal de WorldAlignedTexture kullanıyorsa textureler aynı düzlemde olacagı için texturelerin görünümünde düzensizlik çıkmaz. TextureSize inputuna gelirsek, bunu tiling (tekrarlama) gibi düşünebilirsiniz. Default olarak 64, arttırdıkça texturenin de boyutu büyür, yani tiling azalmış gibi olur, azaltırsanız da tiling artıyormuş gibi olur, 3 boyutlu vektör verip her yöndeki kenarlar için özel TextureSize kullanabilirsiniz ama bu genellikle hatalar çıkarıyor bu yüzden constant kullanın. Eger [World Position](#worldposition) nodunu biliyorsanız bunları anlaması çok kolay, bilmiyosanız bile linkteki videoya bakabilirsiniz.


* #### [WorldAlignedTexture_MipBias]()


* #### [WorldAlignedTexture_SeperateChannels]()
[WorldAlignedTexture](#worldalignedtexture) ile aynıdır ama bu node onun aksine output olarak XYZ için bütün kombinasyonları verir.


* #### [WorldAlignedTextures_Complex]()


* #### [WorldCoordinate3Way]()


* #### [WorldPosition-XY]()


* #### [WorldPositionBehindFromDepth_experimenta]()


* #### [WorldPositionBehindTranslucency]()


* #### [WorldPositionWithScale]()


* #### [WorldUnitsInPixel]()


* #### [ZWorldSpaceFlow]()


## Niagara

* #### [ConvertNiagaraPositionToWorldspace]()


* #### [Niagara_DecompressQuaternion]()


* #### [Niagara_MeshReproductionSpriteUVs]()


* #### [Niagara_RotateMeshParticleWithQuaternion]()



## Normals

* #### [BlendAngleCorrectedNormals]()


* #### [HeightToNormalSmooth]()


## Opacity

* #### [Chroma_Key_Alpha]()


* #### [SoftOpacity]()
The SoftOpacity function takes in an Opacity value and then runs a variety of calculations on it to give it a softer feel. It applies a Fresnel effect, and depth-based alpha, and pixel depth. The end result causes the object to fade away as the camera approaches it.


## Parameter

* #### [ChannelMaskParameter]()


* #### [CollectionParameters](https://youtu.be/i4Z2r7mGA0o)
A Collection Parameter expression is used to reference a Parameter Collection asset. These are groups of parameters that can easily be reused by many different assets such as Materials, Blueprints, and much more. For more information on Parameter Collections, be sure to read the Parameter Collections Documentation.

* #### [CurveAtlasRowParameter]()


* #### [DoubleVectorParameter]()


* #### [DynamicParameter]()
The DynamicParameter expression provides a conduit for particle emitters to pass up to four values to the material to be used in any manner. These values are set in Cascade via a ParameterDynamic module placed on an emitter.

* #### [FontSampleParameter]()
The FontSampleParameter expression provides a way to expose a font-based parameter in a material instance constant, making it easy to use different fonts in different instances. The alpha channel of the font will contain the font outline value. Only valid font pages are allowed to be specified.

* #### [MaterialAttributeLayers]()


* #### [RuntimeVirtualTextureSampleParameter]()


* #### [ScalarParameter(Param)]()
The ScalarParameter expression outputs a single float value (Constant) that can be accessed and changed in an instance of the material or on the fly by code.

* #### [SpriteTextureSampler]()


* #### [StaticBoolParameter]()
[StaticBoolun](#staticbool) parametre halidir.


* #### [StaticComponentMaskParameter]()
The StaticComponentMaskParameter expression behaves just like an ordinary Component Mask, except that the mask values can be set by instances.

* #### [StaticSwitchParameter]()
The StaticSwitchParameter expression takes in two inputs, and outputs the first if the value of the parameter is true, and the second otherwise.

* #### [TextureObjectParameter]()
The TextureObjectParameter expression defines a texture parameter and outputs the texture object, used in materials that call a function with texture inputs. This node does not actually sample the texture, so it must be used in conjunction with a TextureSample node.

* #### [TextureSampleParameter2D]()
The TextureSampleParameter2D expression is identical to the TextureSample except that it is a parameter that can be modified in instances of the material and through code.

* #### [TextureSampleParameter2DArray]()


* #### [TextureSampleParameterCube]()
The TextureSampleParameterCube expression is identical to the TextureSample except that it only accepts cubemaps and it is a parameter that can be modified in instances of the material and through code.

* #### [TextureSampleParameterCubeArray]()


* #### [TextureSampleParameterSubUV]()
The TextureSampleParameterSubUV expression is identical to the ParticleSubUV except that it is a parameter that can be modified in instances of the material and through code.

* #### [TextureSampleParameterVolume]()


* #### [VectorParameter(Param)]()
The VectorParameter expression is identical to the Constant4Vector, except that it is a parameter and can be modified in instances of the material and through code. One nicety of the VectorParameter is that its value can be set using the Color picker.


## Particles

* #### [3dParticleOpacity]()
The purpose of this function is to help setup particles such that they fade away as they move away from the camera.

* #### [Distance_Blend]()


* #### [DynamicParameter]()
The DynamicParameter expression provides a conduit for particle emitters to pass up to four values to the material to be used in any manner. These values are set in Cascade via a ParameterDynamic module placed on an emitter.

* #### [ParticleColor]()
The ParticleColor expression ties into the current color of a given particle based on any per-particle color data defined within Cascade. This must be plugged into the appropriate channel (Emissive Color).

* #### [ParticleDirection]()
The ParticleDirection expression outputs Vector3 (RGB) data on a per-particle basis, representing the direction a given particle is currently traveling.

* #### [ParticleMacroUV]()
The ParticleMacroUV expression outputs UV texture coordinates that can be used to map any 2d texture onto the entire particle system in a continuous way, meaning the texture will be seamless across particles. The UVs will be centered around MacroUVPosition (specified in Cascade on the ParticleSystem, under the MacroUV category) and MacroUVRadius determines the world space radius that the UVs should tile at. The ParticleMacroUV node is useful for mapping continuous noise onto particles to break up the pattern introduced by mapping a texture onto each particle with normal texture coordinates.

* #### [ParticleMotionBlurFade]()
The ParticleMotionBlurFade expression outputs a value representing the amount of fade on a particle as a result of motion blur. A value of 1 represents no blur, black represents complete blur.

* #### [ParticlePositionWS]()
The ParticlePositionWS expression outputs Vector3 (RGB) data representing each individual particle's position in world space.

* #### [ParticleRadius]()
The ParticleRadius expression outputs the radius in Unreal units of each particle individually. This allows, for example, for changes to be made to a material once the radius has reached a certain point.

* #### [ParticleRandom]()


* #### [ParticleRelativeTime]()
The ParticleRelativeTime expression outputs a number between 0 and 1 representing a particle's age, with 0 being the moment of birth and 1 being the moment of death.

* #### [ParticleSize]()
The Particle Size expression outputs the X and Y size of a particle sprite. This can then be used to drive some aspect of a Material.

* #### [ParticleSizeByPixleUnits]()


* #### [ParticleSpeed]()
ParticleSpeed outputs the current speed each particle is traveling, measured in Unreal units per second.

* #### [ParticleSubUV]()
The ParticleSubUV expression is used to render sub-images of a texture to a particle. ParticleSubUV is similar to a flipbook, except that ParticleSubUV allows the texture animation to be manipulated in Cascade.

* #### [ParticleSubUVProperties]()


* #### [SphericalParticleOpacity]()
The SphericalParticleOpacity expression creates a procedural opacity map to cause sprite particles to appear spherical. This can be much simpler than having to create an import a texture map for a similar effect.

* #### [TextureSampleParameterSubUV]()
The TextureSampleParameterSubUV expression is identical to the ParticleSubUV except that it is a parameter that can be modified in instances of the material and through code.


## Pivot Painter

* #### [PivotPainter_HierarchyData]()
This particular function is specifically designed to work with object hierarchies.

* #### [PivotPainter_PerObjectData]()
This particular function is designed to work on a per-object basis.

* #### [PivotPainter_PerObjectFoliageData]()
This function is designed to work specifically with individual foliage objects.

* #### [PivotPainter_TreeData]()
The outputs starting with tree process the model's UV information as it would be stored by the Pivot Painter MAXScript. The outputs starting with Leaf process the UV information as it would be stored by the per-object pivot painting section of the script.


## Pivot Painter 2

* #### [ms_PivotPainter2_CalculateMeshElementIndex]()


* #### [ms_PivotPainter2_Decode8BitAlpahAxisExtent]()


* #### [ms_PivotPainter2_DecodeAxisVector]()


* #### [ms_PivotPainter2_DecodePostion]()


* #### [ms_PivotPainter2_ReturnParentTextureInfo]()


* #### [ms_PivotPainter2_UnpackIntegerAsFloat]()


* #### [PivotPainter2FoliageShader]()


## Procedurals

* #### [GeneratedBand](https://youtu.be/fITAkG3_qP8)
Ya bu çok uzun anlatılmaz. Linkteki videoya bakın. Ben kullanmayı denedim ama mantıklı bişeler yapamadım.

* #### [GeneratedOffsetBands](https://youtu.be/7Ie7mrnVuy8)
Like the GeneratedBand function, GeneratedOffsetBands creates procedurally generated bands of texture across the UV space. However, this function can produce multiple bands instead of just one.

* #### [NormalFromFunction]()


* #### [NormalFromHeightmap]()
This function serves as a quick way to make a normal map out of an existing black and white heightmap, rather than having to load a separate texture into memory.

* #### [NormalFromHeightmapChaos]()
The NormalFromHeightMapChaos function takes a heightmap and pans it in 4 directions, then blends the result back together to make a chaotically animated normal map.

* #### [ObjectSpaceFalloff]()



## Reflections

* #### [CustomReflectionVector]()
This function uses a normal map to generate a reflection vector independent of the default reflection vector and the normal's input on the base shader.

* #### [DistanceLimitedReflections]()


* #### [ViewAlignedReflection]()
This function takes in a spherical reflection texture and aligns it to the view. The calculation can be offset by inputting a custom reflection vector.

* #### [WorldAlignedReflection]()
This function takes in an incoming sphere-based reflection texture and aligns it to the world coordinates. The calculation can be offset by inputting a custom reflection vector.


## Render To Texture

* #### [TransformImposterNormals]()



## Shading

* #### [AbsorptionMediumMaterialOutput]()


* #### [AxisAlignedFresnel]()


* #### [CalcLightsourceAngle]()


* #### [Ellipsoid-ConeShadow-Texture]()


* #### [FuzzyShading]()
This function emulates a surface similar to velvet or moss, and is similar to a Fresnel calculation. Incidentally, it is also useful for shader effects such as a scanning electron microscope.

* #### [FuzzyShadingGrass]()
This function is designed to provide the diffuse portion of grass shading. Similar to FuzzyShading, this function allows you to blend in a new color at the edges by first desaturating by a given percentage and then applying a custom color to the desaturated area.

* #### [MetallicShading]()


* #### [Sphere_AO]()


* #### [Sphere-ConeShadow-Texture]()


* #### [Spherical-Cap-Intersection]()



## Shading Model

* #### [Shading Model]()



## Sky

* #### [SkyAtmosphereAerialPerspective]()


* #### [SkyAtmosphereDistantLightScatteredLuminance]()


* #### [SkyAtmosphereLightDirection]()


* #### [SkyAtmosphereLightDiskLuminance]()


* #### [SkyAtmosphereLightIlluminance]()


* #### [SkyAtmosphereViewLuminance]()


* #### [SkyLightEnvMapSample]()


## Speed Tree

* #### [SpeedTree]()


* #### [SpeedTreeBillboardNormals]()


* #### [SpeedTreeCameraFacing]()


* #### [SpeedTreeColorVariation]()


* #### [SpeedTreeCrossfadeBillboard]()


* #### [SpeedTreeWind]()


* #### [SpeedTreeWindMotion]()


* #### [UnpackDirection]()


## Texture

* #### [FontSample]()
The FontSample expression allows you to sample the texture pages out of a font resource as regular 2D textures. The alpha channel of the font will contain the font outline value. Only valid font pages are allowed to be specified.

* #### [FontSampleParameter]()
The FontSampleParameter expression provides a way to expose a font-based parameter in a material instance constant, making it easy to use different fonts in different instances. The alpha channel of the font will contain the font outline value. Only valid font pages are allowed to be specified.

* #### [ParticleSubUV]()
The ParticleSubUV expression is used to render sub-images of a texture to a particle. ParticleSubUV is similar to a flipbook, except that ParticleSubUV allows the texture animation to be manipulated in Cascade.

* #### [SceneColor]()
The SceneColor expression outputs the existing scene color.

* #### [SceneTexture]()
Get the scene texture

* #### [SpriteTextureSampler]()
A custom sprite material can be created by duplicating one of the existing ones, or creating a new material in the Content Browser. When a sprite is rendered, the texture defined in a sprite asset will be piped into any texture parameters named "SpriteTexture" in the material. The SpriteTextureSampler node can be placed to do this automatically.

* #### [TextureObject]()
The TextureObject expression is used to provide a default texture for a texture function input within a function. This node does not actually sample the texture, so it must be used in conjunction with a TextureSample node.

* #### [TextureObjectParameter]()
The TextureObjectParameter expression defines a texture parameter and outputs the texture object, used in materials that call a function with texture inputs. This node does not actually sample the texture, so it must be used in conjunction with a TextureSample node.

* #### [TextureProperty]()
The TextureProperty exposes a texture's property of your choice such as the texture's size or texel size.

* #### [TextureSample]()
The TextureSample expression outputs the color value(s) from a texture. This texture can be a regular Texture2D (including normal maps), a cubemap, or a movie texture.

* #### [TextureSampleParameter2D]()
The TextureSampleParameter2D expression is identical to the TextureSample except that it is a parameter that can be modified in instances of the material and through code.

* #### [TextureSampleParameter2DArray]()


* #### [TextureSampleParameterCube]()
The TextureSampleParameterCube expression is identical to the TextureSample except that it only accepts cubemaps and it is a parameter that can be modified in instances of the material and through code.

* #### [TextureSampleParameterSubUV]()
The TextureSampleParameterSubUV expression is identical to the ParticleSubUV except that it is a parameter that can be modified in instances of the material and through code.

* #### [TextureSampleParameterVolume]()



## Texturing

* #### [3DSandMayaUVCoordinates]()
This function flips the green channel of incoming UVs to place the 0,0 coordinate in the lower-left corner (as it is in 3ds Max and Maya) instead of the upper-left. This is important for models coming in from these applications, as it prevents you from having to flip textures.

* #### [AbberatedBluer-Texture]()


* #### [BitMask]()


* #### [BrickAndTileUVs]()


* #### [BumpOffset_advanced]()


* #### [CameraWorldBlend]()
Outputs falloff results for the 3 primary world vectors based on the camera angle. Can be used to blend between textures based on direction the camera is looking.

* #### [CustomRotator](https://youtu.be/f9a780XjoKI)
Textureye döndürür. UVs inputuna texturecoordinate baglayın. Rotation Center şu anlama geliyor, default olarak 0.5, 0.5 geliyor yani dönme noktası texturenin tam ortasına geliyor, ama eger (0,0) vermiş olsaydık sol üst köşeyi dönme noktası olarak alırdı. Yani Center X ve Center Y, eksenlerin kordinatını temsil ediyor, 0 derseniz o eksenin başlangıcı, 1 derseniz o eksenin sonu, dönme efekti sizin ayarladıgınız kordinatı dönme efektinin orta noktası olarak alır. Rotation angle döndürme degeri, 0 ve 1 arasında, 1 = 360 derece döndürme verir. Output olarak UV döndürür (Texturelerdeki UV bölümüne baglıyorsunuz). İnputların kısa açıklamaları,
<br>
<br>
<br>
UVs = Texturecoordinate baglayın
<br>
<br>
Rotation Center = Dönme efektinin orta noktası
<br>
<br>
Rotation Angle = Döndürme degeri (0 - 1)

* #### [CylindricalUVs]()
This function tiles a texture around an object using cylindrically projected UVs centered around the object's center.

* #### [DetailTexturing]()
The DetailTexturing function simplifies the process of creating detail textures for your material. Detail texturing allows you to give the illusion of more detail in a texture by bringing in a more highly repeated diffuse and normal map combination which layers over the original diffuse and normal for an object. This gives the illusion of greater detail at close range.

* #### [FlattenNormal]()


* #### [FlowMaps]()


* #### [FlowMapsUV1]()


* #### [FlowMaps_2D]()


* #### [FlowMaps_3D]()


* #### [FlowMaps_Simple]()


* #### [HeightLerp]()
The HeightLerp function allows you perform a linear interpolation between 2 textures based on a heightmap and a transition phase value. This allows you to adjust the value along the hightmap that the lerp takes place.

* #### [HeightLerpWithTwoHeightMaps]()


* #### [HighPrecisionWorldPosTextureSampling]()


* #### [LocalAlignedTexture]()
The LocalAlignedTexture function tiles a texture on an object in local space.

* #### [LocalAlignedTexture_TransformedWorldSpace]()


* #### [MotionBlur-Texture]()


* #### [PackedDistanceField]()


* #### [ParallaxOcclusionMapping]()


* #### [ScreenAlignedPixelToPixelUVs]()


* #### [ScreenAlignedUVs]()


* #### [SkyAtmosphereImage]()


* #### [SkyAtomosphereImage]()


* #### [SkyboxImage]()


* #### [SlopeMask]()


* #### [SpiralBlur-SceneTexture]()


* #### [SpiralBlur-Texture]()


* #### [SteppingPannerTime]()


* #### [StretchGradient]()


* #### [SubUV_Function]()
SubUV_Function is perfect for handling animation across a sprite sheet or texture with multiple frames. The function takes in a texture object, and based on the outputs can show a blended-frame animation of the frames on that texture.

* #### [SubUV_Function_MipDerivative]()


* #### [Swizzle](https://youtu.be/DdyvDf442a0)
Verilen inputun X ve Y boyutlarının yerlerini degiştirir, yani flip yapar (döndürür). Linkteki videodan pek bişe anlayamadım ama [bu abiye](https://www.youtube.com/watch?v=hxIl52S-hzM&t=791s) de bakabilirsiniz, güzel anlatmış.


* #### [TextureCropping]()
The TextureCropping function allows you to crop down a given texture to a smaller and offset location on the texture coordinate plane. This is perfect for placing a block of color on top of an emissive texture region.

* #### [TextureVariation]()


* #### [Texture_Bombing]()


* #### [Texture_Bombing_POM]()


* #### [TriplanarCameraVector]()


* #### [TwoSidedTexturing]()
The TwoSidedTexturing function provides individual texture inputs for both sides of a two-sided material. This function does nothing if the material's Two Sided property is not active.

* #### [UVCropping]()


* #### [VectorDsiplacement]()


* #### [WorldAlignedNormal]()
[WorldAlignedTexture](#worldalignedtexture) nodunun normal mapler için olan versiyonu, özünde aynı denebilir ama farklılıklar var.

* #### [WorldAlignedTexture](https://www.youtube.com/watch?v=MfJ_1LWe2Q4)
Verilen texture objesinin her yüzeyini [World Position](#worldposition) nodu kullanarak yerleştirir. İki materyali iç içe koysanız bile, eger iki materyal de WorldAlignedTexture kullanıyorsa textureler aynı düzlemde olacagı için texturelerin görünümünde düzensizlik çıkmaz. TextureSize inputuna gelirsek, bunu tiling (tekrarlama) gibi düşünebilirsiniz. Default olarak 64, arttırdıkça texturenin de boyutu büyür, yani tiling azalmış gibi olur, azaltırsanız da tiling artıyormuş gibi olur, 3 boyutlu vektör verip her yöndeki kenarlar için özel TextureSize kullanabilirsiniz ama bu genellikle hatalar çıkarıyor bu yüzden constant kullanın. Eger [World Position](#worldposition) nodunu biliyorsanız bunları anlaması çok kolay, bilmiyosanız bile linkteki videoya bakabilirsiniz.

* #### [WorldAlignedTexture_Complex]()


* #### [WorldAlignedTexture_MipBias]()


* #### [WorldAlignedTexture_SeperateChannels]()
[WorldAlignedTexture](#worldalignedtexture) ile aynıdır ama bu node onun aksine output olarak XYZ için bütün kombinasyonları verir.


* #### [WorldCoordinate3Way]()
The WorldCoordinate3Way function projects a texture onto the surface of an object in world coordinates. The user has control over how multiple textures blend together at the edges, and a normal map can be added to perturb the surface prior to the calculation.

* #### [WorldPositionBehindFromDepth_experimental]()


* #### [WorldPositionBehindTranslucency]()


* #### [WorldPrositionWithScale]()


* #### [ZWorldSpaceFlow]()
The ZWorldSpaceFlow function pushes a texture along the tangent space of an object, causing that texture to look like it is "flowing" along that surface. It works by making two variations of the texture panning in the same direction, but each with a slight offset from the other. It then blends each one over the other in a repeating fashion.


## Thin Translucent

* #### [ThinTranslucentMaterialOutput]()



## Units

* #### [Cm-to-Km]()
Verdigimiz inputu 1000000 a böler, 100cm = 1m, 1000m = 1km, yani 100 x 1000 = 100000.

* #### [Km-to-Cm]()
Verdigimiz inputu 1000000 ile çarpar, 100cm = 1m, 1000m = 1km, yani 100 x 1000 = 100000.


## UserInterface

* #### [GetUserInterfaceUV]()



## Utility

* #### [Add Named Reroute Declaration Node]()
İsimlendirilmiş düzenleme nodu.

* #### [Add Reroute Node]()
Düzenleme nodu.

* #### [AntialiasedTextureMask]()
The AntialiasedTextureMask expression allows you to create a material using a soft (anti-aliased) transition mask. The mask can be used to blend between two complex material properties or to fade out an alpha blended material (works well with SoftMasked). Simply specify a texture with the mask specified in one channel (red, green, blue, or alpha), set the used channel in the expression and specify the comparison value. Assuming the channel stores a grayscale value in the range 0 = black to 1 = white the comparison function defines if the resulting mask should be 0 or 1. This expression is a parameter, allowing the Texture property to be overridden by child MaterialInstances.

* #### [AtmosphericLightColor]()


* #### [AtmosphericLightVector]()


* #### [BentNormalCustomOutput]()


* #### [BlackBody](https://youtu.be/yxN7lf0MuvE)
Verilen sıcaklık derecesine göre (sanırım kelvin) renk döndürüyor. Kullanmayın bile.

* #### [BoxMask-2D]()


* #### [BoxMask-3D]()


* #### [BumpOffset](https://youtu.be/70EzAb4CrmA)
Bu node ek ayar yapmadan derinlik efekti vermenize yarar. Mesela duvar yaptınız, tuglalar arasında derinlik olmasını istiyorsunuz. Bu node verilen yükseklik mapine göre siyah olan kısımları geride, beyaz olan kısımları daha önde gösteren bi efekt verir. Mesela yükseklik mapi, texturenin bir kanalı olabilir, eger siyah ve beyaz kısımlar güzel görünüyorsa çalışacaktır. Output olarak gelen degeri texturelar için UV olarak ve ya normal mapler için UV olarak kullanabilirsiniz. Parametreleri,
<br>
<br>
<br>
Coordinate = Texture Coordinate verebilirsiniz.
<br>
<br>
Height = Yükseklik mapi, mesela texturenin bir kanalı olabilir.
<br>
<br>
HeightRatioInput = Artıya gittikçe efektin etkisi artar. Eksileri kullanmıyoruz. Ayrıca bu ayarı unreal enginenin önerilen ayar aralıgında, 0.02 ve 0.1 arasında kullanın.

* #### [ChannelMaskParameter]()


* #### [ClearCoatNormalCustomOutput]()


* #### [ConstantBiasScale](https://youtu.be/7s0T9ckB0bw)
Bu node verilen inputa bias degerini ekler ve scale degeriyle çarpar. Mesela [-1,1] arasındaki degerleri [0,1] arasına taşımak istiyorsunuz. Bias olarak 1.0 scale olarak 0.5 kullanarak bunu yapabilirsiniz.

* #### [DDX]()
The DDX expression exposes DDX derivative calculation, a GPU hardware feature used in pixel shader calculation.

* #### [DDY]()
The DDY expression exposes DDX derivative calculation, a GPU hardware feature used in pixel shader calculation.

* #### [DepthFade](https://youtu.be/2BxrGjPcirk)
Saydam meshler opak olanlar ile kesiştiginde ne olacagını ayarlayabilirsiniz. Parametreleri,
<br>
<br>
<br>
Opacity = Opaklık, sıfırdan (saydam) başlar, arttırdıkça opak olur.
<br>
<br>
FadeDistance = Saydamlık efektinin ne kadar uzaga kadar etkili olacagı, bunu 0 yapmayın çünkü 0 yapınca hareket ederken renkler sürekli birbirine giriyor. En az 0.1 yapın.

* #### [DepthOfFieldFunction](https://youtu.be/YUvQHmjpeJ8)
Depth Of Field (odak noktası) degerini verir (bilmiyorsanız google görsellerden bakabilirsiniz). 0 tam odaklanılmış, 1 tamamen blurlu anlamına gelir. Output olarak gelen deger bu ikisi arasındadır. Unreal enginenin [kendi sayfasında](https://docs.unrealengine.com/5.1/en-US/utility-material-expressions-in-unreal-engine/#depthoffieldfunction) da örnek var.

* #### [Distance](https://youtu.be/ZINJAvhQilg)
Verilen inputların birbirlerine olan uzaklıgını (öklidyen) döndürür. İki inputun da boyut sayısı aynı olmalıdır. 1, 2, 3 boyutlu vektörlerin hepsinde çalışır.

* #### [DistanceFieldGradient]()
The DistanceFieldGradient Material Expression node, when normalized, outputs the X,Y,Z direction an object would move with in the distance field. This makes the Distance Field Gradient Material Expression node well-suited for Materials that need to simulate the flow of liquids.

* #### [DistanceToNearestSurface]()
The Distance To Nearest Surface Material Expression node allows Materials to sample any point in the levels Global Distance Field. This Material Expression works by outputting the signed distance in world space units from the distance field to the nearest occluders in the scene.

* #### [EyeAdaptation]()


* #### [FeatureLevelSwitch](https://youtu.be/wo6fSPJVp2I)
İf gibi, duruma göre ayar yapmanızı saglar. Grafikler için kullanılan uygulama (ya da işleyen birim) neyse, o inputa baglı olan şeyi output olarak verir. Default eger herhangi bir inputa bir şey baglamadıysanız çalışır. Mesela oyun telefondan oynanıyorsa daha düşük kaliteli şeyler kullanabilirsiniz. İnputların anlamları [burda](https://docs.unrealengine.com/5.1/en-US/utility-material-expressions-in-unreal-engine/#featurelevelswitch) yazıyor.

* #### [Fresnel](https://youtu.be/PLwEwIYX454)
Bu materyale sahip meshe bakıldıgında, meshin orta kısımları 0a yakın, kenara yakın tarafları 1e yakın bir deger döndürür. Bu degerler ile meshe ayar yapabilirsiniz. Parametreler,
<br>
<br>
<br>
ExponentIn = Kenarlardan ortaya dogru, fresnelin etkisi diyebiliriz, yani bunu ne kadar arttırırsanız fresenel o kadar etkili olur.
<br>
<br>
BaseReflectFractionIn = Yansıtma degeri, Bu da ExponentIn in aynısı ama dıştan içe degil, her yere etki eder. Eger bunu azaltırsanız yansıma olmaz yani fresnel heryeri kaplar, eger arttırırsanız fresnelin etkisi azalır.

* #### [GeneratedRoundRect]()


* #### [GIReplace](https://youtu.be/Yb9fiof97xQ)
Bu materyale sahip meshin, diyelim ki bu materyale sahip olan mesh bir duvar ve siz de bu duvarın yanına başka bir mesh daha koydunuz, biliyorsunuz ki unreal engine duvar ne renkse duvarın yanındaki meshe de o rengin biraz yansımasını verecek. İşte yansıma rengini ayarlamak için bu nodu kullanıyoruz. Linkteki videoyu izleyin, görsellerle anlaması daha kolay.

* #### [InverseLinearInterpolate]()


* #### [LightmassReplace](https://youtu.be/TkdmgGWTvYM)
The LightmassReplace expression simply passes through the Realtime input when compiling the material for normal rendering purposes, and passes through the Lightmass input when exporting the material to Lightmass for global illumination. This is useful to work around material expressions that the exported version cannot handle correctly, for example WorldPosition.

* #### [LinearInterpolate(Lerp)](https://youtu.be/fckeT6GyvPc)
Verilen alpha degerine göre iki inputu (resim ve ya renk) birbirine karıştırır. İstedigimiz boyutta constant verebiliriz, hem alpha hem de inputlarımız için. Örnegin bir boyutlu constant yani sayı kullanalım, A ve B için iki sayı girin mesela 10 ve 0. Eger alpha degerine 0 verirseniz A, 1 verirseniz B degeri döndürülür. Eger alpha degerine 0.5 verirseniz sayımız da A ve B nin ortası yani 5 olur. Yani 0 a yaklaştıkça A, 1 e yaklaştıkça B. Ayrıca dedigim gibi, istediginiz boyutta input ve alpha verebilirsiniz. Mesela A ve B için iki tane renk (rgb yani 3 boyutlu) verelim. Alpha degeri olarak da 3 boyutlu bi vektör verelim. Alphanın içindeki her kanalı degiştirdiginizde A ve B için de geçerli olan alpha degeri degişir. Mesela r (red) degiştirirseniz A ve B nin r kanalı için alpha degerini belirlemiş olursunuz ama sadece r kanalı için, diger iki kanalı da yine Alphanın içindeki kanallardan degiştirmeniz gerek.

* #### [MaterialProxyReplace]()


* #### [Noise](https://youtu.be/hP3P3WH4TjM)
Gürültü döndürür. Sanırım texture halinde kullanıyoruz. Parametreler,
<br>
<br>
<br>
Scale = Texture büyüklügü, 0 dan başlar yükselttikçe texture da büyür.
<br>
<br>
Quality = Kaliteyi arttırır.
<br>
<br>
Function = Burdan deseni oluşturan fonksiyonu seçiyoruz. Bunları tek tek anlatamam kendiniz test edin ve ya [bakın](https://youtu.be/hP3P3WH4TjM?t=124).
<br>
<br>
Turbulence = Test etsem bile anlayamadım, aralardaki boşlugu arttırıyo ve ya birleştiriyo olmalı.
<br>
<br>
Levels = Düşükken köşeler sanki çizgi film gibi, arttırınca detaylar daha çok ortaya çıkıyor.
<br>
<br>
Output Min = Genellikle ne kadar siyah olacagını seçersiniz, -5 ve 0 arasında denebilir.
<br>
<br>
Output Max = Genellikle ne kadar beyaz olacagını seçersiniz, 0 ve 1 arasında denebilir.
<br>
<br>
Level Scale = 0 dan uzaklaştıkça (eksi artı farketmez) çizgilerin köşeleri düzleşir.
<br>
<br>
Position = Sanırım sadece 3 boyutlu vektör kabul ediyor, Texturenin pozisyonunu ayarlar.
<br>
<br>
Filter Width = Her nokta (ve ya çizgi) arasındaki mesafeyi arttırır.


* #### [QualitySwitch](https://youtu.be/64I4rzyZ6_Q)
İf gibi, duruma göre ayar yapmanızı saglar. Oyundaki kalite neyse, o inputa baglı olan şeyi output olarak verir. Default eger herhangi bir inputa bir şey baglamadıysanız çalışır. Mesela Low a hiçbir şey baglamadınız, eger kalite low da ise o zaman low baglı olmadıgı için Defaulta ne baglıysa o kullanılır. Zaten Defaultu boş bırakamazsınız.

* #### [RayTracingQualitySwithc]()


* #### [ReflectionCapturePassSwitch]()


* #### [RotateAboutAxis](https://youtu.be/ljWoJ7Pp9Ww)
Materyale dönme efekti kazandırır ama kendi çevresinde degil, dünya içinde. Ayrıca bu dönme efekti hareket olarak degil sadece görünüş olarak olan bir dönme efektidir. Yani dönme efektinden sonra materyalin yeri ne kadar degişse de aslında materiyal ilk koydugunuz konumdadır. RotateAboutAxis ile materyale istediginiz yönde dönme efekti verebilir bunu otomatikleştirebilirsiniz de. Linkteki videoyu izleyin çünkü yazı ile anlatmak bi anlam ifade etmiyor, eger izlediyseniz yazdıklarımı anlayacaksınız. Parametreleri,
<br>
<br>
<br>
NormalizedRotationAxis = 3 boyutlu vektör verin, hangi yöne dogru dönme efekti olmasını istiyorsanız o boyuta 1 degeri verin, 1 degeri verdikleriniz dönme yönünü ifade eder.
<br>
<br>
RotationAngle = Ne kadar dönme efekti uygulanacagı, 0 ve 1 arasında, 1 = tam tur
<br>
<br>
PivotPoint = RotationAngle olarak time nodu baglayın. PivotPointi parametreye dönüştürün ve dönme efektinin izledigi yolu takip edin. Normalde daire çizer. Şimdi siz eger PivotPointin herhangi bir yönünü mesela R, arttırırsanız, dönme efektinin çizdigi daire yolunun R yönüne dogru kaymaya başladıgını görürsünüz. Daha dogrusu daireyi sündürürsünüz. Çok fazla arttırırsanız daire çok süner ve dönme efektinin izledigi yol sanki bir yumurta gibi olur. Diger boyutlar ile birlikte bu şekilde dönme efektinin izledigi daireyi büyütebilirsiniz.
<br>
<br>
Position = World Position baglayın
<br>
<br>
Period (node üzerinde) = Normalde 1 dir. Eger arttırsanız, mesela 5 yaparsanız, 5 kat yavaşlar, yani 1 tur atması 5 kat daha yavaş olur. Aynı şekilde, azaltarak hızlandırabilirsiniz.

* #### [ShaderStatgeSwtich]()


* #### [ShadingPathSwtich]()


* #### [ShadowPassSwitch](https://www.youtube.com/watch?v=LqwTLdqEUMo)
Bu node materyalin gölgesine istediginiz ayarı vermenizi saglar. Materyalinizi Masked yapın, ShadowPassSwitch nodunu opacity maske baglayın. Default degerine normal opacity mask inputunuzu verebilirsiniz, yani bu ayar gölgeler ile degil materyalle alakalı. Eger ben opacity mask kullanmayacaktım zaten diyorsanız o zaman bu degere 1 (constant) baglayın, böylelikle opacity mask vermemiş gibi olursunuz, 0 verseydiniz opaklık 0 oldugu için materyale sahip olan mesh görünmez olurdu. Şimdi gelelim asıl meseleye, Shadow inputuna bagladıgınız deger gölgeleri belirler. Eger 0 verirseniz gölgeleri silersiniz, 1 verirseniz gölge neyse onu gösterir yani tamamen opak olur. Bizim yapmak istedigimiz herhangi bir texturenin alpha degerini vermek, böylelikle verdigimiz resim neyse gölgede de o görünecek. Yani shadow degerine herhangi bir texturenin alpha degerini ve ya herhangi bir kanalını vererek bunu gölgeler için maske olarak kullanabilirsiniz.


* #### [SmoothStep]()


* #### [SphereMask](https://youtu.be/xRxkcFOhNrc)
The SphereMask expression outputs a mask value based on a distance calculation. If one input is the position of a point and the other input is the center of a sphere with some radius, the mask value is 0 outside and 1 inside with some transition area. This works on one, two, three, and four component vectors

* #### [Step]()


* #### [VectorNoise]()
The Vector Noise Material expression adds several more 3D or 4D vector noise results to use in your Materials. Due to the run-time expense of these functions, it is recommended that once a look is developed with them, all or part of the computation be baked into a Texture using the Draw Material to Render Target Blueprint feature introduced in Unreal Engine 4.13 and later. These Material graph Expressions allow procedural looks to be developed in the engine on final assets, providing an alternative to creating procedurally generated Textures with an external tool to apply to assets in UE4. Inside of the Vector Noise Material Expression, you will find the following Vector Noise types.

* #### [VertexInterpolator]()



## Utils

* #### [DecalDerivative]()


* #### [DecalLifetimeOpacity]()


* #### [DecalMipmapLevel]()



## Vector Ops

* #### [Append3Vector]()
AppendVector(Append) için geçerli olan kurallar bunda da geçerlidir. Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür.

* #### [Append4Vector]()
AppendVector(Append) için geçerli olan kurallar bunda da geçerlidir. Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür.

* #### [AppendVector(Append)](https://youtu.be/pFkth9GKci4)
Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür. En fazla 4 boyutlu vektör yapılabilir, eger 3 + 2 gibi bir işlem yaparsanız hata verecektir, ama 3 + 1 yaparsanız sanki birinci inputa alpha degeri ekliyormuşsunuz gibi toplar ve 4 boyutlu vektör döndürür.

* #### [ComponentMask(Mask)]()
İnput olarak verdigimiz vektörden (1 boyuttan fazla), istedigimiz kanalı alabilmemizi saglar.

* #### [CrossProduct](https://youtu.be/KWtRiKbNS24)
The CrossProduct expression computes the cross product of two three-channel vector value inputs and outputs the resulting three-channel vector value. Given two vectors in space, the cross product is a vector that is perpendicular to both of the inputs.

* #### [DeriveNormalZ]()
The DeriveNormalZ expression derives the Z component of a tangent space normal given the X and Y components and outputs the resulting three-channel tangent space normal. Z is calculated as Z = sqrt(1 - (x * x + y * y));

* #### [DotProduct]()
The DotProduct expression computes the dot product, which can be described as the length of one vector projected onto the other, or as the cosine between the two vectors multiplied by their magnitudes. This calculation is used by many techniques for computing falloff. DotProduct requires both vector inputs to have the same number of channels.

* #### [Fresnel_Function]()


* #### [Normalize]()
The Normalize expression calculates and outputs the normalized value of its input. Normalized vectors (also called "unit vectors") have an overall length of 1.0. This means each component of the input is divided by the total magnitude (length) of the vector.

* #### [Transform]()
The Transform expression converts a three-channel vector value from one reference coordinate system to another.By default, all shader calculations in a material are done in tangent space. The vector constants, camera vector, light vector, etc are all transformed to tangent space before being used in a material. The Transform expression allows these vectors to be transformed from tangent space to world-space, local-space, or view-space coordinate systems. In addition, it allows world-space and local-space vectors to be transformed to any of the other reference coordinate systems.

* #### [TransformPosition]()
The TransformPosition expression can transform any position from screen space to the destination space specified by the expression's TransformType variable. Currently only transforming into world space is supported. This expression can be used to get world space coordinates in the material. To visualize world position, you can plug it straight into emissive: This node is deprecated due to major precision problems when used to derive world pos away from the origin! Use the WorldPosition node instead.



## Vectors

* #### [ActorPositionWS](https://youtu.be/Kn3ZQ8TxZoE)
Aktörün pozisyonunu dünyaya göre 3d (vektör) olarak verir.

* #### [CameraDirectionVector]()


* #### [CameraPositionWS](https://youtu.be/MRbjCXf1hmg)
Kameranın pozisyonunu dünyaya göre 3d (vektör) olarak verir.


* #### [CameraVectorWithWPOOptions]()


* #### [CameraVectorWS]()
The CameraVector expression outputs a three-channel vector value representing the direction of the camera with respect to the surface, in other words, the direction from the pixel to the camera.

* #### [Constant2Vector]()
Constantın 2 boyutlu hali, içerisinde iki sayı tutar.

* #### [Constant3Vector]()
Constantın 3 boyutlu hali, bu üç boyut rgb ye denk gelir. İçerisinde renk tutar.

* #### [Constant4Vector]()
Constantın 4 boyutlu hali, bu dört boyut rgba ye denk gelir. rgb den farklı olarak içerisinde alpha (opaklık/saydamlık) degeri tutar.

* #### [LightVector]()
This expression has been deprecated in Unreal Engine 4 as lighting calculations are now deferred.

* #### [ObjectBounds]()
The Object Bounds expression outputs the size of the object in each axis. If used as color, the X, Y, and Z axes correspond to R, G, and B, respectively.

* #### [ObjectOrientation](https://youtu.be/eDlSIm0BL6g)
Bu materyale sahip olan objenin yön bilgisini verir (3d vektör). Mesela eger X eksenine dönükse (1, 0, 0), Y eksenine dönükse (0, 1, 0), Z eksenine dönükse (0, 0, 1) verir. Bu deger aralarda da olabilir, obejenin yönüne göre.

* #### [ObjectPositionWS](https://youtu.be/P530OKEXCJo)
Bu materyale sahip olan objenin konum bilgisini verir (3d vektör).

* #### [OctahedronToUnitVector]()



* #### [ParticlePositionWS]()
The ParticlePositionWS expression outputs Vector3 (RGB) data representing each individual particle's position in world space.

* #### [PixelNormalWS]()
The PixelNormalWS expression outputs vector data representing the direction that pixels are facing based on the current normal.

* #### [PreSkinnedLocalBounds]()


* #### [PreSkinnedLocalNormal]()
The Pre-Skinned Local Normals Vector Expression outputs a three-channel vector value representing the local surface normal for Skeletal and Static Meshes. This enables you to achieve locally-aligned tri-planar materials and mesh aligned effects in your materials.In this example, the material is using a tri-planar texture aligned to the mesh's local surface normal.

* #### [PreSkinnedLocalPosition]()
The Pre-Skinned Local Position Vector Expression outputs a three-channel vector value that gives access to a Skeletal Mesh's default pose position data for use in per-vertex outputs. This enables you to have localized effects on an animated character. This vector expression can also be used with Static Meshes, which will return the standard local position.

* #### [ReflectionVectorWS]()


* #### [RotateVector]()


* #### [UnitVectorToOctahedron]()


* #### [SkinningVertexOffsets]()


* #### [VertexNormalWS](https://youtu.be/sGuJxr4Bfxw)
Her kenarın baktıgı yönü vektör olarak döndürür (1 ile -1 arası, mesela x eksenine bakıyorsa 1, x ekseninin zıttına bakıyorsa -1). Mesela eger bu materyale sahip meshinizin sadece yukarı bakan tarafının istediginiz renge sahip olmasını istiyorsanız bunu kullanabilirsiniz. [PixelNormalWS](#pixelnormalws) nin aksine bu node pixel yerine vertex kullanıldıgı için normal map kullanırken hatalar oluşmaz. Linkteki videoya bakın görseller ile anlamak daha kolay.

* #### [VertexTangentWS]()



## VFX

* #### [AppendMany]()
İnput olarak verdigimiz her sayıyı (constant) birleştirir ve vektör oluşturur.



## VirtualTexture

* #### [RuntimeVirtualFeatureSwitch]()


* #### [RuntimeVirtualTextureOutput]()


* #### [RuntimeVirtualTextureReplace]()


* #### [RuntimeVirtualTextureSample]()


* #### [RuntimeVirtualTextureSampleParameter]()



## Volume

* #### [CloudSampleAttribute]()


* #### [VolumetricAdvancedMaterialInput]()


* #### [VolumetricAdvancedMaterialOutput]()


* #### [VolumetricCloudEmptySpaceSkippingInput]()


* #### [VolumetricCloudEmptySpaceSkippingOutput]()


## Water

* #### [SceneDepthWithoutWater]()


* #### [SingleLayerWaterMaterialOutput]()



## WorldPositionOffset

* #### [AlignMeshToTheCamera]()


* #### [AttachMeshToTheCamera]()


* #### [CameraOffset]()
The CameraOffset function is great to assist with depth sorting, as it allows you to move an object in camera space, either toward or away from the camera.

* #### [CanopyCreator_Branches]()


* #### [CenterPivotAroundVector]()


* #### [ConstantScalebyDistance]()


* #### [FixRotateAboutAxisNormals]()


* #### [FlipbookWind]()


* #### [GenerateASpline]()


* #### [Gravity_WPO]()


* #### [MS_CanopyCreatorMeshExpansion]()


* #### [ObjectPivotPoint]()
The ObjectPivotPoint function returns the object's pivot point in world space. This is not compatible with the pixel shader.

* #### [ObjectScale]()
The ObjectScale function returns the object's XYZ scale together and seperately. This is not compatible with the pixel shader.

* #### [OrthoFOV]()


* #### [PivotAxis]()
The PivotAxis function creates a common pivot location on arbitrary axes. This is helpful for creating flag motion. Instead of using a single pivot point near the top of the flag, use a shared Z point and unique X and Y location data to create a more realistic connection along the object's width.

* #### [RotateAboutWorldAxis_Cheap]()
The RotateAboutWorldAxis_cheap function cheaply rotates objects around world axes. Input the angle you would like to use and attach the output to world position offset.

* #### [SimpleGrassWind]()
The SimpleGrassWind function applies a basic wind operator to foliage, giving the ability to specify a weight map and wind strength. This is a non-directional wind that just gives a very general movement to foliage. This should be the last WPO node you add.

* #### [SplineBasedModelDeformation]()


* #### [SplineThicken]()
The SplineThicken function serves as a way to make very thin polygons look thicker at render time. This is perfect for cables, hair, grass, and other such objects.

* #### [Sprite]()


* #### [Sprite_Capsule]()


* #### [Sprite_Ellipsoid]()


* #### [Sprite_TearDrop]()


* #### [StaticMeshMorphTargets]()
The StaticMeshMorphTargets function unpacks morph target data that was added into a via 3ds Max's Morph Packer MAXScript.

* #### [UVLayoutToWorldSpacePosition]()


* #### [Wind]()
The Wind function provides separate outputs for wind strength, speed multiplied by time and a normalized wind vector.



## WPO

* #### [ManualWorldToScreenUVsTransform]()


## No Category

* #### [NewComment]()
Yorum bölümü oluşturur.

* #### [Sobol]()


* #### [TemporalSobol]()


* #### [UnpackDirection]()
