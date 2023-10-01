# Mini-Project

## Latar Belakang
Project data wrangling rekap data kuisioner survey terkait minat program materi belajar dari user.
Kuisioner diberikan kepada user untuk memilih materi belajar yang disukai beserta informasi terkait metode belajar dan harga program.
Pilihan user kemudian dikumpulkan pada file csv untuk dianalisis dan diambil kesimpulan untuk program prioritas.

## Tahapan Pengolahan Data
1. Import library & data
   ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/part%201%20import%20library%20&%20data.png?raw=true)
   
3. Eksplorasi data
   ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/part%202%20eksplorasi%20data.png?raw=true)

   ### Explanation
   berdasarkan hasil eksplorasi terhadap 2 hasil survey tanpa ads dan dengan ads dapat dilihat banyaknya jumlah data yang diperoleh. Dalam hal in survey berhasil mendapatkan data yang lebih banyak yaitu 229         baris yang mengindikasikan ada 229 user yang berpartisipasi dalam survey, sementara itu survey tanpa ads hanya bisa mengumpulkan 56 data user.
   
5. Concate 2 table
   ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/part%203%20concat%202%20table.png?raw=true)
   
7. Cleaning data
  ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/part%204_1%20cleaning%20data.png?raw=true)
  ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/part%204_2%20cleaning%20data.png?raw=true)

  ### Explanation
  Membersihkan data dari user yang menjawab D bersamaan dengan jawaban lain, user yang memberikan jawaban seperti ini akan dianggap tidak valid dan datanya akan dibuang.

9. Create new clean table
  ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/part%205_1%20create%20new%20clean%20table.png?raw=true)
  ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/part%205_2%20create%20new%20clean%20table.png?raw=true)
  ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/part%205_3%20create%20new%20clean%20table.png?raw=true)

  ### Explanation
  dataframe baru dibuat dengan nama kolom yang sesuai, dan disesuaikan dengan jumlah user, berdasarkan eksplorasi sebelumnya terdapat 274 user, sehingga perlu dibuat kolom user_phone, skill, bentuk_program,   
  harga_program mewakilai jumah user * 10 pertanyaan * 3 pilihan untuk setiap pertanyaan. Sementara untuk kolom choice menggunakan logika akan bernilai 1 pada pilihan pertanyaan yang dipilih, dengan 
  memperhatikan urutan baris pada kolom pertanyaan. 
  
  jika pertanyaan 1 dataframe 1 = A maka kolom choice dataframe 2 baris 1 = 1, jika pertanyaan 1 dataframe 1 = B maka kolom choice dataframe 2 baris 2 = 1, jika 
  pertanyaan 1 dataframe 1 = C maka kolom choice dataframe 2 baris 3 = 1, jika pertanyaan 2 dataframe 1 = A maka kolom choice dataframe 2 baris 4 = 1, jika pertanyaan 2 dataframe 1 = B maka kolom choice 
  dataframe 2 baris 5 = 1, jika pertanyaan 2 dataframe 1 = C maka kolom choice dataframe 2 baris 6 = 1, jika pertanyaan 3 dataframe 1 = A maka kolom choice dataframe 2 baris 7 = 1, jika pertanyaan 3 dataframe 1 
  = B maka kolom choice dataframe 2 baris 8 = 1, jika pertanyaan 3 dataframe 1 = C maka kolom choice dataframe 2 baris 9 = 1, dan seterusnya. Selain itu kolom akan bernilai 0

## Hasil
  Before:
  
  ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/Before.png?raw=true)

  After:
  
  ![Alt text](https://github.com/syahruaru/Mini-Project/blob/main/img/After.png?raw=true)


