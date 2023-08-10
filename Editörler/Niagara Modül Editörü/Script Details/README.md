# Script Details
<img src="../../../Dosyalar/Niagara_Module_Editor_Script_Details.jpg">


Buradan yazdıgınız Niagara modül'ü ile ilgili ayarlamaları yaparsınız.


# Bölümler

* [Script](#script)
* [Validation](#validation)
* [Input Parameters](#input-parameters)
* [Output Parameters](#output-parameters)





## Script

* #### Module Usage Bitmask
Modülün kullanım alanlarını belirler. "Function", "Module" ve "Dynamic Input" seçenekleri geçersizdir. Önemli olan asset'in türüdür, yani [Niagara Module Script](../../../Assetler/Niagara%20Module%20Script) türünden bir asset için bu ayar ile "Dynamic Input" seçenegini açsanız bile dinamik input olarak kullanamazsınız. "Function", "Module" ve "Dynamic Input" için her birinin kendi asset türünü kullanabilirsiniz. Bunların haricinde diger seçenekler ise modülün kullanılacagı kategorileri belirler. Modülü seçtiginiz kategorilerde çalıştırabilirsiniz.

* #### Category
Modülü koyarken hangi kategori altında görünecegini belirler.

* #### Suggested
Bu ayarı açtıgınız zaman bu modül, Emitter'ınıza yeni modül eklerken, önerilenler bölümünde gösterilir (sag üstteki "Library Only" kapalı olmalı).

* #### Provided Dependencies
Bazen bir modül başka modüle ihtiyaç duyabilir. Buna dependency denir. Bu kategori şu anki modülün karşıladıgı dependency'lerin listesini tutar. Yani diyelim ki başka bir modülün "deneme" isminde bir dependency'si var. Eger buraya "deneme" diye yeni bir element eklerseniz. O zaman modülümüz bu dependency'i karşılamış olur. Yani bu ayar karşılanan dependency'lerin listesini tutar.

* #### Required Dependencies
Bazen bir modül başka modüle ihtiyaç duyabilir. Buna dependency denir. Bu kategori şu anki modülün ihtiyaç duydugu dependency'lerin listesini tutar. Eklediginiz her bir yeni element aşagıdaki ayarlara sahiptir,

Ayar | İçerik
:---: | :---:
Id | İhtiyaç duyulan dependency'nin ismi.
Type | İhtiyaç duyulan dependency'i karşılayan modülün bu modülden önce mi yoksa sonra mı olması gerektigini belirler.
Script Constraint | İhtiyaç duyulan dependency'i karşılayan modülün bu modül ile aynı kategoride mi yoksa herhangi bir kategoride mi olabilecegini belirler.
Required Version | İhtiyaç duyulan dependency'i karşılayan modülün versiyonunu belirtir. Eger sona "+" koyarsanız minimum bu versiyon olması gerek anlamına gelir. Eger "-" ile iki versiyon yazarsanız bu aralıktaki versiyonlar olması gerek anlamına gelir.
Only Evaluate in Script Usage | Bu modül bu kategorilerde iken bu dependency'e ihtiyaç duyar.
Description | İhtiyaç duyulan dependency için açıklama.


* #### Deprecation Recommendation
Eger bu modül geliştirilmeyi bıraktıysa önerilecek modül.

* #### Conversion Utility
bilmiyorum.

* #### Experimental
"Experimental Message" ayarını açar.

* #### Experimental Message
"Experimental" ayarı açıkken kullanılabilir. Deneysel modüller yani hatalı davranabilecek modüllere uyarı koymanıza yarar. Modülü seçtiginizde detaylar penceresinde en üstte bu açıklama görünür.

* #### Note Message
Modülü seçtiginizde detaylar penceresinde en üstte bu açıklama görünür. Modülün kullanımı ve olabilecek hataları yazabilirsiniz.

* #### Library Visibility
Modülün yeni modül ekleme ekranında gösterilip gösterilmeyecegini belirler. "Exposed" modunda modül gösterilir. "Unexposed" modunda modül gösterilmez ama sag üstteki "Library Only" seçenegi kapatıldıgında görünür. "Hidden" modunda modül hiç gösterilmez.

* #### Numeric Output Type Selection Mode
bilmiyorum.

* #### Description
Modül hakkında açıklama, imlecinizi modül üzerine getirdiginizde görünen açıklamadır.

* #### Keywords
Modül ekleme ekranında arama yaparken bu modülün hangi kelimeler aratıldıgında çıkacagını belirler. Her bir kelimeyi boşluk bırakarak yazın.

* #### Collapsed View Format
bilmiyorum.

* #### Can be Used for Type Conversions
bilmiyorum.

* #### Script Metadata
bilmiyorum.

* #### Input Sections
Buradan modülün kategorilerinden bölümler oluşturabilirsiniz. Oluşturdugunuz bölümler modülü kullanırken detaylar penceresinin en üstünde gösterilir. Eklediginiz her bir yeni element aşagıdaki ayarlara sahiptir,

Ayar | İçerik
:---: | :---:
Section Identifier | Oluşturulan bölümün id'si.
Section Display Name | Modülü kullanırken detaylar penceresinde gösterilecek olan isim.
Categories | Buraya bu bölümde olacak kategorilerin listesini verin.
Enabled | Bölümü aktifleştirir/deaktive eder.


## Validation

* #### Validation Rules
bilmiyorum.

## Input Parameters
Buradan modülün aldıgı inputları, daha dogrusu [ParameterMap](../Terimler%20Sözlügü#parametermap)'leri ayarlayabilirsiniz. Yine de tek bir modülde birden fazla [ParameterMap](../Terimler%20Sözlügü#parametermap) kullanımı karışık bir iş oldugu için burdaki ayarlar ile oynamanıza gerek yok.

## Output Parameters
Buradan modülün outputlarını ayarlayabilirsiniz. Yine de tek bir modülde birden fazla output kullanımı karışık bir iş oldugu için burdaki ayarlar ile oynamanıza gerek yok.
