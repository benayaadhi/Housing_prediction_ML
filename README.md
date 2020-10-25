# Housing prediction ML

![Image of House Prediction](https://camo.githubusercontent.com/d249d1ac904a68fbbb3cd03087e79ca3a371893c/68747470733a2f2f7777772e76616e636f757665727265616c657374617465706f64636173742e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031382f31302f44657461636865642d686f6d652d7072696365732e6a7067)
#### Di project ini, saya mencoba melakukan EDA dan prediksi Harga Rumah menggunakan machine learning.


#### Dari Datasets tersebut, saya menemukan beberapa insight yang menarik. 
### Harga Rumah tidak bisa dibilang setiap tahun meningkat, dikarenakan ternyata harga Rumah termahal sekarang dibangun di tahun 1910. Tetapi , Harga rumah mahal memang mulai banyak bermunculan dari tahun 1990.
![Houses](https://www.lushome.com/wp-content/uploads/2013/11/house-exterior-redesign-glass-addition-2.jpg)

### Rumah yang mempunyai banyak kamar, ternyata belum tentu dia mempunyai harga jual yang mahal, rata-rata orang yang mempunyai harga rumah termahal, mempunyai kamar hanya kurang lebih 5 kamar saja.

### Dari Datasets ini, bisa disimpulkan bahwa rata2 kamar didalam suatu rumah adalah kurang lebih 2-3 kamar. 
![Image Bedrooms](https://hips.hearstapps.com/clv.h-cdn.co/assets/17/08/1487972426-cool-calm-collected-bedroom-1016.jpg)

## Machine Learning

#### Ada beberapa Base yg saya gunakan dalam prediksi Harga Rumah ini,
- Linear Regression
- Polynomial 
- XGB Regressor

#### Setelah menggunakan Base, bisa disimpulkan bahwa Base XGBoost mempunyai nilai r2 yang paling tinggi di angka 0.74 / 74%. 
#### Kemudian saya melakukan Hyper Parameter Tuning terhadap base yang mempunyai nilai r2 paling tinggi yaitu XGBoost 

### Berikut adalah MAE,MSE,RMSE dan R2 Score untuk masing-masing Base dan XGB yang telah dilakukan Hyper Parameter Tuning

|      |       LinReg |   Polynomial |          XGB |     XGB Tune |
|-----:|-------------:|-------------:|-------------:|-------------:|
|  MAE | 1.376473e+05 | 1.258258e+05 | 1.183299e+05 | 1.148515e+05 |
|  MSE | 4.406999e+10 | 3.445335e+10 | 3.257275e+10 | 2.959628e+10 |
| RMSE | 2.099285e+05 | 1.856161e+05 | 1.804792e+05 | 1.720357e+05 |
|   R2 | 6.566701e-01 | 7.315892e-01 | 7.462401e-01 | 7.694285e-01 |


#### Dari Tabel diatas, bisa disimpulkan bahwa data test mendapatkan hasil 76,9%. Angka tersebut merupakan angka yang cukup bagus dikarenakan Train nya mendapatkan nilai 89%. 
#### Tingkat Error (MAE) adalah 21%.
