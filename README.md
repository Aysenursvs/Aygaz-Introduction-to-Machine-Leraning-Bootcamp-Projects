**Aygaz Makine Öğrenmesi Bootcamp: Yeni Nesil Proje Kampı** 


**Supervised Project:**

Kaggle Link: https://www.kaggle.com/code/ayysenurrr/online-fraud-detection-supervised/edit

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

Kaggle Link:https://www.kaggle.com/code/ayysenurrr/online-fraud-detection-unsupervised/edit

Modeli değerlendirmek için "Silhoutte Skor"unu kullnadım.

Skor: 0.4 - Model genel olarak veri noktalarını doğru kümeleri aktarmış.

**MODELLERİN KARŞILAŞTIRILMASI**

Kullandığım veri seti supervised algoritması için daha uygun bir veri seti çünkü veri setinde sınıflandırma yapıyoruz ve supervised algoritması sınıflandırma üzerinde daha iyi çalışıyor. Model değerlendirme aşamalarında da skorlar ile supervised kNN algoritmasının unsupervised KMeans algoritmasına göre daha iyi bir performans sergilediğni sayısal olarak görmüş olduk.
