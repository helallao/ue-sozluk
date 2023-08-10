# Debug Hud
<img src="../../../../Dosyalar/Niagara_Editor_Niagara_Debugger_Debug_Hud.jpg">

Debug Hud, [Level Editörünüzde](../../../Level%20Editörü) Niagara efektleri üzerinde debug yapabilmeniz için gerekli bilgileri ekranda gösterir.


# Bölümler

* [Debug General](#debug-general)
* [Debug Overview](#debug-overview)
* [Debug Filter](#debug-filter)
* [Debug System](#debug-system)
* [Debug Particles](#debug-particles)
* [Perf Overview](#perf-overview)
* [Colors](#colors)
* [Performance](#performance)


<br>
<br>



## [Debug General]()

* #### Debug Hud Enabled
Bu ayar ve "Debug HUD Rendering Enabled" ayarı, Debug Hud'u kullanmak için gerekli olan iki ayardır, Debug Hud'u aktifleştirirler.

* #### Debug HUD Rendering Enabled
Bu ayar ve "Debug Hud Enabled" ayarı, Debug Hud'u kullanmak için gerekli olan iki ayardır, Debug Hud'u aktifleştirirler.

* #### Validate System Simulation Data Buffers
bilmiyorum.

* #### Validate Particle Data Buffers
bilmiyorum.



## [Debug Overview]()

* #### Debug Overview Enabled
Bu seçenek açıldıgında, Debug Hud'un altında bir overview yani degerlendirmeler gibi bi kısım çıkar.

* #### Debug Overview Mode
Debug Overview açıldıgında hangi degerlendirmelerin gösterilecegini belirler. Modlar,

Mod | İşlem
:---: | :---:
Overview | Genel bilgiler
Scalability | bilmiyorum
Performance | Performans bilgileri
Gpu Compute Performance | Gpu için performans bilgileri


* #### Debug Overview Font
Font büyüklügü.

* #### Debug Overview Text Location
Debug Overview için yazıların konumu.

* #### Show Registered Components
Sadece "Debug Overview Mode" ayarı "Overview" modundayken vardır. bilmiyorum.

* #### Overview Show Filtered System Only
Bu seçenek açıldıgında overview degerlendirmelerinde sadece [System Filter](#system-filter) ile filtre edilmiş sistemleri gösterir.





## [Debug Filter]()

* #### System Filter
Sadece ismini verdiginiz System için Debug Hud gösterir ve [Wildcard](../../Terimler%20Sözlügü#wildcard-filtering) kullanabilirsiniz.

* #### Emitter Filter
Emitter'lar için filtreleme yapar ve [Wildcard](../../Terimler%20Sözlügü#wildcard-filtering) kullanabilirsiniz. Emitter'lar için filtreleme yapmak, [Show Particle Attributes]() kullanırken sadece belirli Emitter'ların "Particle attributes" larını görmenize yarar. Yani sadece filtrelenmiş Emitter'ların parçacıkları.

* #### Actor Filter
Sadece ismini verdiginiz Aktörler için Debug Hud gösterir ve [Wildcard](../../Terimler%20Sözlügü#wildcard-filtering) kullanabilirsiniz.

* #### Component Filter
Sadece ismini verdiginiz Component'ler için Debug Hud gösterir ve [Wildcard](../../Terimler%20Sözlügü#wildcard-filtering) kullanabilirsiniz.





## [Debug System]()

* #### System Debug Verbosity
System hakkında gösterilen bilgilerin detay derecesi.

* #### System Emitter Verbosity
Emitter hakkında gösterilen bilgilerin detay derecesi.

* #### Data Interface Verbosity
bilmiyorum.

* #### System Show Bounds
Bu ayar açıldıgında System için sınırları gösterir.

* #### System Show Active Only in World
Bu ayar açıldıgında sadece aktif System'lar (yani kill edilmemiş ve ya inactive mode'a girmemiş) gösterilir.

* #### Show System Attributes
Bu ayar açıldıgında System'lar için System parametrelerini gösterir.

* #### System Attributes
Gösterilecek System parametrelerinin listesi ve [Wildcard](../../Terimler%20Sözlügü#wildcard-filtering) kullanabilirsiniz.

* #### System Text Options
System'ler için gösterilen yazıların ayarları,

Mod | İşlem
:---: | :---:
Font | Font büyüklügü
Horizontal Alignment | Yazının yatay hizası.
Vertical Alignment | Yazının dikey hizası.
Screen Offset | Yazının konumuna offset ekler.




## [Debug Particles]()

* #### Show Particle Attributes
Bu ayar açıldıgında parçacıklar için parçacık parametrelerini gösterir.

* #### Enable Gpu Particle Readback
Bu ayar Gpu kullanan Emitter'lar içindir. Gpu kullanan Emitter'ların parçacıklarının bilgisini görüntülemek için bu ayarı açmalısınız. Parçacıkları Gpu'dan Cpu'ya kopyalar, bu da biraz gecikmeye sebep olur, ayrıca bu ayarı açmak performans ve ram üzerine de biraz etki uygulayabilir.

* #### Show Particle Index
Bu ayar açıldıgında her parçacık için gösterilen yazıların en üstüne parçacık numarasını da ekler.

* #### Particle Attributes
Gösterilecek parçacık parametrelerinin listesi ve [Wildcard](../../Terimler%20Sözlügü#wildcard-filtering) kullanabilirsiniz.

* #### Particle Text Options
Parçacıklar için gösterilen yazıların ayarları,

Mod | İşlem
:---: | :---:
Font | Font büyüklügü
Horizontal Alignment | Yazının yatay hizası.
Vertical Alignment | Yazının dikey hizası.
Screen Offset | Yazının konumuna offset ekler.


* #### Show Particles Attributes With System
Parçacıklar için gösterilen yazıları dünyada, parçacıkların üzerinde göstermek yerine System ile birlikte gösterir.

* #### Show Particle Attributes Vertical
Parçacıklar için gösterilen yazıları alt alta gösterir, kapatırsanız tek satırda (anlaşılmaz) olur.

* #### Use Max Particles to Display
Parçacıklar için gösterilen yazılara bir sınır getirir, çok fazla parçacık olursa bir yerden sonra parçacıklar için yazıları göstermez.

* #### Use Particle Display Clip
Particle Display Clip kullanımını açar. Parçacıkların konumlarının bize uzaklıgına göre bazılarını gösterir bazılarını göstermez.

* #### Particle Display Clip
Parçacıkların konumlarının bize uzaklıgına göre bazılarını gösterir bazılarını göstermez. "X" inputu, parçacık ile aramızda olması gereken minimum mesafe, "Y" inputu, parçacık ile aramızda olması gereken maximum mesafe.

* #### Use Particle Display Center Radius
Bu ayar açıldıgında sadece ekranınızın orta taraflarında olan parçacıklar için bilgiler gösterilir.

* #### Particle Display Center Radius
"Use Particle Display Center Radius" ayarı için geçerli olan alanın radius degeri yani çapı, azaltırsanız sadece tam orta kısımlarda olan parçacıkların bilgileri gösterilir, arttırırsanız bu alan genişler.

* #### Max Particles to Display
Gösterilecek maximum parçacık bilgisi sayısı.




## [Perf Overview]()

Bu kategorideki ayarlar [Debug Overview Mode](#debug-overview-mode) "Performance" modundayken uygulanacak ayarları etkiler.

* #### Perf Report Frames
bilmiyorum.

* #### Perf Sample Mode
bilmiyorum.

* #### Perf Graph Mode
bilmiyorum.

* #### Perf History Frames
Tabloda gösterilecek geçmiş frame sayısı.

* #### Perf Graph Time Range
Tablonun range degerleri, sanırım ms (milisaniye) cinsinden.

* #### Perf Graph Size
Tablo boyutu.

* #### Perf Graph Axis Color
Tablo rengi.

* #### Smoothing Width
Tablo degerleri için yumuşatma uygular.





## [Colors]()

Bu kategorideki ayarlar ile renkleri ayarlayabilirsiniz.



## [Performance]()

* #### Show Global Budget Info
bilmiyorum.


