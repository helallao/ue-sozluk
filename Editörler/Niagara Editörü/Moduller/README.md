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

## [Acceleration Force]()
## [Aerodynamic Drag]()
## [Apply Initial Forces]()
## [Curl Noise Force]()
## [Drag]()
## [Gravity Force]()
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
## [Jitter Position]()
## [Place Particles on Depth Buffer GPU]()
## [Rotate Around Point]()
## [Shape Location]()
## [Skeletal Mesh Location]()
## [Spawn Particles in Grid]()
## [Static Mesh Location]()
## [System Location]()





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



## [Inherit Velocity]()
## [Scale Velocity]()
## [Static Mesh Velocity]()
## [Vortex Velocity]()






# No Category

## [New Scratch Pad Module]()
## [Set new or existing parameter directly]()
