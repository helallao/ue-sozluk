## Force ve Velocity

Velocity parçacıgın üzerindeki hız degerini ifade ederken, force çekim/itim gücünü ifade eder. Bu ikisi iki ayrı etki olarak hesaplanır.


## Local ve World Coordinate Space

Bunun hakkında [şöyle](https://youtu.be/KEJx7ZX25gY) bi video var, isterseniz onu da izleyebilirsiniz. Local ve World arasında 2 fark vardır, World space kullanılırken eger level editörünüzde niagara objesini hareket ettirirseniz spawn olmuş parçacıklar da niagara objesi ile beraber hareket etmez yani spawn olduktan sonra niagara objesine baglı degillerdir. Local space kullanırken bunun tam tersi olur, eger niagara objesini hareket ettirirseniz spawn olmuş parçacıklar da niagara objesine baglı olarak hareket eder. Local ve World space arasındaki ikinci fark ise, World space kullanırken niagara objesinin scale (boyut) degerini degiştirseniz bile niagara sistemindeki hiçbir boyut degeri degişmez. Local space kullanırken bunun tam tersi olur, niagara objesinin scale (boyut) degerini istediginiz gibi degiştirebilirsiniz. Ayrıca emitter ayarlarından Coordinate Space seçmek yerine, modüller üzerindeki ayarlardan da seçebilirsiniz. Birçok modülde "Coordinate Space" inputu var ve bunları kullanıp her modül için ayrı ayrı Coordinate Space'ler kullanabilirsiniz. Bunun hakkında bir [video](https://youtu.be/cJYWzyvSaXY).


## SpawnGroup

Çok kullanışlıdır, bir çok modül'de grup numarasına göre işlem yapabiliyorsunuz. Grup numarası vermek sanki id vermek gibi işlev görüyor. Sadece belirli parçacıklar üzerinde işlemler yapabiliyorsunuz. SpawnGroup'u kullanmak için Emitter'ın [Requires Persistent IDs](../Graph#requires-persistent-ids) ayarı açık olmalıdır.


## Wildcard Filtering

Wildcard bir nevi unreal engine'de kullanılan [regex'dir](https://tr.wikipedia.org/wiki/D%C3%BCzenli_ifade) ama sadece "\*" ve "?" den oluşur. Diyelim ki "Ali veli 49 50" yazısı için bir wildcard yazıcaz. "\*" işareti, kullandıgımız yerin öncesinde ve sonrasında her karakter her sayıda olabilir demektir. Mesela "Ali \*" wildcard'ını kullandıgımız zaman bu wildcard yazımız ile eşleşir çünkü "\*" işaretinden sonra her karakter her sayıda olabilir demektir. Ayrıca "\*" işaretini kullandıktan sonra herhangi bir yazı yazarsanız "\*" işareti o yazıyla karşılaşana kadar çalışır, karşılaştıgı zaman sizin yazdıgınız kısımdan devam eder, yani mesela "Ali * 49 50" yazarsanız bu wildcard yazımız ile eşleşir ama "Ali * 49 48" yazarsanız bu wildcard yazımız ile eşleşmez çünkü "\*" işareti 49 ile karşılaşana kadar gider, karşılaştıktan sonra bizim yazdıgımız şekilde devam eder ve "48" ile "50" birbiriyle eşleşmez. "?" işareti ise, kullandıgımız yerde herhangi bir karakter sadece bir kere olabilir demektir. Mesela "Ali veli ?9 50" wildcard'ını kullandıgımız zaman bu wildcard yazımız ile eşleşir çünkü "?" işareti herhangi bir karakterin yerini tutabilir.
