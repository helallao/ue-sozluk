# Selection
<img src="../../../Dosyalar/Niagara_Editor_Selection.jpg">


Details penceresi gibidir. [Graph](../Graph) üzerinde seçtiginiz şeyin ayarlarını gösterir. Niagara Editör'ünde [Graph](../Graph) üzerinden çok bir şey yapmıyoruz, neredeyse %99 Selection penceresini kullanıcaz, dolayısıyla her şeyi burda anlatıcam. Seçtiginiz modül ile ilgili inputlar burada görünür. Üstte kategorilerden birini seçerek sadece o kategoriye ait inputları görebilirsiniz.

<img src="../../../Dosyalar/Niagara_Editor_Selection_2.png">

İnputların en sagındaki butondan inputu en baştaki degerine yani default degere geri alabilirsiniz. Onun bi solundaki buton ile de input ile ilgili işlemler yapabilirsiniz. Mesela inputu bir [dinamik inputa](#dinamik-inputlar) ve ya bir parametreye baglayabilirsiniz. Eger zaten baglıysa "New Local Value" ile kendiniz deger yazabilirsiniz. "New Expression" ile [hlsl](https://en.wikipedia.org/wiki/High-Level_Shader_Language) kodu bile yazabilirsiniz. Eger kendi dinamik input'unuzu yazmak istiyorsanız "New Scratch Dynamic Input" ile kendi dinamik inputunuzu oluşturabilirsiniz, oluşturdugunuz dinamik input [Local Modules
](../Local%20Modules) bölümünde gösterilir.

<img src="../../../Dosyalar/Niagara_Editor_Selection_3.png">

En alttaki genişlet butonu ile sadece bu modül için gelişmiş inputları açabilirsiniz.

<img src="../../../Dosyalar/Niagara_Editor_Selection_4.png">

Sag üstteki 3 çizgiden "Show All Advanced" ayarı ile gelişmiş inputları şu an oldugunuz Emitter/System'ın bütün modülleri için açabilirsiniz. Yani "Show All Advanced" ayarı açıldıgı zaman eger Emitter üzerindeyseniz Emitter'daki bütün modüllerde, System üzerindeyseniz System'daki bütün modüllerde gelişmiş seçenekleri gösterir. Dolayısıyla bu ayarı birden fazla kez açmanız gerekecek.

<img src="../../../Dosyalar/Niagara_Editor_Selection_5.png">

"Show Parameter Reads" ve "Show Parameter Writes" ayarları ile modülün hangi parametreleri okudugunu ve hangi parametreleri degiştirdigini görebilirsiniz.

<img src="../../../Dosyalar/Niagara_Editor_Selection_6.png">

"Show Only Issues" ayarının tam olarak nasıl çalıştıgını bilmiyorum. Açınca modüller siliniyor, geri kapatsanız bile karışıyor. Yani gereksiz, kullanmayın.


# Dinamik Inputlar

