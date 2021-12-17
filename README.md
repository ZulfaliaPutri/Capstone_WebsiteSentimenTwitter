# We Can No Hate - Capstone - Machine Learning

## Project Capstone Dicoding 2021

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
- Train Test Split
