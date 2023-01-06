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

* #### [DiffColorKeyerErodeSinglePass]()
Kullanışsız (https://youtu.be/CEUGMFLjc4Y), renkleri silmede kullanılıyor.

* #### [MF_Chromakeyer]()
Kullanışsız (https://youtu.be/CEUGMFLjc4Y), renkleri silmede kullanılıyor.


## Color

* #### [Desaturation]()
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


* #### [PerInstanceRandom]()


* #### [PrecomputedAOMask]()
The PrecomputedAOMask node lets you access Lightmass-calculated ambient occlusion (AO) in your Material, which can be useful for procedural texturing or for adding in aging effects and dirt in areas where it would slowly accumulate over time.

* #### [Time]()
Oyun başladıgı andan itibaren geçen süreyi verir. Eger editördeyseniz editörde geçen süreyi verir. Degeri görüntülemek için DebugScalarValues nodeunu kullanabilirsiniz.

* #### [TwoSidedSign]()
Eger materyalinizin iki yüzlü ve iki yüzünde ayrı textureler olmasını istiyorsanız bunu kullanabilirisiniz. Lerp (LinearInterpolate) nodeuna alpha degeri olarak TwoSidedSign nodeunu baglayın.

* #### [VertexColor]()
The VertexColor expression is the access point for the material to the outputs of color modules affecting sprite particles emitters.

* #### [View Property]()
Materyalleri sürekli degiştirebilmeniz/güncelleyebilmeniz ve işlemler yapabilmeniz için, dünya ve oyuncular hakkında bilgiler verir. parametreleri,
Render Target Size = Ekran büyüklügü ile ilgili bişe
Field of View = Görüş alanı
View Size = Render Target Size ile aynı
View Position (Absolute World Space) = Konumumuzu verir (3 boyutlu vektör)
Camera Position (Absolute World Space) = Kameramızın konumunu verir (3 boyutlu vektör)


## Coordinates

* #### [ActorPositionWS]()
Aktörün pozisyonunu dünyaya göre 3d (vektör) olarak verir.

* #### [CameraPositionWS]()
Kameranın pozisyonunu dünyaya göre 3d (vektör) olarak verir.

* #### [LightmapUVs]()
Lightmap UV için texture coordinatelerini verir. X ve Y için iki boyutlu bir vektör verir. Eger Lightmap UV açık degilse 0 verir.

* #### [MapARPassThroughCameraUV]()


* #### [ObjectOrientation]()
The ObjectOrientation expression outputs the world-space up vector of the object. In other words, the object's local positive z-axis is pointing in this direction.

* #### [ObjectPositionWS]()
The ObjectPositionWS expression outputs the world-space center position of the object's bounds. For example, this is useful for creating spherical lighting for foliage.

* #### [ObjectRadius]()
The Object Radius outputs a value equal to the radius of a given object in Unreal units. Scaling is taken into account and the results can be unique for each individual object.

* #### [Panner]()
Texturelara hareket vermenize yarar.

* #### [ParticlePositionWS]()


* #### [ParticleSubUVProperties]()


* #### [PixelNormalWS]()
The PixelNormalWS expression outputs vector data representing the direction that pixels are facing based on the current normal.

* #### [Rotator]()
The Rotator expression outputs UV texture coordinates in the form of a two-channel vector value that can be used to create rotating textures.

* #### [SceneTexelSize]()
The SceneTexelSize expression allows you to offset by texel sizes, as you would when using the SceneColor and SceneDepth expressions. This is useful for edge detection in multi-resolution systems, as without this calculation you would be forced to use a small static value, resulting in inconsistent results at lower resolutions.

* #### [ScreenPosition]()
The ScreenPosition expression outputs the screen-space position of the pixel currently being rendered.

* #### [TextureCoordinate(TexCoord)]()
Textureların UV (tekrarlama) degerini ayarlamamıza yarar. Tiling (tekrarlama) aynı materyali farklı boyutlardaki meshlerde de kullanacagımız zaman materyale meshin boyutuna göre bi oran vermemizi saglar. parametreleri,
UTiling = x ekseninde (yatay) takrarlama sayısı
VTiling = y ekseninde (dikey) takrarlama sayısı

* #### [VertexNormalWS]()
The VertexNormalWS expression outputs the world-space vertex normal. It can only be used in material inputs that are executed in the vertex shader, like WorldPositionOffset. This is useful for making a mesh grow or shrink. Note that offsetting position along the normal will cause the geometry to split apart along UV seams.

* #### [ViewSize]()
The ViewSize expression outputs a 2D vector giving the size of the current view in pixels. This is useful for causing various changes in your materials based on the current resolution of the screen.

* #### [WorldPosition]()
The WorldPosition expression outputs the position of the current pixel in world space. To visualize, simply plug the output into Emissive


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


* #### [DebugBinaryValues-Int]()


* #### [DebugFloat2Values]()
Verilen 2 boyutlu vektörü gösteren bi texture döndürür.

* #### [DebugFloat3Values]()
Verilen 3 boyutlu vektörü gösteren bi texture döndürür.

* #### [DebugFloat4Values]()
Verilen 4 boyutlu vektörü gösteren bi texture döndürür.

* #### [DebugOnOff]()


* #### [DebugScalarValues]()
Verilen sayıyı (constant) gösteren bi texture döndürür.

* #### [DebugTimeSine]()



## Decals

* #### [StaticMeshDecal_Function]()



## Density

* #### [BeersLaw]()


* #### [RayMarchHeightMap]()



## Depth

* #### [DepthFade]()
The DepthFade expression is used to hide unsightly seams that take place when translucent objects intersect with opaque ones.

* #### [DepthFromWorldPosition]()


* #### [PixelDepth]()
The PixelDepth expression outputs the depth, or distance from the camera, of the pixel currently being rendered.

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


* #### [LinearGradient]()
The LinearGradient function uses UV channel 0 to generate a linear gradient in either the U or V direction, depending on which output is used.

* #### [RadialGradientExponential]()
The RadialGradientExponential function uses UV channel 0 to produce a radial gradient, giving the user the ability to adjust the radius and offset the center point.

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


* #### [Abs]()
Mutlak deger.

* #### [Add]()
Toplama.

* #### [AddComponents]()
Verdiginiz vektörden (2, 3, 4) her boyutundaki sayıları toplar. mesela (30, 50, 200) şeklinde 3 boyutlu bi vektör verdiniz, sonuç olarak 30 + 50 + 200 = 280 alırsınız.

* #### [AngleBetweenVectors]()


* #### [Append3Vector]()
AppendVector(Append) için geçerli olan kurallar bunda da geçerlidir. Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür.

* #### [Append4Vector]()
AppendVector(Append) için geçerli olan kurallar bunda da geçerlidir. Verilen inputları birbirine yeni boyut olarak ekler ve daha fazla boyuta sahip vektör döndürür.

* #### [AppendVector(Append)]()
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


* #### [Ceil]()
Verdiginiz sayıyı en yakın küçük tamsayıya yuvarlar. örnegin 
9.9 -> 9
9.1 -> 9

* #### [Clamp]()
The Clamp expression takes in value(s) and constrains them to a specified range, defined by a minimum and maximum value. A minimum value of 0.0 and maximum value of 0.5 means that the resulting value(s) will never be less than 0.0 and never greater than 0.5.

* #### [ComponentMask(Mask)]()
The ComponentMask expression allows you to select a specific subset of channels (R, G, B, and/or A) from the input to pass through to the output. Attempting to pass a channel through that does not exist in the input will cause an error, unless the input is a single constant value. In that case, the single value is passed through to each channel. The current channels selected to be passed through are displayed in the title bar of the expression.

* #### [Cosine]()
The Cosine expression outputs the value of a cosine wave over the input range of [0, 1] and the output range of [-1, 1], both repeating. Most commonly, this is used to output a continuous oscillating waveform by connecting a Time expression to its input, but it can also be used to create ripples in worldspace or screenspace, or any other application where a continuous, smooth cycle is needed. A visual representation of the wave is shown below, scaled to the [0, 1] output range:

* #### [CreateThirdOrthogonalVector]()


* #### [CrossProduct]()
The CrossProduct expression computes the cross product of two three-channel vector value inputs and outputs the resulting three-channel vector value. Given two vectors in space, the cross product is a vector that is perpendicular to both of the inputs.

* #### [CylinderIntersection]()


* #### [DegreesToRadians]()


* #### [DeriveNormalZ_Function]()


* #### [Divide]()
Bölme.

* #### [DotProduct]()
The DotProduct expression computes the dot product, which can be described as the length of one vector projected onto the other, or as the cosine between the two vectors multiplied by their magnitudes. This calculation is used by many techniques for computing falloff. DotProduct requires both vector inputs to have the same number of channels.

* #### [Floor]()
Verdiginiz sayıyı en yakın büyük tamsayıya yuvarlar. örnegin 
9.9 -> 10
9.1 -> 10

* #### [Fmod]()
Verilen A sayısını (constant) B sayısına (constant) böler ve kalanı verir. örn,
30 / 20 = 10
7 / 3 = 1

* #### [Frac]()
The Frac expression takes in values and outputs the fractional portion of those values. In other words, for an input value "X", the result is "X minus Floor of X". The output value will range from zero to one, inclusive on the low end, but not the high end. See also Ceil and Floor.

* #### [If]()
Duruma/koşula göre yapılacak işlemi seçmemize yarar. İki input alıyor A ve B. Üç seçenek sunuyor 
A > B
A == B
A < B
Diyelim ki A = 100 ve B = 10. A B den büyük oldugu için sonuç A > B seçenegine verdigimiz şey olacaktır. Eger A ve B birbirine eşit olsa A == B seçenegine verdigimiz şey sonuç olarak döndürülecekti. Eger A B den küçük olsa A < B seçenegine verdigimiz şey sonuç olarak döndürülecekti. Yani verdigimiz koşula göre hangi işlemin yapılması gerektigini belirliyoruz.

* #### [InverseLinearInterpolate]()


* #### [InverseTransformMatrix]()


* #### [LineIntervalIntersection]()


* #### [LinearInterpolate(Lerp)]()
Verilen alpha degerine göre iki inputu (resim ve ya renk) birbirine karıştırır. İstedigimiz boyutta constant verebiliriz, hem alpha hem de inputlarımız için. Örnegin bir boyutlu constant yani sayı kullanalım, A ve B için iki sayı girin mesela 10 ve 0. Eger alpha degerine 0 verirseniz A, 1 verirseniz B degeri döndürülür. Eger alpha degerine 0.5 verirseniz sayımız da A ve B nin ortası yani 5 olur. Yani 0 a yaklaştıkça A, 1 e yaklaştıkça B. Ayrıca dedigim gibi, istediginiz boyutta input ve alpha verebilirsiniz. Mesela A ve B için iki tane renk (rgb yani 3 boyutlu) verelim. Alpha degeri olarak da 3 boyutlu bi vektör verelim. Alphanın içindeki her kanalı degiştirdiginizde A ve B için de geçerli olan alpha degeri degişir. Mesela r (red) degiştirirseniz A ve B nin r kanalı için alpha degerini belirlemiş olursunuz ama sadece r kanalı için, diger iki kanalı da yine Alphanın içindeki kanallardan degiştirmeniz gerek.

* #### [LinearSine]()
The LinearSine function takes in a scalar value and outputs the linear sine (or rounded linear sine) of that value, running between 0 and 1. If you connect a Time expression to the value input and use the Linear Sine, you can see animation in the output that coincides with a linear sine wave.

* #### [Logarithm10]()
The Logarithm10 node returns the base-10 logarithm, also called the common logarithm, of the input value. That is, if you take a base value of 10 and raise it to the power of the number returned by this expression, you would get the input value.

* #### [Logarithm2]()
The Logarithm2 node returns the base-2 logarithm of the input value. That is, if you take a base value of 2 and raise it to the power of the number returned by this expression, you would get the input value.

* #### [MakeVectorsOrthogonal]()


* #### [Max]()
Verilen iki inputtan büyük olanı döndürür.

* #### [Min]()
Verilen iki inputtan küçük olanı döndürür.

* #### [Multiply]()
Çarpma.

* #### [MultiplyAdd]()


* #### [Normalize]()
The Normalize expression calculates and outputs the normalized value of its input. Normalized vectors (also called "unit vectors") have an overall length of 1.0. This means each component of the input is divided by the total magnitude (length) of the vector.

* #### [OneMinus]()
Verilen inputun 1 den çıkarılmış halini döndürür. 

* #### [Pi]()
Pi.

* #### [Power]()
Verilen inputun (sayı) kuvvetini alır.

* #### [ProjectVectorOntoPlane]()


* #### [QuadraticFormula]()


* #### [RGBtoHSV]()


* #### [RadiansToDegrees]()


* #### [RayTracedSphere]()


* #### [RemapValueRange]()


* #### [Round]()
Verilen inputu (sayı) yuvarlar.


* #### [SafeNormalize]()


* #### [Saturate]()
Verilen input (sayı) eger sıfırdan düşük ise sıfıra, eger birden büyük ise bire, eger sıfır ve bir arasında ise hiç bir degişiklik uygulanmaz.

* #### [Sign]()
The Sign node indicates whether a numeric input is negative, positive, or exactly 0.

* #### [Sine]()
The Sine expression outputs the value of a Sine wave over the input range of [0, 1] and the output range of [-1, 1], both repeating. The difference between this and the output of the Cosine expression is the output waveform is offset by one-quarter of the period, meaning that Cos(X) is equal to Sin(X + 0.25). 

* #### [Sine_Remapped]()


* #### [SmoothCeil]()


* #### [SmoothStep]()


* #### [SquareRoot]()
Verilen inputun karekökünü döndürür. Eger vektör verirseniz her degerinin karekökü ayrı ayrı alınır.

* #### [Step]()


* #### [Subtract]()
Çıkarma.

* #### [SumOfAConsecutiveNumberSequence]()


* #### [Tangent]()
The Tangent node outputs the tangent of the specified value.

* #### [Transform3x3Matrix]()


* #### [TransformToClipSpace]()


* #### [Truncate]()
The Truncate node truncates a value by discarding the fractional part while leaving the whole number untouched.

* #### [UnpackNormalFromFloat]()


* #### [VectorToRadialValue]()
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

* #### [GeneratedBand]()
The GeneratedBand function generates a horizontal or vertical band from the default TextureCoordinates.

* #### [GeneratedOffsetBands]()
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

* #### [CustomRotator]()
The CustomRotator function allows you to rotate a texture. However, it stands apart from the basic Rotator expression node in that it exposes a center point around which the image rotates. It also changes the rotation system to be 0-1 based, so that a value of 1 is considered a complete rotation, or 360 degrees. On a standard Rotator, a complete rotation requires a Time input of approximately 25.1.

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


* #### [BlackBody]()
The BlackBody expression simulates the effects of black body radiation within your Material. The user inputs a temperature (in Kelvin) and the resulting color and intensity can be used to drive Base Color and Emissive values to get a physically accurate result.

* #### [BumpOffset]()
BumpOffset is the Unreal Engine 4 term for what is commonly known as 'Parallax Mapping'. The Bump Offset expression allows a material to give the illusion of depth without the need for additional geometry. BumpOffset materials use a grayscale heightmap to give depth information. The brighter the value in the heightmap, the more 'popped out' the material will be; these areas will parallax (shift) as a camera moves across the surface. Darker areas in the heightmap are 'further away' and will shift the least.

* #### [ChannelMaskParameter]()


* #### [ClearCoatNormalCustomOutput]()


* #### [ConstantBiasScale]()
The ConstantBiasScale expression takes an input value, adds a bias value to it, and then multiplies it by a scaling factor outputting the result. So for example, to convert input data from [-1,1] to [0,1] you would use a bias of 1.0 and a scale of 0.5.

* #### [DDX]()
The DDX expression exposes DDX derivative calculation, a GPU hardware feature used in pixel shader calculation.

* #### [DDY]()
The DDY expression exposes DDX derivative calculation, a GPU hardware feature used in pixel shader calculation.

* #### [DepthFade]()
The DepthFade expression is used to hide unsightly seams that take place when translucent objects intersect with opaque ones.

* #### [DepthOfFieldFunction]()
The Depth of Field Function expression is designed to give artists control over what happens to a Material when it is being blurred by Depth of Field. It outputs a value between 0-1 such that 0 represents "in focus" and 1 represents "completely blurred." This is useful for interpolating between sharp and blurry versions of a texture, for instance. The Depth input allows for the existing results from the scene's Depth of Field calculations to be overridden by other calculations.

* #### [Distance]()
The Distance expression computes the (Euclidian) distance between two points/colors/positions/vectors and outputs the resulting value. This works on one, two, three and four component vectors, but both inputs to the expression must have the same number of channels.

* #### [DistanceFieldGradient]()
The DistanceFieldGradient Material Expression node, when normalized, outputs the X,Y,Z direction an object would move with in the distance field. This makes the Distance Field Gradient Material Expression node well-suited for Materials that need to simulate the flow of liquids.

* #### [DistanceToNearestSurface]()
The Distance To Nearest Surface Material Expression node allows Materials to sample any point in the levels Global Distance Field. This Material Expression works by outputting the signed distance in world space units from the distance field to the nearest occluders in the scene.

* #### [EyeAdaptation]()


* #### [FeatureLevelSwitch]()
The Feature Level Switch node allows you to make simplified materials for lower powered devices. 

* #### [Fresnel]()
The Fresnel expression calculates a falloff based on the dot product of the surface normal and the direction to the camera. When the surface normal points directly at the camera, a value of 0 is output. When the surface normal is perpendicular to the camera, a value of 1 is output. The result is clamped to [0,1] so you do not have any negative color in the center.

* #### [GIReplace]()
GIReplace allows artists to specify a different, usually simpler, expression chain when the material is being used for GI.

* #### [InverseLinearInterpolate]()


* #### [LightmassReplace]()
The LightmassReplace expression simply passes through the Realtime input when compiling the material for normal rendering purposes, and passes through the Lightmass input when exporting the material to Lightmass for global illumination. This is useful to work around material expressions that the exported version cannot handle correctly, for example WorldPosition.

* #### [LinearInterpolate]()
The LinearInterpolate expression blends between two input value(s) based on a third input value used as a mask. This can be thought of as a mask to define transitions between two textures, like a layer mask in Photoshop. The intensity of the mask Alpha determines the ratio of color to take from the two input values. If Alpha is 0.0, the first input is used. If Alpha is 1.0, the second input is used. If Alpha is between 0.0 and 1.0, the output is a blend between the two inputs. Keep in mind that the blend happens per channel. So, if Alpha is an RGB color, Alpha's red channel value defines the blend between A and B's red channels independently of Alpha's green channel, which defines the blend between A and B's green channels.

* #### [MaterialProxyReplace]()


* #### [Noise]()
The Noise expression creates a procedural noise field, giving you control over how it is generated.

* #### [QualitySwitch]()
The QualitySwitch expression allows for the use of different expression networks based on the engine is switched between quality levels, such as using lower quality on lower-end devices.

* #### [RayTracingQualitySwithc]()


* #### [ReflectionCapturePassSwitch]()


* #### [RotateAboutAxis]()
The RotateAboutAxis expression rotates a three-channel vector input given the rotation axis, a point on the axis, and the angle to rotate. It is useful for animations using WorldPositionOffset that have better quality than simple shears.

* #### [ShaderStatgeSwtich]()


* #### [ShadingPathSwtich]()


* #### [ShadowPassSwitch]()


* #### [SmoothStep]()


* #### [SphereMask]()
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

* #### [ActorPositionWS]()
ActorPositionWS outputs Vector3 (RGB) data representing the location of the object with this material on it in world-space.

* #### [CameraPositionWS]()
The CameraWorldPosition expression outputs a three-channel vector value representing the camera's position in world space.

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

* #### [ObjectOrientation]()
The ObjectOrientation expression outputs the world-space up vector of the object. In other words, the object's local positive z-axis is pointing in this direction.

* #### [ObjectPositionWS]()
The ObjectPositionWS expression outputs the world-space center position of the object's bounds. For example, this is useful for creating spherical lighting for foliage.

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

* #### [AppendVector]()
The AppendVector expression allows you to combine channels together to create a vector with more channels than the original. For example, you can take two individual Constants values and append them to make a two-channel Constant2Vector value. This can be useful for reordering the channels within a single texture or for combining multiple grayscale textures into one RGB color texture.

* #### [ComponentMask]()
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
