## Atomsphere

* #### [AtomsphereFogColor]()
Kullanılmıyor. Sis ve atmosferik level efektlerini etkileyen şeyler var. Ama dedigim gibi, kullanılmıyor o yüzden ben de bilmiyorum.


## Blend

* #### [Blend_ColorBurn]()
Blend_ColorBurn textureyi verdigimiz blend texturesi ile yogunlaştırır ve ya birleştirir. sonuç daha renkli ve blend rengi ile birleşmiş bir texture olur. eger blend olarak verdigimiz texture beyaz ise bi etki olmaz çünkü Blend_ColorBurn textureyi daha koyu (yogun) yapmak içindir.

* #### [Blend_ColorDodge]()
Blendi 1 den çıkarıp (rgb için her deger 0 ile 255 arasında yani 255 den çıkarıyo denebilir). Base olarak verdigimiz textureyi blende bölüyor. Çok denemeler yapsam da mantıgını anlayamadım, internette de kaynak yok.

* #### [Blend_Darken]()
Verdigimiz iki texturenin her pikselini karşılaştırır ve koyu (yogun) olanı seçer. (zıttı Blend_Lighten)

* #### [Blend_Difference]()
Base textureyi blendden çıkarıp sonucun mutlak degerini alarak, sanki daldırma gibi bi efekt uygular, karıştırmak gibi ama tam degil.

* #### [Blend_Exclusion]()
Base ve blendi yarı saydam yapıp birbiri üzerine koyar, yani iki texture birden üst üste gelir.

* #### [Blend_HardLight]()
Like a harsher version of Blend_Overlay, Blend_HardLight will either screen or multiply the Base and Blend together. The function does a comparison on the Blend color such that wherever the Blend is brighter than 50% gray, the Base and Blend will be combined via a Screen operation. If the Blend is darker than 50% gray, the Base will be multiplied by the Blend as in the Multiply function. The contrast of the final result is then boosted for a harsh output.

* #### [Blend_Lighten]()
Verdigimiz iki texturenin her pikselini karşılaştırır ve açık olanı seçer. (zıttı Blend_Darken)

* #### [Blend_LinearBurn]()
Baseyi blende ekler (toplar) ve sonuçtan bir çıkarır. Ne oldugunu bilmiyorum.

* #### [Blend_LinearDodge]()
Baseyi blende ekler (toplar).

* #### [Blend_LinearLight]()
Blend_LinearLight is a linear version of Blend_Overlay, providing harsher results. The function does a comparison on the Blend color such that wherever the Blend is brighter than 50% gray, the Base and Blend will be combined via a Screen operation. If the Blend is darker than 50% gray, the Base will be multiplied by the Blend as in the Multiply function.

* #### [Blend_Overlay]()
Blend_Overlay will either screen or multiply the Base and Blend together. The function does a comparison on the Blend color such that wherever the Blend is brighter than 50% gray, the Base and Blend will be combined via a Screen operation. If the Blend is darker than 50% gray, the Base will be multiplied by the Blend as in the Multiply function.

* #### [Blend_PinLight]()
Like Blend_Overlay, Blend_PinLight will either lighten or darken the Base and Blend together. The function does a comparison on the Blend color such that wherever the Blend is brighter than 50% gray, the Base and Blend will be combined via a Screen operation. If the Blend is darker than 50% gray, the Base will be multiplied by the Blend as in the Multiply function. The contrast is softened, making this a less harsh version of Overlay.

* #### [Blend_Screen]()
Base ve Blend olarak verdigimiz texturelerin ikisini de 1-x (one minus) nodeundan geçirir ve sonuçları birbiriyle çarpar. Çıkan sonucu tekrar 1-x den geçirir ve output olarak verir. Ne oldugundan emin degilim.

* #### [Blend_SoftLight]()
Blend_SoftLight is a softer version of Overlay. The function does a comparison on the Blend color such that wherever the Blend is brighter than 50% gray, the Base and Blend will be combined via a Screen operation. If the Blend is darker than 50% gray, the Base will be multiplied by the Blend as in the Multiply function. The contrast is softened, making this a less harsh version of Overlay.

* #### [Lerp_ScratchGrime]()


* #### [Lerp_ScratchGrime2]()



## Chromakeying

* #### [DiffColorKeyerErodeSinglePass](https://youtu.be/CEUGMFLjc4Y)
Kullanışsız, renkleri silmede kullanılıyor.

* #### [MF_Chromakeyer](https://youtu.be/CEUGMFLjc4Y)
Kullanışsız, renkleri silmede kullanılıyor.


## Color

* #### [Desaturation](https://youtu.be/0pPyCZvZ05A)
0 dan bire yaklaştıkça texturenin renkleri solmaya başlar ve 1 olunca siyah beyaz olur. Aynı şekilde -1 e yaklaştıkça da texturenin renkleri daha da artar ve -1 de iki katı renkli olur. Bunu texturenizin renklerini arttırmak ve azaltmak için kullanabilirsiniz.

* #### [LinearTosRGB]()
Verilen texturenin kontrast derecesini arttırır. Mesela ateş resmi düşünün, ateşin oldugu nokta çok parlak ama uç noktalar ise daha az parlaktır. LinearTosRGB kullanırsanız az parlak noktalar daha parlak olur ve ateş daha da büyür (zıttı sRGBToLinear).

* #### [sRGBToLinear]()
Verilen texturenin kontrast derecesini azaltır. Mesela ateş resmi düşünün, ateşin oldugu nokta çok parlak ama uç noktalar ise daha az parlaktır. sRGBToLinear kullanırsanız az parlak noktalar neredeyse yok olur, ateşin çok parlak oldugu kısımlar daha az parlak ve ateş daha da küçük olur (zıttı LinearTosRGB).


## Constants

* #### [Constant]()
Tek bir degere sahip (1 boyutlu) degişken. İçerisinde sayı tutar.

* #### [Constant2Vector]()
Constantın 2 boyutlu hali, içerisinde iki sayı tutar.

* #### [Constant3Vector]()
Constantın 3 boyutlu hali, bu üç boyut rgb ye denk gelir. İçerisinde renk tutar.

