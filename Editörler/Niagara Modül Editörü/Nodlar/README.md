### Yazım şekli
* Bu dökümanı hazırlarken başlangıçta dügümleri "Node" şeklinde yazıyordum ama kesme işareti falan koyunca çok okunmaz oluyo diyo "Node" kelimesini türkçe gibi düşünüp "Nod" diye yazmaya başladım, bunu sadece ek aldıgı zaman kullandım, ek almazsa yine "Node" diyorum.
* Eger bi node aratırken farklı, niagara modül editörüne konuldugunda farklı isme (kısaltma) sahipse, nodun yanına editördeki ismi parantez içinde yazılır. [örnek](#)
* Bazı fonksiyonlar gizli (unexposed) olabilir, çünkü unreal geliştiricileri tarafından fonksiyonun ayarları bu şekilde ayarlanmıştır. Bu fonksiyonları kullanmak için, şu an kullanabildiginiz herhangi bir fonksiyon nodunu kullanıp, fonksiyonun [Selected Details](../Selected%20Details) penceresinden "Function Script" inputunu degiştirip istediginiz fonksiyonu seçebilirsiniz. Gizli (unexposed) olan fonksiyonların başında parantez içinde "bu fonksiyon gizli bir fonksiyondur" yazar.
* Karmaşık anlatıma sahip olan konuların açıklamaları [Terimler Sözlügü](../Terimler%20Sözlügü) bölümünde toplandı.
<br>
<br>
<br>



## Break

Bu kategori sadece çok boyutlu veri tipleri ve özel veri tiplerinde ortaya çıkar. Veriyi parçalayıp içindeki elementleri alabilirsiniz.


## Boolean

* #### [Bool Equal]()
Verilen iki bool birbirine eşit ise True, degilse False döndürür

* #### [Bool Not Equal]()
Verilen iki bool birbirine eşit degil ise True, eşitse False döndürür.

* #### [Logic AND]()
Verilen bool'ların hepsi True ise True, degilse False döndürür.

* #### [Logic NOT]()
Verilen bool'u tersine çevirir, True ise False, False ise True döndürür.

* #### [Logic OR]()
Verilen bool'ların herhangi biri True ise True, hiçbiri degilse False döndürür.


## Comments

* #### [Add Comment]()
Yorum bölümü oluşturur.


## Compiler Tagging

* #### [Add Compiler Output Tag(Output Compiler Tag)]()
bilmiyorum.


## Events

* #### [Add Chaos Destruction Event Read(ChaosDestructionEvent Read)]()
bilmiyorum.

* #### [Add Niagara Collision Payload Event Read(NiagaraCollisionEventPayload Read)]()
bilmiyorum.

* #### [Add Chaos Destruction  Event Write(ChaosDestructionEvent Write)]()
bilmiyorum.

* #### [Add Niagara Collision  Payload Event Write(NiagaraCollisionEventPayload Write)]()
bilmiyorum.


## Functions

* #### [Align Quaternions]()
bilmiyorum.

* #### [Angle Between Quaternions]()
bilmiyorum.

* #### [Angle Unit Converter]()
bilmiyorum.

* #### [Apply Local Inverse Transform]()
bilmiyorum.

* #### [Apply Local Transform]()
bilmiyorum.

* #### [Apply Rotation Vector]()
bilmiyorum.

* #### [Area Of A Truncated Circle]()
bilmiyorum.

* #### [Axis Angle to Euler]()
bilmiyorum.

* #### [Axis Angle to Quaternion]()
bilmiyorum.

* #### [Axis Angle to Rotation Matrix]()
bilmiyorum.

* #### [Calculate A Volume Textures Distance Field Gradient]()
bilmiyorum.

* #### [Calculate Cylinder Plane Intersection*]()
bilmiyorum.

* #### [Calculate Line Plane Intersection]()
bilmiyorum.

* #### [Calculate Link Constraint]()
bilmiyorum.

* #### [Calculate Mesh Radius]()
bilmiyorum.

* #### [Calculate Radius from Sprite Size]()
bilmiyorum.

* #### [Calculate Random Bool]()
bilmiyorum.

* #### [Calculate Random Point in Cone Sphere Intersection]()
bilmiyorum.

* #### [Calculate Random Point in Sphere]()
bilmiyorum.

* #### [Calculate Random Range]()
bilmiyorum.

* #### [Calculate Random Range Float]()
bilmiyorum.

* #### [Calculate Random Range Integer]()
bilmiyorum.

* #### [Calculate Random Unit Vector]()
bilmiyorum.

* #### [Calculate the Global Distance Field Surface Normal GPU]()
bilmiyorum.

* #### [Calculate the Volume Of A Box]()
bilmiyorum.

* #### [Calculate Triangle Area]()
bilmiyorum.

* #### [Calculate Volume Of A Sphere]()
bilmiyorum.

* #### [Calculate Waveform]()
bilmiyorum.

* #### [Centimeter Meter Conversion]()
bilmiyorum.

* #### [Collision Query and Response]()
bilmiyorum.

* #### [Compose System and Local Transform]()
bilmiyorum.

* #### [Compress Quaternion GPU]()
bilmiyorum.

* #### [Cone Constraint]()
bilmiyorum.

* #### [Cone Mask]()
bilmiyorum.

* #### [Convert Index to 2DLookup]()
bilmiyorum.

* #### [Custom Hlsl]()
HLSL dili (High-Level Shader Language) ile yazılan kodları çalıştırmanıza yarar. Zaten nodların hepsi küçük küçük HLSL dili ile yazılmış kodlardır. Biz de bu nodları birleştirerek işlemler yapıyoruz.

* #### [Decompress Quaternion GPU]()
bilmiyorum.

* #### [Default Function*]()
bilmiyorum.

* #### [Derive Third Orthogonal Vector]()
bilmiyorum.

* #### [Derive Triangle Information]()
bilmiyorum.

* #### [Derive Z]()
bilmiyorum.

* #### [Direction and Length]()
Verilen vektörün (V3) yönünü (normalized olarak) ve uzunlugunu (yani (0,0,0) ile verdiginiz konum arasındaki mesafenin uzunlugunu veriyor) verir.

* #### [Direction and Length Safe]()
"Direction and Length" nodunun safe versiyonudur yani aynısıdır, sadece ek özelligi var. Eger verdiginiz vektörün uzunlugu "Threshold" olarak verdiginiz degerden küçükse, "Direction" olarak "Fallback Vector" inputuna verdiginiz vektörü (normalized degil, direktmen aynı şekilde) ve "Length" olarak da bu vektörün uzunlugunu döndürür. Eger verdiginiz vektörün uzunlugu "Threshold" degerinden büyükse, "Direction" olarak "Vector" inputuna verdiginiz vektörü (normalized olarak) ve "Length" olarak da bu vektörün uzunlugunu döndürür. Bunlara ek olarak da, eger "Vector" inputu "Threshold" degerinden küçükse "Below Threshold" outputu True döndürür, degilse False.

* #### [Distance Based Falloff]()
Bu fonksiyon özünde [Normalize Distance Range](#normalize-distance-range) kullanır, o fonksiyonu bilmeden şimdi anlattıklarımı anlayamazsınız. [Normalize Distance Range'e](#normalize-distance-range) ek olarak bir iki şey vardır. İlk olarak "InvertFalloff" diye bir input var, eger kodlara bakarsanız görürsünüz, bu inputa True verdiginizde normal degeri degil de inverse edilmiş degeri kullanıyor. "Falloff Scale" diye bir input daha var, bu da "Falloff" output degerini verdiginiz deger ile çarpıyor, yani "Falloff" outputu olarak bu deger ile çarpılmış degeri veriyor. Bu şu anlama geliyor, hani normalde bizim normalize edilmiş degerlerimiz 0 - 1 arası idi ya. İşte bu input bu degeri çarpıyor, yani eger "Falloff Scale" olarak 2 verirseniz, normalize edilmiş deger 0 - 2 arası olur. Ayrıca "Falloff" ve "Normalized Falloff" diye iki output var, bunlar şu anlama geliyor. Bu output degerleri aslında [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Normalized Range" ile aynıdır, ama "Falloff" outputu verdiginiz "Falloff Scale" inputuna göre çarpılmış olabilir. Yani bu deger "Falloff Scale" olarak 2 verirseniz, 0 - 1 arası degil de 0 - 2 arası olabilir, yani bu "Falloff Scale" degerine göre aralıgı degiştirilmiş deger, eger aralıgı degiştirilmemiş, 0 - 1 arası olan degeri almak istiyorsanız "Normalized Falloff" outputunu kullanın. "Normalized Falloff" degeri her zaman [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Normalized Range" ile aynıdır. Kısacası bu iki output size hem "Falloff Scale" degerine göre aralıgı degiştirilmiş, hem de degiştirilmemiş (0 - 1) degerleri veriyor, ikisini de gerektigi zaman kullanın diye. Son olarak "Normalized Distance" ve "Normalized Distance Inverted" outputları hakkında söylemem gereken bir şey var, eger kodları incelerseniz [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Normalized Range" ve "Inverse Normalized Range" outputlarının bu ikisine direktmen baglandıgını görürsünüz. Bu iki output şu sebeple vardır, "Falloff" ve ya "Normalized Falloff" outputu olarak gelen deger "InvertFalloff" inputuna göre invert edilmiş olabilir. "Normalized Distance" ve "Normalized Distance Inverted" outputlarını kullanarak invert edilmemiş degerleri alabilirsiniz. Dedigim gibi, bu iki output [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Normalized Range" ve "Inverse Normalized Range" outputları ile aynıdırlar.


İnput | İşlem
:---: | :---:
Start Position | Başlangıç noktası
End Position | Bitiş noktası
Distance | Mesafe degeri, sınır
InvertFalloff | Output olarak inverse edilmiş degeri verir
Falloff Scale | "Falloff" outputunu bu deger ile çarparak verir
Fallback Vector | Eger başlangıç ve bitiş noktaları arasındaki mesafe 0 ise, "Normalized Vector Between Positions" outputu olarak bu degeri verir.

Output | İçerik
:---: | :---:
Falloff | [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Normalized Range" ile aynıdır ama "Falloff Scale" inputuna göre çarpılmıştır, aralıgı degiştirilmiştir
Normalized Falloff | "Falloff" outputunun aksine bu deger degiştirilmemiştir, 0 - 1 arasındadır
Normalized Vector Between Positions | [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Normalized Vector Between Positions" ile aynıdır
Normalized Distance | [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Normalized Range" ile aynıdır ve "InvertFalloff" inputu True olsa bile etkilenmezler
Normalized Distance Inverted | [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Inverse Normalized Range" ile aynıdır ve "InvertFalloff" inputu True olsa bile etkilenmezler
Position Is Within Range | [Normalize Distance Range](#normalize-distance-range) fonksiyonundaki "Within Range" ile aynıdır



* #### [Distance Based Falloff*]()
Bu node yanlışlıkla tekrar eklenmiş sanırım. [Distance Based Falloff](#distance-based-falloff) ile aynıdır.

* #### [Do Once Fn]()
bilmiyorum.

* #### [Drag Velocity*]()
bilmiyorum.

* #### [Emitter Change State]()
bilmiyorum.

* #### [Euler to Axis Angle]()
bilmiyorum.

* #### [Euler to Quaternion]()
bilmiyorum.

* #### [Euler to Rotation Matrix]()
bilmiyorum.

* #### [Extract Basis Vectors from Quaternion]()
bilmiyorum.

* #### [Find Angle Between Vectors]()
bilmiyorum.

* #### [Find Barycentric Coordinate]()
bilmiyorum.

* #### [Find Closest Point on Line]()
bilmiyorum.

* #### [Find Grid Location Ribbon ID]()
bilmiyorum.

* #### [Find Mid Point Between Positions]()
bilmiyorum.

* #### [Find Nearest Barycentric Coordinate Edge]()
bilmiyorum.

* #### [Find Nearest Distance Field Surface GPU]()
bilmiyorum.

* #### [Find Perpendicular 2d Vector]()
bilmiyorum.

* #### [Find Pixel Center 1D]()
bilmiyorum.

* #### [Find Pixel Center 2D]()
bilmiyorum.

* #### [Find Plane Normal]()
bilmiyorum.

* #### [Find Position on Bezier Spline]()
bilmiyorum.

* #### [Find Position on Catmull Rom Spline]()
bilmiyorum.

* #### [Find Quat Between]()
bilmiyorum.

* #### [Find Skeletal Mesh Triangle Normal*]()
bilmiyorum.

* #### [Find Tangential Velocity on Sphere]()
bilmiyorum.

* #### [Float as Int*]()
bilmiyorum.

* #### [FN First Frame Numeric]()
bilmiyorum.

* #### [Gaussian Random Float]()
bilmiyorum.

* #### [Get Matrix Scale]()
bilmiyorum.

* #### [Get Matrix Translation]()
bilmiyorum.

* #### [Get Random Info*]()
Bu fonksiyon RNG (Random Number Generator) kullanımı ve determinisim degerlerini hesaplamak için vardır. Output olarak [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) verir. Eger "RandomnessMode" inputuna verilen deger deterministik ise belirli düzene göre degerler (3 tane, vektör gibi) oluşturup verir, bu degerler seed görevi görür. Eger deterministik degil ise (-1, -1, -1) şeklinde [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) degeri verir. Eger "OverrideSeed" ayarını açtıysanız verdiginiz seed numarasına göre [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) oluşturur. Normalde oluşturdugu [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) degerinin 1. sırasında, varsa parçacık numarası. 2. sırasında toplamda geçen tick (kare, frame) sayısı. 3. sırasında ise seed numarası vardır. Eger "Fixed Override Seed" ayarını açarsanız oluşturulan [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) degerinin 1. sırasında seed numarası, geriye kalan degerlerinde de 0 olur. Yani oluşturulan [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) degerine başka şeyler katmaz, bu da sadece verdiginiz seed numarası degiştigi zaman [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) degerinin degişecegi anlamına gelir. Yani %100 seed numarası kullanımını açar, her şey verdiginiz seed numarasına göre olur.


İnput | İşlem
:---: | :---:
Seed | "RandomInfo" outputundaki oluşturulan [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) degerinin 3. sırasındaki deger bu seed numarasıdır. 1. ve 2. degerler ise varsa parçacık numarası ve toplamda geçen tick (kare, frame) sayısıdır.
OverrideSeed | "Seed" kullanımını açar
Fixed Override Seed | Bu ayarı açarsanız oluşturulan [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) degerinin 1. sırasında seed numarası, geriye kalan degerlerinde de 0 olur. (seed, 0, 0)
RandomnessMode | [ENiagaraRandomnessMode](../../Niagara%20Editörü/Parameters#eniagararandomnessmode) türünden determinism/rastgelelik degeri.

Output | İçerik
:---: | :---:
RandomInfo | Oluşturulan [Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) degeri.
Use Deterministic Randoms | Degerlerin deterministik olarak hazırlanıp hazırlanmadıgını belirtir.



* #### [Height Lerp]()
bilmiyorum.

* #### [Houdini Quat to Unreal Quat]()
bilmiyorum.

* #### [Houdini Vector to Unreal Vector]()
bilmiyorum.

* #### [HSVTO RGB*]()
bilmiyorum.

* #### [Hue Shift Linear Color]()
bilmiyorum.

* #### [Increment Over Time]()
bilmiyorum.

* #### [Index to Grid Location]()
bilmiyorum.

* #### [Int as Float*]()
bilmiyorum.

* #### [Interpolate Over Time Float]()
bilmiyorum.

* #### [Interpolate Over Time Linear Color]()
bilmiyorum.

* #### [Interpolate Over Time Quaternion]()
bilmiyorum.

* #### [Interpolate Over Time V2]()
bilmiyorum.

* #### [Interpolate Over Time V3]()
bilmiyorum.

* #### [Interpolate Over Time V4]()
bilmiyorum.

* #### [Invert Quaternion]()
bilmiyorum.

* #### [Is Point Above Plane]()
Bu fonksiyon verilen inputlara göre sanal (hayali) bir plaka, yani bir yüzey oluşturur. Verdiginiz nokta bu yüzeyin baktıgı yönde mi (plane normal) diye kontrol eder.


İnput | İşlem
:---: | :---:
Point | Noktanın konumu
Plane Position | Oluşturulacak plakanın, yüzeyin konumu
Plane Normal | Oluşturulacak plakanın, yüzeyin bakış açısı, yönü. Yani bu degere göre oluşturdugunuz yüzeyin baktıgı yön bulunacak ve noktanın konumu ile karşılaştırılacak

Output | İçerik
:---: | :---:
IsAbovePIane | Nokta plakanın, yüzeyin baktıgı yönde ise True, degilse False
Dot Between Point and Plane | Noktanın plakanın, yüzeyin üstünde oldugunu hesaplamak için [Dot Product](#dot) kullanılıyor. Eger nokta biraz bile (yani 0'dan büyük oldugu sürece) plakanın baktıgı yönde ise, o zaman "IsAbovePIane" outputu True döndürüyor. Bu deger ise hesaplanan [Dot Product](#dot) degeri



* #### [Is Point Between Slabs]()
Bu fonksiyon verilen inputlara göre 2 tane sanal (hayali) plaka, yani yüzey oluşturur. Verdiginiz nokta bu 2 yüzeyin arasında mı diye kontrol eder.


İnput | İşlem
:---: | :---:
Point | Noktanın konumu
Slab Origin | Oluşturulacak yüzeylerin konumu (iki yüzeyin ortası)
Slab Axis | Oluşturulacak yüzeylerin bakış açısı, yönü.
Slab Width | Oluşturulacak yüzeylerin aralıgı

Output | İçerik
:---: | :---:
IsBetweenSlabs | Nokta 2 yüzeyin arasında ise True, degilse False
Signed Result | "IsBetweenSlabs" outputunun degerinin [Sign'dan](#sign) geçirilmiş hali, yani "IsBetweenSlabs" False iken bu deger -1, degilken +1



* #### [Is Point Inside Box]()
bilmiyorum.

* #### [Is Point Inside Cone]()
Bu fonksiyon verilen inputlara göre sanal (hayali) bir koni oluşturur ve verdiginiz nokta bu koninin içinde mi diye kontrol eder.


İnput | İşlem
:---: | :---:
Point | Noktanın konumu
Cone Origin | Koninin orijin (orta) noktası
Cone Angle | Koninin açısı, genişligi
Normalized Cone Axis | Oluşturulacak koninin bakış açısı, yönü.
Cone Length | Koninin uzunlugu

Output | İçerik
:---: | :---:
IsInsideCone | Nokta koninin içindeyse True, degilse False



* #### [Is Point Inside Sphere]()
Bu fonksiyon verilen inputlara göre sanal (hayali) bir küre oluşturur ve verdiginiz nokta bu kürenin içinde mi diye kontrol eder.


İnput | İşlem
:---: | :---:
Point | Noktanın konumu
Sphere Origin | Kürenin orijin (orta) noktası
Sphere Radius | Kürenin çapı

Output | İçerik
:---: | :---:
IsInsideSphere | Nokta kürenin içindeyse True, degilse False



* #### [Is Value Within Range]()
bilmiyorum.

* #### [Isolate Longest Vector Component]()
bilmiyorum.

* #### [Lerp Multiple Numeric Fn]()
bilmiyorum.

* #### [Lerp Quaternion]()
bilmiyorum.

* #### [Line Segment Plane Intersection]()
bilmiyorum.

* #### [Maintain in Camera Particle Scale]()
bilmiyorum.

* #### [Make Quaternion from 3Basis Vectors]()
bilmiyorum.

* #### [Make Quaternion from XAnd YVectors]()
bilmiyorum.

* #### [Make Quaternion from XAnd ZVectors]()
bilmiyorum.

* #### [Make Scale Matrix]()
bilmiyorum.

* #### [Make Translation Matrix]()
bilmiyorum.

* #### [Make Vectors Orthogonal]()
bilmiyorum.

* #### [Match Velocity Via Force]()
bilmiyorum.

* #### [Matrix to Quaternion]()
bilmiyorum.

* #### [Ms Pivot Painter 2 Calculate Mesh Element Index NF]()
bilmiyorum.

* #### [Ms Pivot Painter 2 Decode 8Bit Alpha Axis Extent NF]()
bilmiyorum.

* #### [Ms Pivot Painter 2 Decode Axis Vector NF]()
bilmiyorum.

* #### [Ms Pivot Painter 2 Decode Postion NF]()
bilmiyorum.

* #### [Ms Pivot Painter 2 Pack Integer as Float NF]()
bilmiyorum.

* #### [Ms Pivot Painter 2 Return Parent Texture Info NF]()
bilmiyorum.

* #### [Ms Pivot Painter 2 Unpack Integer as Float NF]()
bilmiyorum.

* #### [Multiply by 2PI]()
bilmiyorum.

* #### [Multiply Quaternion]()
bilmiyorum.

* #### [Multiply Vector with Quaternion]()
bilmiyorum.

* #### [New Niagara Script*]()
bilmiyorum.

* #### [Niagara Distance Field Collisions]()
bilmiyorum.

* #### [Nlerp Function]()
bilmiyorum.

* #### [Normalize Distance Range]()
Bu fonksiyon şu işe yarar. Verdiginiz iki noktanın arasındaki mesafe degerini, input olarak verdiginiz "distance" degerine göre 0 - 1 arasında oranlar, yani normalize eder. Bu da bize Falloff degerini vermiş olur, yani bi uzaklık degeri belirleyip sanal bir küre oluştururuz ve bu uzaklık degeri çap görevi görür, bu alan içinde orta noktadan en uç noktaya dogru, verdigimiz noktanın sınıra ne kadar yakın oldugunu buluruz. Mesela diyelim ki "Start Position" olarak (0,0,0), "End Position" olarak (150,0,0), ve "Distance" olarak 300 verdik. Bu durumda başlangıç ve bitiş noktası arasındaki mesafe 150 olacaktır. "Distance" olarak 300 verdigimiz için, 150'nin 300'e göre oranı %50 dir, %50 nin 0 - 1 arasındaki karşılıgı 0.5 oldugu için "Normalized Range" outputu 0.5 verir.


İnput | İşlem
:---: | :---:
Start Position | Başlangıç noktası, genellikle (0,0,0) veririz çünkü (0,0,0) konumunu baz alırız, yani hiç hareket etmemiş, başlangıç konumunu. Eger herhangi bir şeyin konumunu baz alarak Falloff degeri almak istiyorsanız, o şeyin konumunu verebilirsiniz
End Position | Bitiş noktası, bu noktanın başlangıç noktasına olan uzaklıgına, "Distance" inputuna verdigimiz sınır degerine göre, noktanın sınıra ne kadar yakın oldugu belirlenir.
Distance | Mesafe degeri, sınır, bu deger ile sanal bir küre oluştururuz gibi düşünün, küremiz başlangıç noktasını orta nokta olarak baz alır, bitiş noktasının konumu sınır degerini geçtigi zaman, sınırın dışına çıkmış olur
Fallback Vector | Eger başlangıç ve bitiş noktaları arasındaki mesafe 0 ise, "Normalized Vector Between Positions" outputu olarak bu degeri verir.

Output | İçerik
:---: | :---:
Normalized Range | İki noktanın arasındaki mesafe degerinin, input olarak verdiginiz "distance" degerine göre 0 - 1 arasındaki oranı, yani normalize edilmiş degeri. Bu deger bize bitiş noktasının sınıra ne kadar yakın oldugunu söyler, tam orta noktada iken 0 yani sınırdan en uzak mesafede, tam uç noktada iken 1 yani sınır üzerinde demektir.
Inverse Normalized Range | "Normalized Range" output degerinin 1'den çıkarılmış hali yani inverse edilmiş hali. "Normalized Range" outputu sınıra olan yakınlıgı veriyorsa, bu deger de sınıra olan uzaklıgı verir, yani "Normalized Range" outputu 0.4 ise, bu deger 0.6 dır.
Normalized Vector Between Positions | Bitiş noktasından başlangıç noktasına dogru olan yönü verir, yani bitiş noktasının başlangıç noktasına dogru gitmek için gidecegi yönü.
Within Range | Bitiş noktasının sınır içinde olup olmadıgı bilgisini verir. Bitiş noktası sınırı geçmediyse True döndürür, geçtiyse False.



* #### [Normalized Execution Index]()
bilmiyorum.

* #### [Octahedron to Unit Vector GPU]()
bilmiyorum.

* #### [Owner Axes]()
Owner için (yani direktmen simulasyon, dünya üzerindeki niagara objesi) için yön degerlerini verir (Bkz. [Engine.Owner.SystemXAxis](../../Niagara%20Editörü/Parameters#engineownersystemxaxis), [Engine.Owner.SystemYAxis](../../Niagara%20Editörü/Parameters#engineownersystemyaxis), [Engine.Owner.SystemZAxis](../../Niagara%20Editörü/Parameters#engineownersystemzaxis)). Eger [Local Space](../../Niagara%20Editörü/Graph#local-space) açıksa XYZ için (1,0,0), (0,1,0), (0,0,1) döndürür. 

* #### [Parametric Torus]()
bilmiyorum.

* #### [Parametric Torus Knot]()
bilmiyorum.

* #### [Place Particles on A Rectangle Fn]()
bilmiyorum.

* #### [Plane Sphere Collision Detection]()
bilmiyorum.

* #### [Point Plane Distance]()
bilmiyorum.

* #### [Point to Line Segment Distance]()
(Bu fonksiyon gizli bir fonksiyondur, [bkz](#yazım-şekli)) Bu fonksiyon sizden bir nokta ve bir çizgi/dogru (line) alır. Bunları kullanarak noktanın dogruya ulaşmak için gidecegi yol ve yön bilgisini, ayrıca dogru üzerinde bizim verdigimiz noktaya en yakın olan noktanın konumunu ve dogru ile noktamız arasındaki mesafeyi verir.


İnput | İşlem
:---: | :---:
Point | Noktanın konumu (V3)
Line Segment Start | Dogrunun başlangıç noktası
Line Segment End | Dogrunun bitiş noktası
Parameter Map | Fonksiyonun işlemleri gerçekleştirmesi için simulasyon bilgilerine ihtiyacı var, [ParameterMap](../Terimler%20Sözlügü#parametermap) vermelisiniz
Line Segment in Localspace | Dogrunun [Local Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space) üzerinde olup olmayacagını belirler.

Output | İçerik
:---: | :---:
Vector from Point to Line | Verdiginiz nokta ile dogru arasındaki mesafe (sanırım dogruya en yakın olan nokta ile arasındaki mesafe), yani bu degeri noktanız ile toplarsanız, dogruya ulaşırsınız, bu vektör noktanızın dogruya gitmesi için gerekli olan yolu belirtir
Normalized Vector from Point to Line | "Vector from Point to Line" outputunun [normalize](#normalize) edilmiş hali, normalized oldugu için yön degeri görevi görüyor yani bu deger noktanızın dogruya ulaşması için gidecegi yön degeridir, dogrunun noktaya olan yönüdür.
Closest Point on Line Segment | Dogru üzerindeki, verdigimiz noktaya en yakın olan noktanın konumu
Distance from Point to Line | Dogru ile verdigimiz nokta arasındaki mesafe



* #### [Polar to Cartesian Coordinates]()
bilmiyorum.

* #### [Position to Vector]()
bilmiyorum.

* #### [Project Position on Plane]()
bilmiyorum.

* #### [Project Vector on Plane]()
bilmiyorum.

* #### [Quaternion to Axis Angle]()
bilmiyorum.

* #### [Quaternion to Rotation Matrix]()
bilmiyorum.

* #### [Random Point in Box]()
bilmiyorum.

* #### [Random Quaternion]()
bilmiyorum.

* #### [Random Range]()
(Bu fonksiyon gizli bir fonksiyondur, [bkz](#yazım-şekli)) Bu fonksiyon verdiginiz iki sayı arasında rastgele deger verir (min dahil, max hariç). Geriye kalan bütün inputlar [Get Random Info](#get-random-info) fonksiyonundaki inputlar ile aynıdır, bu inputları anlamak için [Get Random Info](#get-random-info) fonksiyonuna bakın. Eger kodlara bakarsanız inputlarınızı [Get Random Info](#get-random-info) fonksiyonuna verdigini görebilirsiniz.


İnput | İşlem
:---: | :---:
Min | Minimum deger
Max | Maximum deger
Seed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
OverrideSeed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
Fixed Override Seed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
RandomnessMode | [Get Random Info](#get-random-info) fonksiyonuna bakın.

Output | İçerik
:---: | :---:
Result | Rastgele seçilen deger (float)



* #### [Random Range Float]()
(Bu fonksiyon gizli bir fonksiyondur, [bkz](#yazım-şekli)) Bu fonksiyon verdiginiz iki sayı arasında rastgele deger verir (min dahil, max hariç). Geriye kalan bütün inputlar [Get Random Info](#get-random-info) fonksiyonundaki inputlar ile aynıdır, bu inputları anlamak için [Get Random Info](#get-random-info) fonksiyonuna bakın. Eger kodlara bakarsanız inputlarınızı [Get Random Info](#get-random-info) fonksiyonuna verdigini görebilirsiniz.


İnput | İşlem
:---: | :---:
Min | Minimum float
Max | Maximum float
Seed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
OverrideSeed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
Fixed Override Seed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
RandomnessMode | [Get Random Info](#get-random-info) fonksiyonuna bakın.

Output | İçerik
:---: | :---:
Result | Rastgele seçilen deger (float)



* #### [Random Range Integer]()
(Bu fonksiyon gizli bir fonksiyondur, [bkz](#yazım-şekli)) Bu fonksiyon verdiginiz iki sayı arasında rastgele deger verir (min dahil, max hariç). Geriye kalan bütün inputlar [Get Random Info](#get-random-info) fonksiyonundaki inputlar ile aynıdır, bu inputları anlamak için [Get Random Info](#get-random-info) fonksiyonuna bakın. Eger kodlara bakarsanız inputlarınızı [Get Random Info](#get-random-info) fonksiyonuna verdigini görebilirsiniz.


İnput | İşlem
:---: | :---:
Min | Minimum integer
Max | Maximum integer
Seed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
OverrideSeed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
Fixed Override Seed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
RandomnessMode | [Get Random Info](#get-random-info) fonksiyonuna bakın.

Output | İçerik
:---: | :---:
Result | Rastgele seçilen deger (integer)



* #### [Random Unit Vector]()
(Bu fonksiyon gizli bir fonksiyondur, [bkz](#yazım-şekli)) Bu fonksiyon unit vektörleri verir, yani 1 birimlik vektörler. 1 birimlik vektörler aynı zamanda yön degeri de ifade eder. Vektörlerin hiçbir boyutu 1'den fazla -1'den az olamaz, aynı yön degerleri gibi. Aldıgı bütün inputlar [Get Random Info](#get-random-info) fonksiyonundaki inputlar ile aynıdır, bu inputları anlamak için [Get Random Info](#get-random-info) fonksiyonuna bakın. Eger kodlara bakarsanız inputlarınızı [Get Random Info](#get-random-info) fonksiyonuna verdigini görebilirsiniz.


İnput | İşlem
:---: | :---:
Seed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
OverrideSeed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
Fixed Override Seed | [Get Random Info](#get-random-info) fonksiyonuna bakın.
RandomnessMode | [Get Random Info](#get-random-info) fonksiyonuna bakın.

Output | İçerik
:---: | :---:
Unit Vector 3D | 3 boyutlu yön degeri (Unit Vector)
Unit Vector 2D | 2 boyutlu yön degeri (Unit Vector)



* #### [Random Vector]()
(Bu fonksiyon gizli bir fonksiyondur, [bkz](#yazım-şekli)) Bu fonksiyon özünde [Random Unit Vector](#random-unit-vector) kullanır. Bütün inputları [Random Unit Vector](#random-unit-vector) ile aynıdır, aldıgı inputlar ile [Random Unit Vector](#random-unit-vector) fonksiyonunu çalıştırır ve [Random Unit Vector'un](#random-unit-vector) "Unit Vector 3D" outputunu verir. Yani [Random Unit Vector'dan](#random-unit-vector) tek farkı direktmen "Unit Vector 3D" outputunu vermesidir.

* #### [Random Vector in Cone*]()
bilmiyorum.

* #### [Randomize Collision Normals*]()
bilmiyorum.

* #### [Reflect Vector]()
bilmiyorum.

* #### [Region Mask Box*]()
bilmiyorum.

* #### [Region Mask Plane*]()
bilmiyorum.

* #### [Region Mask Slab*]()
bilmiyorum.

* #### [Region Mask Sphere*]()
bilmiyorum.

* #### [Remap Range]()
bilmiyorum.

* #### [RGBTo HSV*]()
bilmiyorum.

* #### [Rotate Angle on Axis]()
bilmiyorum.

* #### [Rotate Vector 2D]()
bilmiyorum.

* #### [Saturate Float]()
Sıfır ve bir arasında [clamp](#clamp) yapar. [Clamp(0, 1)](#clamp) ile eşit yani, ama çok kullanılan bir noddur.

* #### [Scale and Offset Vector]()
bilmiyorum.

* #### [Scale UVs by Center]()
bilmiyorum.

* #### [Scene Depth Test]()
bilmiyorum.

* #### [Select V2Channel]()
bilmiyorum.

* #### [Select V3Channel]()
bilmiyorum.

* #### [Select V4Channel]()
bilmiyorum.

* #### [Set Bool by Timer]()
bilmiyorum.

* #### [Simulation Position]()
Eger [Local Space](../../Niagara%20Editörü/Graph#local-space) açıksa (0,0,0), kapalıysa [Engine.Owner.Position](../../Niagara%20Editörü/Parameters#engineownerposition) parametresindeki degeri döndürür.

* #### [Simulation Stage Iteration Info]()
bilmiyorum.

* #### [Sin XOver XIn Radians*]()
bilmiyorum.

* #### [Slerp Quaternion]()
bilmiyorum.

* #### [Slerp Vectors]()
bilmiyorum.

* #### [Smooth Gradient Threshold]()
bilmiyorum.

* #### [Smooth Lerp Over Time]()
bilmiyorum.

* #### [Sphere Cast Global Distance Field]()
bilmiyorum.

* #### [Sphere Plane Intersection]()
bilmiyorum.

* #### [Sphere Trace Distance Field GPU]()
bilmiyorum.

* #### [Spherical to Cartesian Coordinates]()
bilmiyorum.

* #### [Spot Light Overlap Test]()
bilmiyorum.

* #### [Spring Force]()
bilmiyorum.

* #### [Sub UV Texture Coordinates]()
bilmiyorum.

* #### [System Change State]()
bilmiyorum.

* #### [Transform 2DLocal Position to World Space]()
bilmiyorum.

* #### [Transform Base]()
[Transform Offset](#transform-offset), [Transform Vector](#transform-vector), [Transform Position](#transform-position) fonksiyonları özünde bu fonksiyonu kullanır. Bu fonksiyon konum degerlerinin [Coordinate Space'ini](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space) degiştirmemize yarar.


İnput | İşlem
:---: | :---:
Source Space | Kaynak [Coordinate Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space)
Destination Space | Hedef [Coordinate Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space)
LocalToWorldTransform | Bilmiyorum.
WorldToLocalTransform | Bilmiyorum.
bLocalSpace | Bilmiyorum.


Output | İçerik
:---: | :---:
bUseOriginal | Bilmiyorum.
OutTransform | Bilmiyorum.
LocalToWorld | Bilmiyorum.



* #### [Transform Offset]()
[Transform Vector](#transform-vector) ile aynıdır. Özünde [Transform Base](#transform-base) kullanır. [Transform Vector'den](#transform-vector) tek farkı kodları farklı oldugu için, ek bir input olarak [ParameterMap](../Terimler%20Sözlügü#parametermap) almasıdır.


İnput | İşlem
:---: | :---:
InputMap | Fonksiyonun işlemleri gerçekleştirmesi için simulasyon bilgilerine ihtiyacı var, [ParameterMap](../Terimler%20Sözlügü#parametermap) vermelisiniz
InVector | [Coordinate Space'i](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space) degiştirilecek vektör (V3)
Source Space | Kaynak [Coordinate Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space)
Destination Space | Hedef [Coordinate Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space)
Apply Scale | Eger True ise Scale degerlerini de kullanır, yani [Engine.Owner.SystemLocalToWorldNoScale](../../Niagara%20Editörü/Parameters#engineownersystemlocaltoworldnoscale) yerine [Engine.Owner.SystemLocalToWorld](../../Niagara%20Editörü/Parameters#engineownersystemlocaltoworld), [Engine.Owner.SystemWorldToLocalNoScale](../../Niagara%20Editörü/Parameters#engineownersystemworldtolocalnoscale) yerine [Engine.Owner.SystemWorldToLocal](../../Niagara%20Editörü/Parameters#engineownersystemworldtolocal) kullanılır.


Output | İçerik
:---: | :---:
OutVector | [Coordinate Space'i](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space) degiştirilmiş vektör.



* #### [Transform Position]()
[Transform Vector](#transform-vector) ile aynıdır. Özünde [Transform Base](#transform-base) kullanır. [Transform Vector'den](#transform-vector) tek farkı input ve output olarak [Position](../../Niagara%20Editörü/Parameters#position) kullanmasıdır.


İnput | İşlem
:---: | :---:
Position | [Coordinate Space'i](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space) degiştirilecek pozisyon
Source Space | Kaynak [Coordinate Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space)
Destination Space | Hedef [Coordinate Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space)
Apply Scale | Eger True ise Scale degerlerini de kullanır, yani [Engine.Owner.SystemLocalToWorldNoScale](../../Niagara%20Editörü/Parameters#engineownersystemlocaltoworldnoscale) yerine [Engine.Owner.SystemLocalToWorld](../../Niagara%20Editörü/Parameters#engineownersystemlocaltoworld), [Engine.Owner.SystemWorldToLocalNoScale](../../Niagara%20Editörü/Parameters#engineownersystemworldtolocalnoscale) yerine [Engine.Owner.SystemWorldToLocal](../../Niagara%20Editörü/Parameters#engineownersystemworldtolocal) kullanılır.


Output | İçerik
:---: | :---:
Position | [Coordinate Space'i](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space) degiştirilmiş pozisyon.



* #### [Transform Stack Rotation*]()
bilmiyorum.

* #### [Transform Vector]()
[Transform Position](#transform-position) ile aynıdır. Özünde [Transform Base](#transform-base) kullanır. [Transform Position'dan](#transform-position) tek farkı input ve output olarak [Vector](../../Niagara%20Editörü/Parameters#vector) kullanmasıdır.


İnput | İşlem
:---: | :---:
InVector | [Coordinate Space'i](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space) degiştirilecek vektör (V3)
Source Space | Kaynak [Coordinate Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space)
Destination Space | Hedef [Coordinate Space](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space)
Apply Scale | Eger True ise Scale degerlerini de kullanır, yani [Engine.Owner.SystemLocalToWorldNoScale](../../Niagara%20Editörü/Parameters#engineownersystemlocaltoworldnoscale) yerine [Engine.Owner.SystemLocalToWorld](../../Niagara%20Editörü/Parameters#engineownersystemlocaltoworld), [Engine.Owner.SystemWorldToLocalNoScale](../../Niagara%20Editörü/Parameters#engineownersystemworldtolocalnoscale) yerine [Engine.Owner.SystemWorldToLocal](../../Niagara%20Editörü/Parameters#engineownersystemworldtolocal) kullanılır.


Output | İçerik
:---: | :---:
OutVector | [Coordinate Space'i](../../Niagara%20Editörü/Terimler%20Sözlügü#local-ve-world-coordinate-space) degiştirilmiş vektör.



* #### [Transform Vector to Mesh Space]()
bilmiyorum.

* #### [Translate Barycentric Edge Coordinates]()
bilmiyorum.

* #### [Unit Vector to Octahedron GPU]()
bilmiyorum.

* #### [Validate Barycentric Coordinates]()
bilmiyorum.

* #### [Vector to Position]()
bilmiyorum.

* #### [Wedge Location]()
bilmiyorum.

* #### [World Position to Screen UV]()
bilmiyorum.

* #### [XYZRotation to Quaternion]()
bilmiyorum.


## Integer

* #### [Bitwise AND](https://code.tutsplus.com/articles/understanding-bitwise-operators--active-11301)
Bitwise "And" operatörü kullanmanıza yarar. Bitwise işlemleri ögrenmek istiyorsanız linke bakabilirsiniz.

* #### [Bitwise Left Shift](https://code.tutsplus.com/articles/understanding-bitwise-operators--active-11301)
Bitwise "Left Shift" operatörü kullanmanıza yarar. Bitwise işlemleri ögrenmek istiyorsanız linke bakabilirsiniz.

* #### [Bitwise NOT](https://code.tutsplus.com/articles/understanding-bitwise-operators--active-11301)
Bitwise "Not" operatörü kullanmanıza yarar. Bitwise işlemleri ögrenmek istiyorsanız linke bakabilirsiniz.

* #### [Bitwise OR](https://code.tutsplus.com/articles/understanding-bitwise-operators--active-11301)
Bitwise "Or" operatörü kullanmanıza yarar. Bitwise işlemleri ögrenmek istiyorsanız linke bakabilirsiniz.

* #### [Bitwise Right Shift](https://code.tutsplus.com/articles/understanding-bitwise-operators--active-11301)
Bitwise "Right Shift" operatörü kullanmanıza yarar. Bitwise işlemleri ögrenmek istiyorsanız linke bakabilirsiniz.

* #### [Bitwise XOR](https://code.tutsplus.com/articles/understanding-bitwise-operators--active-11301)
Bitwise "Xor" operatörü kullanmanıza yarar. Bitwise işlemleri ögrenmek istiyorsanız linke bakabilirsiniz.


## Make

* #### [bool(Make bool)]()
[Bool](../../Niagara%20Editörü/Parameters#bool) oluşturmanıza yarar, verdiginiz inputa göre True ve ya False döndürür.

* #### [Chaos Destruction Event]()
bilmiyorum.

* #### [ECollisionChannel]()
bilmiyorum.

* #### [EFieldIntegerType]()
bilmiyorum.

* #### [EFieldScalarType]()
bilmiyorum.

* #### [EFieldVectorType]()
bilmiyorum.

* #### [ENiagara_AngleInput]()
bilmiyorum.

* #### [ENiagara_AttributeSamplingApplyOutput]()
bilmiyorum.

* #### [ENiagara_AutomaticManual]()
bilmiyorum.

* #### [ENiagara_BoxPlaneMode]()
bilmiyorum.

* #### [ENiagara_ColorInitializationMode]()
bilmiyorum.

* #### [ENiagara_ConeMode]()
bilmiyorum.

* #### [ENiagara_CPUCollisionType]()
bilmiyorum.

* #### [ENiagara_CylinderMode]()
bilmiyorum.

* #### [ENiagara_EmitterStateOptions]()
bilmiyorum.

* #### [ENiagara_Float4Channel]()
bilmiyorum.

* #### [ENiagara_FPSPlayrate]()
bilmiyorum.

* #### [ENiagara_GPUCollisionType]()
bilmiyorum.

* #### [ENiagara_InfiniteLoopDuration]()
bilmiyorum.

* #### [ENiagara_LifetimeMode]()
bilmiyorum.

* #### [ENiagara_LocationShapes]()
bilmiyorum.

* #### [ENiagara_MassInitializationMode]()
bilmiyorum.

* #### [ENiagara_OffsetMode]()
bilmiyorum.

* #### [ENiagara_PositionInitializationMode]()
bilmiyorum.

* #### [ENiagara_RotationMode]()
bilmiyorum.

* #### [ENiagara_ScaleMode]()
bilmiyorum.

* #### [ENiagara_SizeScaleMode]()
bilmiyorum.

* #### [ENiagara_SpriteRotationMode]()
bilmiyorum.

* #### [ENiagara_SubUVLookupMode]()
bilmiyorum.

* #### [ENiagara_SubUVLookupModeV2]()
bilmiyorum.

* #### [ENiagara_TransformOrder]()
bilmiyorum.

* #### [ENiagara_TransformType]()
bilmiyorum.

* #### [ENiagara_UnsetDirectSet]()
bilmiyorum.

* #### [ENiagara_UnsetDirectSetRandom]()
bilmiyorum.

* #### [ENiagara_UVFlippingMode]()
bilmiyorum.

* #### [ENiagara_VelocityMode]()
bilmiyorum.

* #### [ENiagara_WrapClamp]()
bilmiyorum.

* #### [ENiagaraAerodynamicDragPivotMode]()
bilmiyorum.

* #### [ENiagaraCalculateRadiusOptions]()
bilmiyorum.

* #### [ENiagaraChannelCorrelation]()
bilmiyorum.

* #### [ENiagaraCollisionRadiusOptions]()
bilmiyorum.

* #### [ENiagaraCompileUsageStaticSwitch]()
bilmiyorum.

* #### [ENiagaraCoordinateSpace]()
bilmiyorum.

* #### [ENiagaraCurlNoiseQuality]()
bilmiyorum.

* #### [ENiagaraDragCoefficientShapeMode]()
bilmiyorum.

* #### [ENiagaraEmitterLifeCycleMode]()
bilmiyorum.

* #### [ENiagaraEmitterScalabilityMode_Limited]()
bilmiyorum.

* #### [ENiagaraExecutionState]()
bilmiyorum.

* #### [ENiagaraExecutionStateManagement]()
bilmiyorum.

* #### [ENiagaraExecutionStateSource]()
bilmiyorum.

* #### [ENiagaraExpansionMode]()
bilmiyorum.

* #### [ENiagaraFrictionMergeType]()
bilmiyorum.

* #### [ENiagaraFunctionDebugState]()
bilmiyorum.

* #### [ENiagaraGridPlacementType]()
bilmiyorum.

* #### [ENiagaralnactiveMode]()
bilmiyorum.

* #### [ENiagaraLegacyTrailWidthMode]()
bilmiyorum.

* #### [ENiagaraMeshOrSprite]()
bilmiyorum.

* #### [ENiagaraMeshTransforms]()
bilmiyorum.

* #### [ENiagaraOrientationAxis]()
bilmiyorum.

* #### [ENiagaraRandomnessEvaluation]()
bilmiyorum.

* #### [ENiagaraRandomnessMode]()
bilmiyorum.

* #### [ENiagaraRendererSourceDataMode]()
bilmiyorum.

* #### [ENiagaraRestitutionMergeType]()
bilmiyorum.

* #### [ENiagaraRingDiscMode]()
bilmiyorum.

* #### [ENiagaraScaleColorMode]()
bilmiyorum.

* #### [ENiagaraScriptContextStaticSwitch]()
bilmiyorum.

* #### [ENiagaraShapeTorusMode]()
bilmiyorum.

* #### [ENiagaraSimTarget]()
bilmiyorum.

* #### [ENiagaraSphereDistributionMode]()
bilmiyorum.

* #### [ENiagaraSpriteAlignment]()
bilmiyorum.

* #### [ENiagaraSpriteFacingMode]()
bilmiyorum.

* #### [ENiagaraSystemInactiveMode]()
bilmiyorum.

* #### [ENiagaraTorusDistributionMode]()
bilmiyorum.

* #### [ENiagaraVector4_Channels]()
bilmiyorum.

* #### [ENiagaraWindCombingMode]()
bilmiyorum.

* #### [ENiagaraWindFrictionDistanceMode]()
bilmiyorum.

* #### [ENiagaraWindFrictionMode]()
bilmiyorum.

* #### [ENiagaraWindGroundMaskMode]()
bilmiyorum.

* #### [ENiagaraWindOffsetMode]()
bilmiyorum.

* #### [ENiagaraWindTurbulenceContributionMode]()
bilmiyorum.

* #### [ENiagaraWindTurbulenceFrequencyMode]()
bilmiyorum.

* #### [ENiagaraWindTurbulenceMode]()
bilmiyorum.

* #### [float]()
[Float](../../Niagara%20Editörü/Parameters#float) oluşturmanıza yarar, verdiginiz inputa göre float döndürür.

* #### [Half]()
Half veri tipinin ne oldugu ve nerelerde kullanıldıgından emin degilim ama sanırım float gibi.

* #### [Half Vector3]()
Half veri tipinden oluşan 3 boyutlu vektör.

* #### [Half Vector4]()
Half veri tipinden oluşan 4 boyutlu vektör.

* #### [int32]()
[İnteger](../../Niagara%20Editörü/Parameters#int32) oluşturmanıza yarar, verdiginiz inputa göre integer döndürür.

* #### [Linear Color]()
[Linear Color](../../Niagara%20Editörü/Parameters#linear-color) yani renk verisi oluşturmanıza yarar. RGBA olmak üzere 4 float alır.

* #### [Matrix]()
[Matrix](../../Niagara%20Editörü/Parameters#matrix) oluşturmanıza yarar. 4 tane 4 boyutu vektör alır.

* #### [Mesh Tri Coordinate]()
[Mesh Tri Coordinate](../../Niagara%20Editörü/Parameters#mesh-tri-coordinate) oluşturmanıza yarar.

* #### [Niagara Collision Event Payload]()
[Niagara Collision Event Payload](../../Niagara%20Editörü/Parameters#niagara-collision-event-payload) oluşturmanıza yarar.

* #### [Niagara ID]()
[Niagara ID](../../Niagara%20Editörü/Parameters#niagara-id) oluşturmanıza yarar.

* #### [Niagara Rand Info]()
[Niagara Rand Info](../../Niagara%20Editörü/Parameters#niagara-rand-info) oluşturmanıza yarar.

* #### [Position]()
[Position](../../Niagara%20Editörü/Parameters#position) yani pozisyon verisi oluşturmanıza yarar. XYZ olmak üzere 3 float alır.

* #### [Quat]()
[Quat](../../Niagara%20Editörü/Parameters#quat) oluşturmanıza yarar.

* #### [Spawn Info]()
[Spawn Info](../../Niagara%20Editörü/Parameters#spawn-info) oluşturmanıza yarar.

* #### [Static bool]()
[Static bool](../../Niagara%20Editörü/Parameters#static-bool) oluşturmanıza yarar. Normal bool'un aksine, yürütme esnasında (runtime) degiştirilemez, degiştirirseniz hata alırsınız.

* #### [Static ENiagaraRandomnessMode]()
bilmiyorum.

* #### [Static int32]()
[Static int32](../../Niagara%20Editörü/Parameters#static-int32) oluşturmanıza yarar. Normal int32'nin aksine, yürütme esnasında (runtime) degiştirilemez, degiştirirseniz hata alırsınız.

* #### [Vector]()
[Vector](../../Niagara%20Editörü/Parameters#vector) oluşturmanıza yarar.

* #### [Vector 2D]()
[Vector 2D](../../Niagara%20Editörü/Parameters#vector-2d) oluşturmanıza yarar.

* #### [Vector 4]()
[Vector 4](../../Niagara%20Editörü/Parameters#vector-4) oluşturmanıza yarar.



## Matrix

* #### [Matrix Transform Position]()
bilmiyorum.

* #### [Matrix Transform Vector]()
bilmiyorum.

* #### [Multiply (Matrix * Matrix)](https://ncalculators.com/matrix/4x4-matrix-multiplication-calculator.htm)
Matrix * Matrix işlemi, linke bakabilirsiniz.

* #### [Multiply (Matrix * Vector4)]()
Matrix * Vector4 işlemi.

* #### [Row 0]()
Verilen matrix'in 1. dizesini döndürür.

* #### [Row 1]()
Verilen matrix'in 2. dizesini döndürür.

* #### [Row 2]()
Verilen matrix'in 3. dizesini döndürür.

* #### [Row 3]()
Verilen matrix'in 4. dizesini döndürür.

* #### [Transpose]()
Verilen matrix'e [transpose](https://en.wikipedia.org/wiki/Transpose) uygular.


## Numeric

* #### [Abs]()
Mutlak deger.

* #### [Add]()
Verilen bütün degerleri toplar.

* #### [ArcCosine]()
bilmiyorum.

* #### [ArcCosine(Degrees)]()
bilmiyorum.

* #### [ArcCosine(Radians)]()
bilmiyorum.

* #### [ArcSine]()
bilmiyorum.

* #### [ArcSine(Degrees)]()
bilmiyorum.

* #### [ArcSine(Radians)]()
bilmiyorum.

* #### [ArcTangent]()
bilmiyorum.

* #### [ArcTangent(Degrees)]()
bilmiyorum.

* #### [ArcTangent(Radians)]()
bilmiyorum.

* #### [ArcTangent2]()
bilmiyorum.

* #### [ArcTangent2(Degrees)]()
bilmiyorum.

* #### [ArcTangent2(Radians)]()
bilmiyorum.

* #### [Ceil]()
Verdiginiz sayıyı en yakın küçük tamsayıya yuvarlar (zıttı [Floor](#floor)). örnegin 
<br>
<br>
9.9 -> 9
<br>
9.1 -> 9

* #### [Clamp]()
Verdigimiz inputu "min" ve "max" degerine göre düzenler. Eger input min degerinden küçükse min degerine, input max degerinden büyükse max degerine taşınır.

* #### [Cosine]()
bilmiyorum.

* #### [Cosine(Degrees)]()
bilmiyorum.

* #### [Cosine(Radians)]()
bilmiyorum.

* #### [Cross]()
Türkçesi [Çapraz Çarpım](https://tr.wikipedia.org/wiki/%C3%87apraz_%C3%A7arp%C4%B1m) ve ya [Vektörel Çarpım](https://www.youtube.com/watch?v=QaaqS8oTl6E) olan matematik işlemi. İngilizce [wikipedia](https://en.wikipedia.org/wiki/Cross_product) sayfasına da bakabilirsiniz. Verilen iki vektöre dik inen bir vektör veriyor. Ne işe yaradıgını bilmiyorum.

* #### [DegreesToRadians]()
Verdigimiz dereceyi (yani açıyı) [radyana](https://tr.wikipedia.org/wiki/Radyan) dönüştürür ve ya radyan degerini verir de denebilir.

* #### [Divide]()
Bölme.

* #### [Dot]()
Türkçesi [Nokta Çarpım](https://tr.wikipedia.org/wiki/Nokta_%C3%A7arp%C4%B1m) ve ya [İç Çarpım](https://www.youtube.com/watch?v=JsB-XP0V3PE) olan matematik işlemi. İngilizce [wikipedia](https://en.wikipedia.org/wiki/Dot_product) sayfasına da bakabilirsiniz. Neyse işte, bu nodu iki vektörün yönlerini karşılaştırmak için kullanıyoruz. Mesele yönler oldugu için, eger vektörünüzün herhangi bir boyutunun degeri 1'den büyükse [Normalize](#normalize--%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F) kullanmalısınız, çünkü her yön degeri -1 ve 1 arasında oluyor, mesela eger X eksenine bakıyorsa 1, eger X ekseninin tam tersine bakıyorsa -1 gibi.

* #### [Equal]()
Verilen sayılar eşit ise True degil ise False döndürür.

* #### [Exp]()
Verdiginiz sayı kadar [e sayısının](https://tr.wikipedia.org/wiki/E_say%C4%B1s%C4%B1) üssünü alır.

* #### [Exp2]()
Verdiginiz sayı kadar 2'nin üssünü alır. Yani 2^x.

* #### [Floor]()
Verdiginiz sayıyı en yakın büyük tamsayıya yuvarlar (zıttı [Ceil](#ceil)). örnegin 
<br>
<br>
9.9 -> 10
<br>
9.1 -> 10

* #### [Frac]()
Verilen inputun kesirli yani . (nokta) dan sonraki kısmını verir. örnegin,
<br>
<br>
1.5 = 0.5
<br>
2.0 = 0
<br>
0.99 = 0.99

* #### [Greater Than]()
Verdiginiz ilk sayı ikinciden büyükse True degilse False döndürür.

* #### [Greater Than Or Equal]()
Verdiginiz ilk sayı ikinciden büyük ve ya eşitse True degilse False döndürür.

* #### [Hash Float]()
bilmiyorum.

* #### [Hash Integer]()
bilmiyorum.

* #### [Length]()
Verdiginiz vektörün boyunu ölçer. 1 boyutlu sayı verirseniz aynı degeri döndürür. 2 boyutlu vektör verirseniz, sanki (0,0) konumu ile sizin verdiginiz 2 boyutlu vektörün konumu arasındaki mesafeyi ölçermiş gibi hesaplar, 2 boyutlu vektör kullanırsanız [Pythagorean theorem'ini](https://en.wikipedia.org/wiki/Pythagorean_theorem) ([daha basit açıklama](https://byjus.com/maths/distance-between-two-points-formula/)) kullanır. 3 boyutlu vektör verirseniz, sanki (0,0,0) konumu ile sizin verdiginiz 3 boyutlu vektörün konumu arasındaki mesafeyi ölçermiş gibi hesaplar, aslında vektörün [Magnitude'ünü](https://byjus.com/maths/magnitude-of-a-vector/) verir. [Distance](#distance) nodunu kullanıp birine vektörünüzü diger inputa da (0,0,0) verince de aynı sonucu alırsınız.

* #### [Lerp]()
Formül: [(a * (1 - c)) + (b * c)](https://www.desmos.com/calculator/gtuwm4l27u). Verilen "c" degerine göre "a" ve "b" inputunu birbirine karıştırır, oranlar. Örnegin "a" ve "b" için iki sayı girin mesela 10 ve 0. Eger "c" degerine 0 verirseniz A, 1 verirseniz B degeri döndürülür. Eger "c" degerine 0.5 verirseniz sayımız da "a" ve "b" nin ortası yani 5 olur. Yani 0'a yaklaştıkça A, 1'e yaklaştıkça B. Kısacası en basit tanımıyla oranlama yapar diyebiliriz, yüzde olarak degilde 0 - 1 arası gibi düşünün, 0 = %0, 1 = %100.

* #### [Less Than]()
Verdiginiz ilk sayı ikinciden küçükse True degilse False döndürür.

* #### [Less Than Or Equal]()
Verdiginiz ilk sayı ikinciden küçükse ve ya eşitse True degilse False döndürür.

* #### [Log]()
[Logaritma](https://tr.wikipedia.org/wiki/Logaritma)

* #### [Log2]()
[İkilik logaritma](https://tr.wikipedia.org/wiki/Logaritma)

* #### [Max]()
Verilen inputlardan büyük olanı döndürür.

* #### [Min]()
Verilen inputlardan küçük olanı döndürür.

* #### [Modulo]()
Verdiginiz ilk sayının ikinciye bölümünden kalanı döndürür.

* #### [Modulo Fast]()
"Modulo" ile aynı ama precise yani dogruluk degeri daha düşük ama daha hızlı. Eger yüksek dogruluga ihtiyacınız yoksa bunu kullanabilirsiniz.

* #### [Multiply]()
Verdiginiz sayıları çarpar.

* #### [MultiplyAdd]()
"A" ve "B" olarak verilen sayıları çarpar ve sonuç ile "C" sayısını toplar.

* #### [Negate]()
Verilen sayıyı eksiye çevirir (-x), verdiginiz sayı eksi ise artı, artı ise eksi olur.

* #### [Noise]()
bilmiyorum.

* #### [Normalize]()
Verdiginiz vektör'ün degerlerini birbirleriyle oranlayıp en fazla 1'e eşit olacak şekilde 0 ve 1 arasına taşır (bütün boyutların toplamı 1 degil, her boyut en fazla 1 olabilir). Yani her boyuttaki sayılar, birbirlerine oranını kaybetmeden 0 ve 1 arasına taşınır.

* #### [Not Equal]()
Verilen iki input birbirine eşit degilise True eşitse False döndürür.

* #### [One Minus]()
Verilen inputun 1'den çıkarılmış halini döndürür. Aslında bu node 0 ve 1 arasındaki herşeyi karşıya geçirir, yani flip yapar. Mesela aşagıdaki örneklerde 0'a yakın olan degerler artık 1'e, 1'e yakın olan degerler artık 0'a yakın. Bakın,
<br>
<br>
1 için 1 - 1 = 0, yani 1 olan deger 0 oldu
<br>
0 için 1 - 0 = 1, yani 0 olan deger 1 oldu
<br>
0.3 için 1 - 0.3 = 0.7, yani 0.3 olan deger 0.7 oldu

* #### [PI]()
Pi sayısı.

* #### [Pow]()
Verilen "A" degerinin "B" degeri kadar kuvvetini alır. Eger "A" "B" den küçükse sonuç 0 olur.

* #### [RadiansToDegrees]()
Verdigimiz [radyan](https://tr.wikipedia.org/wiki/Radyan) (1 radyan ≈= 57,2958) degerini açı degerine dönüştürür.

* #### [Random]()
0 ile verdiginiz deger arasında rastgele sayı (noktalı yani kesirli, float) döndürür.

* #### [Random Float]()
0 ile verdiginiz deger arasında rastgele float döndürür.

* #### [Random Integer]()
0 ile verdiginiz deger'in 1 eksigi (x - 1) arasında rastgele integer döndürür.

* #### [Reciprocal](https://en.wikipedia.org/wiki/Multiplicative_inverse)
1'in verilen sayıya bölümünü verir. 1/x.

* #### [Reciprocal Fast]()
"Reciprocal" ile aynı ama precise yani dogruluk degeri daha düşük ama daha hızlı. Eger yüksek dogruluga ihtiyacınız yoksa bunu kullanabilirsiniz.

* #### [Reciprocal Sqrt]()
"Reciprocal" ile aynı ama 1'e bölmeden önce verdiginiz sayının karekökünü alır.

* #### [Round]()
Verilen sayıyı yuvarlar (sayıyı yuvarlar yani).

* #### [Seeded Float Random]()
[Random Float](#random-float) ile aynıdır ama seed verebilirsiniz, seed id görevi görür. Aynı seed hep aynı sonucu verir. Mesela eger bu noda input olarak 5 (float) verirseniz ve "Seed 1" inputunun degerini 1, digerlerini 0 yaparsanız. Sonuç 3.70 olacaktır, aynı seed numarasını kullanıp işlemi tekrar ederseniz siz de aynı sonucu alırsınız.

* #### [Seeded Integer Random]()
[Random Integer](#random-integer) ile aynıdır ama seed verebilirsiniz, seed id görevi görür. Aynı seed hep aynı sonucu verir. Mesela eger bu noda input olarak 5 (integer) verirseniz ve "Seed 1" inputunun degerini 1, digerlerini 0 yaparsanız. Sonuç 3 olacaktır, aynı seed numarasını kullanıp işlemi tekrar ederseniz siz de aynı sonucu alırsınız.

* #### [Seeded Random]()
[Random](#random) ile aynıdır ama seed verebilirsiniz, seed id görevi görür. Aynı seed hep aynı sonucu verir. Mesela eger bu noda input olarak 5 (float) verirseniz ve "Seed 1" inputunun degerini 1, digerlerini 0 yaparsanız. Sonuç 3.70 olacaktır, aynı seed numarasını kullanıp işlemi tekrar ederseniz siz de aynı sonucu alırsınız. Eger fark ettiyseniz sonuç "Seeded Float Random" ile aynı sonucu verdi çünkü input olarak float verdik, ama eger integer verseydiniz o zaman "Seeded Integer Random" ile aynı sonucu vermezdi çünkü "Seeded Integer Random" verdiginiz sayının bir eksigini (x - 1) alıyor. Dolayısıyla "Seeded Integer Random" ile aynı sonucu almak için verdigimiz degerin bir eksigini (x - 1) vermeliyiz.

* #### [Sign]()
Sayıların artı ve ya eksi oldugunu tespit etmede kullanılır. Sayı 0'dan küçükse -1, eşit ve ya büyükse +1 döndürür.

* #### [Sine]()
bilmiyorum.

* #### [Sine(Degrees)]()
bilmiyorum.

* #### [Sine(Radians)]()
bilmiyorum.

* #### [Sqrt]()
Verilen sayının karekökünü alır.

* #### [Step]()
bilmiyorum.

* #### [Subtract]()
Verilen bütün inputları sırasıyla ilk inputtan çıkarır.

* #### [Tangent]()
bilmiyorum.

* #### [Tangent(Degrees)]()
bilmiyorum.

* #### [Tangent(Radians)]()
bilmiyorum.

* #### [Trunc]()
Verilen sayının kesirli kısmını siler, tam sayı halinde verir. örnegin 
<br>
<br>
1.9 -> 1
<br>
1.1 -> 1

* #### [TWO_PI]()
Pi sayısı * 2.


## Parameter Map

* #### [Parameter Map For]()
bilmiyorum.

* #### [Parameter Map For Current Index]()
bilmiyorum.

* #### [Parameter Map For With Continue]()
bilmiyorum.

* #### [Parameter Map Get(Map Get)]()
[ParameterMap'den](../Terimler%20Sözlügü#parametermap) parametre almanıza yarar. Artı işaretine tıkladıgınızda çıkan kategorilerin içinde "Make New" adında bir kategori var, eger bu kategoridekilerden birini seçerseniz, adının önünde kırmızı "INPUT" yazan parametre eklemiş olursunuz. Eger ParameterMap'in [açıklamasını](../Terimler%20Sözlügü#parametermap) okuduysanız ParameterMap'lerin aslında referans objeleri oldugunu görebilirsiniz, dolayısı ile eger "Make New" kategorisinden adının önünde kırmızı "INPUT" yazan bir parametre eklediyseniz bu parametre modülün inputu olur. Modülü kullanırken kullanıcıdan bu inputa deger girmesini beklersiniz. Bu inputların default degerlerini [Parameters](../Parameters) bölümünden ayarlayabilirsiniz. Artı işaretine tıkladıgınızda çıkan kategorilerde "Make New" dışındaki kategoriler ise parametre almaya yarar. Sistem/Emitter/Parçacık parametrelerini alabilirsiniz.

* #### [Parameter Map Set(Map Set)]()
[ParameterMap'in](../Terimler%20Sözlügü#parametermap) parametrelerini ayarlamanıza yarar. İnput olarak da ParameterMap alır. Artı işaretine tıkladıgınızda çıkan kategorilerin içinde "Make New" adında bir kategori var, eger bu kategoridekilerden birini seçerseniz, adının önünde kırmızı "LOCAL" yazan parametre eklemiş olursunuz. Local parametreler sadece bu modül içerisinde tek bir kerelik kullanılabilirler, yani sonraki frame'de de kullanamazsınız, tek yol bu degeri başka bir parametreye kaydetmektir. Ayrıca artı işaretine tıkladıgınızda çıkan kategorilerin içinde "Add Existing Parameter" adında bir kategori var, bu kategori de aynı şekilde tek bir kerelik "Local" parametreleri ayarlamanıza yarar ama bunun dışında [Parameters](../Parameters) bölümündeki "Module Outputs" bölümündeki parametreleri de ayarlamanıza yarar, bu parametreler Emitter'ınızın [Module Outputs](../../Niagara%20Editörü/Parameters#module-outputs) kategorisinde kaydedilmesini saglar. Artı işaretine tıkladıgınızda bu kategorilerin dışındaki kategoriler ise diger parametreleri ayarlamaya yarar. Sistem/Emitter/Parçacık parametrelerini ayarlayabilirsiniz.


## Position

* #### [Distance]()
Verdiginiz iki pozisyonun arasındaki uzaklıgı verir, [formül](https://www.desmos.com/calculator/yik6xcdesy).


## Script Parameters

* #### [InputMap]()
"Script Parameters" kategorisinde oluşturdugunuz [ParameterMap'ler](../Terimler%20Sözlügü#parametermap) görünür. Buradan ParameterMap'inizi node olarak koyabilirsiniz ve ya isterseniz [Graph](../Graph) üzerinde duran ParameterMap'inizi kopyalabilirsiniz. Yeni bir niagara modülü oluşturdugunuzda default olarak oluşturulan ParameterMap'in ismi "InputMap" oldugu için buraya da "InputMap" adında bir örnek koydum, isimler sizin ParameterMap'lerinize göre degişir.


## Special Purpose Parameters

* #### [Begin Defaults]()
Bu modül parametrelerin default (başlangıç) degerlerini ayarlamak için kullanılan bir noddur ama artık kullanılmıyor, parametrelerin default (başlangıç) degerlerini [Parameters](../Parameters) bölümünden ayarlayabilirsiniz.

* #### [Translator.CallID]()
bilmiyorum.


## Swizzles

* #### [XYZW]()
Bu kategori sadece çok boyutlu veri tiplerinde ortaya çıkar. Boyutların yerlerini degiştirmenize yarar. Sadece istediginiz kombinasyonu yazmanız yeterlidir. Kullanabileceginiz bütün kombinasyonlar "XYZW" harfleridir.


## Utility

* #### [Execution Index]()
Her bir frame'de, şu an, bu modülün çalıştıgı parçacıgın index numarasını verir. Şöyle anlatayım, diyelim ki siz yazdıgınız bu niagara modülünü bir niagara sisteminde kullandınız ve modül [Particle Update](../../Niagara%20Editörü/Graph#particle-update) kategorisinde. Her bir frame'de bu modül her bir parçacık için işlemler gerçekleştirir, içerisindeki kodu çalıştırır. İşte "Execution Index" nodu size şu anki parçacıgın index numarasını verir, yani sıra numarası.

* #### [Reroute]()
Düzenleme nodu.

* #### [Select / If(Select)]()
İki input alır ve koşul degerine (selector) göre seçim yapar. Kısacası if else nodudur.

* #### [Spawn Interpolation]()
bilmiyorum.

* #### [Static Switch]()
"Select / If" nodunun static versionudur. İki input alır ve koşul degerine göre seçim yapar. "Select / If" nodunun aksine koşul degerini kod içinde belirleyemezsiniz. Kullanıcıdan parametre olarak alınır. Nodu seçtiginiz zaman detaylar penceresinde "Input parameter name" ayarı ile parametrenin ismini belirleyebilirsiniz, "Default value" ayarı ile default degeri ayarlayabilirsiniz. Her bir Static Switch nodu parametreler bölümünde [Static Switch Inputs](../Parameters#static-switch-inputs) kategorisinde görünür.


## No Category

* #### [Convert]()
Verilen inputun veri tipini degiştirir.

* #### [Output Module]()
Her bir oluşturdugunuz niagara modülünde otomatik olarak bir tane "Output Module" vardır. Output Module [ParameterMap](../Terimler%20Sözlügü#parametermap) alır.




