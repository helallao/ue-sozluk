# Stats
<img src="../../../Dosyalar/Materyal_Editor_Stats.jpg">

Burada [materyalinizin](../../../Assetler/Material) ne kadar kompleks oldugunu, sistem (ekran kartı) için ne kadar pahalı (expensive) ve ya ucuz (cheap) oldugunu, kısacası grafik kalitesini, komplekslik seviyesini görebilirsiniz. (Resmin çogu boş oldugu için kırpılmıştır.)



## [Base pass shader]()

Burdaki instruction sayısı, sistemin (ekran kartı) materyal için ne kadar işlem gerçekleştirdigini gösterir. İşlem sayısı materyalin tam olarak ne kadar pahalı oldugunu tam dogru göstermeyebilir çünkü instruction sayısı fazla olsa bile, mesela tek bir instruction diger instruction'lara göre 10 kat daha uzun sürüyor olabilir, bu da onu 10 tane instruction degerinde yapar. Yani instruction sayısı materyalin pahalılıgını ölçmek için kullanılan en yaygın yöntemdir ama tahminidir. "Base pass shader" ın farklı farklı durumlarda kaç instruction sayısına sahip oldugunu da Stats penceresinde görebilirsiniz, bunların hepsi "Base pass" şeklinde başlıyor.




## [MaxSampler]()




## [Texture samplers]()

Toplamda kullanılan [Texture Sampler](../Nodlar#texturesample-%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F%EF%B8%8F) sayısını verir. En başta 2 dir, her [Save](../Toolbar#save-butonu) yapmaya 1 artar, sanırım sonuç olarak verilen texture da bir "Texture Sampler" dolayısıyla hiç "Texture Sampler" kullanmasanız bile 2 + 1 = 3 oluyor. Tabi bu benim durumuma özel, daha farklı sebeplerden dolayı daha farklı sonuçlar alabilirsiniz, karşılaştıkça buraya yazıcam.



## [Texture Lookups (Est.)]()

[VS ve PS](../Terimler%20Sözlügü#vertex-shader-ve-pixel-shader) için "Texture Lookup" sayısını yani bir texturenin hesaplamaları yapılırken UVs koordinatına kaç defa bakıldıgı, yani kaç kere işlendigini verir.




## [User interpolators]()

Sanırım kullanılan [VertexInterpolator](../Nodlar#vertexinterpolator-) noduna baglı olarak bilgiler döndürüyor. Yani [Vertex Shader](../Terimler%20Sözlügü#vertex-shader-ve-pixel-shader) ile interpolate olan işlemler sayısı.




## [Shader Count]()




# Kaynaklar
* [Stats](https://docs.unrealengine.com/5.1/en-US/unreal-engine-material-editor-ui/#statspanel) - Stats Panel, Unreal Engine'in kendi dökümanı
