# Lapres Modul 1 Jarkom 2021 - T2
Laporan Hasil Praktikum Modul 1 Jarkom 2021
Kelompok T2
  * Herwinda Marwaa Salsabila (05311940000009)
  * Dian Arofati N. Z. (05311940000011)
  * Dava Aditya Jauhar (05311940000030)

---

## Nomor 01
   **Soal**
   
   Sebutkan web server yang digunakan pada "ichimarumaru.tech"!

  **Jawaban**
  
  Dari file 1-5.pcapng, kami mendapatkan Webserver ``nginx`` berkomunikasi menggunakan protokol HTTP dengan cara melakukan *filtering display* ``http``. 
  
  **Tata Cara:**
  1. Lakukan filtering display ``http.host contains "testing.mekanis.me"``, lalu akan muncul beberapa paket. 
  
  2. Di mana pada salah satu paket, kita dapat melihat web server yang digunakan pada bagian Hypertext Transfer Protocol. 
  
  
  
## Nomor 02
  **Soal**
 
  Temukan paket dari web-web yang menggunakan *Basic Authentication Method*!

  **Jawaban**
  
  Dari file 1-5.pcapng, Website yang menggunakan *Basic Authentication Method* adalah [basic.ichimarumaru.tech](basic.ichimarumaru.tech)

  **Tata Cara:**
  1. Lakukan *display filtering* menggunakan filter ``http.authbasic``
  2. Akan ditampilkan seluruh paket yang menggunakan basic authentication method
  3. Setelah diitelaah terdapat satu website yang menggunakan metode tersebut, yaitu [basic.ichimarumaru.tech](basic.ichimarumaru.tech)
  

## Nomor 03
  **Soal**

  Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!

  **Jawaban**
 
 a. Username dan Password
 
  ``` 
     Username: kuncimenujulautan
     
     Password: tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN
  ```

b. Jawaban Pada Website

  ```
  Putih Hijau - Hijau - Putih Oranye - Biru - Putih Biru - Oranye - Putih Cokelat - Cokelat
  ```
  **Tata Cara**
  1. Pada file 1-5.pcapng, Lakukan display filtering menggunakan filter ``http.host == basic.ichimaru.tech`` 
  2. Lalu pilih paket dengan info GET
  3. Pada Hypertext Transfer Protocol terdapat Authentication  yang berisikan credential:
     
     ``` 
     Username: kuncimenujulautan
     
     Password: tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN
     ```
     
  4. Gunakan username dan password tersebut untuk mengakses [basic.ichimarumaru.tech](basic.ichimarumaru.tech) dan pertanyaan pada website dijawab.



## Nomor 04
   **Soal**
   Temukan paket mysql yang mengandung perintah query select!

  **Jawaban**
  
  
  
  **Tata Cara**
  1. Melakukan display filtering menggunakan 
     ```
     mysql.query
     ```
  2. Klik paket nomor 3 dan pada MySQL Protocol terdapat dropdown Request Command Query di mana menunjukkan statement ``SELECT DATABASE``
  3. Kami juga melakukan display filtering:
     ```
     mysql.query && frame contains “select”
     ```
  
  ## Nomor 05
   **Soal**
   Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!


  **Jawaban**
  a. Username dan Password
     ```
     Username : akakanomi
     Password : pemisah4lautan
     ```
  b. Jawaban Pertanyaan
     ```
     Putih Oranye - Oranye -Putih Hijau - Biru - Putih Biru - Hijau - Putih Cokelat - Cokelat 
     ```
     
  **Tata Cara**
  1. Lakukan display filtering 
     ```
     Mysql.query && frame contains “users”
     ```
  2. Didapatkan:
     ```
     Username : akakanomi
     Password : pemisah4lautan
     ```
  3. Jawab pertanyaan **Sebutkan Konfigurasi Pengkabelan T568B!**
  
  
## Nomor 06
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
  
## Nomor 07
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
  
## Nomor 08
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
## Nomor 09
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
## Nomor 10
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
  
## Nomor 11
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
  
## Nomor 12
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
  
## Nomor 13
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
  
## Nomor 14
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
  
## Nomor 15
   **Soal**



  **Jawaban**
  
  
  
  **Tata Cara**
  
  
  
  
