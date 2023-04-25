# Parameters
<img src="../../../Dosyalar/Niagara_Editor_Parameters.jpg">


Niagara'da parametreler çok önemlidir, parametreleri inputların yerine kullanabilirsiniz, aynı zamanda degişken mantıgıyla da kullanılabilir. "User Exposed" bölümündeki parametreler sizin oluşturdugunuz ve degiştirilebilen parametrelerdir, bunları burda anlatmicam, [User Parameters](../User%20Parameters) bölümüne bakın. Çogu [modül](../Moduller) kullanıldıgı zaman kendi parametrelerini de oluşturur. Örnegin,


<img src="../../../Dosyalar/Niagara_Editor_Parameters_Age.jpg">


Bu parametreler kullanıcı tarafından degiştirilemez. Yanlarında kilit vardır. Resimde en solda gördügünüz küçük renk parametrenin türünü belirtiyor, imlecinizi üzerine getirirseniz türünü görebilirsiniz. Bir sagında "System" yazıyor, bu parametrenin dalı, her parametre dallara sahiptir (motor tarafından oluşturulanlar, kullanıcının oluşturduklarının dışındakiler), mesela resimdeki parametrenin adı "Age" ve dalı "System" o zaman bu parametrenin gerçek ismi "System.Age" dir. Eger parametreye sag tıklayıp "Copy Reference" derseniz, parametrenin tam ismini, dalları ile birlikte kopyalamış olursunuz. Bir yere yapıştırırsanız, isminin "System.Age" oldugunu görürsünüz. Dalları klasör gibi düşünebilirsiniz. En sagda ise "5" yazıyor, bu parametrenin kaç defa kullanıldıgının/referans verildiginin sayısıdır. Eger [Graph](../Graph) üzerinde bir şey seçmediyseniz bütün parametreleri göremeyebilirsiniz, bütün parametrelerini görmek için [Graph](../Graph) üzerinde bir şey seçmelisiniz (emitter ve ya system). Parametreler ekranında bir parametreyi seçtiginiz zaman modüllerin üzerinde aşagıdaki resimdeki gibi işaretler çıkar.


<img src="../../../Dosyalar/Niagara_Editor_Parameters_Parameter_Focus.jpg">


Soldaki üç işaret okuma, yazma ve hem okuma hem yazmayı ifade eder.

* okuma
<img src="../../../Dosyalar/Niagara_Editor_Parameters_Read.jpg">

* yazma
<img src="../../../Dosyalar/Niagara_Editor_Parameters_Write.jpg">

* okuma/yazma
<img src="../../../Dosyalar/Niagara_Editor_Parameters_Read_Write.jpg">


<br>


Bütün bu parametrelerin içeriklerini ve kullanılış şekillerini aşagıda bulabilirsiniz. Parametreleri "Degişken", "Durumsal" ve "Sabit" olmak üzere 3 türe ayırdım ve her parametrenin başında parantez içinde türünü görebilirsiniz, bu türlerin anlamları şunlardır,

<br>

* Degişken

