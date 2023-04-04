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