* #### [Constant4Vector]()
Constantın 4 boyutlu hali, bu dört boyut rgba ye denk gelir. rgb den farklı olarak içerisinde alpha (opaklık/saydamlık) degeri tutar.

* #### [DeltaTime]()
İki fps arasındaki süreyi gösterir, her fpsde deger döndürür.

* #### [DistanceCullFade]()
Bunu kullanabilmeniz için ilk baş dünyanıza [CullDistanceVolume](https://docs.unrealengine.com/5.1/en-US/cull-distance-volumes-in-unreal-engine/) eklemelisiniz. Ardından bu volume içinde sizin oluşturdugunuz materyale sahip meshler olacak. Ne zaman ki bir oyuncu bu volume içine girerse DistanceCullFade nodeu deger döndürür ve bu degeri kullanarak oyuncu bu volume içine girdiginde yapmak istediginiz basit efektleri uygulayabilirsiniz. Mesela opaklıga DistanceCullFade baglayın ve volume içerisine giridiginiz anda içerdeki mesh görünmez iken yavaşça görünür hale gelicek.

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
The PrecomputedAOMask node lets you access Lightmass-calculated ambient occlusion (AO) in your Material, which can be useful for procedural texturing or for adding in aging effects and dirt in areas where it would slowly accumulate over time.

* #### [Time](https://youtu.be/SMQI9_MEfRM)
Oyun başladıgı andan itibaren geçen süreyi verir. Eger editördeyseniz editörde geçen süreyi verir. Degeri görüntülemek için DebugScalarValues nodeunu kullanabilirsiniz. Period parametresi ile kaç saniyede bir sıfılanacagı, daha dogrusu kaça kadar sayacagını belirleyebilirisiniz.

* #### [TwoSidedSign]()
Eger materyalinizin iki yüzlü ve iki yüzünde ayrı textureler olmasını istiyorsanız bunu kullanabilirisiniz. Lerp (LinearInterpolate) nodeuna alpha degeri olarak TwoSidedSign nodeunu baglayın.

* #### [VertexColor]()
The VertexColor expression is the access point for the material to the outputs of color modules affecting sprite particles emitters.

* #### [View Property]()
Materyalleri sürekli degiştirebilmeniz/güncelleyebilmeniz ve işlemler yapabilmeniz için, dünya ve oyuncular hakkında bilgiler verir. parametreleri,
<br>
<br>
Render Target Size = Ekran büyüklügü ile ilgili bişe
<br>
Field of View = Görüş alanı
<br>
View Size = Render Target Size ile aynı
<br>
View Position (Absolute World Space) = Konumumuzu verir (3 boyutlu vektör)
<br>
Camera Position (Absolute World Space) = Kameramızın konumunu verir (3 boyutlu vektör)


## Coordinates

* #### [ActorPositionWS](https://youtu.be/Kn3ZQ8TxZoE)
Aktörün pozisyonunu dünyaya göre 3d (vektör) olarak verir.

* #### [CameraPositionWS](https://youtu.be/MRbjCXf1hmg)
Kameranın pozisyonunu dünyaya göre 3d (vektör) olarak verir.

* #### [LightmapUVs]()
Lightmap UV için texture coordinatelerini verir. X ve Y için iki boyutlu bir vektör verir. Eger Lightmap UV açık degilse 0 verir.

* #### [MapARPassThroughCameraUV]()


* #### [ObjectOrientation](https://youtu.be/eDlSIm0BL6g)
Bu materyale sahip olan objenin yön bilgisini verir (3d vektör). Mesela eger X eksenine dönükse (1, 0, 0), Y eksenine dönükse (0, 1, 0), Z eksenine dönükse (0, 0, 1) verir. Bu deger aralarda da olabilir, obejenin yönüne göre.

* #### [ObjectPositionWS](https://youtu.be/P530OKEXCJo)
Bu materyale sahip olan objenin konum bilgisini verir (3d vektör).

* #### [ObjectRadius](https://youtu.be/Om3k66NY7Jc)
Bu materyale sahip olan objenin kapladıgı alanın yarıçapını verir.

* #### [Panner](https://youtu.be/24mfLY7aQFQ)
Texturelara hareket vermenize yarar.

* #### [ParticlePositionWS]()


* #### [ParticleSubUVProperties]()


* #### [PixelNormalWS](https://youtu.be/gTK2EHj6ycg)
Her pikselin baktıgı yönü vektör olarak döndürür. Mesela eger bu materyale sahip meshinizin sadece yukarı bakan tarafının istediginiz renge sahip olmasını istiyorsanız bunu kullanabilirsiniz. Eger normal map kullanırsanız, egimli noktalardaki pikseller hatalara yol açabilir, bunun olmasını istemiyorsanız VertexNormalWS kullanın. Linkteki videoya bakın görseller ile anlamak daha kolay.

* #### [Rotator](https://youtu.be/0wFUoN63F6I)
Textureye dönme efekti kazandırır. UV texture kordinatı döndürür (Texturelerdeki UV bölümüne baglıyorsunuz). Coordinate olarak TextureCoordinate verebilirsiniz, böylelikle tiling (tekrarlama) ayarlayabilirsiniz. Center X ve Center Y şu anlama geliyor, default olarak 0.5, 0.5 geliyor yani dönme efekti texturenin tam ortasına geliyor, ama eger (0,0) vermiş olsaydık sol üst köşeyi dönme efektinin tam orta noktası olarak alırdı. Yani Center X ve Center Y, eksenlerin kordinatını temsil ediyor, 0 derseniz o eksenin başlangıcı, 1 derseniz o eksenin sonu, dönme efekti sizin ayarladıgınız kordinatı dönme efektinin orta noktası olarak alır. Bunu en iyi deneyerek anlayabilirsiniz.


* #### [SceneTexelSize]()
The SceneTexelSize expression allows you to offset by texel sizes, as you would when using the SceneColor and SceneDepth expressions. This is useful for edge detection in multi-resolution systems, as without this calculation you would be forced to use a small static value, resulting in inconsistent results at lower resolutions.

* #### [ScreenPosition](https://youtu.be/OKIJlsOxNPI)
ScreenPosition, verdiginiz materyale sahip olan meshin, sizin ekranınızda tam olarak hangi pikseller üzerinde durdugunu verir (2 boyutlu vektör). Bunu anlatması çok zor o yüzden linkteki videoya kesin bakın. Diyelim ki bir meshe bu materyali verdiniz, ekranınızı yavaşça başka bir tarafa döndürün, ScreenPosition degeri sürekli degişecektir. X ve Y olarak iki deger verir, eger mesh ekranınızın sol kenarında ve neredeyse kaybolacaksa, Y degeri sıfıra çok yakın demektir, eger mesh ekranınızın üst kenarında ve neredeyse kaybolacaksa, X degeri sıfıra çok yakın demektir. ScreenPosition iki output döndürür ama ikisi aynı anlama gelir, ViewportUV bu degeri 0 ve 1 arasında verirken, PixelPosition bu degeri gerçek piksel sayısına göre verir.

* #### [TextureCoordinate(TexCoord)](https://youtu.be/_thf1Z3j73s)
Textureların UV (tekrarlama) degerini ayarlamamıza yarar. Tiling (tekrarlama) aynı materyali farklı boyutlardaki meshlerde de kullanacagımız zaman materyale meshin boyutuna göre bi oran vermemizi saglar. parametreleri,
<br>
<br>
UTiling = x ekseninde (yatay) takrarlama sayısı
<br>
VTiling = y ekseninde (dikey) takrarlama sayısı

* #### [VertexNormalWS](https://youtu.be/j2BEEtpPgdk)
Her pikselin baktıgı yönü vektör olarak döndürür. Mesela eger bu materyale sahip meshinizin sadece yukarı bakan tarafının istediginiz renge sahip olmasını istiyorsanız bunu kullanabilirsiniz. PixelNormalWS nin aksine bu node pixel yerine vertex kullanıldıgı için normal map kullanırken hatalar oluşmaz. Linkteki videoya bakın görseller ile anlamak daha kolay.

* #### [ViewSize](https://youtu.be/CLW73n19N_U)
Ekran boyutunu piksel olarak verir. 2 boyutlu vektör döndürür. Eger ekranınızı küçültürseniz bu deger de degişir.

* #### [WorldPosition](https://youtu.be/8aYe54XrZYI)
Pixellerin uzay/zaman da konumunu döndürür. Eger materyallerinizin texture kordinatlarının aynı olmasını istiyorsanız, yani aynı datayı kullanmaları, aynı konumları kullanmaları için, bunu kullanabilirsiniz. Ya da texturelerin konumlarının kameraya göre görünmesini istiyorsanız da bunu kullanabilirsiniz. Bu dediklerim anlamsız gelebilir, linkteki videoyu izleyin.


## Coorinates

* #### [1Dto2DIndex]()


* #### [1Dto3DIndex]()


* #### [2Dto1DIndex]()


* #### [3Dto1DIndex]()


* #### [BlurSampleOffsets]()


* #### [BoundingBoxBased_0-1_UVW]()


* #### [LocalPosition]()


* #### [LongLatToUV]()


* #### [ObjectAlignedVirtualPlaneCoordinates]()


* #### [PanTextureCoordinateChannelfrom-1ton+1]()


* #### [PanTextureCoordinateFrom-1toN+1]()


* #### [SampleSceneDepth]()


* #### [ScreenResolution]()


* #### [UVBrickPatterns]()


* #### [UVRemap_0-1_ToRange]()


* #### [UVToLongLat]()


* #### [VirtualPlaneCorrdinates]()


* #### [WorldSpaceAlignedScreenCoordinates]()



## Cubemaps

* #### [InteriorCubemap]()


* #### [LongLatToUV]()


* #### [UBToLongLat]()



## Custom

* #### [Custom]()


* #### [PerInstanceCustomDate]()


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

* #### [StaticMeshDecal_Function]()



## Density

* #### [BeersLaw]()


* #### [RayMarchHeightMap]()



## Depth

* #### [DepthFade]()
The DepthFade expression is used to hide unsightly seams that take place when translucent objects intersect with opaque ones.

* #### [DepthFromWorldPosition]()


* #### [PixelDepth](https://youtu.be/AHOidP7olg0)
Bu materyale sahip meshin, ekranınızın ortasına olan uzaklıgı ve cameranızın meshe olan uzaklıgını verir. Yanlış anlaşılmasın iki output vermiyor, bu ikisine baglı olarak ekranınızda görünen piksellerin size ve ekranınızın ortasına olan uzaklıgını veriyor. Ben baya denemeler yaptım ve çıkardıgım sonuca göre şu şekilde düşünmeniz yeterli; bu node tam olarak piksellerin ekranınızda ne kadar yer kapladıgı (yakındayken büyük uzaktayken küçük) ve ya bu piksellerin ne kadar kaliteli oldugunu veriyor ve bunu yaparken de sizin meshe olan uzaklıgınız ve kamera açınızı baz alıyor. Daha iyi anlamak için linkteki videoya bakın.

* #### [SceneDepth]()
The SceneDepth expression outputs the existing scene depth. This is similar to PixelDepth, except that PixelDepth can sample the depth only at the pixel currently being drawn, whereas SceneDepth can sample depth at any location.


## DistanceFields

* #### [DistanceField_Capsule]()


* #### [DistanceField_Cylinder]()


* #### [DistanceField_Intersection]()


* #### [DistanceField_Sphere]()


* #### [DistanceField_Subtract]()


* #### [DistanceField_Union]()


* #### [RayTraceSphereFalloff]()



## Foliage

* #### [PixelDepthOffset_Foliage]()



## Font

* #### [FontSample]()
The FontSample expression allows you to sample the texture pages out of a font resource as regular 2D textures. The alpha channel of the font will contain the font outline value. Only valid font pages are allowed to be specified.

* #### [FontSampleParameter]()
The FontSampleParameter expression provides a way to expose a font-based parameter in a material instance constant, making it easy to use different fonts in different instances. The alpha channel of the font will contain the font outline value. Only valid font pages are allowed to be specified.


## Functions

* #### [MaterialFunctionCall]()
The MaterialFunctionCall expression allows you to use an external MaterialFunction from another material or function. The external function's input and output nodes become inputs and outputs of the function call node. If a MaterialFunction is selected in the Content Browser when placing one of these expressions, it will automatically be assigned.

* #### [PreviousFrameSwitch]()


* #### [StaticBool]()
The StaticBool expression is used to provide a default bool value for a static bool function input within a function. This node does not switch between anything, so it must be used in conjunction with a StaticSwitch node.

* #### [StaticSwitch]()
The StaticSwitch expression works like a StaticSwitchParameter, except that it only implements the switch and does not create a parameter.

* #### [TextureObject]()
The TextureObject expression is used to provide a default texture for a texture function input within a function. This node does not actually sample the texture, so it must be used in conjunction with a TextureSample node.


## GetPostProcessSetting

* #### [GetAmbientCuvemapIntensity]()


* #### [GetAmbientCuvemapTint]()



## Gradient

* #### [DiamondGradient]()
The DiamondGradient function uses UV channel 0 to produce a radial gradient, giving the user the ability to adjust the falloff rate of the gradient.

* #### [GetGradientMapRow]()


* #### [GradientMap_Multi]()


* #### [GradientMap_Multi_TexObjSamplerType]()


* #### [LinearGradient](https://youtu.be/g7UreR23luA)
İnput olarak texturecoordinate verin. Verdiginiz deger sıfıra yaklaştıkça U kanalı (X) için soldan saga, V kanalı (Y) için yukarıdan aşagıya siyah efekt uygular, yani kenarlarda siyah bölümler oluşturur. Output olarak gelen U ve V kanallarını kullanıp, mesela bi textureden gelen rgb degerini U degeriyle çarparak, resminizin kenarlarına siyahlık ekleyebilirsiniz. İşe yarar mı ben de bilmiyorum. Ayrıca linkteki videoya bakın, görseller ile anlamak daha kolay.

* #### [RadialGradientExponential](https://youtu.be/0xNFriRv-Bc)
LinearGradient gibi ama bu daire şeklinde beyazlık oluşturuyor. İnput olarak texturecoordinate verin. UVs degerini degiştirmek bu node için tekrarlama degil küçültme anlamına geliyor, yani [şurdaki](https://youtu.be/0xNFriRv-Bc?t=355) gibi. Center Position şu anlama geliyor, default olarak 0.5, 0.5 geliyor dairenin orta noktası texturenin tam ortasına geliyor, ama eger (0,0) vermiş olsaydık sol üst köşeyi orta noktası olarak alırdı. Yani Center X ve Center Y, eksenlerin kordinatını temsil ediyor, 0 derseniz o eksenin başlangıcı, 1 derseniz o eksenin sonu, daire sizin ayarladıgınız kordinatı orta noktası olarak alır. Radius dairenin çapı, büyüklügü yani. Density beyazlık şiddeti. İnvert density, açık degilken density degeri beyazlıgın şiddetinin temsil eder ve ortadan dışarıya dogrudur, açıkken density degeri beyazlıgın degil beyazlıgın çevresindeki siyahlıgın şiddetinin temsil eder ve dışarıdan ortaya dogrudur. Linkteki videoyu izleyin, görseller ile anlamak daha kolay.

* #### [SmoothCurve]()
The SmoothCurve function takes in an existing texture channel or gradient and uses a procedural curve to control the transition from dark to light. The user can adjust the tangents of this curve to change the result.

* #### [ValueStep]()
The ValueStep function takes in an existing texture channel or gradient and outputs a pure black and white image based on inputs from the user. The result is a mask that represents what portion of the gradient equals the value of the inputs.


## Hair Attributes

* #### [Hair Attributes]()



## Hair Color

* #### [Hair Color]()



## ImageAdjustment

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


* #### [HueShift]()
The HueShift function offsets the current hue value of an input color by a given percentage. This percentage is 1-based and centered around the color wheel. For instance, a shift of 0.5 (50%) will shift to a complimentary hue, or the hue on the opposite side of the color wheel. A shift of 1.0 (100%) gives no change, as this is the equivalent of rotating completely around the color wheel.

* #### [Luminosity_And_Color]()


* #### [RaiseBlackLevelsByPercentage]()


* #### [SCurve]()
The SCurve function boosts contrast of an image by interpolating the values of each channel values of an image along an S-curve. This is similar to applying a Curves adjustment in Photoshop and setting the RGB curve to an S-curve or using the Increase Contrast (RGB) preset.

* #### [SmoothThreshold]()
The SmoothThreshold function takes in a gradient, an interpolation rate, and a threshold value (Cutoff Value). It then applies a smooth contrast to the gradient, based on the inputs. Here is a breakdown of what each input does:

* #### [UnSharpMaskFunction]()


* #### [UnSharpMaskTexture]()



## Landscape

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

* #### [PixelDepthOffset_Foliage]()



## MAXScripts

* #### [MS_MultiNormal_UVnormals]()


* #### [MS_MultiNormal_VertexColorNormals]()


* #### [MS_SequencePainter_Sequence]()


* #### [MS_SequencePainter_SequenceFlipbook]()


* #### [MS_VertexAnimationTools_MorphTargets]()


* #### [ms_StaticMeshSkeletalAnimation]()


* #### [ms_StaticMeshSkeletalAnimationHighQuality]()



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

* #### [MaterialLayerBlend_AO]()


* #### [MaterialLayerBlend_AddWroldPositionOffset]()


* #### [MaterialLayerBlend_BakedNormal]()


* #### [MaterialLayerBlend_BakedNormal_SimpleAdd]()


* #### [MaterialLayerBlend_BlendAngleCorrectedNormals]()


* #### [MaterialLayerBlend_BreakBaseColor]()


* #### [MaterialLayerBlend_BreakNormal]()


* #### [MaterialLayerBlend_Decal]()


* #### [MaterialLayerBlend_Decal_UV3]()


* #### [MaterialLayerBlend_Emissive]()


* #### [MaterialLayerBlend_LightmassReplace]()


* #### [MaterialLayerBlend_MaterialLayerBlend_MultiplyBaseColor]()


* #### [MaterialLayerBlend_ModulateRoughness]()


* #### [MaterialLayerBlend_ModulateSpecular]()


* #### [MaterialLayerBlend_Multiply]()


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


* #### [MaterialLayerBlend_RoughnessOverrid]()


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
Clamp = min ve max çalışır.
<br>
Clamp Min = sadece min çalışır, input max degerinden büyük olsa bile max çalışmaz.
<br>
Clamp Max = sadece max çalışır, input min degerinden küçük olsa bile min çalışmaz.

* #### [ComponentMask(Mask)]()
İnput olarak verdigimiz vektörden (1 boyuttan fazla), istedigimiz kanalı alabilmemizi saglar.

* #### [Cosine](https://youtu.be/gn5Zbsq8eFs)
Cosine yani kosinüs, sürekli 1 ve 0 arasında dönen bi dalga. Kendini tekrar eder, çogu durumda kullanışlıdır. İnput olarak time nodeunu baglayabilirsiniz, böylelikle sürekli tekrarlayan bi deger döndürür. Linkteki videoda görseller ile anlatılmış kesin izleyin. (Bkz. Sine)

* #### [CreateThirdOrthogonalVector]()


* #### [CrossProduct]()
The CrossProduct expression computes the cross product of two three-channel vector value inputs and outputs the resulting three-channel vector value. Given two vectors in space, the cross product is a vector that is perpendicular to both of the inputs.

* #### [CylinderIntersection]()


* #### [DegreesToRadians]()


* #### [DeriveNormalZ_Function]()


* #### [Divide](https://youtu.be/ibGKUNCM8e8)
Bölme.

* #### [DotProduct]()
The DotProduct expression computes the dot product, which can be described as the length of one vector projected onto the other, or as the cosine between the two vectors multiplied by their magnitudes. This calculation is used by many techniques for computing falloff. DotProduct requires both vector inputs to have the same number of channels.

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


* #### [LineIntervalIntersection]()


* #### [LinearInterpolate(Lerp)](https://youtu.be/fckeT6GyvPc)
Verilen alpha degerine göre iki inputu (resim ve ya renk) birbirine karıştırır. İstedigimiz boyutta constant verebiliriz, hem alpha hem de inputlarımız için. Örnegin bir boyutlu constant yani sayı kullanalım, A ve B için iki sayı girin mesela 10 ve 0. Eger alpha degerine 0 verirseniz A, 1 verirseniz B degeri döndürülür. Eger alpha degerine 0.5 verirseniz sayımız da A ve B nin ortası yani 5 olur. Yani 0 a yaklaştıkça A, 1 e yaklaştıkça B. Ayrıca dedigim gibi, istediginiz boyutta input ve alpha verebilirsiniz. Mesela A ve B için iki tane renk (rgb yani 3 boyutlu) verelim. Alpha degeri olarak da 3 boyutlu bi vektör verelim. Alphanın içindeki her kanalı degiştirdiginizde A ve B için de geçerli olan alpha degeri degişir. Mesela r (red) degiştirirseniz A ve B nin r kanalı için alpha degerini belirlemiş olursunuz ama sadece r kanalı için, diger iki kanalı da yine Alphanın içindeki kanallardan degiştirmeniz gerek.

* #### [LinearSine]()
The LinearSine function takes in a scalar value and outputs the linear sine (or rounded linear sine) of that value, running between 0 and 1. If you connect a Time expression to the value input and use the Linear Sine, you can see animation in the output that coincides with a linear sine wave.

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
Verilen inputun 1 den çıkarılmış halini döndürür. 

* #### [Pi]()
Pi.

* #### [Power](https://youtu.be/zR7ZjwpNV5c)
Verilen inputun (sayı) kuvvetini alır.

* #### [ProjectVectorOntoPlane]()


* #### [QuadraticFormula]()


* #### [RGBtoHSV]()


* #### [RadiansToDegrees]()


* #### [RayTracedSphere]()


* #### [Remap]()
Verdigimiz inputtaki belirli bir aralıgı (range) başka bi aralıga almamızı saglar (acaba :D). İnput Low ve High arasındaki sayıların hepsi Target Low ve High arasına taşınır ama DİKKAT bu işlem random degil yani bi orana göre gidiyor, mesela verdiginiz İnput, İnput Low ve High ın tam ortasında ise o zaman output da Target Low ve High ın da tam ortasında olacaktır. Ayrıca verdiginiz İnput, İnput Low ve High dışında olsa bile bu node herşeyi orana göre degiştirecektir. Yani mesela İnputunuz İnput High dan daha yüksek, verdiginiz İnput orana göre düzenlenecek ve output yine bu orana göre olacaktır. Eger İnput Low ve High arasında bi remap yapmak istiyorsanız if kullanıp düzenleme yaparak küçük ve büyük degerleri remap dışına alabilirsiniz.


* #### [RemapValueRange](https://youtu.be/V0by6a5Xesk)
Verdigimiz inputtaki belirli bir aralıgı (range) başka bi aralıga almamızı saglar (acaba :D). İnput Low ve High arasındaki sayıların hepsi Target Low ve High arasına taşınır ama DİKKAT bu işlem random degil yani bi orana göre gidiyor, mesela verdiginiz İnput, İnput Low ve High ın tam ortasında ise o zaman output da Target Low ve High ın da tam ortasında olacaktır. Ayrıca verdiginiz İnput, İnput Low ve High dışında olsa bile bu node herşeyi orana göre degiştirecektir. Yani mesela İnputunuz İnput High dan daha yüksek, verdiginiz İnput orana göre düzenlenecek ve output yine bu orana göre olacaktır. Ayrıca bu node fonksiyon oldugu için inputlara illaki bişeler baglamanız gerekiyo, node üzerinden veremiyorsunuz, bu da kodları çok karıştırıyo. Bu yüzden "Remap" isimli diger nodeu kullanın, o da bununla aynı işi yapıyor. Ayrıca son bi tavsiye, eger İnput Low ve High arasında bi remap yapmak istiyorsanız if kullanıp düzenleme yaparak küçük ve büyük degerleri remap dışına alabilirsiniz.


* #### [RemapValueRangeNormalized]()
Sıfır ve bir arasında clamp yapar. Clamp(0, 1) ile eşit yani. Kullanmayın bile.


* #### [Round]()
Verilen inputu (sayı) yuvarlar.


* #### [SafeNormalize]()


* #### [Saturate]()
Sıfır ve bir arasında clamp yapar. Clamp(0, 1) ile eşit yani. Kullanmayın bile.

* #### [Sign]()
The Sign node indicates whether a numeric input is negative, positive, or exactly 0.

* #### [Sine](https://youtu.be/gn5Zbsq8eFs)
Sine yani sinüs, sürekli 1 ve 0 arasında dönen bi dalga. Kendini tekrar eder, çogu durumda kullanışlıdır. İnput olarak time nodeunu baglayabilirsiniz, böylelikle sürekli tekrarlayan bi deger döndürür. Linkteki videoda görseller ile anlatılmış kesin izleyin. (Bkz. Cosine)

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


## Niagara

* #### [Niagara_MeshReproductionSpriteUVs]()



## Normals

* #### [BlendAngleCorrectedNormals]()



## Opacity

* #### [Chroma_Key_Alpha]()


* #### [SoftOpacity]()
The SoftOpacity function takes in an Opacity value and then runs a variety of calculations on it to give it a softer feel. It applies a Fresnel effect, and depth-based alpha, and pixel depth. The end result causes the object to fade away as the camera approaches it.


## Parameter

* #### [ChannelMaskParameter]()


* #### [CollectionParameters]()
A Collection Parameter expression is used to reference a Parameter Collection asset. These are groups of parameters that can easily be reused by many different assets such as Materials, Blueprints, and much more. For more information on Parameter Collections, be sure to read the Parameter Collections Documentation.

* #### [CurveAtlasRowParameter]()


* #### [DynamicParameter]()
The DynamicParameter expression provides a conduit for particle emitters to pass up to four values to the material to be used in any manner. These values are set in Cascade via a ParameterDynamic module placed on an emitter.

* #### [FontSampleParameter]()
The FontSampleParameter expression provides a way to expose a font-based parameter in a material instance constant, making it easy to use different fonts in different instances. The alpha channel of the font will contain the font outline value. Only valid font pages are allowed to be specified.

* #### [MaterialAttributeLayers]()


* #### [RuntimeVirtualTextureSampleParameter]()


* #### [ScalarParameter(Param)]()
The ScalarParameter expression outputs a single float value (Constant) that can be accessed and changed in an instance of the material or on the fly by code.

* #### [StaticBoolParameter]()


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


## PivotPainter

* #### [PivotPainter_HierarchyData]()
This particular function is specifically designed to work with object hierarchies.

* #### [PivotPainter_PerObjectData]()
This particular function is designed to work on a per-object basis.

* #### [PivotPainter_PerObjectFoliageData]()
This function is designed to work specifically with individual foliage objects.

* #### [PivotPainter_TreeData]()
The outputs starting with tree process the model's UV information as it would be stored by the Pivot Painter MAXScript. The outputs starting with Leaf process the UV information as it would be stored by the per-object pivot painting section of the script.


## PivotPainter2

* #### [PivotPainter2FoliageShader]()


* #### [ms_PivotPainter2_CalculateMeshElementIndex]()


* #### [ms_PivotPainter2_Decode8BitAlpahAxisExtent]()


* #### [ms_PivotPainter2_DecodeAxisVector]()


* #### [ms_PivotPainter2_DecodePostion]()


* #### [ms_PivotPainter2_ReturnParentTextureInfo]()


* #### [ms_PivotPainter2_UnpackIntegerAsFloat]()



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


## RenderToTexture

* #### [TransformImposterNormals]()



## Shading

* #### [AxisAlignedFresnel]()


* #### [CalcLightsourceAngle]()


* #### [Ellipsoid-ConeShadow-Texture]()


* #### [FuzzyShading]()
This function emulates a surface similar to velvet or moss, and is similar to a Fresnel calculation. Incidentally, it is also useful for shader effects such as a scanning electron microscope.

* #### [FuzzyShadingGrass]()
This function is designed to provide the diffuse portion of grass shading. Similar to FuzzyShading, this function allows you to blend in a new color at the edges by first desaturating by a given percentage and then applying a custom color to the desaturated area.

* #### [MetallicShading]()


* #### [Sphere-ConeShadow-Texture]()


* #### [Sphere_AO]()


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



## Speed Tree

* #### [SpeedTree]()



## SpeedTree

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
UVs = Texturecoordinate baglayın
<br>
Rotation Center = Dönme efektinin orta noktası
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
WorldAlignedNormal takes in a normal map and aligns its texture to the world, rather than locally to the object. It also allows for scaling in world units, rather than as a percentage of the texture size.

* #### [WorldAlignedTexture]()
The WorldAlignedTexture function serves as a way to tile a texture across the surface of an object in world space, independently of that object's size or rotation. This function allows you to specify the direction in which the texture will be projected, and offers scaling in world units rather than as a percentage of the texture size.

* #### [WorldAlignedTexture_Complex]()


* #### [WorldAlignedTexture_MipBias]()


* #### [WorldAlignedTexture_SeperateChannels]()


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
İsimlendirilmiş düzenleme nodeu.

* #### [Add Reroute Node]()
Düzenleme nodeu.

* #### [AntialiasedTextureMask]()
The AntialiasedTextureMask expression allows you to create a material using a soft (anti-aliased) transition mask. The mask can be used to blend between two complex material properties or to fade out an alpha blended material (works well with SoftMasked). Simply specify a texture with the mask specified in one channel (red, green, blue, or alpha), set the used channel in the expression and specify the comparison value. Assuming the channel stores a grayscale value in the range 0 = black to 1 = white the comparison function defines if the resulting mask should be 0 or 1. This expression is a parameter, allowing the Texture property to be overridden by child MaterialInstances.

* #### [AtmosphericLightColor]()


* #### [AtmosphericLightVector]()


* #### [BentNormalCustomOutput]()


* #### [BlackBody](https://youtu.be/yxN7lf0MuvE)
Verilen sıcaklık derecesine göre (sanırım kelvin) renk döndürüyor. Kullanmayın bile.

* #### [BumpOffset](https://youtu.be/70EzAb4CrmA)
Bu node ek ayar yapmadan derinlik efekti vermenize yarar. Mesela duvar yaptınız, tuglalar arasında derinlik olmasını istiyorsunuz. Bu node verilen yükseklik mapine göre siyah olan kısımları geride, beyaz olan kısımları daha önde gösteren bi efekt verir. Mesela yükseklik mapi, texturenin bir kanalı olabilir, eger siyah ve beyaz kısımlar güzel görünüyorsa çalışacaktır. Output olarak gelen degeri texturelar için UV olarak ve ya normal mapler için UV olarak kullanabilirsiniz. Parametreleri,
<br>
<br>
Coordinate = Texture Coordinate verebilirsiniz.
<br>
Height = Yükseklik mapi, mesela texturenin bir kanalı olabilir.
<br>
HeightRatioInput = Artıya gittikçe efektin etkisi artar. Eksileri kullanmıyoruz. Ayrıca bu ayarı unreal enginenin önerilen ayar aralıgında, 0.02 ve 0.1 arasında kullanın.

* #### [ChannelMaskParameter]()


* #### [ClearCoatNormalCustomOutput]()


* #### [ConstantBiasScale]()
The ConstantBiasScale expression takes an input value, adds a bias value to it, and then multiplies it by a scaling factor outputting the result. So for example, to convert input data from [-1,1] to [0,1] you would use a bias of 1.0 and a scale of 0.5.

* #### [DDX]()
The DDX expression exposes DDX derivative calculation, a GPU hardware feature used in pixel shader calculation.

* #### [DDY]()
The DDY expression exposes DDX derivative calculation, a GPU hardware feature used in pixel shader calculation.

* #### [DepthFade](https://youtu.be/2BxrGjPcirk)
Saydam meshler opak olanlar ile kesiştiginde ne olacagını ayarlayabilirsiniz. Parametreleri,
<br>
<br>
Opacity = Opaklık, sıfırdan (saydam) başlar, arttırdıkça opak olur.
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


* #### [FeatureLevelSwitch]()
The Feature Level Switch node allows you to make simplified materials for lower powered devices. 

* #### [Fresnel](https://youtu.be/PLwEwIYX454)
Bu materyale sahip meshe bakıldıgında, meshin orta kısımları 0a yakın, kenara yakın tarafları 1e yakın bir deger döndürür. Bu degerler ile meshe ayar yapabilirsiniz. Parametreler,
<br>
<br>
ExponentIn = Kenarlardan ortaya dogru, fresnelin etkisi diyebiliriz, yani bunu ne kadar arttırırsanız fresenel o kadar etkili olur.
<br>
BaseReflectFractionIn = Yansıtma degeri, Bu da ExponentIn in aynısı ama dıştan içe degil, her yere etki eder. Eger bunu azaltırsanız yansıma olmaz yani fresnel heryeri kaplar, eger arttırırsanız fresnelin etkisi azalır.

* #### [GIReplace]()
GIReplace allows artists to specify a different, usually simpler, expression chain when the material is being used for GI.

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
Scale = Texture büyüklügü, 0 dan başlar yükselttikçe texture da büyür.
<br>
Quality = Kaliteyi arttırır.
<br>
Function = Burdan deseni oluşturan fonksiyonu seçiyoruz. Bunları tek tek anlatamam kendiniz test edin ve ya [bakın](https://youtu.be/hP3P3WH4TjM?t=124).
<br>
Turbulence = Test etsem bile anlayamadım, aralardaki boşlugu arttırıyo ve ya birleştiriyo olmalı.
<br>
Levels = Düşükken köşeler sanki çizgi film gibi, arttırınca detaylar daha çok ortaya çıkıyor.
<br>
Output Min = Genellikle ne kadar siyah olacagını seçersiniz, -5 ve 0 arasında denebilir.
<br>
Output Max = Genellikle ne kadar beyaz olacagını seçersiniz, 0 ve 1 arasında denebilir.
<br>
Level Scale = 0 dan uzaklaştıkça (eksi artı farketmez) çizgilerin köşeleri düzleşir.
<br>
Position = Sanırım sadece 3 boyutlu vektör kabul ediyor, Texturenin pozisyonunu ayarlar.
<br>
Filter Width = Her nokta (ve ya çizgi) arasındaki mesafeyi arttırır.


* #### [QualitySwitch](https://youtu.be/64I4rzyZ6_Q)
İf gibi, duruma göre ayar yapmanızı saglar. Oyundaki kalite neyse, o inputa baglı olan şeyi output olarak verir. Default, eger herhangi bir inputa bir şey baglamadıysanız çalışır. Mesela Low a hiçbir şey baglamadınız, eger kalite low da ise o zaman low baglı olmadıgı için Defaulta ne baglıysa o kullanılır. Zaten Defaultu boş bırakamazsınız.

* #### [RayTracingQualitySwithc]()


* #### [ReflectionCapturePassSwitch]()


* #### [RotateAboutAxis](https://youtu.be/ljWoJ7Pp9Ww)
Materyale dönme efekti kazandırır ama kendi çevresinde degil, dünya içinde. Ayrıca bu dönme efekti hareket olarak degil sadece görünüş olarak olan bir dönme efektidir. Yani dönme efektinden sonra materyalin yeri ne kadar degişse de aslında materiyal ilk koydugunuz konumdadır. RotateAboutAxis ile materyale istediginiz yönde dönme efekti verebilir bunu otomatikleştirebilirsiniz de. Linkteki videoyu izleyin çünkü yazı ile anlatmak bi anlam ifade etmiyor, eger izlediyseniz yazdıklarımı anlayacaksınız. Parametreleri,
<br>
<br>
NormalizedRotationAxis = 3 boyutlu vektör verin, hangi yöne dogru dönme efekti olmasını istiyorsanız o boyuta 1 degeri verin, 1 degeri verdikleriniz dönme yönünü ifade eder.
<br>
RotationAngle = Ne kadar dönme efekti uygulanacagı, 0 ve 1 arasında, 1 = tam tur
<br>
PivotPoint = RotationAngle olarak time nodeu baglayın. PivotPointi parametreye dönüştürün ve dönme efektinin izledigi yolu takip edin. Normalde daire çizer. Şimdi siz eger PivotPointin herhangi bir yönünü mesela R, arttırırsanız, dönme efektinin çizdigi daire yolunun R yönüne dogru kaymaya başladıgını görürsünüz. Daha dogrusu daireyi sündürürsünüz. Çok fazla arttırırsanız daire çok süner ve dönme efektinin izledigi yol sanki bir yumurta gibi olur. Diger boyutlar ile birlikte bu şekilde dönme efektinin izledigi daireyi büyütebilirsiniz.
<br>
Position = World Position baglayın
<br>
Period (node üzerinde) = Normalde 1 dir. Eger arttırsanız, mesela 5 yaparsanız, 5 kat yavaşlar, yani 1 tur atması 5 kat daha yavaş olur. Aynı şekilde, azaltarak hızlandırabilirsiniz.

* #### [ShaderStatgeSwtich]()


* #### [ShadingPathSwtich]()


* #### [ShadowPassSwitch]()


* #### [SmoothStep]()


* #### [SphereMask](https://youtu.be/xRxkcFOhNrc)
The SphereMask expression outputs a mask value based on a distance calculation. If one input is the position of a point and the other input is the center of a sphere with some radius, the mask value is 0 outside and 1 inside with some transition area. This works on one, two, three, and four component vectors

* #### [Step]()


* #### [VectorNoise]()
The Vector Noise Material expression adds several more 3D or 4D vector noise results to use in your Materials. Due to the run-time expense of these functions, it is recommended that once a look is developed with them, all or part of the computation be baked into a Texture using the Draw Material to Render Target Blueprint feature introduced in Unreal Engine 4.13 and later. These Material graph Expressions allow procedural looks to be developed in the engine on final assets, providing an alternative to creating procedurally generated Textures with an external tool to apply to assets in UE4. Inside of the Vector Noise Material Expression, you will find the following Vector Noise types.

* #### [VertexInterpolator]()



## Utillity

* #### [BoxMask-2D]()


* #### [BoxMask-3D]()


* #### [GeneratedRoundRect]()



## Utils

* #### [DecalDerivative]()


* #### [DecalLifetimeOpacity]()


* #### [DecalMipmapLevel]()



## VFX

* #### [AppendMany]()
İnput olarak verdigimiz her sayıyı (constant) birleştirir ve vektör oluşturur.



## Vector

* #### [ActorPositionWS](https://youtu.be/Kn3ZQ8TxZoE)
ActorPositionWS outputs Vector3 (RGB) data representing the location of the object with this material on it in world-space.

* #### [CameraPositionWS](https://youtu.be/MRbjCXf1hmg)
Kameranın pozisyonunu dünyaya göre 3d (vektör) olarak verir.

* #### [CameraVectorWS]()
The CameraVector expression outputs a three-channel vector value representing the direction of the camera with respect to the surface, in other words, the direction from the pixel to the camera.

* #### [Constant2Vector]()
The Constant2Vector expression outputs a two-channel vector value, in other words, two constant numbers.

* #### [Constant3Vector]()
The Constant3Vector expression outputs a three-channel vector value, in other words, three constants numbers. An RGB color can be thought of as a Constant3Vector, where each channel is assigned to a color (red, green, blue).

* #### [Constant4Vector]()
The Constant4Vector expression outputs a four-channel vector value, in other words, four constants numbers. An RGBA color can be thought of as a Constant4Vector, where each channel is assigned to a color (red, green, blue, alpha).

* #### [LightVector]()
This expression has been deprecated in Unreal Engine 4 as lighting calculations are now deferred.

* #### [ObjectBounds]()
The Object Bounds expression outputs the size of the object in each axis. If used as color, the X, Y, and Z axes correspond to R, G, and B, respectively.

* #### [ObjectOrientation](https://youtu.be/eDlSIm0BL6g)
Bu materyale sahip olan objenin yön bilgisini verir (3d vektör). Mesela eger X eksenine dönükse (1, 0, 0), Y eksenine dönükse (0, 1, 0), Z eksenine dönükse (0, 0, 1) verir. Bu deger aralarda da olabilir, obejenin yönüne göre.

* #### [ObjectPositionWS](https://youtu.be/P530OKEXCJo)
Bu materyale sahip olan objenin konum bilgisini verir (3d vektör).

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


* #### [SkinningVertexOffsets]()


* #### [VertexNormalWS]()
The VertexNormalWS expression outputs the world-space vertex normal. It can only be used in material inputs that are executed in the vertex shader, like WorldPositionOffset. This is useful for making a mesh grow or shrink. Note that offsetting position along the normal will cause the geometry to split apart along UV seams.

* #### [VertexTangentWS]()



## VectorOps

* #### [AppendVector(Append)](https://youtu.be/pFkth9GKci4)
Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür. En fazla 4 boyutlu vektör yapılabilir, eger 3 + 2 gibi bir işlem yaparsanız hata verecektir, ama 3 + 1 yaparsanız sanki birinci inputa alpha degeri ekliyormuşsunuz gibi toplar ve 4 boyutlu vektör döndürür.

* #### [ComponentMask(Mask)]()
İnput olarak verdigimiz vektörden (1 boyuttan fazla), istedigimiz kanalı alabilmemizi saglar.

* #### [CrossProduct]()
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

* #### [CameraDirectionVector]()


* #### [CameraVectorWithWPOOptions]()


* #### [OctahedronToUnitVector]()


* #### [RotateVector]()


* #### [UnitVectorToOctahedron]()



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



## WPO

* #### [ManualWorldToScreenUVsTransform]()


* #### [UnpackDirection]()



## Water

* #### [NewComment]()


* #### [SceneDepthWithoutWater]()


* #### [SingleLayerWaterMaterialOutput]()


* #### [Sobol]()


* #### [TemporalSobol]()



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
