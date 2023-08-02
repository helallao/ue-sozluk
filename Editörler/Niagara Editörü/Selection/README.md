# Selection
<img src="../../../Dosyalar/Niagara_Editor_Selection.jpg">


Details penceresi gibidir. [Graph](../Graph) üzerinde seçtiginiz şeyin ayarlarını gösterir. Niagara Editör'ünde [Graph](../Graph) üzerinden çok bir şey yapmıyoruz, neredeyse %99 Selection penceresini kullanıcaz, dolayısıyla her şeyi burda anlatıcam. Seçtiginiz modül ile ilgili inputlar burada görünür. Üstte kategorilerden birini seçerek sadece o kategoriye ait inputları görebilirsiniz.

<img src="../../../Dosyalar/Niagara_Editor_Selection_2.png">

İnputların en sagındaki butondan inputu en baştaki degerine yani default degere geri alabilirsiniz. Onun bi solundaki buton ile de input ile ilgili işlemler yapabilirsiniz. Mesela inputu bir [dinamik inputa]() baglayabilirsiniz ve ya bir parametreye baglayabilirsiniz. Eger zaten baglıysa "New Local Value" ile kendiniz deger yazabilirsiniz. "New Expression" ile [hlsl](https://en.wikipedia.org/wiki/High-Level_Shader_Language) kodu bile yazabilirsiniz.

<img src="../../../Dosyalar/Niagara_Editor_Selection_3.png">

En alttaki genişlet butonu ile sadece bu modül için gelişmiş inputları açabilirsiniz.

<img src="../../../Dosyalar/Niagara_Editor_Selection_4.png">

Sag üstteki 3 çizgiden "Show All Advanced" ayarı ile gelişmiş inputları şu an oldugunuz Emitter/System'ın bütün modülleri için açabilirsiniz. Yani "Show All Advanced" ayarı açıldıgı zaman eger Emitter üzerindeyseniz Emitter'daki bütün modüllerde, System üzerindeyseniz System'daki bütün modüllerde gelişmiş seçenekleri gösterir. Dolayısıyla bu ayarı birden fazla kez açmanız gerekecek.

<img src="../../../Dosyalar/Niagara_Editor_Selection_5.png">

"Show Parameter Reads" ve "Show Parameter Writes" ayarları ile modülün hangi parametreleri okudugunu ve hangi parametreleri degiştirdigini görebilirsiniz.

<img src="../../../Dosyalar/Niagara_Editor_Selection_6.png">

"Show Only Issues" ayarının tam olarak nasıl çalıştıgını bilmiyorum. Açınca modüller siliniyor, geri kapatsanız bile karışıyor. Yani gereksiz, kullanmayın.


# Dinamik Inputlar
