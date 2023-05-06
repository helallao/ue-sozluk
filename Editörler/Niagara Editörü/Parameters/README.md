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

* #### [Emitter.SpawnParticlesInGrid.Grid Location Spawn Count]()
[Spawn Particles in Grid](../Moduller#spawn-particles-in-grid) tarafından oluşturulur. bilmiyorum.

* #### [Emitter.SpawnParticlesInGrid.Grid Location X Count]()
(Sabit) [Spawn Particles in Grid](../Moduller#spawn-particles-in-grid) tarafından oluşturulur. [X Count](../Moduller#x-count) inputuna baglıdır.

* #### [Emitter.SpawnParticlesInGrid.Grid Location XYZ Count]()
[Spawn Particles in Grid](../Moduller#spawn-particles-in-grid) tarafından oluşturulur.

* #### [Emitter.SpawnParticlesInGrid.Grid Location Y Count]()
(Sabit) [Spawn Particles in Grid](../Moduller#spawn-particles-in-grid) tarafından oluşturulur. [Y Count](../Moduller#y-count) inputuna baglıdır.

* #### [Emitter.SpawnParticlesInGrid.Grid Location Z Count]()
(Sabit) [Spawn Particles in Grid](../Moduller#spawn-particles-in-grid) tarafından oluşturulur. [Z Count](../Moduller#z-count) inputuna baglıdır.

* #### [Emitter.SpawnParticlesInGrid.SpawnBurst]()
[Spawn Particles in Grid](../Moduller#spawn-particles-in-grid) tarafından oluşturulur. bilmiyorum.

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

* #### [Particles.ID]()
(Sabit) Emitter'ın [Requires Persistent IDs](../Graph#requires-persistent-ids) ayarı açık iken her parçacıga id verilir ve bu id "Particles.ID" parametresinde tutulur.

* #### [Particles.Initial.Color]()
(Sabit) Parçacıgın ilk renk degerini verir. Dolayısıyla sabittir, Initialize Particle'ın [Color](../Moduller#color-3) degerine baglıdır da denebilir.

* #### [Particles.Initial.Velocity]()
bilmiyorum.

* #### [Particles.JitterDelayTimer]()
(Degişken) [Jitter Position](../Moduller#jitter-position) kullanıldıgı zaman oluşturulur. Eger [Jitter Delay](../Moduller#jitter-delay) inputuna deger verilmişse, bir sonraki jitter'ın çagırılmasına kalan süreyi verir.

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

* #### [Particles.RotateAroundPoint.IncrementingCounter]()
[Rotate Around Point](../Moduller#rotate-around-point) kullanıldıgı zaman oluşturulur.

* #### [Particles.RotateAroundPoint.VectorFromCenter]()
[Rotate Around Point](../Moduller#rotate-around-point) kullanıldıgı zaman oluşturulur.

* #### [Particles.ShapeLocation.ShapeBitangent]()
[Shape Location](../Moduller#shape-location) kullanıldıgı zaman oluşturulur.

* #### [Particles.ShapeLocation.ShapeNormal]()
[Shape Location](../Moduller#shape-location) kullanıldıgı zaman oluşturulur.

* #### [Particles.ShapeLocation.ShapePosition]()
[Shape Location](../Moduller#shape-location) kullanıldıgı zaman oluşturulur.

* #### [Particles.ShapeLocation.ShapeTangent]()
[Shape Location](../Moduller#shape-location) kullanıldıgı zaman oluşturulur.

* #### [Particles.ShapeLocation.ShapeVector]()
[Shape Location](../Moduller#shape-location) kullanıldıgı zaman oluşturulur.

* #### [Particles.VectorNoiseInterval]()
(Degişken) [Vector Noise Force](../Moduller#vector-noise-force) kullanıldıgı zaman oluşturulur. Sıradaki yön degiştirme zamanına kalan süreyi tutar.

* #### [Particles.Velocity]()
bilmiyorum.




## Module Outputs

* #### [Output.CurlNoiseForce.CurlNoiseForce]()
(Degişken) [Curl Noise Force](../Moduller#curl-noise-force) kullanıldıgı zaman oluşturulur. Her parçacık için, parçacıga [Curl Noise Force](../Moduller#curl-noise-force) efektinin uygulandıgı konumu verir.

* #### [Output.GridLocation.GridCellCoordinate]()
[Grid Location](../Moduller#grid-location) kullanıldıgı zaman oluşturulur.

* #### [Output.GridLocation.GridSpacing]()
[Grid Location](../Moduller#grid-location) kullanıldıgı zaman oluşturulur.

* #### [Output.GridLocation.GridUVW]()
[Grid Location](../Moduller#grid-location) kullanıldıgı zaman oluşturulur.

* #### [Output.GridLocation.Normalized Array location]()
[Grid Location](../Moduller#grid-location) kullanıldıgı zaman oluşturulur.

* #### [Output.GridLocation.XYZ Spacing]()
[Grid Location](../Moduller#grid-location) kullanıldıgı zaman oluşturulur.

* #### [Output.GridLocation.XYZCountAsVector]()
[Grid Location](../Moduller#grid-location) kullanıldıgı zaman oluşturulur.

* #### [Output.ParticleState.FirstFrame]()
(Durumsal) Her parçacık için sadece FirstFrame yani ilk frame'de (kare, fps) true degeri döndürür, sonra false.

* #### [Output.PointForce.NormalizedDistance]()
(Degişken) [Point Force](../Moduller#point-force) tarafından oluşturulur. Eger Point Force'un [Force Falloff Distance](../Moduller#force-falloff-distance) ayarı açılmış ise, falloff çapını belirlemişsiniz demektir ve Output.PointForce.NormalizedDistance parametresi Point Force'un orijin noktası ile bu uzaklık degerinin arasındaki mesafeyi normalized olarak verir. Eger Point Force'un [Force Falloff Distance](../Moduller#force-falloff-distance) ayarı açılmış ise, default olarak bunu 1000 varsayar (bu Point Force'un sadece bu çapta etkili olacagı anlamına gelmiyor, sadece bu paramtrede 1000 kullanılmış). Normalize işlemi, degeri 0 - 1 arasına taşır. Mesela diyelim ki parçacık Point Force'un orijin noktası ile Falloff Distance için belirlenen uzaklıklıgın tam ortasında, bu durumda deger 0.5 olur. Normalize yani 0 - 1 arasına taşıma işlemini yüzde olarak almak gibi düşünebilirsiniz, yani 0.5 = %50.

* #### [Output.PointForce.NormalizedDistanceInverted]()
(Degişken) Output.PointForce.NormalizedDistance parametresi ile aynıdır ama uzaklıgı degil yakınlıgı verir, yani tam tersini verir. Yakındayken 1, uzaklaştıkça 0'a dogru kayar ve Falloff Distance olarak belirlenen uzaklık degerini geçtikten sonra 0 verir.

* #### [Output.PointForce.NormalizedFalloff]()
(Degişken) Parçacık için Point Force'un şu anki Falloff (etkisi) degerini verir. Bunu parçacıgın Falloff Distance olarak belirlenen uzaklık degerine olan uzaklıgı gibi düşünebilirsiniz. Falloff çapına yaklaştıkça bu deger de azalır ve Falloff Distance çapını geçtikten sonra 0 olur.

* #### [Output.PointForce.WithinRange]()
(Durumsal) Parçacıgın force etkisi alanının içinde olup olmadıgı bilgisini verir. Yani Falloff Distance olarak belirlenen uzaklık degerini geçmedigi sürece true, geçtikten sonra false verir.

* #### [Output.RotateAroundPoint.LocalForwardVector]()
[Rotate Around Point](../Moduller#rotate-around-point) kullanıldıgı zaman oluşturulur.

* #### [Output.RotateAroundPoint.OutputPosition]()
[Rotate Around Point](../Moduller#rotate-around-point) kullanıldıgı zaman oluşturulur.

* #### [Output.SpawnBurst_Instantaneous.HasSpawnedThisFrame]()
(Durumsal) [Spawn Burst Instantaneous](../Moduller#spawn-burst-instantaneous) tarafından oluşturulur. Eger bu frame'de (kare, fps) parçacık spawn edildiyse true, edilmediyse false döndürür.

* #### [Output.SpawnParticlesInGrid.HasSpawnedThisFrame]()
(Durumsal) [Spawn Particles in Grid](../Moduller#spawn-particles-in-grid) tarafından oluşturulur. Eger bu frame'de (kare, fps) parçacık spawn edildiyse true, edilmediyse false döndürür.

* #### [Output.SpawnPerUnit.HasSpawnedThisFrame]()
(Durumsal) [Spawn Per Unit](../Moduller#spawn-per-unit) tarafından oluşturulur. Eger bu frame'de (kare, fps) parçacık spawn edildiyse true, edilmediyse false döndürür.

* #### [Output.SpawnRate.HasSpawnedThisFrame]()
(Durumsal) [SpawnRate](../Moduller#spawn-rate) tarafından oluşturulur. Eger bu frame'de (kare, fps) parçacık spawn edildiyse true, edilmediyse false döndürür.

* #### [Output.SpringForce.PotentialEnergy]()
[Spring Force](../Moduller#spring-force) tarafından oluşturulur.

* #### [Output.SpringForce.SpringForce]()
[Spring Force](../Moduller#spring-force) tarafından oluşturulur.



## Engine Provided

* #### [Engine.DeltaTime]()
(Degişken) Her frame (kare, fps) arasındaki DeltaTime yani gecikme süresini verir.

* #### [Engine.Emitter.NumParticles]()
(Degişken) Şu anki parçacık sayısını verir.

* #### [Engine.Emitter.SimulationPosition]()
(Degişken) Simulasyon konumunu verir. Emitter'ın [Local Space](../Graph#local-space) inputuna baglıdır. [Local Space](../Graph#local-space) açık ise (0,0,0), kapalı ise dünya üzerindeki konumu verir.

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

* #### [Engine.Owner.Position]()
(Sabit) Dünyanıza koydugunuz niagara'nın konum degerini verir.

* #### [Engine.Owner.Scale]()
(Sabit) Dünyanıza koydugunuz niagara'nın scale degerini verir.

* #### [Engine.Owner.SystemLocalToWorld]()
bilmiyorum.

* #### [Engine.Owner.SystemLocalToWorldNoScale]()
bilmiyorum.

* #### [Engine.Owner.SystemWorldToLocal]()
bilmiyorum.

* #### [Engine.Owner.SystemWorldToLocalNoScale]()
bilmiyorum.

* #### [Engine.Owner.Velocity]()
(Degişken) Owner için (Emitter/System, yani direktmen simulasyon) her frame arasındaki hareket edilen mesafeyi hesaplayıp, şu anki hızı (velocity) verir.

* #### [Engine.Time]()
Oyunda geçen toplam süreyi (saniye cinsinden) verir. Blueprint'deki "Game Time in Seconds" ile aynıdır.




## Stack Context Sensitive
## Stage Transients

* #### [Transient.FirstFrame]()
(Durumsal) Sadece FirstFrame yani ilk frame'de (kare, fps) true degeri döndürür, sonra false.

* #### [Transient.ParticleColorScaleFactor]()
(Durumsal) [Scale Color](../Moduller#scale-color-1) ve ya [Scale Color by Speed](../Moduller#scale-color-by-speed) modülü kullanıldıgında, kullanılan scale degerlerini (RGBA) bu parametreye kaydeder.

* #### [Transient.PhysicsForce]()
bilmiyorum.

* #### [Transient.PhysicsPotentialEnergy]()
bilmiyorum.

* #### [Transient.ScalabilityEmitterExecutionState]()
bilmiyorum.

* #### [Transient.ScalabilityEmitterSpawnCountScale]()
bilmiyorum.

* #### [Transient.ScalabilityExecutionState]()
bilmiyorum.

* #### [Transient.SpawningbCanEverSpawn]()
bilmiyorum.



## Niagara Parameter Collection
