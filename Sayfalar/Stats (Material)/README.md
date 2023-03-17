# Stats
<img src="../../Dosyalar/Materyal_Editor_Stats.jpg">

Burada materyalinizin ne kadar kompleks oldugunu, sistem (ekran kartı) için ne kadar pahalı (expensive) ve ya ucuz (cheap) oldugunu, kısacası grafik kalitesini, komplekslik seviyesini görebilirsiniz. (Resmin çogu boş oldugu için kırpılmıştır.)



## [Base pass shader]()

Burdaki instruction sayısı, sistemin (ekran kartı) materyal için ne kadar işlem gerçekleştirdigini gösterir. İşlem sayısı materyalin tam olarak ne kadar pahalı oldugunu tam dogru göstermeyebilir çünkü instruction sayısı fazla olsa bile, mesela tek bir instruction diger instruction'lara göre 10 kat daha uzun sürüyor olabilir, bu da onu 10 tane instruction degerinde yapar. Sonuç olarak instruction sayısı materyalin pahalılıgını ölçmek için kullanılan en yaygın yöntemdir ama tahminidir.



## [Base pass vertex shader]()

Base Pass Shader ile aynı şey ama [vertexler](../../Editörler/Materyal%20Editörü/Terimler%20Sözlügü#vertex) için, ne ifade ettigini bilmiyorum.



## [MaxSampler]()




## [Texture samplers]()

Toplamda kullanılan [Texture Sampler](../../Editörler/Materyal%20Editörü/Nodlar#texturesample-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F) sayısını verir. En başta 2 dir, her [Save](../../Editörler/Materyal%20Editörü/Toolbar#save-butonu) yapmaya 1 artar, sanırım sonuç olarak verilen texture da bir "Texture Sampler" dolayısıyla hiç "Texture Sampler" kullanmasanız bile 2 + 1 = 3 oluyor. Tabi bu benim durumuma özel, daha farklı sebeplerden dolayı daha farklı sonuçlar alabilirsiniz, karşılaştıkça buraya yazıcam.



## [Texture Lookups (Est.)]()

[VS ve PS](../../Editörler/Materyal%20Editörü/Terimler%20Sözlügü#vertex-shader-ve-pixel-shader) için "Texture Lookup" sayısını yani bir texturenin hesaplamaları yapılırken UVs koordinatına kaç defa bakıldıgı, yani kaç kere işlendigini verir.




## [User interpolators]()

Sanırım kullanılan [VertexInterpolator](../../Editörler/Materyal%20Editörü/Nodlar#vertexinterpolator-) noduna baglı olarak bilgiler döndürüyor. Yani Vertex Shader ile interpolate olan işlemler sayısı.




## [Shader Count]()