Simulasyon ilerledikçe ve ya olaylar gerçekleştikçe sürekli degişen parametrelerdir, mesela [System.Age](#systemage) sürekli güncellenir.

* Durumsal

Simulasyon esnasında degişebilen parametrelerdir ama sürekli degişmezler, sadece belirli durumlarda degişirler. Mesela [System.ExecutionState](#systemexecutionstate)

* Sabit

Sabit parametreler genellikle bilgi sunan parametrelerdir, belki simulasyon esnasında degişebilirler ama genellikle degişmezler. Sabit parametreler genellikle niagara sisteminiz ve ya emitter üzerinde bi degişiklik yaptıgınızda degişirler, mesela bir modülün inputunu degiştirmek gibi. Örnegin [System.CurrentLoopDuration](#systemcurrentloopduration)

<br>
<br>


## System Attributes

* #### [System.Age](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Degişken) Sistemin yaşını, yaşam süresini, çalıştıgı süreyi verir (saniye türünden). Zaman geçtikçe artar.

* #### [System.bCompleteOnInactive]()
bilmiyorum.

* #### [System.CurrentLoopDelay](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Sabit) System State'in [Loop Delay](../Moduller#loop-delay-1) inputuna baglıdır.

* #### [System.CurrentLoopDuration](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Sabit) System State'in [Loop Duration](../Moduller#loop-duration-1) inputuna baglıdır.

* #### [System.ExecutionState](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Durumsal) Sistemin yürütülme durumuna baglıdır. Sistemin yürütülme durumu degişirse bu parametre de degişir. 4 modu vardır,
<br>
<br>
Active = Aktif
<br>
Inactive = Aktif degil, "Inactive" modunda olan Sistem/Emitter parçacık spawn edemez.
<br>
Inactive Clear = "Inactive Clear" moduna geçildiginde bütün parçacıklar silinir ve "Inactive" moduna geçilir.
<br>
Complete = Tamamlanmış

* #### [System.ExecutionStateSource](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
bilmiyorum.

* #### [System.LoopCount](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Degişken) Sistemin geçirdigi loop sayısını belirtir, başlangıçta 0'dır, her loop bittiginde bu parametre 1 artar.

* #### [System.LoopedAge](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Degişken) Sistemin şu anki loop için yaşını, yaşam süresini, çalıştıgı süreyi verir (saniye türünden). Mesela diyelim simulasyonun 8. saniyesindeyiz ve [sistemin loop süresi](../Moduller#loop-duration-1) 5 saniye, bu durumda birinci loop bitmiş ikinci loop'a geçmişiz demektir ve bu parametrenin degeri 3'tür. Yeni loop'a geçince deger tekrar sıfırlanır.

* #### [System.NormalizedLoopAge](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Degişken) Sistemin şu anki loop için yaşını, yaşam süresini, çalıştıgı süreyi normalized olarak verir. Normalize işlemi, degeri 0 - 1 arasına taşır. Mesela diyelim simulasyonun 3. saniyesindeyiz ve [sistemin loop süresi](../Moduller#loop-duration-1) 5 saniye, bu durumda deger 3/5 = 0.6 olur. Normalize yani 0 - 1 arasına taşıma işlemini yüzde olarak almak gibi düşünebilirsiniz, yani 0.6 = %60.





## Emitter Attributes

* #### [Emitter.Age]()
(Degişken) Emitter'ın yaşını, yaşam süresini, çalıştıgı süreyi verir (saniye türünden). Zaman geçtikçe artar.

* #### [Emitter.AlphaScale]()
(Durumsal) Parçacıkların renkleri için Alpha kanalı degeri.

* #### [Emitter.CurrentLoopDelay]()
(Sabit) Emitter State'in [Loop Delay](../Moduller#loop-delay) inputuna baglıdır.

* #### [Emitter.CurrentLoopDuration]()
(Sabit) Emitter State'in [Loop Duration](../Moduller#loop-duration) inputuna baglıdır.

* #### [Emitter.DistanceTraveled]()
(Degişken) Emitter'ın toplamda hareket ettigi mesafeyi verir (cm). Hareket ettikçe artar.

* #### [Emitter.ExecutionState]()
(Durumsal) Emitter'ın yürütülme durumuna baglıdır. Emitter'ın yürütülme durumu degişirse bu parametre de degişir. 4 modu vardır,
<br>
<br>
Active = Aktif
<br>
Inactive = Aktif degil, "Inactive" modunda olan Sistem/Emitter parçacık spawn edemez.
<br>
Inactive Clear = "Inactive Clear" moduna geçildiginde bütün parçacıklar silinir ve "Inactive" moduna geçilir.
<br>
Complete = Tamamlanmış

* #### [Emitter.ExecutionStateSource]()
bilmiyorum.

* #### [Emitter.LocalSpace]()
(Sabit) Emitter'ın [Local Space](../Graph#local-space) inputuna baglıdır.

* #### [Emitter.LoopCount]()
(Degişken) Emitter'ın geçirdigi loop sayısını belirtir, başlangıçta 0'dır, her loop bittiginde bu parametre 1 artar.

* #### [Emitter.LoopedAge]()
(Degişken) Emitter'ın şu anki loop için yaşını, yaşam süresini, çalıştıgı süreyi verir (saniye türünden). Mesela diyelim simulasyonun 8. saniyesindeyiz ve [emitter'ın loop süresi](../Moduller#loop-duration) 5 saniye, bu durumda birinci loop bitmiş ikinci loop'a geçmişiz demektir ve bu parametrenin degeri 3'tür. Yeni loop'a geçince deger tekrar sıfırlanır.

* #### [Emitter.NormalizedLoopAge]()
(Degişken) Emitter'ın şu anki loop için yaşını, yaşam süresini, çalıştıgı süreyi normalized olarak verir. Normalize işlemi, degeri 0 - 1 arasına taşır. Mesela diyelim simulasyonun 3. saniyesindeyiz ve [emitter'ın loop süresi](../Moduller#loop-duration) 5 saniye, bu durumda deger 3/5 = 0.6 olur. Normalize yani 0 - 1 arasına taşıma işlemini yüzde olarak almak gibi düşünebilirsiniz, yani 0.6 = %60.

* #### [Emitter.Scalability.DistanceFraction]()
bilmiyorum.

* #### [Emitter.SpawnBurst_Instantaneous.SpawnBurst]()
[Spawn Burst Instantaneous](../Moduller#spawn-burst-instantaneous) tarafından oluşturulur. bilmiyorum.

* #### [Emitter.SpawnPerFrame.SpawnBurst]()
[Spawn Per Frame](../Moduller#spawn-per-frame) tarafından oluşturulur. bilmiyorum.

* #### [Emitter.SpawnPerUnit.SpawnOutputInfo]()
[SpawnRate](../Moduller#spawn-per-unit) tarafından oluşturulur. bilmiyorum.

* #### [Emitter.SpawnPerUnit.SpawnRemainder]()
[SpawnRate](../Moduller#spawn-per-unit) tarafından oluşturulur. Bir sonraki parçacıgı spawn etmeye kalan mesafeyi belirtir (cm cinsinden).

* #### [Emitter.SpawnRate.SpawnOutputInfo]()
[SpawnRate](../Moduller#spawn-rate) tarafından oluşturulur. bilmiyorum.

* #### [Emitter.SpawnRate.SpawnRemainder]()
(Degişken) [SpawnRate](../Moduller#spawn-rate) tarafından oluşturulur. Bir sonraki parçacıgı spawn etmeye kalan süreyi belirtir (saniye cinsinden).



## Particle Attributes

* #### [Particles.Age]()
(Degişken) Parçacıgın yaşını, yaşam süresini, yaşadıgı süreyi verir (saniye türünden). Zaman geçtikçe artar.

* #### [Particles.Color]()
(Durumsal) Parçacıgın renk degeri.

* #### [Particles.Initial.Color]()
(Sabit) Parçacıgın ilk renk degerini verir. Dolayısıyla sabittir, Initialize Particle'ın [Color](../Moduller#color-3) degerine baglıdır da denebilir.

* #### [Particles.Lifetime]()
(Sabit) Initialize Particle'ın [Lifetime](../Moduller#lifetime) inputuna baglıdır.

* #### [Particles.Mass]()
bilmiyorum.

* #### [Particles.MaterialRandom]()
bilmiyorum.

* #### [Particles.NormalizedAge]()
(Degişken) Parçacıgın şu anki yaşını, yaşam süresini, çalıştıgı süreyi normalized olarak verir. Normalize işlemi, degeri 0 - 1 arasına taşır. Mesela diyelim ki parçacık spawn olalı 3 saniye oldu ve [parçacıgın lifetime süresi](../Moduller#lifetime) 5 saniye, bu durumda deger 3/5 = 0.6 olur. Normalize yani 0 - 1 arasına taşıma işlemini yüzde olarak almak gibi düşünebilirsiniz, yani 0.6 = %60.

* #### [Particles.Position]()
(Degişken) Parçacıgın konumunu verir, eger Emitter'ın [Local Space](../Graph#local-space) seçenegi açıksa konumu 0,0,0'a göre verir, eger kapalıysa dünya üzerindeki konumunu verir.

* #### [Particles.RibbonUVDistance]()
bilmiyorum.





## Module Outputs

* #### [Output.ParticleState.FirstFrame]()
(Durumsal) Her parçacık için sadece FirstFrame yani ilk frame'de (kare, fps) true degeri döndürür, sonra false.

* #### [Output.SpawnBurst_Instantaneous.HasSpawnedThisFrame]()
(Durumsal) [Spawn Burst Instantaneous](../Moduller#spawn-burst-instantaneous) tarafından oluşturulur. Eger bu frame'de (kare, fps) parçacık spawn edildiyse true, edilmediyse false döndürür.

* #### [Output.SpawnPerUnit.HasSpawnedThisFrame]()
(Durumsal) [Spawn Per Unit](../Moduller#spawn-per-unit) tarafından oluşturulur. Eger bu frame'de (kare, fps) parçacık spawn edildiyse true, edilmediyse false döndürür.

* #### [Output.SpawnRate.HasSpawnedThisFrame]()
(Durumsal) [SpawnRate](../Moduller#spawn-rate) tarafından oluşturulur. Eger bu frame'de (kare, fps) parçacık spawn edildiyse true, edilmediyse false döndürür.




## Engine Provided

* #### [Engine.DeltaTime]()
(Degişken) Her frame (kare, fps) arasındaki DeltaTime yani gecikme süresini verir.

* #### [Engine.Emitter.NumParticles]()
(Degişken) Şu anki parçacık sayısını verir.

* #### [Engine.Emitter.SpawnCountScale]()
bilmiyorum.

* #### [Engine.Owner.ExecutionState]()
(Durumsal) Yürütülme durumuna baglıdır. Yürütülme durumu degişirse bu parametre de degişir. 4 modu vardır,
<br>
<br>
Active = Aktif
<br>
Inactive = Aktif degil, "Inactive" modunda olan Sistem/Emitter parçacık spawn edemez.
<br>
Inactive Clear = "Inactive Clear" moduna geçildiginde bütün parçacıklar silinir ve "Inactive" moduna geçilir.
<br>
Complete = Tamamlanmış

* #### [Engine.Owner.LODDistanceFraction]()
bilmiyorum.

* #### [Engine.Owner.Velocity]()
(Degişken) Owner için (Emitter/System, yani direktmen simulasyon) her frame arasındaki hareket edilen mesafeyi hesaplayıp, şu anki hızı (velocity) verir.





## Stack Context Sensitive
## Stage Transients

* #### [Transient.FirstFrame]()
(Durumsal) Sadece FirstFrame yani ilk frame'de (kare, fps) true degeri döndürür, sonra false.

* #### [Transient.ParticleColorScaleFactor]()
(Durumsal) [Scale Color](../Moduller#scale-color-1) ve ya [Scale Color by Speed](../Moduller#scale-color-by-speed) modülü kullanıldıgında, kullanılan scale degerlerini (RGBA) bu parametreye kaydeder.

* #### [Transient.ScalabilityEmitterExecutionState]()
bilmiyorum.

* #### [Transient.ScalabilityEmitterSpawnCountScale]()
bilmiyorum.

* #### [Transient.ScalabilityExecutionState]()
bilmiyorum.

* #### [Transient.SpawningbCanEverSpawn]()
bilmiyorum.



## Niagara Parameter Collection
