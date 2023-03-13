# Stats
<img src="../../Dosyalar/Materyal_Editor_Stats.jpg">

Burada materyalinizin ne kadar kompleks oldugunu, sistem (ekran kartı) için ne kadar pahalı (expensive) ve ya ucuz (cheap) oldugunu, kısacası grafik kalitesini, komplekslik seviyesini görebilirsiniz.

## [Base Pass Shader]()

Burdaki instruction sayısı, sistemin (ekran kartı) materyal için ne kadar işlem gerçekleştirdigini gösterir. İşlem sayısı materyalin tam olarak ne kadar pahalı oldugunu tam dogru göstermeyebilir çünkü instruction sayısı fazla olsa bile, mesela tek bir instruction diger instruction'lara göre 10 kat daha uzun sürüyor olabilir, bu da onu 10 tane instruction degerinde yapar, bunu Unreal Engine dersleri anlatan [birinden](https://youtu.be/D8E47BJOE6E?t=192) duydum ama ne kadar etkileyeceginden emin degilim. Instruction sayısı materyalin pahalılıgını ölçmek için kullanılan en yaygın yöntemdir.


## [Base Pass Vertex Shader]()

Base Pass Shader ile aynı şey ama [vertexler](../../Editörler/Materyal%20Editörü/Terimler%20Sözlügü#vertex) için, ne ifade ettigini bilmiyorum.
