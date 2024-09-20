# Bitcoin Veri Analizi ve Kümeleme ile Regresyon Modelleri

Bu projede iki farklı yaklaşımla Bitcoin fiyat verileri üzerinde analiz ve modelleme çalışmaları yapılmaktadır:

1. **K-Means Algoritması ile Kümeleme**
2. **Linear Regression Modeli ile Tahmin**

## 1. K-Means Algoritması ile Kümeleme

### Veri Seti
Bu proje, Bitcoin fiyat verilerini kullanarak K-Means kümeleme algoritmasını uygulamaktadır. Kullanılan veri seti dakikalık Bitcoin fiyat verilerini içermektedir. Verilerde eksik ya da sonsuz değerler uygun şekillerde işlenmiş ve kümeleme için dört özellik kullanılmıştır: `Open`, `High`, `Low` ve `Volume`.

### K-Means Kümeleme

K-Means algoritması ile veriler üç kümeye ayrılmıştır. Aşağıdaki görselde K-Means ile oluşturulan kümelerin bir örneklemesi gösterilmektedir:

![1](https://github.com/user-attachments/assets/01d647d6-110b-4926-9e23-83476667649a)

### Elbow Yöntemi ve Inertia Değeri

En uygun küme sayısını bulmak için Elbow yöntemi kullanılmıştır. Aşağıdaki grafikte, küme sayısına göre inertia değerinin nasıl değiştiğini görebilirsiniz:

![1](https://github.com/user-attachments/assets/030b7009-0058-4048-ac91-cef576a5f649)


---

## 2. Linear Regression Modeli ile Tahmin

### Veri Seti
Bu bölümde, aynı veri setini kullanarak Bitcoin kapanış fiyatlarını tahmin etmek için bir lineer regresyon modeli oluşturulmuştur. Model `Open`, `High`, `Low` ve `Volume` sütunlarını kullanarak `Close` fiyatını tahmin etmeye çalışmaktadır.

### Model Performansı

Modelin performansı Mean Squared Error (MSE) ve R2 Score metrikleri ile ölçülmüştür. Aşağıda, modelin tahminlerinin gerçek değerlerle olan ilişkisi ve tahmin hatalarının dağılımı gösterilmektedir:

#### Modelin Tahmin Performansı (İlk Model)

![1](https://github.com/user-attachments/assets/d5ec2e52-2f94-4c55-8a5c-878f092ebe3c)


#### Tahmin Hatalarının Dağılımı

![2](https://github.com/user-attachments/assets/048af0b4-818e-48a4-a0b2-fbab863a5d55)


### Model Tuning (GridSearch ile En İyi Parametreler)

Modelin hiperparametrelerini GridSearchCV ile optimize ettikten sonra, yeni tahmin sonuçları ve hata dağılımı aşağıdaki gibi olmuştur:

#### İyileştirilmiş Modelin Tahmin Performansı

![3](https://github.com/user-attachments/assets/72191241-e91f-42dc-9f8b-24bf298858a5)


#### İyileştirilmiş Modelin Hata Dağılımı

![4](https://github.com/user-attachments/assets/f01b9d82-b89a-469e-8c91-5c28250613a7)


---

## Kullanılan Kütüphaneler ve Kurulum

Bu projelerde aşağıdaki Python kütüphaneleri kullanılmıştır:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `sklearn`

##Linkler
- https://www.kaggle.com/code/zekiakkan/btc-g-zetimsiz1
- https://www.kaggle.com/code/zekiakkan/btc-gozetimli
