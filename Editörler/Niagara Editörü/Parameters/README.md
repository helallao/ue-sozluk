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

Simulasyon esnasında degişebilen parametrelerdir ama sürekli degişmezler, sadece belirli durumlarda degişirler.

* Sabit

Sabit parametreler genellikle bilgi sunan parametrelerdir, belki simulasyon esnasında degişebilirler ama genellikle degişmezler. Sabit parametreler genellikle niagara sisteminiz ve ya emitter üzerinde bi degişiklik yaptıgınızda degişirler. Mesela bir modülün inputunu degiştirmek gibi.

<br>
<br>


## System Attributes

* #### [System.Age](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Degişken) Sistemin yaşını, yaşam süresini, çalıştıgı süreyi verir (saniye türünden). Zaman geçtikçe artar.

* #### [System.bCompleteOnInactive]()
bilmiyorum.

* #### [System.CurrentLoopDelay](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Sabit) Sistemin [Loop Delay](../Moduller#loop-delay-1) inputuna baglıdır.

* #### [System.CurrentLoopDuration](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Sabit) Sistemin [Loop Duration](../Moduller#loop-duration-1) inputuna baglıdır.

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
(Degişken) Sistemin geçirdigi loop sayısını belirtir, başlangıçta 1'dir, her loop bittiginde bu parametre 1 artar.

* #### [System.LoopedAge](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Degişken) Sistemin şu anki loop için yaşını, yaşam süresini, çalıştıgı süreyi verir (saniye türünden). Mesela diyelim simulasyonun 8. saniyesindeyiz ve [sistemin loop süresi](../Moduller#loop-duration-1) 5 saniye, bu durumda birinci loop bitmiş ikinci loop'a geçmişiz demektir ve bu parametrenin degeri 3'tür. Yeni loop'a geçince deger tekrar sıfırlanır.

* #### [System.NormalizedLoopAge](https://docs.unrealengine.com/5.1/en-US/system-update-group-reference-for-niagara-effects-in-unreal-engine/#addparameter)
(Degişken) Sistemin şu anki loop için yaşını, yaşam süresini, çalıştıgı süreyi normalized olarak verir. Normalize işlemi, degeri 0 - 1 arasına taşır. Mesela diyelim simulasyonun 3. saniyesindeyiz ve [sistemin loop süresi](../Moduller#loop-duration-1) 5 saniye, bu durumda deger 3/5 = 0.6 olur. Normalize yani 0 - 1 arasına taşıma işlemini yüzde olarak almak gibi düşünebilirsiniz, yani 0.6 = %60.





## Emitter Attributes
## Particle Attributes
## Module Outputs
## Engine Provided
## Stack Context Sensitive
## Stage Transients
## Niagara Parameter Collection
