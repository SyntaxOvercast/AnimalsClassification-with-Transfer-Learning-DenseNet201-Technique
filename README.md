##Penerapan deep learning untuk klasifikasi gambar hewan##
Dataset yang digunakan adalah bersumber dari Kaggle antobenedetti/animals
dengan karakteristik dataset sebagai berikut :
Labels
cat         3037
elephant    2992
lion        2936
dog         2927
horse       2754
Name: count, dtype: int64
Total gambar after filter: 14646
Total kelas unik after filter: 5

Arsitektur :
Model ini menggunakan arsitektur transfer learning berbasis DenseNet201 sebagai feature extractor yang diikuti oleh 6 layer tambahan (Conv2D, BatchNormalization, LeakyReLU, GlobalAveragePooling2D, Dense, Dropout, dan Dense output) untuk melakukan klasifikasi multi-kelas menggunakan softmax.

Evaluasi model :
Training Set
loss: 0.4858 - accuracy: 0.9694 - 
Validation Set
val_loss: 0.4725 - val_accuracy: 0.9665 - lr: 1.0000e-04
Testing set 
loss: 0.4741 - accuracy: 0.9696

Accuracy : 0.9696
Precision: 0.9702
Recall   : 0.9696
F1-score : 0.9696


