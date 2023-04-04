# Graph
<img src="../../../Dosyalar/Niagara_Editor_Graph.jpg">


Sadece Emitter ve System'lerden oluşur. Niagara Editör'ünde diger editörler gibi Graph üzerinden kodlama yapmazsınız. Sadece Emitter ve System'leri (varsa) gösterir. Graph üzerine sag tıklayarak yeni Emitter oluşturabilirsiniz. Emmitter'ların üzerindeki tik işaretine basarak devre dışı bırakabilirsiniz. Tik işaretinin altındaki adam işaretine basarak isole edebilirsiniz, izole edince sadece o Emmitter'ı gösterir. Geriye kalan bütün ayarları [Selection](../Selection) bölümünden yapabilirsiniz. Graph bölümü boş kalmasın diye System ve Emitter'ın açıklamalarını buraya yazdım. Sonuçta Graph üzerinde sadece onlar var.


# Bölümler

* [System](#system)
* [Emitter](#emitter)


## [System](https://docs.unrealengine.com/5.1/en-US/overview-of-niagara-effects-for-unreal-engine/#systems)
System, efekti baştan sona yapabilmemiz için gerekli olan her şeyi birleştiren sistemdir. Birden fazla Emitter kullanabilir ve bunları düzenleyebiliriz.


## [Emitter](https://docs.unrealengine.com/5.1/en-US/overview-of-niagara-effects-for-unreal-engine/#emitters)

Emitter parçacıkları yönetir. Parçacıkların bütün ayarlarını Emitter üzerinden yaparız. Bunun için [Modul'leri](../Moduller) kullanırız. Emitter yukardan aşagı dogru ilerler, zaten bütün adımlar kategorilere ayrılmış. Kategorilere aşagıdan ulaşabilirsiniz.

* ### [Emitter Spawn](https://docs.unrealengine.com/5.1/en-US/overview-of-niagara-effects-for-unreal-engine/#emitters)
* ### [Emitter Update](https://docs.unrealengine.com/5.1/en-US/overview-of-niagara-effects-for-unreal-engine/#emitters)
* ### [Particle Spawn](https://docs.unrealengine.com/5.1/en-US/overview-of-niagara-effects-for-unreal-engine/#emitters)
* ### [Particle Update](https://docs.unrealengine.com/5.1/en-US/overview-of-niagara-effects-for-unreal-engine/#emitters)
* ### [Event Handler](https://docs.unrealengine.com/5.1/en-US/overview-of-niagara-effects-for-unreal-engine/#emitters)
* ### [Render](https://docs.unrealengine.com/5.1/en-US/overview-of-niagara-effects-for-unreal-engine/#emitters)