Dinamik inputlar istediginiz inputu belirli kodlar ile oluşturabilmenize yarar, [Niagara Modül Editörü'nde](../../Niagara%20Modül%20Editörü) olan çogu kodu barındırır. Yani mesela "Float" bir inputa "Float" döndüren dinamik input baglayabilirsiniz. Bagladıgınız dinamik input sizden başka inputlar alabilir, aldıgı inputlar ile işlemler yapar ve çıkan degeri dinamik inputun baglı oldugu input degeri olarak ayarlar. Bir dinamik inputu döndürdügü degerin dışında bir inputa baglayamazsınız. Yani "Vector" döndüren bir dinamik inputu "Float" deger alan bir inputa baglayamazsınız. Aşagıdan bütün deger türlerine göre dinamik inputlara ve açıklamalarına ulaşabilirsiniz.

* [bool](#bool)
* [float](#float)



# bool

## [Boolean and Operation]()

İki input alır. Eger ikisi de True ise True döndürür (bkz. [Logic AND](../../Niagara%20Modül%20Editörü/Nodlar#logic-and)).


## [Boolean not Operation]()
Aldıgı bool degerinin tersini verir. Yani True verdiyseniz False, False verdiyseniz True (bkz. [Logic Not](../../Niagara%20Modül%20Editörü/Nodlar#logic-not)).


## [Boolean or Operation]()

İki input alır. Eger ikisinden biri True ise True döndürür (bkz. [Logic OR](../../Niagara%20Modül%20Editörü/Nodlar#logic-or)).


## [Invert Bool]()

Aldıgı bool degerinin tersini verir. Yani True verdiyseniz False, False verdiyseniz True (bkz. [Logic Not](../../Niagara%20Modül%20Editörü/Nodlar#logic-not)).


## [Is Platform Set Active]()

bilmiyorum.


## [Mask Bool by Spawn Group]()

Eger parçacıgın [SpawnGroup](../../Niagara%20Editörü/Terimler%20Sözlügü#spawngroup) numarası "Spawn Group Mask" inputuna verdiginiz numaraya eşitse "Masked Bool" inputuna verdiginiz degeri, degilse "Passthrough Bool" inputuna verdiginiz degeri kullanır.

* #### Masked Bool
Parçacıgın [SpawnGroup](../../Niagara%20Editörü/Terimler%20Sözlügü#spawngroup) numarası "Spawn Group Mask" inputuna verdiginiz numaraya eşitse bu deger kullanılır.

* #### Passthrough Bool
Parçacıgın [SpawnGroup](../../Niagara%20Editörü/Terimler%20Sözlügü#spawngroup) numarası "Spawn Group Mask" inputuna verdiginiz numaraya eşit degilse bu deger kullanılır.

* #### Spawn Group Mask
Parçacıgın [SpawnGroup](../../Niagara%20Editörü/Terimler%20Sözlügü#spawngroup) numarası ile eşit mi diye karşılaştırılacak numara.


## [Random Bool]()

Rastgele bool döndürür. Eger "Evaluation Type" inputu "Spawn Only" ise tek bir kere rastgele bool seçer ve sonraki frame'lerde de hep aynı degeri döndürür, "Every Frame" ise her frame'de tekrar rastgele bool döndürür. Ayrıca "Randomness Mode" ayarı ile "Random Seed" ayarını açabilir ve kullanabilirsiniz (bkz. [Calculate Random Bool](../../Niagara%20Modül%20Editörü/Nodlar#calculate-random-bool)).

* #### Evaluation Type
"Spawn Only" ise tek bir kere rastgele bool seçer ve sonraki frame'lerde de hep aynı degeri döndürür, "Every Frame" ise her frame'de tekrar rastgele bool döndürür.

* #### Randomness Mode
[Calculate Random Bool](../../Niagara%20Modül%20Editörü/Nodlar#calculate-random-bool) fonksiyonunun "Randomness Mode" inputu.

* #### Random Seed
"Randomness Mode" ayarı deterministik ise seed verebilirsiniz.


## [Set Bool by Float Comparison]()

İki float degeri alır ve bu degerleri "Comparison Type" inputuna verdiginiz koşula göre karşılaştırıp sonucu döndürür.

* #### A
A degeri.

* #### B
B degeri.

* #### Comparison Type
Koşulu belirler. 6 modu vardır.

Mod | İşlem
:---: | :---:
A Greater Than B | A B'den büyükse True, degilse False.
A Greater Than Or Equal To B | A B'den büyük ve ya eşitse True, degilse False.
A Equal To B | A B'ye eşitse True, degilse False.
A Not Equal To B | A B'ye eşit degilse True, degilse False.
A Less Than B | A B'den küçükse True, degilse False.
A Less Than Or Equal To B | A B'den küçük ve ya eşitse True, degilse False.


## [Set Bool by Int Comparison]()

İki integer degeri alır ve bu degerleri "Comparison Type" inputuna verdiginiz koşula göre karşılaştırıp sonucu döndürür.

* #### A
A degeri.

* #### B
B degeri.

* #### Comparison Type
Koşulu belirler. 6 modu vardır.

Mod | İşlem
:---: | :---:
A Greater Than B | A B'den büyükse True, degilse False.
A Greater Than Or Equal To B | A B'den büyük ve ya eşitse True, degilse False.
A Equal To B | A B'ye eşitse True, degilse False.
A Not Equal To B | A B'ye eşit degilse True, degilse False.
A Less Than B | A B'den küçükse True, degilse False.
A Less Than Or Equal To B | A B'den küçük ve ya eşitse True, degilse False.



<br>
<br>


# float

## [Abs Float]()

Aldıgı inputun mutlak degerini verir (bkz. [Abs](../../Niagara%20Modül%20Editörü/Nodlar#abs)).


## [Add Float]()

İki input alır ve toplamlarını döndürür (bkz. [Add](../../Niagara%20Modül%20Editörü/Nodlar#add)).


## [Angle Conversion]()

Aldıgı derece degerini başka bir derece degerine dönüştürür.

* #### Angle
Derece degeri.

* #### Angle Input
Verdiginiz derece degerinin türü.

Tür | İçerik
:---: | :---:
Degrees | Derece
Normalized Angle (0-1) | 0 - 360 yerine 0 - 1 arası degerler.
Radians | [Radyan](https://tr.wikipedia.org/wiki/Radyan)

* #### Angle Output
Verdiginiz derece degerinin dönüştürülecegi tür.

Tür | İçerik
:---: | :---:
Degrees | Derece
Normalized Angle (0-1) | 0 - 360 yerine 0 - 1 arası degerler.
Radians | [Radyan](https://tr.wikipedia.org/wiki/Radyan)


## [Calculate Particle Radius]()

"Radius Calculation Type" inputuna göre Sprite'ın ve ya Mesh'in yarıçapını hesaplar. "Sprite" modunda iken Sprite'ın (bkz. [Sprite Renderer](../Moduller#sprite-renderer)), Mesh modundayken Mesh'in (bkz. [Mesh Renderer](../Moduller#mesh-renderer)) yarıçapını verir, Sprite için [Particles.SpriteSize](../Parameters#particlesspritesize) parametresini, Mesh için [Particles.Scale](../Parameters#particlesscale) parametresini kullanır. Ayrıca "Mesh" modunda iken "Mesh Dimensions" diye bir input daha açılır, bu input yarıçap hesaplanırken [Particles.Scale](../Parameters#particlesscale) parametresi için çarpan görevi görür, yani deger bu inputa verdiginiz deger ile çarpılır. "Radius Calculation Type" inputu "Custom" modunda iken manuel olarak yarıçap degerini verebilirsiniz, hiçbir işlem yapılmadan aynı deger döndürülür.

* #### Radius Calculation Type
"Sprite" modunda iken Sprite'ın (bkz. [Sprite Renderer](../Moduller#sprite-renderer)), Mesh modundayken Mesh'in (bkz. [Mesh Renderer](../Moduller#mesh-renderer)) yarıçapını verir, Sprite için [Particles.SpriteSize](../Parameters#particlesspritesize) parametresini, Mesh için [Particles.Scale](../Parameters#particlesscale) parametresini kullanır. Ayrıca "Mesh" modunda iken "Mesh Dimensions" diye bir input daha açılır, bu input yarıçap hesaplanırken [Particles.Scale](../Parameters#particlesscale) parametresi için çarpan görevi görür, yani deger bu inputa verdiginiz deger ile çarpılır. "Custom" modunda iken manuel olarak yarıçap degerini verebilirsiniz, hiçbir işlem yapılmadan aynı deger döndürülür.

* #### Mesh Dimensions
Sadece "Radius Calculation Type" "Mesh" modunda iken vardır. [Particles.Scale](../Parameters#particlesscale) parametresi için çarpan görevi görür.

* #### Particle Radius
Sadece "Radius Calculation Type" "Custom" modunda iken vardır. Manuel olarak yarıçap degerini verebilirsiniz, hiçbir işlem yapılmadan aynı deger döndürülür.

* #### Method for Calculating Particle Radius
3 method vardır, "Minimum Axis", "Maximum Axis" ve "Bounds". Minimum Axis methodu kısa olan ekseni seçer ve yarıçapını verir. Maximum Axis methodu uzun olan ekseni seçer ve yarıçapını verir. Bounds methodu iki eksenin uzunlugunu/büyüklügünü (magnitude) yani [Pythagorean theorem'ini](https://en.wikipedia.org/wiki/Pythagorean_theorem) alır ve yarıçapını verir.


## [Ceil Float]()

Verdiginiz sayıyı en yakın küçük tamsayıya yuvarlar (bkz. [Ceil](../../Niagara%20Modül%20Editörü/Nodlar#ceil)). örnegin
<br>
<br>
9.9 -> 9
<br>
9.1 -> 9


## [Clamp Float]()

Verdiginiz inputu "Min" ve "Max" degerine göre düzenler. Eger input Min degerinden küçükse Min degerine, Max degerinden büyükse Max degerine taşınır (bkz. [Clamp](../../Niagara%20Modül%20Editörü/Nodlar#clamp)).

* #### Float
Deger.

* #### Min
Minimum deger.

* #### Max
Maximum deger.


## [Compare Floats]()

Verdiginiz inputların arasından en büyük/küçük olanını seçer.

* #### Comparison Mode
"Return Largest" modundayken en büyük olanı, "Return Smallest" modundayken en küçük olanı döndürür.

* #### Comparison Count
Kaç tane inputun karşılaştırılacagını belirler. 5'e kadar çıkarılabilir. A, B, C, D, E şeklinde inputlar oluşturur.


## [Cone Mask]()

bilmiyorum.


## [Cosine]()

"Normalized Angle" inputu için kosinüs degeri döndürür. Kosinüs degerinin periyodunu "Period" inputundan belirleyebilirsiniz. Hesaplanan kosinüs degeri "Scale" inputu ile çarpılır yani "Scale" inputu kosinüs degeri için çarpan görevi görür. Sonra hesaplanan degere "Bias" inputu eklenir. (bkz. [Cosine](../../Niagara%20Modül%20Editörü/Nodlar#cosine))

* #### Normalized Angle
Kosinüsü alınacak deger.

* #### Period
Kosinüs degerinin periyodu.

* #### Scale
Hesaplanan kosinüs degeri bu input ile çarpılır yani bu input kosinüs degeri için çarpan görevi görür.

* #### Bias
Hesaplanan degere eklenir.


## [Distance Between Positions]()

Verdiginiz iki konum arasındaki mesafe degerini döndürür (bkz. [Distance](../../Niagara%20Modül%20Editörü/Nodlar#distance)).

* #### A
A konumu.

* #### B
B konumu.


## [Divide Float]()

Verdiginiz A inputunu B inputuna böler (bkz. [Divide](../../Niagara%20Modül%20Editörü/Nodlar#divide)). 

* #### A
A degeri.

* #### B
B degeri.


## [Dot Product]()

Verdiginiz iki inputun [Dot Product'ını](https://en.wikipedia.org/wiki/Dot_product) verir (bkz. [Dot](../../Niagara%20Modül%20Editörü/Nodlar#dot)).

* #### Vector A
A vektörü.

* #### Vector B
B vektörü.


## [Float from Curve]()

Curve ile float degeri üretmenize yarar.


## [Floor Float]()

Verdiginiz sayıyı en yakın büyük tamsayıya yuvarlar (bkz. [Floor](../../Niagara%20Modül%20Editörü/Nodlar#floor)). örnegin
<br>
<br>
9.9 -> 10
<br>
9.1 -> 10


## [Frac Float]()

Verilen inputun kesirli yani . (nokta) dan sonraki kısmını verir (bkz. [Frac](../../Niagara%20Modül%20Editörü/Nodlar#frac)). örnegin,
<br>
<br>
1.5 = 0.5
<br>
2.0 = 0
<br>
0.99 = 0.99


## [Lerp Float]()

Formül: [(a * (1 - c)) + (b * c)](https://www.desmos.com/calculator/gtuwm4l27u). Verilen "Alpha" degerine göre "A" ve "B" inputlarını birbirine karıştırır, oranlar. Örnegin "A" ve "B" için iki sayı girin mesela 10 ve 0. Eger "Alpha" degerine 0 verirseniz A, 1 verirseniz B degeri döndürülür. Eger "Alpha" degerine 0.5 verirseniz sayımız da "A" ve "B" nin ortası yani 5 olur. Yani 0'a yaklaştıkça A, 1'e yaklaştıkça B. Kısacası en basit tanımıyla oranlama yapar diyebiliriz, yüzde olarak degilde 0 - 1 arası gibi düşünün, 0 = %0, 1 = %100. (bkz. [Lerp](../../Niagara%20Modül%20Editörü/Nodlar#lerp))

* #### A
A degeri.

* #### B
B degeri.

* #### Alpha
Alpha degeri.


## [Lerp Multiple Floats]()

Veridiginiz inputları Lerp eder. Sadece 2 degeri degil daha fazlasını da Lerp edebilir. En fazla 5 degeri birden Lerp edebilirsiniz. Çalışma şekli şudur, normal Lerp işleminde iki deger vardır, yani 2 nokta vardır. Bu noktaların birincisi 0 degerinde iken, ikincisi 1 degerinde iken kullanılır. Lerp edilen deger sayısı arttıkça nokta sayısı da artar, mesela 3 degeri Lerp ederseniz 3 nokta oluşur, bu 3 nokta, 0, 0.5 ve 1'dir. 0'da iken 1. deger kullanılır, 0.5'e dogru kaydıkça sonuç da 2. degere dogru kayar. 0.5'de iken 2. deger kullanılır. Sonra 0.5'den 1'e dogru kaydıkça sonuç da 3. degere dogru kayar ve 1'de iken sonuç da 3. degere eşit olur. İşte çalışma mantıgı bu, 4 ve 5 inputu Lerp ederken de aynı mantık kullanılıyor. Mesela 4 inputlu Lerp işleminde 4 nokta vardır, bu noktalar, 0, 0.33, 0.66, 1'dir. 5 inputlu işlemde 5 nokta vardır, bu noktalar, 0, 0.25, 0.5, 0.75, 1'dir. Desmos üzerinde yaptıgım [örnege](https://www.desmos.com/calculator/3hswgubepl) de bakabilirsiniz. (bkz. [Lerp Multiple Numeric Fn](../../Niagara%20Modül%20Editörü/Nodlar#lerp-multiple-numeric-fn))

* #### Float Count
Lerp edilecek input sayısı.


## [Make Custom Float from Bool]()
"Bool" inputuna verdiginiz deger True ise "True Float" inputunu, False ise "False Float" inputunu kullanır.

* #### Bool
True ise "True Float" inputu, False ise "False Float" inputu kullanılır.

* #### True Float
"Bool" inputu True iken kullanılacak deger.

* #### False Float
"Bool" inputu False iken kullanılacak deger.


## [Make Float from Int]()
Verdiginiz integer'ı float'a dönüştürür.

* #### Int
Integer degeri.


## [Make Float from Linear Color]()
Verdiginiz Linear Color'ın tek bir kanalındaki float degerini kullanır.

* #### LinearColor
Linear Color degeri.

* #### Channel
Linear Color'dan float degerinin alınacagı kanal.


## [Make Float from Linear Vector]()
Verdiginiz vectör'ün tek bir kanalındaki float degerini kullanır.

* #### Vector
Vektör degeri.

* #### Channel
Vektör'den float degerinin alınacagı kanal.


## [Make Float from Linear Vector 2d]()
Verdiginiz 2 boyutlu vectör'ün tek bir kanalındaki float degerini kullanır.

* #### Vector 2D
2 boyutlu vektör degeri.

* #### Channel
2 boyutlu vektör'den float degerinin alınacagı kanal.


## [Make Float from Linear Vector 4]()
Verdiginiz 4 boyutlu vectör'ün tek bir kanalındaki float degerini kullanır.

* #### Vector 4
4 boyutlu vektör degeri.

* #### Channel
4 boyutlu vektör'den float degerinin alınacagı kanal.


## [Mask Float by Spawn Group]()
Eger parçacıgın [SpawnGroup](../../Niagara%20Editörü/Terimler%20Sözlügü#spawngroup) numarası "Spawn Group Mask" inputuna verdiginiz numaraya eşitse "Masked Float" inputuna verdiginiz degeri, degilse "Passthrough Float" inputuna verdiginiz degeri kullanır.

* #### Masked Float
Parçacıgın [SpawnGroup](../../Niagara%20Editörü/Terimler%20Sözlügü#spawngroup) numarası "Spawn Group Mask" inputuna verdiginiz numaraya eşitse bu deger kullanılır.

* #### Passthrough Float
Parçacıgın [SpawnGroup](../../Niagara%20Editörü/Terimler%20Sözlügü#spawngroup) numarası "Spawn Group Mask" inputuna verdiginiz numaraya eşit degilse bu deger kullanılır.

* #### Spawn Group Mask
Parçacıgın [SpawnGroup](../../Niagara%20Editörü/Terimler%20Sözlügü#spawngroup) numarası ile eşit mi diye karşılaştırılacak numara.


## [Max Float]()
Verdiginiz 2 inputun büyük olanını kullanır (bkz. [Max](../../Niagara%20Modül%20Editörü/Nodlar#max)).

* #### A
A degeri.

* #### B
B degeri.


## [Min Float]()
Verdiginiz 2 inputun küçük olanını kullanır (bkz. [Min](../../Niagara%20Modül%20Editörü/Nodlar#min)).

* #### A
A degeri.

* #### B
B degeri.


## [Modulo Float]()
Verdiginiz ilk sayının ikinciye bölümünden kalanı kullanır. (bkz. [Modulo](../../Niagara%20Modül%20Editörü/Nodlar#modulo)).

* #### A
A degeri.

* #### B
B degeri.


## [Multiply Float]()
Verdiginiz 2 inputun çarpımını kullanır. (bkz. [Multiply](../../Niagara%20Modül%20Editörü/Nodlar#multiply)).

* #### A
A degeri.

* #### B
B degeri.


## [Multiply Float by Int]()
Verdiginiz float ile integer'ın çarpımını kullanır (bkz. [Multiply](../../Niagara%20Modül%20Editörü/Nodlar#multiply)).

* #### Float
Float degeri.

* #### Integer
Integer degeri.


## [Normalize Distance Range]()
Verdiginiz inputları direktmen [Normalize Distance Range](../../Niagara%20Modül%20Editörü/Nodlar#normalize-distance-range) fonksiyonundan geçirir ve sonucu kullanır. Açıklama için [Normalize Distance Range](../../Niagara%20Modül%20Editörü/Nodlar#normalize-distance-range) fonksiyonuna bakın.

* #### Start Position
[Normalize Distance Range](../../Niagara%20Modül%20Editörü/Nodlar#normalize-distance-range) fonksiyonunun "Start Position" inputu.

* #### End Position
[Normalize Distance Range](../../Niagara%20Modül%20Editörü/Nodlar#normalize-distance-range) fonksiyonunun "End Position" inputu.

* #### Distance
[Normalize Distance Range](../../Niagara%20Modül%20Editörü/Nodlar#normalize-distance-range) fonksiyonunun "Distance" inputu.

* #### Invert Normalized Range
Bu ayar kapalıyken [Normalize Distance Range](../../Niagara%20Modül%20Editörü/Nodlar#normalize-distance-range) fonksiyonunun "Normalized Range" outputu kullanılır, açıkken "Inverse Normalized Range" outputu kullanılır.


## [Normalize Float]()
Bilmiyorum.


## [One Minus Float]()
Verdiginiz degerin 1'den çıkarılmış halini kullanır (bkz. [One Minus](../../Niagara%20Modül%20Editörü/Nodlar#one-minus)).

* #### Float
Deger.


## [Power]()
Verilen "A" degerinin "B" degeri kadar kuvvetini alır. Eger "A" "B" den küçükse sonuç 0 olur (bkz. [Pow](../../Niagara%20Modül%20Editörü/Nodlar#pow)).

* #### a
A degeri.

* #### b
B degeri.


## [Random Range Float]()
Verdiginiz inputları [Calculate Random Range Float](../../Niagara%20Modül%20Editörü/Nodlar#calculate-random-range-float) fonksiyonundan geçirir ve sonucu kullanır. Açıklama için [Calculate Random Range Float](../../Niagara%20Modül%20Editörü/Nodlar#calculate-random-range-float) fonksiyonuna bakın.

* #### Minimum
[Calculate Random Range Float](../../Niagara%20Modül%20Editörü/Nodlar#calculate-random-range-float) fonksiyonunun "Float Min" inputu.

* #### Maximum
[Calculate Random Range Float](../../Niagara%20Modül%20Editörü/Nodlar#calculate-random-range-float) fonksiyonunun "Float Max" inputu.

* #### Evaluation Type
"Spawn Only" ise tek bir kere rastgele float seçer ve sonraki frame'lerde de hep aynı degeri döndürür, "Every Frame" ise her frame'de tekrar rastgele float döndürür.

* #### Randomness Mode
[Calculate Random Range Float](../../Niagara%20Modül%20Editörü/Nodlar#calculate-random-range-float) fonksiyonunun "Randomness Mode" inputu.

* #### Random Seed
"Randomness Mode" ayarı deterministik ise seed verebilirsiniz.

* #### Fixed Random Seed
[Calculate Random Range Float](../../Niagara%20Modül%20Editörü/Nodlar#calculate-random-range-float) fonksiyonunun "Fixed Random Seed" inputu.


## [Remap Range]()
Verdiginiz inputları direktmen [Remap Range](../../Niagara%20Modül%20Editörü/Nodlar#remap-range) fonksiyonundan geçirir ve sonucu kullanır. Açıklama için [Remap Range](../../Niagara%20Modül%20Editörü/Nodlar#remap-range) fonksiyonuna bakın.

* #### Input Value To Remap
Remap edilecek deger.

* #### Clamp Results
[Remap Range](../../Niagara%20Modül%20Editörü/Nodlar#remap-range) fonksiyonunun "Clamp Results" inputu.

* #### Input Min
[Remap Range](../../Niagara%20Modül%20Editörü/Nodlar#remap-range) fonksiyonunun "Input Min" inputu.

* #### Input Max
[Remap Range](../../Niagara%20Modül%20Editörü/Nodlar#remap-range) fonksiyonunun "Input Max" inputu.

* #### Output Min
[Remap Range](../../Niagara%20Modül%20Editörü/Nodlar#remap-range) fonksiyonunun "Output Min" inputu.

* #### Output Max
[Remap Range](../../Niagara%20Modül%20Editörü/Nodlar#remap-range) fonksiyonunun "Output Max" inputu.


## [Return Normalized Exec Index]()
[Normalized Execution Index](../../Niagara%20Modül%20Editörü/Nodlar#normalized-execution-index) fonksiyonundan degeri kullanır. Açıklama için [Normalized Execution Index](../../Niagara%20Modül%20Editörü/Nodlar#normalized-execution-index) fonksiyonuna bakın.

* #### Normalized Index Scale
[Normalized Execution Index](../../Niagara%20Modül%20Editörü/Nodlar#normalized-execution-index) fonksiyonundan gelen deger bu input ile çarpılır yani bu input [Normalized Execution Index](../../Niagara%20Modül%20Editörü/Nodlar#normalized-execution-index) fonksiyonundan gelen deger için çarpan görevi görür.

* #### Normalized Index Includes One
[Normalized Execution Index](../../Niagara%20Modül%20Editörü/Nodlar#normalized-execution-index) fonksiyonunun "Normalized Index Includes One" inputu.


## [Round Float]()
Verdiginiz degeri yuvarlar (bkz. [Round](../../Niagara%20Modül%20Editörü/Nodlar#round)).

* #### Float
Yuvarlanacak deger.


## [Scalability Distance Based Float]()
bilmiyorum.


## [Scale and Bias Float]()
Verdiginiz degeri "Scale" ile çarpıp "Bias" ile toplar (bkz. [MultiplyAdd](../../Niagara%20Modül%20Editörü/Nodlar#multiplyadd)).

* #### Float
Deger.

* #### Scale
"Float" inputunun çarpılacagı deger.

* #### Bias
"Float" inputu ile "Scale" inputunun çarpımından çıkan sonuca eklenecek deger.


## [Select Float from Array]()
bilmiyorum.


## [Sine]()
"Normalized Angle" inputu için sinüs degeri döndürür. Sinüs degerinin periyodunu "Period" inputundan belirleyebilirsiniz. Hesaplanan sinüs degeri "Scale" inputu ile çarpılır yani "Scale" inputu sinüs degeri için çarpan görevi görür. Sonra hesaplanan degere "Bias" inputu eklenir. (bkz. [Sine](../../Niagara%20Modül%20Editörü/Nodlar#sine))

* #### Normalized Angle
Sinüsü alınacak deger.

* #### Period
Sinüs degerinin periyodu.

* #### Scale
Hesaplanan sinüs degeri bu input ile çarpılır yani bu input sinüs degeri için çarpan görevi görür.

* #### Bias
Hesaplanan degere eklenir.


## [Smooth Lerp Over Time Float]()
Verdiginiz inputları direktmen [Smooth Lerp Over Time](../../Niagara%20Modül%20Editörü/Nodlar#smooth-lerp-over-time) fonksiyonundan geçirir ve sonucu kullanır. Açıklama için [Smooth Lerp Over Time](../../Niagara%20Modül%20Editörü/Nodlar#smooth-lerp-over-time) fonksiyonuna bakın.

* #### Convergence Rate
[Smooth Lerp Over Time](../../Niagara%20Modül%20Editörü/Nodlar#smooth-lerp-over-time) fonksiyonunun "Convergence Rate" inputu.

* #### Smooth Value
[Smooth Lerp Over Time](../../Niagara%20Modül%20Editörü/Nodlar#smooth-lerp-over-time) fonksiyonunun "Smooth Value" inputu.

* #### Target Value
[Smooth Lerp Over Time](../../Niagara%20Modül%20Editörü/Nodlar#smooth-lerp-over-time) fonksiyonunun "Target Value" inputu.


## [Subtract Float]()

Verdiginiz A inputundan B inputunu çıkarır (bkz. [Subtract](../../Niagara%20Modül%20Editörü/Nodlar#subtract)).

* #### A
A degeri.

* #### B
B degeri.


## [Uniform AOr BFloat]()
Yazı tura görevi görür. A ve B degerinin arasında "Distribution Weight" inputundaki ihtimale göre seçilim yapılır. "Distribution Weight" inputu A ve B arasındaki ihtimal oranını belirler. 0.5 iken ikisinin de ortasındadır yani ikisi de %50 ihtimalle çıkabilir. Eger degeri 0'a kaydırırsanız A inputunun seçilme ihtimali artar, degeri 1'e kaydırırsanız B inputunun seçilme ihtimali artar. Mesela 0.3 iken A inputunun çıkma ihtimali %70, B inputunun çıkma ihtimali %30 olur.

* #### A
A degeri.

* #### B
B degeri.

* #### Distribution Weight
İhtimal dagılımı. A ve B arasındaki ihtimal oranını belirler. 0.5 iken ikisinin de ortasındadır yani ikisi de %50 ihtimalle çıkabilir. Eger degeri 0'a kaydırırsanız A inputunun seçilme ihtimali artar, degeri 1'e kaydırırsanız B inputunun seçilme ihtimali artar. Mesela 0.3 iken A inputunun çıkma ihtimali %70, B inputunun çıkma ihtimali %30 olur.

* #### Randomness Mode
[Random Range Float](../../Niagara%20Modül%20Editörü/Nodlar#random-range-float) fonksiyonunun "RandomnessMode" inputu.

* #### Random Seed
"Randomness Mode" ayarı deterministik ise seed verebilirsiniz.

* #### Fixed Random Seed
[Random Range Float](../../Niagara%20Modül%20Editörü/Nodlar#random-range-float) fonksiyonunun "Fixed Override Seed" inputu.


## [Vector 2DLength]()
Verdiginiz 2 boyutlu vektörün uzunlugunu, büyüklügünü (magnitude) verir (bkz. [Length](../../Niagara%20Modül%20Editörü/Nodlar#length)).

* #### Vector
Vektör degeri.


## [Vector Length]()
Verdiginiz vektörün uzunlugunu, büyüklügünü (magnitude) verir. Eger "Safe Length Calculation" ayarı açıksa [Direction and Length Safe](../../Niagara%20Modül%20Editörü/Nodlar#direction-and-length-safe) fonksiyonunu kullanır, kapalıysa [Length](../../Niagara%20Modül%20Editörü/Nodlar#length) nodunu kullanır.

* #### Vector
Vektör degeri.

* #### Safe Length Calculation
Bu ayar açıksa [Direction and Length Safe](../../Niagara%20Modül%20Editörü/Nodlar#direction-and-length-safe) fonksiyonu kullanılır, kapalıysa [Length](../../Niagara%20Modül%20Editörü/Nodlar#length) nodu kullanılır.

* #### Fallback Vector
"Safe Length Calculation" ayarı açıksa kullanılır. [Direction and Length Safe](../../Niagara%20Modül%20Editörü/Nodlar#direction-and-length-safe) fonksiyonunun "Fallback" inputu.

* #### Fallback Threshold
"Safe Length Calculation" ayarı açıksa kullanılır. [Direction and Length Safe](../../Niagara%20Modül%20Editörü/Nodlar#direction-and-length-safe) fonksiyonunun "Threshold" inputu.

* #### Fallback Length
"Safe Length Calculation" ayarı açıksa kullanılır. [Direction and Length Safe](../../Niagara%20Modül%20Editörü/Nodlar#direction-and-length-safe) fonksiyonunun "Fallback Length" inputu.





