# FX Outliner
<img src="../../../../Dosyalar/Niagara_Editor_Niagara_Debugger_FX_Outliner.jpg">

FX Outliner, istediginiz frame'i ve ya frame'leri (kare) capture edip, sonra da incelemenize yarar.


# Bölümler

* [Toolbar](#toolbar)
* [Simulasyon Ögeleri](#simulasyon-ögeleri)


<br>
<br>



## [Toolbar]()

<img src="../../../../Dosyalar/Niagara_Editor_Niagara_Debugger_FX_Outliner_Toolbar.jpg">


* #### Capture
Tıkladıgınız anda capture işlemini tetikler.

* #### Perf
Bu ayar açıkken performans bilgilerini de capture eder.

* #### Delay
Capture işlemi gerçekleşmeden önce beklenecek frame (kare) sayısı. [Capture](#capture) butonuna tıkladıgınız anda, verdiginiz delay kadar beklenir sonra capture işlemi gerçekleşir.

* #### Sim Cache Frames
"Sim Cache Data" yani simulasyon önbellegi bilgisi capture edilirken, kaç tane frame'in capture edilecegini ayarlar.

* #### View Mode
Capture edilen simulasyon ögeleri üzerinde yapacagınız işleme göre mod seçmenize yarar. Modlar,
<br>
<br>
State = Genel durum bilgilerini gösterir.
<br>
Performance = Performans bilgilerini gösterir.
<br>
Debug = Debug işlemleri için gerekli olan kontrol butonlarını gösterir.

* #### Filters
Capture edilen simulasyon ögeleri üzerinde filtreleme yapar.

* #### Descending
Sıralama düzenini yukarıdan aşagı/aşagıdan yukarı çevirir.

* #### Sort Mode
Sıralama düzeni, modlar,
<br>
<br>
Auto = [View Mode'a](#view-mode) göre kendisi seçer.
<br>
Filter Matches = Filtre'nize olan uyumluluk degerine göre sıralar.
<br>
Average Time = bilmiyorum.
<br>
Max Time = bilmiyorum.

* #### Units
Zaman degerlerinin gösterilecegi birim (genellikle performans modunda zaman degerleri vardır).






## [Simulasyon Ögeleri]()

<img src="../../../../Dosyalar/Niagara_Editor_Niagara_Debugger_FX_Outliner_Simulasyon_Ogeleri.jpg">

* Eger sizde de fotograftaki gibi ögeler listelenmemişse [Capture](#capture) işlemi yapmamışsınız demektir.

Simulasyon Ögeleri ekranı size dünyanızdaki niagara'ları gösterir.

<img src="../../../../Dosyalar/Niagara_Editor_Niagara_Debugger_FX_Outliner_Simulasyon_Ogeleri_2.jpg">

Yukardaki fotografta görebileceginiz gibi, en üstte level (map), onun altında niagara sistemleri kırmızı renkle, sistemin altında o sistem'in instance'ları mavi renkle, sistem instance'larının altında emitter'lar turuncu renkle gösterilir. Üzerine tıkladıgınızda sag taraftaki boşlukta bilgiler çıkar.

