# Main Material Node
<img src="../../../../Dosyalar/Materyal_Editor_Main_Material_Node.jpg">


# Bölümler

* [Attributes](#attributes)
* [Physical Material](#physical-material)
* [Material](#material)


## [Attributes](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/)

* ### [Base Color](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#basecolor)
Materyalin ana rengidir, ışık yansıdıgında görünecek rengi belirler. Degerler 0-1 arasındadır. 0 siyah, 1 beyazı temsil eder.

* ### [Metallic](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#metallic)
Materyalin metalik olup olmayacagını belirler. Materyalin metalik olması az da olsa yansımayı etkiler. Degerler 0-1 arasındadır. 0 metalik olmayan, 1 metalik olanı temsil eder.

* ### [Specular](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#specular)
Materyalin ne kadar ışık yansıtacagını belirler. Materyalin specular olması parlaklıgı da etkiler. Degerler 0-1 arasındadır. 0 hiç yansıtmamayı, 1 tam yansıtmayı temsil eder.

* ### [Roughness](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#roughness)
Materyalin ne kadar pürüzlü oldugunu belirler. Materyalin ne kadar pürüzlü olup olmaması materyalin yansıtma özelligini en çok etkileyen etkendir. Degerler 0-1 arasındadır. 0 pürüzssüzü (ayna gibi yansıtma), 1 pürüzlüyü (yansıtmama) temsil eder.

* ### [Anisotropy](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#anisotropyandtangent)
Anisotropy ve Tangent nodlarının ne işe yaradıgını bilmiyorum, zaten çok kullanılmıyorlar, isterseniz linkten bakabilirsiniz.

* ### [Emissive Color](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#emissivecolor)
Emissive Color neon gibidir. Degerler 0-1 arasında degildir, istediginiz kadar arttırabilirsiniz. Base Color gibi verdiginiz rengi yansıtır ama degeri arttırdıkça neon gibi olur ve parlamaya başlar, etrafına ışık saçar. Parlaklıgı arttırıyormuşsunuz gibi.

* ### [Opacity](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#opacity)
Materyalin ne kadar opak oldugunu belirler. Degerler 0-1 arasındadır. 0 saydamı, 1 opagı temsil eder.

* ### [Opacity Mask](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#opacitymask)
Opacity gibidir ama ya saydam ya da opak olmak zorundadır. Yani Opacity gibi istediginiz derecede opaklık veremezsiniz. Degerler 0-1 arasındadır ama "Opacity Mask Clip Value" degerine altta olanlar 0a üstte olanlar 1e yuvarlanır. 0 saydamı, 1 opagı temsil eder.

* ### [Normal](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#normal)
Genellikle Normal Map şeklinde kullanılır. Normal, verilen degerlere göre bazı kısımları yüksek bazı kısımları alçak gösterir, yani 3d gibi, zaten bundan dolayı bazı yerlerde Height Map diye de geçer. Map diye kastedilen şey bir texture yani resimdir.

* ### [Tangent](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#anisotropyandtangent)
Anisotropy ve Tangent nodlarının ne işe yaradıgını bilmiyorum, zaten çok kullanılmıyorlar, isterseniz linkten bakabilirsiniz.

* ### [World Position Offset](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#worldpositionoffset)
World Position Offset konum degiştirme daha dogrusu hareket kazandırma amaçlı kullanılır. Blueprint ile yazmak yerine materyal içinde bunu yapabilmek çok büyük kolaylık. Bu materyale sahip olan meshlerin belirli hareketler yapmasını istediginizde kullanabilirsiniz. Konum degişse bile aslında meshin gerçek konumu degişmez yani aslında World Position Offset konumu degiştirmez.

* ### [Subsurface Color](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#subsurfacecolor)
Subsurface Color arkadan ışık vurdugunda, bizim gördügümüz taraftaki renge etki edecek rengi belirler. Yani arkadan bi ışık vurdugunda, materyalin içindeki şeyin rengi ortaya çıkmaya başlar, mesela insan cildi için ışık vurdugunda kan rengi olarak kırmızı rengin ortaya çıkması gibi, telefon ışıgıyla falan parmagınızı üstüne tutup görebilirsiniz.

* ### [Custom Data 0](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#customdata)
* ### [Custom Data 1](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#customdata)
* ### [Ambient Occlusion](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#ambientocclusion)
* ### [Refraction](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#refraction)
* ### [Pixel Depth Offset](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#pixeldepthoffset)
* ### [Shading Model](https://docs.unrealengine.com/5.1/en-US/material-inputs-in-unreal-engine/#shadingmodel)
* ### [Front Material]()




## [Physical Material]()

## [Material]()

### [Material Domain](https://docs.unrealengine.com/5.1/en-US/unreal-engine-material-properties/#material)

* #### [Surface](https://docs.unrealengine.com/5.1/en-US/unreal-engine-material-properties/#material)
* #### [Deferred Decal](https://docs.unrealengine.com/5.1/en-US/unreal-engine-material-properties/#material)
* #### [Light Function](https://docs.unrealengine.com/5.1/en-US/unreal-engine-material-properties/#material)
* #### [Volume](https://docs.unrealengine.com/5.1/en-US/unreal-engine-material-properties/#material)
* #### [Post Process](https://docs.unrealengine.com/5.1/en-US/unreal-engine-material-properties/#material)
* #### [User Interface](https://docs.unrealengine.com/5.1/en-US/unreal-engine-material-properties/#material)


### [Blend Mode](https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/Materials/MaterialProperties/BlendModes/)

* #### [Opaque](https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/Materials/MaterialProperties/BlendModes/#opaque)
Surface yani yüzey oluşturur, içerisinden ışık geçmez. Sadece bu, normal materyal.

* #### [Masked](https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/Materials/MaterialProperties/BlendModes/#masked)
[Opacity Mask](#opacity-mask) seçenegini aktifleştirir. [Translucent](#translucent) gibi degildir, [Opacity Mask](#opacity-mask) kullanılıp da silinmiş kısımlar motor tarafından hiç çizilmez, yansıma özellikleri de silinir yani. Eger bu özelliklerin kalmasını istiyorsanız [Translucent](#translucent) kullanmalısınız.

* #### [Translucent](https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/Materials/MaterialProperties/BlendModes/#translucent)
Türkçesi Saydam. [Opacity](#opacity) ve [Refraction](#refraction) seçenegini aktifleştirir.

* #### [Additive](https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/Materials/MaterialProperties/BlendModes/#additive)
[Opacity](#opacity) ve [Refraction](#refraction) seçenegini aktifleştirir. Additive'nin özelligi şudur, bu materyale sahip birden fazla mesh arka arkaya durursa, bizim görüş açımıza göre üst üste geldikleri kısımda, iki materyalin de renkleri toplanır. Toplanan deger sadece rengi degiştirmez yani sadece [Base Color](#base-color) gibi degildir, toplanan degerler çok fazla olursa [Emissive Color](#emissive-color) gibi etrafa renk saçmaya başlar, parlar.

* #### [Modulate](https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/Materials/MaterialProperties/BlendModes/#modulate)
Additive'e benzer. Modulate'in özelligi şudur, bu materyale sahip birden fazla mesh arka arkaya durursa, bizim görüş açımıza göre üst üste geldikleri kısımda, iki materyalin de renkleri çarpılır ve koyu renge sahip olur. Sanırım ışık ile uyumsuz oldugu için, [Shading Model](#shading-model-1)'ını ["Unlit"](#unlit) yapmak zorundasınız.

* #### [AlphaComposite (Premultiplied Alpha)](https://youtu.be/BtHgF_VmaSI?t=1856)
Particle Effects için iyi oldugu söyleniyor, pek bilgim yok.

* #### [AlphaHoldout](https://youtu.be/BtHgF_VmaSI?t=1914)
Sanırım ışık ile uyumsuz oldugu için, [Shading Model](#shading-model-1)'ını ["Unlit"](#unlit) yapmak zorundasınız. AlphaHoldout'un özelligi şudur, bu materyale sahip mesh, kendisinin arkasında duran saydam (burası çok önemli) materyale sahip meshleri görünmez yapar, yani arkasını gösterir. AlphaHoldout için [Opacity](#opacity) degeri vermelisiniz, bu bir şekil olabilir ve ya başka bir şey, sizin bakış açınıza göre AlphaHoldout arkasına gelen saydam materyallerin üzerinde görünmezlik efekti uygulayacaktır yani aldıgı [Opacity](#opacity) degerini arkasındaki saydam materyallere de uygular.



### [Shading Model](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/)

* #### [Unlit](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#unlit)
[Emissive Color](#emissive-color) kullanabiliyorsunuz. Unlit modu etrafa ışık saçmaz, verilen [Emissive Color](#emissive-color) degerine göre parlama efekti uygular, ama aslında etrafa ışık saçmaz.

* #### [Default Lit](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#defaultlit)
Default Lit modu ışıgı kullanır, ışık saçar. Yani ışıkla ilgili özellikler açıktır.

* #### [Subsurface](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#subsurface)
[Opacity](#opacity) ve [Subsurface Color](#subsurface-color) seçenegini aktifleştirir. Subsurface arkadan ışık vurdugunda, bizim gördügümüz taraftaki renge etki edecek rengi ayarlamamıza yarar. Yani arkadan bi ışık vurdugunda, materyalin içindeki şeyin rengi ortaya çıkmaya başlar, mesela insan cildi için ışık vurdugunda kan rengi olarak kırmızı rengin ortaya çıkması gibi, telefon ışıgıyla falan parmagınızı üstüne tutup görebilirsiniz.

* #### [Preintegrated Skin](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#preintegratedskin)
* #### [Clear Coat](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#clearcoat)
* #### [Subsurface Profile](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#subsurfaceprofile)
* #### [Two Sided Foliage](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#twosidedfoliage)
* #### [Hair](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#hair)
* #### [Cloth](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#cloth)
* #### [Eye](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#eye)
* #### [Single Layer Water](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#singlelayerwater)
* #### [Thin Translucent](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#thintranslucent)
* #### [From Material Expression](https://docs.unrealengine.com/5.1/en-US/shading-models-in-unreal-engine/#frommaterialexpression)
