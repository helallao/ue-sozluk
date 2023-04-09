# Attribute Reader

## [Sample Particles from Other Emitter]()






# Audio

## [Play Audio]()
## [Play Persistent Audio]()
## [Update Persistent Audio]()




# Beam

## [Beam Emitter Setup]()
## [Beam Width]()
## [Scale Beam Width]()
## [Spawn Beam]()
## [Update Beam]()





# Camera

## [Camera Offset]()
## [Maintain in Camera Particle Scale]()
## [Recreate Camera Projection]()





# Chaos

## [Apply Chaos Data]()
## [Spawn from Chaos]()





# Collision

## [Align Particles with Collision Plane]()
## [Collision]()





# Color

## [Color]()
## [Scale Color]()
## [Scale Color by Speed]()







# Constraints

## [Maintain A Set Distance Between Points]()
## [Pendulum Constraint]()
## [Pendulum Setup]()









# Debug

## [Sprite Based Line]()







# Default

## [Timeline]()







# Distance Fields

## [Avoid Distance Field Surfaces GPU]()
## [Move to Nearest Distance Field Surface GPU]()






# Emitter

## [Emitter State]()






# Events

## [Generate Collision Event]()
## [Generate Death Event]()
## [Generate Location Event]()





# Export

## [Export Particle Data to Blueprint]()







# Forces

## [Acceleration Force](https://youtu.be/iW867tJ93lU?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=79)

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) Parçacıklara hız ekler. Genellikle [Particle Update'de](../Graph#particle-update) kullanılır, sürekli artan hız verir.


* #### Acceleration
XYZ olmak üzere her eksende hız degerleri.

* #### Coordinate Space
bilmiyorum.




## [Aerodynamic Drag]()
## [Apply Initial Forces]()
## [Curl Noise Force](https://youtu.be/iW867tJ93lU?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=464)

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) Parçacıklara rastgele yönlere dogru force ekler.


* #### Noise Strength
Şiddet.

* #### Noise Frequency
bilmiyorum.

* #### Noise Quality / Cost
Noise efekti kalitesi, degerlendirmeler aşagıda,
<br>
<br>
Low --> 65KB
<br>
Medium --> 524KB
<br>
High --> 4.2MB
<br>
Ultra --> ?

* #### Pan Noise Field
Bunu noise deseninde hareket etmek gibi düşünebilirsiniz. Yani oluşturulan desen üzerinde hareket edip, diger kısımlardan geçiyormuşsunuz gibi, kısacası noise deseninin ilerleme hızı.

* #### Sample Position
Curl noise'inin uygulandıgı pozisyon.

* #### Randomize Noise Sample
Bu seçenek açıksa, emitter noise degerlerini rastgele offsetler yani rastgele olan degerler ekler, böylelikle diger emitter'lar ile aynı noise'yi kullanmaz. Eger bütün emitterların aynı noise'yi kullanmasını istiyorsanız bu seçenegi kapatabilirsiniz.

* #### Random Seed
Seed vermenize yarar ama ben test etsem bile göremedim, muhtemelen sadece farklı bir noise desenine geçmek için kullanılıyor.

* #### Randomization Vector
Bu deger "Randomize Noise Sample" açıkken kullanılan deger. Tam olarak nasıl çalıştıgını bilmiyorum.

* #### Scale Curl Lookup By Engine Owner Scale
Bilmiyorum.

* #### Mask Curl Noise
Bilmiyorum.





## [Drag](https://youtu.be/iW867tJ93lU?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=703)

