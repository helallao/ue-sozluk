# Attribute Reader

## [Sample Particles from Other Emitter]()






# Audio

## [Play Audio]()
## [Play Persistent Audio]()
## [Update Persistent Audio]()




# Beam

## [Beam Emitter Setup]()
## [Beam Width]()
## [Spawn Beam]()





# Camera

## [Camera Offset]()
## [Maintain in Camera Particle Scale]()
## [Recreate Camera Projection]()





# Chaos

## [Apply Chaos Data]()
## [Spawn from Chaos]()






# Color

## [Color]()






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

## [Generate Location Event]()






# Export

## [Export Particle Data to Blueprint]()







# Forces

## [Acceleration Force]()
## [Apply Initial Forces]()
## [Curl Noise Force]()
## [Gravity Force]()
## [Limit Force]()
## [Line Attraction Force]()
## [Linear Force]()
## [Mesh Rotation Force]()
## [Point Attraction Force]()
## [Point Force]()
## [Vector Noise Force]()
## [Vortex Force]()







# Initialization

## [Initialize Particle]()






# Kill

## [Kill Particles]()
## [Kill Particles in Volume]()







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







# Physics

## [Add Rotational Velocity]()
## [Find Kinetic and Potential Energy]()






# Skeletal Mesh

## [Sample Skeletal Mesh]()





# Spawning

## [Spawn Burst Instantaneous](https://youtu.be/JepePaqD7-Y?list=PLUi8nuTUEtTshYxpmR7brPE3tV7JsO0VP&t=640)

Oldugu yerde parçacıkların hepsini aynı anda spawn eder.


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

Oldugu yerde, her frame'de parçacık spawn eder. Frame degerini oyunun fps'i gibi düşünebilirsiniz.


* #### Spawn Count
Her frame'de spawn edilecek parçacık sayısı.

* #### SpawnGroup
Parçacıklara grup numarası vermeye yarar. Çok kullanışlıdır, bir çok modul'de grup numarasına göre işlem yapabiliyorsunuz. Grup numarası vermek sanki id vermek gibi işlev görüyor. Sadece belirli parçacıklar üzerinde işlemler yapabiliyorsunuz.

* #### Spawn Probability
0 - 1 arasında, spawn olma ihtimali.

* #### Spawn
Spawn etmeyi açar/kapatır.




## [Spawn Per Unit](https://youtu.be/JepePaqD7-Y?list=PLUi8nuTUEtTshYxpmR7brPE3tV7JsO0VP&t=734)

Dünya üzerindeki her birimde (cm) parçacık spawn eder. Dolayısıyla harekete baglıdır, parçacıkları spawn edebilmesi için hareket etmeli. Mesela diyelim ki havai fişek efekti yaptınız, havai fişek yukarı yükselirken arkasında izler bırakmasını istiyorsunuz, o zaman bunu kullanabilirsiniz.


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

Oldugu yerde sürekli parçacık spawn eder.


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
## [Increment Over Time]()
## [Partition Particles]()
## [Update MS Vertex Animation Tools Morph Targets]()
## [Waveform]()






# Vector Field

## [Apply Vector Field]()
## [Sample Vector Field]()







# Velocity

## [Add Velocity]()
## [Inherit Velocity]()
## [Static Mesh Velocity]()
## [Vortex Velocity]()






# No Category

## [New Scratch Pad Module]()
## [Set new or existing parameter directly]()
