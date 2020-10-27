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

#### Setelah menggunakan Base, bisa disimpulkan bahwa Base XGBoost mempunyai nilai r2 yang paling tinggi di angka 0.89 / 89%. 
#### Kemudian saya melakukan Hyper Parameter Tuning terhadap base yang mempunyai nilai r2 paling tinggi yaitu XGBoost 

### Berikut adalah MAE,MSE,RMSE dan R2 Score untuk masing-masing Base dan XGB yang telah dilakukan Hyper Parameter Tuning

|      |       LinReg |   Polynomial |          XGB |     XGB Tune |
|-----:|-------------:|-------------:|-------------:|-------------:|
|  MAE | 1.233683e+05 | 1.011974e+05 | 6.773873e+04 | 6.517926e+04 |
|  MSE | 3.751736e+10 | 2.455409e+10 | 1.401585e+10 | 1.258816e+10 |
| RMSE | 1.936940e+05 | 1.566975e+05 | 1.183885e+05 | 1.121970e+05 |
|   R2 | 7.077188e-01 | 8.087099e-01 | 8.908087e-01 | 9.019312e-01 |


#### Dari Tabel diatas, bisa disimpulkan bahwa data test mendapatkan hasil 90.1%. Angka tersebut merupakan angka yang cukup bagus dikarenakan Train nya mendapatkan nilai 96%. 
#### Tingkat Error (MAE) adalah 12%.