([Particle Update](../Graph#particle-update)) Parçacıkların hızını azaltır (sürekli).


* #### Drag
Azaltma degeri, 1'de iken parçacıkların hızını yarıya düşürüyor denebilir, 2'de iken 4/1'e, 3'de iken 8/1 ... gibi. Tabi bu süreye ve hız degerine göre degişir, kullanıp anlamalısınız.

* #### Rotational Drag
bilmiyorum.

* #### Ignore Mass
Parçacıkların kütlesini dikkate almaz, bütün parçacıklara aynı drag etkisini uygular.




## [Gravity Force](https://youtu.be/iW867tJ93lU?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=743)

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) [Acceleration Force](#acceleration-force) ile aynıdır. Parçacıklara hız ekler. Genellikle [Particle Update'de](../Graph#particle-update) kullanılır, sürekli artan hız verir.


* #### Gravity
Verilen konumdan parçacıklara çekim gücü uygulanır. Gücü arttırmak için konumu daha da uzaklaştırırız.

* #### Coordinate Space
bilmiyorum.




## [Inherit Source Movement]()
## [Limit Force]()
## [Line Attraction Force]()
## [Linear Force]()
## [Mesh Rotation Force]()
## [Point Attraction Force]()
## [Point Force]()
## [Solve Forces and Velocity]()
## [Spring Force]()
## [Vector Noise Force]()
## [Vortex Force]()
## [Wind Force]()






# Initialization

## [Initialize Particle]()






# Kill

## [Kill Particles]()
## [Kill Particles in Volume]()






# Lifetime

## [Particle State]()







# Location

## [Grid Location]()

([Particle Spawn](../Graph#particle-spawn)) Bu modul [Spawn Particles in Grid](#spawn-particles-in-grid) ile birlikte kullanılmak zorundadır. Grid şekli ile ilgili ayarları barındırır.

* #### Grid Origin
Grid'in orijin noktası.

* #### Coordinate Space
bilmiyorum.

* #### Placement Randomness Mode
"Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Placement Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Placement Seed" kullanımını kapatır.

* #### Random Placement Seed
"Placement Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Randomize Overriden Seed
bilmiyorum

* #### Normalize Offsets
Eger bu ayar açıksa, offset degerlerini cell degerlerine göre düzenler ve 1 offset degeri 1 cell boyutuna eşit hale getirilir.

* #### Randomize Placement Within Cell
Parçacıklara rastgele offset degeri verir. XYZ eksenleri olmak üzere bütün eksenlerdeki rastgele offset verme derecesini ayarlayabilirsiniz. "Normalize Offsets" ayarı açıksa bu degeri 0 - 1 arasında kullanın. 0 = offset yok, 1 = en fazla rastgele offset demektir.

* #### Offset
XYZ eksenleri olmak üzere bütün eksenlerde offset verebilirsiniz.

* #### Dimensions Definition
Parçacıklar arasındaki boşluk ayarı, "Padding Per Cell" modunda iken her parçacık arasındaki boşlugu, "Bounding Box Size" modunda iken bütün grid'in büyüklügüne göre parçacıklar arasındaki boşlugu ayarlar. Zaten bunları test edip anlarsınız.

* #### XYZ Dimensions
"Dimensions Definition" için XYZ yönlerinde boşluk degerleri.

* #### Use A Custom Transformation Matrix
bilmiyorum.

* #### Exec Index
bilmiyorum.

* #### Grid X Count
bilmiyorum.

* #### Grid Y Count
bilmiyorum.

* #### Grid Z Count
bilmiyorum.










## [Jitter Position](https://youtu.be/btUjODoqSnI?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=941)

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) Parçacıklara titreşim (jitter) ekler.


* #### Jitter Amount
Titreşim derecesi, kaç cm hareket edecegi bilgisi de olabilir ama emin degilim. 

* #### Jitter Offset
Bilmiyorum.

* #### Jitter Delay
Bilmiyorum.







## [Place Particles on Depth Buffer GPU]()
## [Rotate Around Point](https://youtu.be/btUjODoqSnI?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=995)

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) Parçacıkları tek bir nokta etrafında döndürür.


* #### Rotation Phase
Başlangıç noktası (0 - 1).

* #### Rotation Rate
Saniye başına atılacak tur sayısı.

* #### Delta Time
bilmiyorum.

* #### Set Particle Position
bilmiyorum.

* #### Radius
Çap.

* #### Rotation Center
Orta nokta, parçacıklar bu nokta etrafında dönecek.

* #### Derive the Rotation Axis
X Axis ve Y Axis kullanımı açar.

* #### X Axis
X Axis ve Y Axis, dönüş efekti için vektörleri ayarlamanıza yarar.

* #### Y Axis
X Axis ve Y Axis, dönüş efekti için vektörleri ayarlamanıza yarar.








## [Shape Location]()

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) Parçacıkların spawn olacagı bölgeyi belirler. Birden fazla "Shape Primitive" a sahiptir. Bu yüzden her birinin inputlarını ayrı ayrı anlattım. Location modullerinde, şekilleri tam olarak anlamak için parçacık sayısını arttırabilir ve bütün hareketleri kapatabilirsiniz.


<br>

## Sphere
Küre şeklinde alan oluşturur.

* #### Sphere Radius
Kürenin çapı.

* #### Apply To Particle Position
Bilmiyorum.

* #### Sphere Surface Distribution
Sadece "Sphere Distribution" "Random" modundayken vardır. Bu ayar 0 - 1 arası olmak zorundadır. 0'dayken parçacıklar kürenin her noktasında spawn olabilir. Eger bu degeri yükseltirseniz, mesela 0.1 yaparsanız, kürenin tam orta noktasında bir boşluk oluşacaktır. Degeri arttırdıkça boşluk büyür ve 1 yaptıgınızda, artık parçacıklar sadece kürenin çevresinde yani yüzeyinde oluşur. Kısacası bu ayar parçacıkları 0 degerinden 1 degerine dogru yükseldikçe, kürenin çevresine yaklaştırır.

* #### Hemisphere Distribution
Sadece "Sphere Distribution" "Random" modundayken vardır. X ve Y olarak iki inputu vardır ve degerler 0 - 1 arası olmak zorundadır. X küreyi X ekseninde, Y ise Y ekseninde oranlar. Bunu sanki pastayı dilimliyormuşsunuz gibi düşünebilirsiniz. Kendiniz test etmeden size bunu anlatamam, parçacıkların sayısını yükseltip bu degerler ile oynayın.

* #### Hemisphere Angle Type
Sadece "Sphere Distribution" "Random" modundayken vardır. "Hemisphere Distribution" için kullanılacak degerin türünü belirler.
<br>
<br>
Degrees = Derece
<br>
Normalized Angle (0-1) = 0 - 360 yerine 0 - 1 arası degerler.
<br>
Radians = [Radyan](https://tr.wikipedia.org/wiki/Radyan)

* #### Spawn Group Mask
Bilmiyorum.

* #### Randomness Mode
Sadece "Sphere Distribution" "Random" modundayken vardır. "Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Seed" kullanımını kapatır.

* #### Random Seed
Sadece "Sphere Distribution" "Random" modundayken vardır. "Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Fixed Random Seed
Sadece "Sphere Distribution" "Random" modundayken vardır. Ne işe yaradıgını bilmiyorum.

* #### U Position
Sadece "Sphere Distribution" "Direct" modundayken vardır. Direct modu U ve V inputu alır, bunlar X ve Y gibidir ve belirli bir noktayı temsil etmek için kullanılır, yani koordinat.

* #### V Position
Sadece "Sphere Distribution" "Direct" modundayken vardır. Direct modu U ve V inputu alır, bunlar X ve Y gibidir ve belirli bir noktayı temsil etmek için kullanılır, yani koordinat.

* #### Sphere Radius Position
Sadece "Sphere Distribution" "Direct" modundayken vardır. Kürenin çapını temsil eder.

* #### Uniform Distribution
Sadece "Sphere Distribution" "Uniform" modundayken vardır. Uniform modu noktaları eşit aralıklarla dagıtmaya yarar (bazen tek sayı geldiginde falan bozulabilir ama sonuç olarak eşit dagıtır). Bu ayar kürenin ne kadarı üzerinde dagıtma işleminin uygulanacagını belirler. 1 tam küre, 0.5 yarım küre anlamına gelir.

* #### Uniform Spiral Amount
Sadece "Sphere Distribution" "Uniform" modundayken vardır. Kaç tane spiralden oluşacagını ayarlarsınız.

* #### Uniform Count
Sadece "Sphere Distribution" "Uniform" modundayken vardır. Uniform sayısı, parçacıklar bu deger kadar uniforma dagıtılacak.

* #### Uniform Particle Index
Sadece "Sphere Distribution" "Uniform" modundayken vardır. Bu bizi ilgilendiren bir şey degil. Parçacıkların index numarası.

* #### Uniform Endpoint Offset
Sadece "Sphere Distribution" "Uniform" modundayken vardır. Uniformlar için offset verir.

* #### Transform Order
Bir işe yarayacagını sanmıyorum. Belki gerekir de kullanırsınız. Yapılacak işlemlerin sırasını degiştiriyor, daha dogrusu sadece offset ve rotation işlemlerinin yerini degiştiriyor. İlk baş rotate edip sonra offset verirseniz, offsetin ne yönde olacagını bilirsiniz ama ilk baş offset verip sonra rotate ederseniz, offsetin ne yöne oldugunu bilemeyebilirsiniz.

* #### Non Uniform Scale
Kürenin boyut degerlerini ayarlarsınız.

* #### Apply Owner Scale
Bilmiyorum.

* #### Rotation
Rotation ile ilgili bir açıklama yapmicam, gereksiz.

* #### Shape Origin
Orijin noktası.

* #### Offset
Offset vermenize yarar, yani konum üzerine ekleme yapmanıza.

* #### Offset Coordinate Space
Bilmiyorum.





<br>
<br>

## Cylinder
Silindir şeklinde alan oluşturur.

* #### Cylinder Height
Silindirin yüksekligi.

* #### Cylinder Radius
Silindirin çapı/genişligi.

* #### Cylinder Height Midpoint
Silindirin yükseklik degerinin ne yöne olacagını belirtir. Default olarak 0.5 tir ve iki yöne dogru da olur. Eger 1 yaparsanız yükseklik arttıkça silindir aşagıya dogru uzar. Eger 0 yaparsanız yükseklik arttıkça silindir yukarıya dogru uzar.

* #### Apply To Particle Position
Bilmiyorum.

* #### Surface Only Band Thickness
Sadece "Cylinder Distribution" "Random" modundayken vardır. Parçacıkları sadece silindirin yüzeyinde/çevresinde spawn eder. 0 iken bu katman incedir, yani sadece yüzeydir. Eger sayıyı yükseltirseniz bu katman büyür, yani dıştan içe dogru genişler ve 1 yaptıgınız zaman katman ortaya kadar ulaşır, eger ortaya kadar ulaşırsa default halindeki gibi yani içi dolu olur (parçacıklar içinde de spawn olur).

* #### Use Endcaps In Surface Only Mode
Sadece "Surface Only Band Thickness" ayarı açıkken vardır. Silindirin uç noktalarını (tabanlarını) açar/kapatır.

* #### Hemicircle X
Sadece "Cylinder Distribution" "Random" modundayken vardır. X ekseninde silindirin yarısını keser.

* #### Hemicircle Y
Sadece "Cylinder Distribution" "Random" modundayken vardır. Y ekseninde silindirin yarısını keser.

* #### Enable Lathe Profile
Sadece "Cylinder Distribution" "Random" modundayken vardır.

* #### Spawn Group Mask
bilmiyorum.

* #### Randomness Mode
Sadece "Cylinder Distribution" "Random" modundayken vardır. "Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Seed" kullanımını kapatır.

* #### Random Seed
Sadece "Cylinder Distribution" "Random" modundayken vardır. "Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Fixed Random Seed
Sadece "Cylinder Distribution" "Random" modundayken vardır. Ne işe yaradıgını bilmiyorum.

* #### U Position
Sadece "Cylinder Distribution" "Direct" modundayken vardır. Direct modu U ve V inputu alır, bunlar X ve Y gibidir ve belirli bir noktayı temsil etmek için kullanılır, yani koordinat.

* #### V Position
Sadece "Cylinder Distribution" "Direct" modundayken vardır. Direct modu U ve V inputu alır, bunlar X ve Y gibidir ve belirli bir noktayı temsil etmek için kullanılır, yani koordinat.

* #### Transform Order
Bir işe yarayacagını sanmıyorum. Belki gerekir de kullanırsınız. Yapılacak işlemlerin sırasını degiştiriyor, daha dogrusu sadece offset ve rotation işlemlerinin yerini degiştiriyor. İlk baş rotate edip sonra offset verirseniz, offsetin ne yönde olacagını bilirsiniz ama ilk baş offset verip sonra rotate ederseniz, offsetin ne yöne oldugunu bilemeyebilirsiniz.

* #### Non Uniform Scale
Silindirin boyut degerlerini ayarlarsınız.

* #### Apply Owner Scale
Bilmiyorum.

* #### Rotation
Rotation ile ilgili bir açıklama yapmicam, gereksiz.

* #### Shape Origin
Orijin noktası.

* #### Offset
Offset vermenize yarar, yani konum üzerine ekleme yapmanıza.

* #### Offset Coordinate Space
Bilmiyorum.





<br>
<br>

## Box / Plane
Kutu/dörtgen şeklinde alan oluşturur. Sadece Box'u anlatıcam, zaten box ile plane'in yaptıklarını yapabiliyorsunuz, aynı şeyler. Aşagıdaki inputlar "Box / Plane Mode" ayarı "Box" iken gelen inputlardır.

* #### Cylinder Height
Silindirin yüksekligi.

* #### Box Size
Dörtgenin boyut degerlerini ayarlarsınız.

* #### Box Midpoint
Dörtgenin XYZ olmak üzere her eksen için orta noktasını belirtir yani boyut degerlerini degiştirdiginizde ne yöne dogru genişleyecegini belirtir. Default olarak 0.5 tir ve iki yöne dogru da olur. Eger 0 yaparsanız o eksenin boyut degeri arttıkça o eksen tarafına dogru uzar çünkü 0 yaptıgınızda o eksenin tabanını başlangıç noktası olarak almışsınızdır. Eger 1 yaparsanız o eksenin boyut degeri arttıkça o eksenin tersi tarafına dogru uzar çünkü 1 yaptıgınızda o eksenin ucunu başlangıç noktası olarak almışsınızdır.

* #### Apply To Particle Position
Bilmiyorum.

* #### Surface Only Band Thickness
Parçacıkları sadece dörtgenin yüzeyinde/çevresinde spawn eder. 0 iken bu katman incedir, yani sadece yüzeydir. Eger sayıyı yükseltirseniz bu katman büyür, yani dıştan içe dogru genişler. Sayı bu katmanın içeriye dogru kaç birim genişleyecegini belirtiyor, eger katmanı dörtgeni kaplayacak kadar genişletirseniz yine dörtgen şekli elde etmiş olursunuz.

* #### Surface Expansion Mode
Sadece "Surface Only Band Thickness" ayarı açıkken vardır. "Surface Only Band Thickness" ayarının modunu degiştirir. Default olarak "Inside" yani degeri arttırdıkça katman içeriye dogru genişler. Eger "Outside" yaparsanız degeri arttırdıkça katman dışarıya dogru genişler. Eger "Centered" yaparsanız degeri arttırdıkça katman iki yöne dogru genişler.

* #### Spawn Group Mask
bilmiyorum.

* #### Randomness Mode
"Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Seed" kullanımını kapatır.

* #### Random Seed
"Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Fixed Random Seed
Ne işe yaradıgını bilmiyorum.

* #### Transform Order
Bir işe yarayacagını sanmıyorum. Belki gerekir de kullanırsınız. Yapılacak işlemlerin sırasını degiştiriyor, daha dogrusu sadece offset ve rotation işlemlerinin yerini degiştiriyor. İlk baş rotate edip sonra offset verirseniz, offsetin ne yönde olacagını bilirsiniz ama ilk baş offset verip sonra rotate ederseniz, offsetin ne yöne oldugunu bilemeyebilirsiniz.

* #### Non Uniform Scale
Dörtgenin boyut degerlerini ayarlarsınız.

* #### Apply Owner Scale
Bilmiyorum.

* #### Rotation
Rotation ile ilgili bir açıklama yapmicam, gereksiz.

* #### Shape Origin
Orijin noktası.

* #### Offset
Offset vermenize yarar, yani konum üzerine ekleme yapmanıza.

* #### Offset Coordinate Space
Bilmiyorum.





<br>
<br>

## Torus
"Torus" modunda simit/donut şeklinde alan oluşturur. "TorusKnot" modunda ise etrafından [sarmallar](https://en.wikipedia.org/wiki/Helix) geçen [simit benzeri bir şekil](https://en.wikipedia.org/wiki/Torus_knot) oluşturur.

* #### Knot Helix Loops
Sadece "Torus Mode" "TorusKnot" modundayken vardır. [Sarmal](https://en.wikipedia.org/wiki/Helix) sayısını belirtir.

* #### Knot Ring Loops
Sadece "Torus Mode" "TorusKnot" modundayken vardır. "TorusKnot" ismindeki "Knot" kısımları belirtir, köşe/dügüm sayısını belirtir.

* #### Torus Knot Tube Radius
Sadece "Torus Mode" "TorusKnot" modundayken vardır. TorusKnot'un çapı.

* #### Large Radius
Torus'un çapı.

* #### Handle Radius
Torus'un genişligi/kalınlıgı.

* #### Apply To Particle Position
Bilmiyorum.

* #### Surface Distribution
Sadece "Torus Distribution Mode" "Random" modundayken vardır. Parçacıkları sadece torus'un yüzeyinde/çevresinde spawn eder. 1 iken bu katman incedir, yani sadece yüzeydir. Eger sayıyı azaltırsanız bu katman büyür, yani dıştan içe dogru genişler ve 0 yaptıgınız zaman katman ortaya kadar ulaşır, eger ortaya kadar ulaşırsa default halindeki gibi yani içi dolu olur (parçacıklar içinde de spawn olur).

* #### U Distribution
Sadece "Torus Distribution Mode" "Random" modundayken vardır. U Distribution ve V Distribution, torus'u X ve Y ekseninde oranlar/böler.

* #### V Distribution
Sadece "Torus Distribution Mode" "Random" modundayken vardır. U Distribution ve V Distribution, torus'u X ve Y ekseninde oranlar/böler.

* #### Spawn Group Mask
bilmiyorum.

* #### Randomness Mode
Sadece "Torus Distribution Mode" "Random" modundayken vardır. "Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Seed" kullanımını kapatır.

* #### Random Seed
Sadece "Torus Distribution Mode" "Random" modundayken vardır. "Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Fixed Random Seed
Sadece "Torus Distribution Mode" "Random" modundayken vardır. Ne işe yaradıgını bilmiyorum.

* #### U Position
Sadece "Torus Distribution Mode" "Direct" modundayken vardır. Direct modu U ve V inputu alır, bunlar X ve Y gibidir ve belirli bir noktayı temsil etmek için kullanılır, yani koordinat.

* #### V Position
Sadece "Torus Distribution Mode" "Direct" modundayken vardır. Direct modu U ve V inputu alır, bunlar X ve Y gibidir ve belirli bir noktayı temsil etmek için kullanılır, yani koordinat.

* #### Transform Order
Bir işe yarayacagını sanmıyorum. Belki gerekir de kullanırsınız. Yapılacak işlemlerin sırasını degiştiriyor, daha dogrusu sadece offset ve rotation işlemlerinin yerini degiştiriyor. İlk baş rotate edip sonra offset verirseniz, offsetin ne yönde olacagını bilirsiniz ama ilk baş offset verip sonra rotate ederseniz, offsetin ne yöne oldugunu bilemeyebilirsiniz.

* #### Non Uniform Scale
Torus'un boyut degerlerini ayarlarsınız.

* #### Apply Owner Scale
Bilmiyorum.

* #### Rotation
Rotation ile ilgili bir açıklama yapmicam, gereksiz.

* #### Shape Origin
Orijin noktası.

* #### Offset
Offset vermenize yarar, yani konum üzerine ekleme yapmanıza.

* #### Offset Coordinate Space
Bilmiyorum.





<br>
<br>

## Ring / Disc
"Circle" modunda simit/donut şeklinde alan oluşturur. "Hexagon" modunda ise çokgen şekli oluşturur.


* #### Ring Radius
Çap degeri.

* #### Apply To Particle Position
Bilmiyorum.

* #### Disc Coverage
Sadece "Ring / Disc Distribution Mode" "Random" modundayken vardır. Deger 0'dan 1'e dogru yaklaştıkça, simit/çokgen şeklinin ortası dolar, yani ortaya dogru yaklaşır.

* #### U Distribution
Sadece "Ring / Disc Distribution Mode" "Random" modundayken vardır. Simit/çokgen şeklini oranlar/böler.

* #### Spawn Group Mask
bilmiyorum.

* #### Randomness Mode
Sadece "Ring / Disc Distribution Mode" "Random" modundayken vardır. "Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Seed" kullanımını kapatır.

* #### Random Seed
Sadece "Ring / Disc Distribution Mode" "Random" modundayken vardır. "Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Fixed Random Seed
Sadece "Ring / Disc Distribution Mode" "Random" modundayken vardır. Ne işe yaradıgını bilmiyorum.

* #### U Position
Sadece "Ring / Disc Distribution Mode" "Direct" modundayken vardır. Simit/çokgen şeklini oranlar/böler.

* #### Radius Position
Sadece "Ring / Disc Distribution Mode" "Direct" modundayken vardır. Çap degeri.

* #### Uniform Spiral Amount
Sadece "Ring / Disc Distribution Mode" "Uniform" modundayken vardır. Spiral sayısı.

* #### Uniform Spiral Falloff
Sadece "Ring / Disc Distribution Mode" "Uniform" modundayken vardır. Spirallerin ne kadar kıvrılacagını ayarlar. Daha fazla kıvrılırsa daha kısa olur.

* #### Uniform Count
Sadece "Ring / Disc Distribution Mode" "Uniform" modundayken vardır. Uniform sayısı, parçacıklar bu deger kadar uniforma dagıtılacak.

* #### Uniform Particle Index
Sadece "Ring / Disc Distribution Mode" "Uniform" modundayken vardır. Bu bizi ilgilendiren bir şey degil. Parçacıkların index numarası.

* #### Transform Order
Bir işe yarayacagını sanmıyorum. Belki gerekir de kullanırsınız. Yapılacak işlemlerin sırasını degiştiriyor, daha dogrusu sadece offset ve rotation işlemlerinin yerini degiştiriyor. İlk baş rotate edip sonra offset verirseniz, offsetin ne yönde olacagını bilirsiniz ama ilk baş offset verip sonra rotate ederseniz, offsetin ne yöne oldugunu bilemeyebilirsiniz.

* #### Non Uniform Scale
Torus'un boyut degerlerini ayarlarsınız.

* #### Apply Owner Scale
Bilmiyorum.

* #### Rotation
Rotation ile ilgili bir açıklama yapmicam, gereksiz.

* #### Shape Origin
Orijin noktası.

* #### Offset
Offset vermenize yarar, yani konum üzerine ekleme yapmanıza.

* #### Offset Coordinate Space
Bilmiyorum.





<br>
<br>

## Cone
"Spherical Cone" modunda bildigimiz normal koni şeklinde alan oluşturur. "Spherical Wedge" modunda ise ucu kare koni oluşturur, türkçesinden tam emin degilim.


* #### Cone Length
Koni uzunlugu.

* #### Cone Angle
Sadece "Cone Mode" "Spherical Cone" modundayken vardır. Koninin çapı.

* #### Cone Inner Angle
Sadece "Cone Mode" "Spherical Cone" modundayken vardır. Koninin iç çapı.

* #### Cone Radial Angle
Sadece "Cone Mode" "Spherical Cone" modundayken vardır. Koniyi oranlar/böler/keser.

* #### Cone Angle Type
Sadece "Cone Mode" "Spherical Cone" modundayken vardır. Açı degerleri için kullanılacak degerin türünü belirler.
<br>
<br>
Degrees = Derece
<br>
Normalized Angle (0-1) = 0 - 360 yerine 0 - 1 arası degerler.
<br>
Radians = [Radyan](https://tr.wikipedia.org/wiki/Radyan)

* #### Flatten Endcaps
Sadece "Cone Mode" "Spherical Cone" modundayken vardır. Koninin uç kısımlarını düzleştirir.

* #### Wedge Horizontal Angle
Sadece "Cone Mode" "Spherical Wedge" modundayken vardır. Koninin açısının yatay eksende büyüklügünü ayarlamamıza yarar.

* #### Wedge Vertical Angle
Sadece "Cone Mode" "Spherical Wedge" modundayken vardır. Koninin açısının dikey eksende büyüklügünü ayarlamamıza yarar.

* #### Apply To Particle Position
Bilmiyorum.

* #### Cone Surface Distribution
Bu ayar sanırım bozuk, düzgün çalışmıyor.

* #### Spawn Group Mask
bilmiyorum.

* #### Randomness Mode
"Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Seed" kullanımını kapatır.

* #### Random Seed
"Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Fixed Random Seed
Ne işe yaradıgını bilmiyorum.

* #### Transform Order
Bir işe yarayacagını sanmıyorum. Belki gerekir de kullanırsınız. Yapılacak işlemlerin sırasını degiştiriyor, daha dogrusu sadece offset ve rotation işlemlerinin yerini degiştiriyor. İlk baş rotate edip sonra offset verirseniz, offsetin ne yönde olacagını bilirsiniz ama ilk baş offset verip sonra rotate ederseniz, offsetin ne yöne oldugunu bilemeyebilirsiniz.

* #### Non Uniform Scale
Torus'un boyut degerlerini ayarlarsınız.

* #### Apply Owner Scale
Bilmiyorum.

* #### Rotation
Rotation ile ilgili bir açıklama yapmicam, gereksiz.

* #### Shape Origin
Orijin noktası.

* #### Offset
Offset vermenize yarar, yani konum üzerine ekleme yapmanıza.

* #### Offset Coordinate Space
Bilmiyorum.








## [Skeletal Mesh Location](https://youtu.be/btUjODoqSnI?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=1070)
## [Spawn Particles in Grid]()

([Emitter Spawn](../Graph#emitter-spawn), [Emitter Update](../Graph#emitter-update)) Bu modul [Grid Location](#grid-location) ile birlikte kullanılmak zorundadır. Grid şekli bir alanda parçacıkların hepsini aynı anda spawn eder, sadece spawn ayarlarını barındırır, grid şekli ile ilgili ayarları [Grid Location](#grid-location) üzerinden yaparsınız.


* #### X Count
X ekseninde spawn edilecek parçacık sayısı.

* #### Y Count
Y ekseninde spawn edilecek parçacık sayısı.

* #### Z Count
Z ekseninde spawn edilecek parçacık sayısı.

* #### Spawn Time
Spawn edecegi saniye.

* #### Age
Bilmiyorum.

* #### SpawnGroup
Parçacıklara grup numarası vermeye yarar. Çok kullanışlıdır, bir çok modul'de grup numarasına göre işlem yapabiliyorsunuz. Grup numarası vermek sanki id vermek gibi işlev görüyor. Sadece belirli parçacıklar üzerinde işlemler yapabiliyorsunuz.







## [Static Mesh Location]()
## [System Location]()

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) Tek bir nokta konum belirler.


* #### Offset
Offset verebilirsiniz.

* #### Offset Coordinate Space
Bilmiyorum.

* #### Spawn Group Mask
Bilmiyorum.




# Mask

## [Region Mask]()







# Mass

## [Calculate Mass and Rotational Inertia by Volume]()
## [Calculate Size and Rotational Inertia by Mass]()





# Material

## [Dynamic Material Parameters]()





# MAXScripts

## [Spawn MS Vertex Animation Tools Morph Target Particles]()





# Math

## [Cone Mask]()
## [Constrain Vector to Cone]()
## [Fade Over Time]()
## [Find Closest Point on Line Segment]()
## [Find Closest Point on Triangle]()
## [Interpolate Over Time]()
## [Lerp Particle Attributes]()






# Mesh

## [Initialize Mesh Reproduction Sprite]()
## [Traverse Skeletal Mesh]()
## [Update Mesh Reproduction Sprite]()






# Orientation

## [Align Sprite to Mesh Orientation]()
## [Initial Mesh Orientation]()
## [Sprite Rotation Rate]()
## [Update Mesh Orientation]()






# Physics

## [Add Rotational Velocity]()
## [Find Kinetic and Potential Energy]()








# Post Solve

## [Calculate Accurate Velocity]()





# Ribbon

## [Scale Ribbon Width]()







# Size

## [Apply Owner Scale to Attributes]()
## [Scale Mesh Size]()
## [Scale Mesh Size by Speed]()
## [Scale Sprite Size]()
## [Scale Sprite Size by Speed]()









# Skeletal Mesh

## [Sample Skeletal Mesh]()





# Spawning

## [Spawn Burst Instantaneous](https://youtu.be/JepePaqD7-Y?list=PLUi8nuTUEtTshYxpmR7brPE3tV7JsO0VP&t=640)

([Emitter Update](../Graph#emitter-update)) Oldugu yerde parçacıkların hepsini aynı anda spawn eder.


* #### Spawn Count
Spawn edilecek parçacık sayısı.

* #### Spawn Time
Spawn işleminin gerçekleşecegi zaman (saniye).

* #### Spawn Probability
0 - 1 arasında, spawn olma ihtimali. Bu ihtimal bütün parçacıkları kapsar.

* #### SpawnGroup
Parçacıklara grup numarası vermeye yarar. Çok kullanışlıdır, bir çok modul'de grup numarasına göre işlem yapabiliyorsunuz. Grup numarası vermek sanki id vermek gibi işlev görüyor. Sadece belirli parçacıklar üzerinde işlemler yapabiliyorsunuz.

* #### Age
parametre

* #### Loop Count Limit
yazılacak




## [Spawn Particles from Other Emitter]()





## [Spawn Per Frame](https://youtu.be/_18Y4-jeXUs?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=726)

([Emitter Update](../Graph#emitter-update)) Oldugu yerde, her frame'de parçacık spawn eder. Frame degerini oyunun fps'i gibi düşünebilirsiniz.


* #### Spawn Count
Her frame'de spawn edilecek parçacık sayısı.

* #### SpawnGroup
Parçacıklara grup numarası vermeye yarar. Çok kullanışlıdır, bir çok modul'de grup numarasına göre işlem yapabiliyorsunuz. Grup numarası vermek sanki id vermek gibi işlev görüyor. Sadece belirli parçacıklar üzerinde işlemler yapabiliyorsunuz.

* #### Spawn Probability
0 - 1 arasında, spawn olma ihtimali.

* #### Spawn
Spawn etmeyi açar/kapatır.




## [Spawn Per Unit](https://youtu.be/JepePaqD7-Y?list=PLUi8nuTUEtTshYxpmR7brPE3tV7JsO0VP&t=734)

([Emitter Spawn](../Graph#emitter-spawn), [Emitter Update](../Graph#emitter-update)) Dünya üzerindeki her birimde (cm) parçacık spawn eder. Dolayısıyla harekete baglıdır, parçacıkları spawn edebilmesi için hareket etmeli. Mesela diyelim ki havai fişek efekti yaptınız, havai fişek yukarı yükselirken arkasında izler bırakmasını istiyorsunuz, o zaman bunu kullanabilirsiniz.


* #### Spawn Spacing
Kaç birimde spawn edilecegini belirler.

* #### Max Movement Threshold
Eger tek bir frame'deki (fps, kare) hız degeri bu degerden fazlaysa, o zaman parçacık spawn etmez.

* #### Movement Tolerance
Eger tek bir frame'deki (fps, kare) hız degeri bu degerden azsa, o zaman parçacık spawn etmez.

* #### Spawn Probability
0 - 1 arasında, spawn olma ihtimali.

* #### Velocity Vector
parametre

* #### Delta Time
parametre

* #### SpawnGroup
Parçacıklara grup numarası vermeye yarar. Çok kullanışlıdır, bir çok modul'de grup numarasına göre işlem yapabiliyorsunuz. Grup numarası vermek sanki id vermek gibi işlev görüyor. Sadece belirli parçacıklar üzerinde işlemler yapabiliyorsunuz.





## [Spawn Rate](https://youtu.be/_18Y4-jeXUs?list=PLwMiBtF6WzsoNsDquipGfD-uLUb-fyRSV&t=68)

([Emitter Spawn](../Graph#emitter-spawn), [Emitter Update](../Graph#emitter-update)) Oldugu yerde sürekli parçacık spawn eder.


* #### SpawnRate
Saniye başına spawn olacak parçacık sayısı.

* #### Spawn Probability
0 - 1 arasında, her parçacık için spawn olma ihtimali.

* #### SpawnGroup
Parçacıklara grup numarası vermeye yarar. Çok kullanışlıdır, bir çok modul'de grup numarasına göre işlem yapabiliyorsunuz. Grup numarası vermek sanki id vermek gibi işlev görüyor. Sadece belirli parçacıklar üzerinde işlemler yapabiliyorsunuz.








# Sprite

## [Sprite Facing and Alignment]()






# SubUV

## [Sub UVAnimation]()







# Texture

## [Sample Pseudo Volume Texture]()
## [Sample Texture]()
## [Sub UV Texture Sample]()
## [World Aligned Texture Sample]()










# Utility

## [Do Once]()
## [Emitter Frame Counter]()
## [Frame Counter]()
## [Increment Over Time]()
## [Partition Particles]()
## [Time Based State Machine]()
## [Update MS Vertex Animation Tools Morph Targets]()
## [Waveform]()






# Vector Field

## [Apply Vector Field]()
## [Sample Vector Field]()







# Velocity

## [Add Velocity](https://youtu.be/BadHGIYkrMw?list=PLUi8nuTUEtTshYxpmR7brPE3tV7JsO0VP&t=41)

([Particle Spawn](../Graph#particle-spawn)) Parçacıklara velocity (hız) ekler, başka bir yönden güç uygular da denebilir. Birden fazla "Velocity Mode" a sahiptir. Bu yüzden her birinin inputlarını ayrı ayrı anlattım.


<br>

### Linear
Tek yöne dogru velocity ekler.

* #### Velocity
1 saniyede hangi yöne kaç birim (cm) ilerleyecegini ayarlarsınız, yani hızını.

* #### Velocity Speed Scale
Yukarıda 1 saniye dedim ya, işte bu ayar velocity speed'ini arttırıyor. Bunu 2 yaparsanız, o zaman 2 kat hızlı olur, yani ulaşacagı yere 1 degil yarım saniyede ulaşır.

* #### Rotation
Rotation ile ilgili bir açıklama yapmicam, gereksiz.


<br>

### From Point
Belirli bir noktadan etrafa dogru güç uygular, yani itme kuvveti oluşturur.

* #### Velocity Speed
1 saniyede hangi yöne kaç birim (cm) ilerleyecegini ayarlarsınız, yani hızını.

* #### Constrain To Radius
Uygulanan kuvvetin (velocity) alanını daraltır, kuvvetin uygulanacagı bir küre alanı oluşturur.

* #### Radius Falloff Near / Far
"Constrain To Radius" seçenegini açtıgınızda gelir. Oluşturdugunuz kürenin orta noktasına yakın/uzak olan noktalarında uygulanacak kuvveti (velocity) belirler.

* #### Radius Falloff Exponent
"Constrain To Radius" seçenegini açtıgınızda gelir. "Radius Falloff Near / Far" ayarının katsayısnı arttırır. Böylelikle daha fazla etki eder.

* #### Invert Velocity Falloff
Ne işe yaradıgını bilmiyorum.

* #### Random Seed
"Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Fixed Random Seed
Ne işe yaradıgını bilmiyorum.

* #### Randomness Mode
"Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Seed" kullanımını kapatır.

* #### Velocity Origin
Orijin noktası, yani orta nokta.

* #### Origin Offset
Orijin noktasına offset vermenize yarar.

* #### Origin Offset Coordinate Space
Ne işe yaradıgını bilmiyorum.

* #### Default Position
Ne işe yaradıgını bilmiyorum.


<br>

### In Cone
Koni şeklinde velocity ekler.

* #### Velocity Speed
1 saniyede hangi yöne kaç birim (cm) ilerleyecegini ayarlarsınız, yani hızını.

* #### Distribution Along Cone Axis
Koni içindeki kuvvetin ne kadar dagınık şekilde uygulanacagını belirler. Eger 0 yaparsanız dagınık yani kuvvet koninin herhangi bir yönüne olabilir, 1 yaparsanız düze yakın yani kuvvet koninin baktıgı yöne (orta nokta) dogru olur.

* #### Speed Falloff From Cone Axis
Koni içindeki parçacıkların yönü koninin baktıgı yöne (orta nokta) dogru degil ise, onları yavaşlatır, yönü koninin baktıgı yöne bakan parçacıkları hızlandırır. 0'da iken yavaşlatma uygulanmaz, 1'de iken maximum yavaşlatma uygulanır.

* #### Random Seed
"Randomness Mode" ayarı "Deterministic" modunda ise, seed verebilirsiniz.

* #### Fixed Random Seed
Ne işe yaradıgını bilmiyorum.

* #### Randomness Mode
"Simulation Defaults" ayarında iken default ayarları kullanır. "Deterministic" modunda iken "Random Seed" kullanımını açar. "Non-Deterministic" modunda iken "Random Seed" kullanımını kapatır.

* #### Cone Axis
Koninin yönü.

* #### Cone Angle
Koninin genişligi (açı)

* #### Inner Cone Angle
Koninin başlangıç noktasındaki genişligi (açı)

* #### Cone Angle Mode
Açı degerlerinin türünü degiştirir.
<br>
<br>
Degrees = Derece
<br>
Normalized Angle (0-1) = 0 - 360 yerine 0 - 1 arası degerler.
<br>
Radians = [Radyan](https://tr.wikipedia.org/wiki/Radyan)

* #### Rotation
Rotation ile ilgili bir açıklama yapmicam, gereksiz.





## [Inherit Velocity](https://youtu.be/BadHGIYkrMw?list=PLUi8nuTUEtTshYxpmR7brPE3tV7JsO0VP&t=488)

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) Parçacıklara şu anki hareket hızı kadar velocity (hız) ekler. Her bir frame (fps, kare) arasındaki hız kadar, parçacıklara hız ekler. Linkteki videoya bakın.


* #### Inherited Velocity Amount Scale
Yönlere göre hız degeri çarpanı. Mesela diyelim ki X degerini 2 yaptınız, o zaman X ekseninde uygulanan velocity degeri 2 ile çarpılır. Bu şekilde XYZ olmak üzere 3 yön için hız degeri çarpanı ayarlayabilirsiniz. "Inherited Velocity Amount Scale" ayarı "Inherited Velocity Speed Limit" den sonra gelir. Yani hız limiti koymuşsanız, ilk baş hız limiti hesaplanır, ardından "Inherited Velocity Amount Scale" ayarına verdiginiz degere göre hız degeri çarpılır. Kısacası bu ayar limit ayarından sonra uygulanır yani limitten bagımsızdır.

* #### Inherited Velocity Speed Limit
En fazla bu hız degerini alabilir, bundan fazla olan hız degerleri yerine bu deger kullanılır, yani limit.

* #### Source Speed Threshold
Minimum hız degerini belirtir. Eger hız degeri bu degerin altındaysa parçacıga hiç hız uygulamaz. Yani en az bu deger kadar hızlı olmak gerek, yoksa "Inherit Velocity" çalışmaz.

* #### Velocity Source
parametre







## [Scale Velocity]()

([Particle Update](../Graph#particle-update)) Parçacıgın sahip oldugu velocity degerini scale etmemize yani azaltmamıza/arttırmamıza yarar.


* #### Coordinate Space
Ne işe yaradıgını bilmiyorum.

* #### Velocity Scale
Yönlere göre hız degeri çarpanı. Mesela diyelim ki X degerini 2 yaptınız, o zaman X ekseninde sahip olunan velocity degeri 2 ile çarpılır. Bu şekilde XYZ olmak üzere 3 yön için hız degeri çarpanı ayarlayabilirsiniz.




## [Static Mesh Velocity]()




## [Vortex Velocity](https://youtu.be/BadHGIYkrMw?list=PLUi8nuTUEtTshYxpmR7brPE3tV7JsO0VP&t=375)

([Particle Spawn](../Graph#particle-spawn), [Particle Update](../Graph#particle-update)) Parçacıklara girdap şeklinde velocity (hız) ekler.


* #### Velocity Amount
1 saniyede hangi yöne kaç birim (cm) ilerleyecegini ayarlarsınız, yani hızını.

* #### Vortex Axis
Yön degerleri.

* #### Vortex Origin
Orijin noktası, yani orta nokta.

* #### Vortex Axis Coordinate Space
Ne işe yaradıgını bilmiyorum.

* #### Influence Falloff Exponent
"Influence Falloff Radius" seçenegini açtıgınızda gelir. "Influence Falloff Radius" degeri için katsayıdır, yani degeri bu sayı ile katlar, gereksiz.

* #### Influence Falloff Radius
Parçacıkların girdapda kalma süresini arttırır. Deger yükseldikçe parçacıklar daha kısa süre girdapta kalır, azaldıkça parçacıklar daha uzun süre girdapta kalır. Yani girdaptan çıkma süresini belirler.

* #### Invert Influence Falloff
"Influence Falloff Radius" degerinin çalışma mantıgını tersine çevirir. Default olarak zaten açıktır. Deger yükseldikçe parçacıklar daha uzun süre girdapta kalır, azaldıkça parçacıklar daha kısa süre girdapta kalır. Yani girdapta kalma süresini belirler.









# No Category

## [New Scratch Pad Module]()
## [Set new or existing parameter directly]()
