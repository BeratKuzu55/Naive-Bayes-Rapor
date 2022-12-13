# Naive-Bayes-Rapor

Naïve Bayes sınıflandırma algoritması, adını Matematikçi Thomas Bayes’den alan bir sınıflandırma/ kategorilendirme algoritmasıdır. Naïve Bayes sınıflandırması olasılık ilkelerine göre tanımlanmış bir dizi hesaplama ile, sisteme sunulan verilerin sınıfını yani kategorisini tespit etmeyi amaçlar.

</br>

Naïve Bayes sınıflandırmasında sisteme belirli bir oranda öğretilmiş veri sunulur (Örn: 100 adet). Öğretim için sunulan verilerin mutlaka bir sınıfı/kategorisi bulunmalıdır. Öğretilmiş veriler üzerinde yapılan olasılık işlemleri ile, sisteme sunulan yeni test verileri, daha önce elde edilmiş olasılık değerlerine göre işletvilir ve verilen test verisinin hangi kategoride olduğu tespit edilmeye çalışılır.

<img src="https://miro.medium.com/max/640/1*DrLi-HXAtSw7NHkQPB6Xlw.webp">
</br>
P ( A | B ) = B olayı gerçekleştiğinde A olayının gerçekleşme olasılığı
P ( A ) = A olayının gerçekleşme olasılığı
P ( B | A ) = A olayı gerçekleştiğinde B olayının gerçekleşme olasılığı
P ( B ) = B olayının gerçekleşme olasılığı
</br></br>
<h3> İşleme Şekli </h3>
  Arkadaşlarımızdan ailemizden ve çeşitli şirketlerden e-postalar aldığımızı düşünelim ailemizden ve arkadaşlarımızdan gelen e-postaları dğier reklam kampanya tarzı e-postalardan ayırmak istiyoruz bunun için öncelikle bir veri seti kullanıp olasılık hesabı yapmamız gerekiyor.
</br></br>
  Örneğin 8 tane normal 4 tane gereksiz mesajın olduğu bir veri setini kullanıyoruz ve normal mesajlarda 10 adet x , 5 adet y , 1 adet z kelimesi var gereksizlerde ise 2 x , 1 y ve 10 z kelimesi olsun.
</br></br>
  Sonrasında xxy içeren bir mesajın hangi klasörde olacağını bulmak istedğimizi düşünelim bu durumda normal klasörde olma ihtimali için (gelen mesajın normal olma olasılığı) * (x kelimesinin normal mesajda olma olsılığının karesi) * (y mesajın normal mesajda olma olasılığı) ile sonuç elde ederiz
</br>
  Sonrasında aynı işlemi gereksiz mesaj olasılıkları ile de yapıp bulduğumuz sonuçları karşılaştırırz hangi olasılık daha yüksek ise mesajı o klasöre koyarız
Bu messaj xxy den oluştuğundan ve x ile y nin olasılıkları gerekli klasörde yüksek olduğundan muhtemelen gerekli bir mesaj olarak tahmin edilecektir eğer mesajımız zzzy gibi bir mesaj olsaydı bunun çok daha yüksek ihtimalle gereksiz mesaj klasöründe olacağını öngörebiliriz. 
</br></br>
  Buraya kadar olan kısmı bayes teoremiydi
</br></br>
  Biz bu sınıflandırmayı yaparken herhangi bir sıralamyı göz önünde bulundurmadık yani mesajın xxy olması durumuyla yxx olması bizim olasılığımızı etkilemediğinden biz bu şekildeki sınıflandırmaya Naive Bayes diyoruz 
</br>
    Çeşitleri

<ul>
<li>Multinomial Naive Bayes:
Bu çoğunlukla belge sınıflandırma problemi için kullanılır, yani bir belgenin spor, politika, teknoloji vb. kategorisine ait olup olmadığı. Sınıflandırıcının kullandığı özellikler / öngörücüler belgede bulunan kelimelerin sıklığıdır.
  </li>
  <li>
Bernoulli Naive Bayes:
Bu, multinomial saf naive bayese benzer, ancak tahmin ediciler boole değişkenleridir. Sınıf değişkenini tahmin etmek için kullandığımız parametreler, örneğin metinde bir kelime olduğunda veya olmasa da, sadece evet veya hayır değerlerini alır.
  </li>
  <li>
Gauss Naive Bayes:
Tahmin ediciler sürekli bir değer aldıklarında ve ayrık olmadıklarında, bu değerlerin bir gauss dağılımından örneklendiğini varsayıyoruz.
  </li>
  </ul>


</br>
Naive Bayes Sınıflandırıcısının Avantajları
</br>
Her özellik birbirinden bağımsız kabul edildiği için logistic regresyon gibi modellerden daha iyi performans gösterebilir.
Az veriyle iyi işler başarabilir.
Sürekli ve kesikli veriler ile kullanılabilir.
Yüksek boyutlu verilerde iyi çalışabilir.
</br></br>
Naive Bayes Sınıflandırıcısının Dezavantajları</br>
Özellikler birbirinden bağımsız varsayılarak işlem yapıldığı için değişkenler arası ilişkiler modellenemez.
Sıfır olasılık problemi ile karşı karşıya kalabilirsiniz. Sıfır olasılık istediğimiz örneğin veri setinde hiç bulunmaması durumudur.Yani herhangi bir işleme alındığında sonucu sıfır yapacaktır. Bunun için en basit yöntem tüm verilere minimum değer ekleyerek (genellikle 1) bu olasılık ortadan kaldırılabilir. Bu duruma Laplace kullanılarak tahminleme de denmektedir.
</br></br>
<h3>KAYNAKÇA</h3>
https://kodedu.com/2014/05/naive-bayes-siniflandirma-algoritmasi/

https://medium.com/@ekrem.hatipoglu/machine-learning-classification-naive-bayes-part-11-4a10cd3452b4#:~:text=Naive%20Bayes%20Classifier&text=lazy%20(%20tembel%20)%20bir%20%C3%B6%C4%9Frenme%20algoritmas%C4%B1d%C4%B1r,verisiyle%20%C3%A7ok%20ba%C5%9Far%C4%B1l%C4%B1%20i%C5%9Fler%20%C3%A7%C4%B1kartabilir.

https://youtu.be/O2L2Uv9pdDA
https://devhunteryz.wordpress.com/2019/12/02/naive-bayes-siniflandirici/
https://www.datasciencearth.com/algorithm-naive-bayes-classifier/


