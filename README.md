# Nadiaa
Proyek ini membangun sebuah Kebijakan / Bertujuan untuk menjadi:

-Penulis aturan diizinkan untuk menulis aturan 
-Penulis aturan tidak perlu menerapkan kebijakan secara terpisah
-Seorang pengguna mesin dapat melakukan Foward-chaining dan Backward-chaining dengan aturan / kebijakan yang ditetapkan

Cara kerja Rantai Mundur dan Maju
Seperti ada aturan sebagai berikut:

1. JIKA salah satu <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan B' benar; atau <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan C' benar <br/>
   LALU <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan A' benar.
2. JIKA keduanya <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan D' benar; dan <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan E' benar <br/>
   LALU <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan C' benar.
3. JIKA <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan F' benar <br/>
   LALU <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan D' salah.
4. JIKA <br/>
     & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan G' salah <br/>
   LALU <br/>
      & nbsp; & nbsp; & nbsp; & nbsp; 'pernyataan E' benar.

Rantai mundur :
Mesin inferensi saat menggunakan rantai mundur menelusuri aturan inferensi hingga menemukan aturan yang memiliki konsekuensi yang cocok. 
Misalnya : 
-jika kita ingin mengetahui apakah aturan 'pernyataan A' adalah 'benar' atau 'tidak benar 'salah', mesin menemukan aturan mana yang harus diperiksa untuk menyimpulkan.
Dalam hal ini, mesin membutuhkan informasi tentang aturan 'pernyataan B' adalah 'benar' atau 'tidak benar (salah)',
atau 'pernyataan F' dan 'pernyataan G' adalah 'benar' atau 'tidak benar (salah) 'masing-masing.

Rantai maju :
Sebuah mesin inferensi menggunakan rantai maju mencari aturan inferensi sampai menemukan satu di mana anteseden (klausa If) diketahui benar.
Misalnya :
-jika kita memiliki fakta bahwa 'pernyataan G' benar dan 'pernyataan F' benar maka mesin menyimpulkan sebagai berikut;
- 'Pernyataan G' benar.
- 'pernyataan F' benar.
- 'pernyataan E' salah karena 'pernyataan G' tidak salah.
- 'pernyataan D' salah karena 'pernyataan F' itu benar.
- 'pernyataan C' salah karena 'pernyataan D' itu benar dan 'pernyataan E' salah.
- 'pernyataan B' tidak diketahui karena tidak ada informasi yang diberikan untuk menyimpulkan tentang 'pernyataan B'.
- 'pernyataan A' salah dengan informasi yang diberikan 'pernyataan B' dan 'pernyataan C',
namun dapat diubah berdasarkan kesimpulan dari 'pernyataan B' karena 'pernyataan B' tidak diketahui.

Fungsi Forward Dan Backward Chaining didalam Aplikasi Nadia.

-Backward Chaining 	: Kebijakan berikutnya dalam rantai mundur untuk memeriksa untuk menyelesaikan logika kumpulan aturan.
-Forward Chaining 	: Memeriksa semua kebenaran atau nilai yang dihitung dalam rantai maju.
