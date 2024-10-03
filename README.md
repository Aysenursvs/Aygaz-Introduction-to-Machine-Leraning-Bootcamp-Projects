**Aygaz Makine Öğrenmesi Bootcamp: Yeni Nesil Proje Kampı** 

 Bu proje kampı makine öğrenmesine girişi konu alan bir bootcmap. Bootcamp süresince bizden iki tane proje geliştirilmemiz istendi: Supervised ve Unsupervised. Bu github reposu proje boyunca geliştirdiğim iki proje ile ilgili. Projelerde bizden EDA aşaması, algoritma seçimi ve hiperparametre optimizasyonu gibi konulara yer vermemiz istendi.

 Readme dosyasında projenin son çıktıları yer alıyor.(Projeler ile ilgili teknik detaylar ve veri seti ilgili teknik, görsel detaylar repodaki notebooklarda yer alıyor)

 Supervised Projesinde KNeighborsClassifier algoritmasını, Unsupervised Projesinde KMeans algoritmasını kullandım.

 Projeleri kaggldan bulduğum bir veri seti üzerinde geliştirdim. İki projede de aynı veri setini kullandım.

 **VERİ SETİ**

 Online ödemelerdeki dolandırıcılık tespiti ile ilgili bir veri seti kullandım projelerimde. Veri setim 6362620 veri noktası içeriyor. Float, integer ve object olmak üzere üç veri tipi bulunduruyor.

 Veri setimde yer alan özellikler: step,	amount,	oldbalanceOrg,	newbalanceOrig,	oldbalanceDest,	newbalanceDest,	isFraud,	isFlaggedFraud

 Supervised projesinde bu veri setinde isFraud kısmını sınıflandırma ile tespit etmeye çalıştım.

 Unsupervised projesinde ise bu işelemi kümeleme yaparak yaptım. Küme merkezlerini belirledim, sonra optimize ettim.

**SON ÇIKTILAR**

**Supervised Project:**

Kaggle Link: https://www.kaggle.com/code/ayysenurrr/online-fraud-detection-supervised

Accuracy Score - 0.9994315758812146

Confision Matrix - 

[[1906054     297]
 
 [    788    1647]]

True Pozitive(TP):1906054 - Model doğru bir şekilde negatif değerleri tahmin etti.

True Negative(TN):1647 - Model doğru bir şekilde pozitif değerleri tahmin etti.

False Pozitive(FP):788 - Model yanlış bir şekilde negatif değerleri tahmin etti.

False Negative(FN):297 - Model yanlış bir şekilde pozitif değerleri tahmin etti.

NOT: 0 = Not Fraud , 1 = Fraud. Negatif değer Not Fraud değeri ve veri setimizde not fraud çoğunlukta.

Yaptığım model negatif sınıflar için gayet iyi çalışıyor ama pozitif sınıflarda biraz sıkıntı yaşıyor.


**Unsupervised Project:**

Kaggle Link: https://www.kaggle.com/code/ayysenurrr/online-fraud-detection-unsupervised

Modeli değerlendirmek için "Silhoutte Skor"unu kullnadım.

Skor: 0.4 - Model genel olarak veri noktalarını doğru kümeleri aktarmış.

**MODELLERİN KARŞILAŞTIRILMASI**

Kullandığım veri seti supervised algoritması için daha uygun bir veri seti çünkü veri setinde sınıflandırma yapıyoruz ve supervised algoritması sınıflandırma üzerinde daha iyi çalışıyor. Model değerlendirme aşamalarında da skorlar ile supervised kNN algoritmasının unsupervised KMeans algoritmasına göre daha iyi bir performans sergilediğni sayısal olarak görmüş olduk.
