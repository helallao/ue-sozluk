# Main Material Node
<img src="../../../../Dosyalar/Materyal_Editor_Main_Material_Node.jpg">


# Bölümler

* [Attributes](#attributes)
* [Physical Material](#physical-material)
* [Material](#material)


## [Attributes]()

### Base Color
Materyalin ana rengidir, ışık yansıdıgında görünecek rengi belirler. Degerler 0-1 arasındadır. 0 siyah, 1 beyazı temsil eder.

### Metallic
Materyalin metalik olup olmayacagını belirler. Materyalin metalik olması az da olsa yansımayı etkiler. Degerler 0-1 arasındadır. 0 metalik olmayan, 1 metalik olanı temsil eder.

### Specular
Materyalin ne kadar ışık yansıtacagını belirler. Materyalin specular olması parlaklıgı da etkiler. Degerler 0-1 arasındadır. 0 hiç yansıtmamayı, 1 tam yansıtmayı temsil eder.

### Roughness
Materyalin ne kadar pürüzlü oldugunu belirler. Materyalin ne kadar pürüzlü olup olmaması materyalin yansıtma özelligini en çok etkileyen etkendir. Degerler 0-1 arasındadır. 0 pürüzssüzü (ayna gibi yansıtma), 1 pürüzlüyü (yansıtmama) temsil eder.

### Anisotropy

### Emissive Color
Emissive Color neon gibidir. Degerler 0-1 arasında degildir, istediginiz kadar arttırabilirsiniz. Base Color gibi verdiginiz rengi yansıtır ama degeri arttırdıkça neon gibi olur ve parlamaya başlar, etrafına ışık saçar. Parlaklıgı arttırıyormuşsunuz gibi.

### Opacity
Materyalin ne kadar opak oldugunu belirler. Degerler 0-1 arasındadır. 0 saydamı, 1 opagı temsil eder.

### Opacity Mask
Opacity gibidir ama ya saydam ya da opak olmak zorundadır. Yani Opacity gibi istediginiz derecede opaklık veremezsiniz. Degerler 0-1 arasındadır ama yakın olan sayıya yuvarlanır. 0 saydamı, 1 opagı temsil eder.

### Normal
Genellikle Normal Map şeklinde kullanılır. Normal, verilen degerlere göre bazı kısımları yüksek bazı kısımları alçak gösterir, yani 3d gibi, zaten bundan dolayı bazı yerlerde Height Map diye de geçer. Map diye kastedilen şey bir texture yani resimdir.

### Tangent

### World Position Offset
World Position Offset konum degiştirme daha dogrusu hareket kazandırma amaçlı kullanılır. Blueprint ile yazmak yerine materyal içinde bunu yapabilmek çok büyük kolaylık. Bu materyale sahip olan meshlerin belirli hareketler yapmasını istediginizde kullanabilirsiniz. Konum degişse bile aslında meshin gerçek konumu degişmez yani aslında World Position Offset konumu degiştirmez.

### Subsurface Color

### Custom Data 0

### Custom Data 1

### Ambient Occlusion

### Refraction

### Pixel Depth Offset

### Shading Model

### Front Material




## [Physical Material]()

## [Material]()
