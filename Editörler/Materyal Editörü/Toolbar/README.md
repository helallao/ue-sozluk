# Toolbar
<img src="../../../Dosyalar/Materyal_Editor_Toolbar.jpg">



# Bölümler (Soldan Saga)

* [Save Butonu](#save-butonu)
* [Dosya Konumunu Göster](#dosya-konumunu-g%C3%B6ster)
* [Apply Butonu](#apply-butonu)
* [Arama Butonu](#arama-butonu)
* [Home](#home)
* [Hierarchy](#hierarchy)
* [Live Update](#live-update)
* [Clean Graph](#clean-graph)
* [Preview State](#preview-state)
* [Hide Unrelated](#hide-unrelated)
* [Stats](#stats)
* [Platform Stats](#platform-stats)




## [Save Butonu]()
Hem [Apply](#apply-butonu) uygular hem de dosyayı kaydeder.

## [Dosya Konumunu Göster]()
Şu an işlem yapılan materyalin dosya konumunu açar, eger content browser yoksa yeni açar.

## [Apply Butonu]()
Apply butonu, şu an bu materyale sahip olan her meshe, yani dünyanızdaki bu materyale sahip olan objelere, yaptıgınız degişiklikleri uygular, materyale yaptıgınız degişiklikleri apply yapmadan dünya üzerindeki objelerde göremezsiniz. Apply Butonu yerine [Save Butonu](#save-butonu) da kullanılabilir ama çok kullanılmaz çünkü save yapmak daha uzun sürer, editörde materyal tasarlarken sürekli beklemek sıkıcı olur, o yüzden Apply Butonu kullanılır.

## [Arama Butonu]()
Arama pencerisini açar, arama penceresinde her isime göre arama yapabilir ve arama sonuçlarına tıklayıp hemen o noda gidebilirsiniz.

## [Home]()
Materyalin ana attribute noduna (her şeyi bagladıgımız palet) götürür.

## [Hierarchy]()
Materyalin instancelarını gösterir.

## [Live Update]()
Preview Material = [Preview Viewport](../Preview%20Viewport) bölümünde canlı olarak önizleme ayarını açar/kapatır.

Mod | İşlem
:---: | :---:
Realtime Nodes | Realtime olarak yani sürekli güncellenen nodları aktif/deaktif eder. Bu ayar açıksa, hani nodların kenarında texturenin ufak resmi olur ya, o resim resim her degiştiginde güncellenir, aynı ana materyaldeki gibi. Eger bu seçenek kapalıysa realtime nodlar çalışmaz.
All Node Previews | Bütün nodların Realtime Preview ayarını açar.


## [Clean Graph]()

Mod | İşlem
:---: | :---:
Clean Up | Ana attribute noduna (her şeyi bagladıgımız palet) baglı olmayan nodları siler.
Hide Unused Connectors | Baglı olmayan pinleri gizler.


## [Preview State]()

Mod | İşlem
:---: | :---:
Quality Level | Kalite ayarı
Feature Level | Bilmiyorum
Hide Disabled (Switch Params) | Bilmiyorum


## [Hide Unrelated]()
Seçilen node ile ilgisi olamayan nodları gizler. İlgisi olan nodlar, kendi inputlarına baglı olan ve output nodlarının baglandıgı diger nodlardır.

Mod | İşlem
:---: | :---:
Lock Node State | Şu an ki durumu kilitler, ilgili olan nodlardan başka node seçseniz bile degişmez. Belki anlaması zor olabilir diye örnek vericem, mesela bir nodu seçtiniz ve bu node ile ilgili olmayan nodlar gizlendi, bu seçenegi aktifleştirdikten sonra istediginiz noda tıklayabilirsiniz, ilgili olan node ayarları bozulmaz, böylelikle ilgisi olmayan nodlarla da işlemler yapabilirsiniz.
Focus Whole Chain | Normalde sadece output nodlarının baglandıgı nodlar ilgili nodlardır, ama bu seçenegi açarsanız o nodlara baglanan diger nodlar da ilgili nodlar arasına girer, yani sadece output nodları degil input nodları da ilgili node olur.

## [Stats]()
[Stats](../../../Sayfalar/Stats%20(Material)) bölümünü açar/kapatır.

## [Platform Stats]()
[Platform Stats](../../../Sayfalar/Platform%20Stats%20(Material)) bölümünü açar/kapatır. Platform Stats bölümünü Window'dan da açabilirsiniz ama kapatamazsınız (ilginç). 

