# Parameters
<img src="../../../Dosyalar/Niagara_Module_Editor_Parameters.jpg">


Buradan yazdıgınız Niagara modül'ünün içindeki parametreleri görebilirsiniz. Burası oluşturulan ve kullanılan parametreleri gösterir ve yeni parametreleri de buradan oluşturabilirsiniz. Bu parametreleri kullanabilmek için modülün nerede kullanıldıgı da önemli, mesela eger sistem parametresi ayarlamak istiyorsanız bu modülü ya [System Spawn](../../Niagara%20Editörü/Graph#system-spawn) ya da [System Update](../../Niagara%20Editörü/Graph#system-update) kategorisinde kullanmalısınız. Eger bu kategoride kullandıysanız parametreleri de ayarlayabilirsiniz.

* Parametre türlerine Niagara Editörü'nün [Parametreler](../../Niagara%20Editörü/Parameters#parametre-türleri) bölümünden ulaşabilirsiniz

<br>
<br>


## System Attributes
Sistem parametreleri. Eger sistem parametresi ayarlamak istiyorsanız bu modülü ya [System Spawn](../../Niagara%20Editörü/Graph#system-spawn) ya da [System Update](../../Niagara%20Editörü/Graph#system-update) kategorisinde kullanmalısınız.

## Emitter Attributes
Emitter parametreleri. Eger emitter parametresi ayarlamak istiyorsanız bu modülü ya [Emitter Spawn](../../Niagara%20Editörü/Graph#emitter-spawn) ya da [Emitter Update](../../Niagara%20Editörü/Graph#emitter-update) kategorisinde kullanmalısınız.

## Particle Attributes
Parçacık parametreleri. Eger parçacık parametresi ayarlamak istiyorsanız bu modülü ya [Particle Spawn](../../Niagara%20Editörü/Graph#particle-spawn) ya da [Particle Update](../../Niagara%20Editörü/Graph#particle-update) kategorisinde kullanmalısınız.

## Module Inputs
Modül'ün aldıgı inputlar. Modül inputu olan parametreleri illaki buradan oluşturmak zorunda degilsiniz. [Parameter Map Get](../Nodlar#parameter-map-getmap-get) nodunun "Make New" kategorisini kullanarak da oluşturabilirsiniz.

## Static Switch Inputs
Modül'ün içinde kullanılan [Static Switch](../Nodlar#static-switch) nodlarının default degerleri buradan ayarlayabilirsiniz.

## Module Locals
Modül'ün içinde kullanılan local parametreler. Bunları degişken gibi düşünebilirsiniz. Bir kerelik kullanılırlar, eger degerini başka bir parametre üzerine kaydetmezsiniz yok olurlar. 

## Module Outputs
Modül'ün output olarak verdigi parametreler. Bu parametreler [Module Outputs](../../Niagara%20Editörü/Parameters#module-outputs) kategorisine kaydolur.

## Engine Provided
[Engine Provided](../../Niagara%20Editörü/Parameters#engine-provided) parametreleri.

## Stack Context Sensitive
[Stack Context Sensitive](../../Niagara%20Editörü/Parameters#stack-context-sensitive) parametreleri.

## Stage Transients
[Stage Transient](../../Niagara%20Editörü/Parameters#stage-transients) parametreleri.

## Niagara Parameter Collection
Bu kategori [Niagara Parameter Collection](../../../Assetler/Niagara%20Parameter%20Collection) assetinden parametre almanıza yarar.

## Data Instance
Sadece tek bir parametresi vardır: "DataInstance.Alive", bu parametre parçacıgın yaşayıp yaşamadıgını gösterir.




# Parametre Ayarları

Buradaki ayarlar Niagara Modül Editöründe parametreler penceresinde herhangi bir parametreyi seçtiginiz zaman [Selected Details](../Selected%20Details) penceresinde açılan ayarlardır.


## Default Value

* #### Default Mode
Parametrenin degeri için kullanılacak modu belirtir. 5 modu vardır,

Mod | İşlem
:---: | :---:
Definition | Sadece [Niagara Parameter Definitions](../../../Assetler/Niagara%20Parameter%20Definitions#niagara-parameter-definitions) assetinden alınmış parametrelerde olan bir seçenektir.
Value | Parametrenin başlangıç (default) degerini ayarlarsınız.
Binding | Parametrenin degerini başka bir parametreye baglayabilirsiniz.
Custom | Parametrenin degerini kod yazarak script'in içinde kendiniz belirlersiniz. Bu ayarı seçtiginiz zaman kod içinde bu parametreyi aldıgınız [Parameter Map Get(Map Get)](../Nodlar#parameter-map-getmap-get) nodunun üzerinde bu parametre için bir input pin'i oluşturulur.
Fail if Previously Not Set | Eger parametrenin degeri daha önceden ayarlanmadıysa hata verir.


* #### Default Value
Sadece "Default Mode" ayarı "Value" modundayken vardır. Default degeri belirtir.

* #### Default Binding
Sadece "Default Mode" ayarı "Binding" modundayken vardır. Parametrenin degeri hangi parametreden alacagını belirtir.

* #### Description
Parametre için açıklama.

* #### Category Name
Parametrenin ait oldugu kategori ismi.

* #### Advanced Display
Bu ayar sadece input olan parametrelerde işe yarar. İnputun Niagara Editöründe [Selection](../../Niagara%20Editörü/Selection) penceresinde gelimiş inputları açınca görünecegini belirtir.

* #### Display in Overview Stack
Bu ayar sadece input olan parametrelerde işe yarar.

* #### Inline Parameter Sort Priority
Bu ayar sadece input olan parametrelerde işe yarar.

* #### Inline Parameter Color Override
Bu ayar sadece input olan parametrelerde işe yarar.

* #### Inline Parameter Bool Override
Bu ayar sadece input olan parametrelerde işe yarar.

* #### Editor Sort Priority
bilmiyorum.

* #### Inline Edit Condition Toggle
bilmiyorum.

* #### Edit Condition
bilmiyorum.

* #### Visible Condition
bilmiyorum.

* #### Property Metadata
bilmiyorum.

* #### Parent Attribute
bilmiyorum.

* #### Alternate Aliases For Variable
bilmiyorum.








