# We Can No Hate - Capstone - Machine Learning

## Project Capstone Dicoding 2021

## About File
<p align=justify>Pada repository ini terdapat 5 file yaitu binary_label_with_sklearn_classification.ipynb, data_cleaning.ipynb, data.csv, dataset_clean.csv, dan readme.md. Untuk penjelasan masing-masing file yaitu sebagai berikut :</p>

  1. File binary_label_with_sklearn_classification.ipynb berisi code program metode atau model yang digunakan dalam proyek capstone.
  2. File data_cleaning.ipynb berisi code program yang digunakan untuk proses pembersihan data atau pemrosesan data. Pada akhir program terdapat code untuk menyimpan dataset yang sudah dibersihkan.
  3. File data.csv berisi dataset awal atau original yang belum dilakukan proses apa pun.
  4. File dataset_clean.csv berisi dataset yang sudah dibersihkan pada program data_cleaning.ipynb.
  5. File readme.md berisi penjelasan terhadap proyek yang dikerjakan.

## Data Understanding
<p align=justify>Dataset yang diambil berasal dari kaggle. Dataset berisi teks cuitan-cuitan pada twitter yang mengandung ujaran kebencian (hatespeech), kata-kata kasar (abusive), dan netral. Dataset terdiri dari 13 kolom yaitu 1 kolom untuk data tweet dan 12 kolom untuk data label. Untuk keterangan pada masing-masing kolom yaitu sebagai berikut :</p>

  1. Tweet : berisi cuitan twitter yang akan digunakan untuk proses analisis sentimen.
  2. HS : label untuk ujaran kebencian (hate speech) dengan nilai 0 atau 1.
  3. Abusive : label untuk kata-kata kasar (abusive) dengan nilai 0 atau 1.
  4. HS_Individual : label untuk ujaran kebencian (hate speech) yang ditargetkan secara individual atau kepada seseorang dengan nilai 0 atau 1.
  5. HS_Group : label untuk ujaran kebencian (hate speech) yang ditargetkan secara kelompok atau kepada sekelompok orang dengan nilai 0 atau 1.
  6. HS_Religion : label untuk ujaran kebencian (hate speech) yang berkaitan dengan agama dengan nilai 0 atau 1.
  7. HS_Race : label untuk ujaran kebencian (hate speech) yang berkaitan dengan ras dengan nilai 0 atau 1.
  8. HS_Physical : label untuk ujaran kebencian (hate speech) yang berkaitan dengan fisik atau disabilitas dengan nilai 0 atau 1.
  9. HS_Gender : label untuk ujaran kebencian (hate speech) yang berkaitan dengan gender atau orientasi seksual dengan nilai 0 atau 1.
  10. HS_Other : label untuk ujaran kebencian (hate speech) lainnya dengan nilai 0 atau 1.
  11. HS_Weak : label untuk ujaran kebencian (hate speech) yang bernilai lemah dengan nilai 0 atau 1.
  12. HS_Moderate : label untuk ujaran kebencian (hate speech) yang bernilai sedang dengan nilai 0 atau 1.
  13. HS_Strong : label untuk ujaran kebencian (hate speech) yang bernilai kuat dengan nilai 0 atau 1.

[Link download dataset](https://www.kaggle.com/ilhamfp31/indonesian-abusive-and-hate-speech-twitter-text "Dataset Kaggle")

## Data Preparation
Pada tahap data preparation ini melakukan beberapa tahapan agar data dapat dengan baik diimplementasikan ke dalam model, tahapan tersebut yaitu sebagai berikut :
- Preprocessing Data
  <p align=justify>Preprocessing adalah tahapan yang penting untuk dilakukan jika mengolah data, terlebih apabila data yang diolah adalah data teks. Data cuitan twitter yang disediakan adalah data apa adanya dari twitter yang masih belum diolah sama sekali. Sehingga perlu dilakukan preprocessing terhadap data tersebut agar ketika dimasukkan ke dalam model nantinya memiliki kualitas yang bagus. Beberapa proses yang dilakukan pada tahap preprocessing yaitu :</p>
  
  * Lowercase : mengubah seluruh karakter menjadi huruf kecil
  * Menghapus karakter yang tidak perlu
  * Menghapus karakter yang bukan alfabet dan numerik
  * Normalisasi kata : mengganti kata yang tidak baku, bahasa-bahasa gaul, serta singkatan menjadi kata-kata yang baku
  * Menghapus stopwords : menghapus kata-kata yang sering muncul tetapi tidak bermakna
  * Stemming : mengganti kata-kata yang berimbuhan menjadi kata dasar
  
- Memilih Fitur
  <p align=justify>Pada dataset terdapat 12 kolom label, tetapi pada proyek ini tidak dipakai keseluruhannya. Sehingga dilakukan pemilihan fitur yang ada pada dataset. Fitur yang diambil yaitu tweet, label HS dan label Abusive. Selanjutnya pada label HS dan label Abusive dilakukan penggabungan nilai dengan operator OR, sehingga dataset final terdiri dari 2 kolom yaitu kolom tweet serta kolom label hatespeech dan abusive.</p>
  
- Train Test Split
  <p align=justify>Proses selanjutnya pada data preparation yaitu train test split. Proses ini dilakukan dengan tujuan membagi data latih dan data uji sesuai dengan porsi yang diinginkan. Hal ini dilakukan agar nantinya tidak mengotori data uji dengan informasi yang kita dapat dari data latih karena data uji akan berperan sebagai data baru. Pada proyek ini train test split dibagi dengan rasio 80:20, dimana 80% dari keseluruhan data berperan sebagai data latih dan 20% sisanya berperan sebagai data uji.</p>
