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
  
  Dari file 1-5.pcapng, Webserver yanng berkomunikasi menggunakan protokol HTTP adalah ``nginx``. 
  
  **Tata Cara:**
  1. Lakukan filtering display ``http.host contains "testing.mekanis.me"``, lalu akan muncul beberapa paket. 
  2. Di mana pada salah satu paket, kita dapat melihat web server yang digunakan pada bagian Hypertext Transfer Protocol.
  
     <img src="https://user-images.githubusercontent.com/57520495/134288591-1f9cbf70-dd64-4518-a92d-896894de9967.png" width="800">

  
## Nomor 02
  **Soal**
 
  Temukan paket dari web-web yang menggunakan *Basic Authentication Method*!

  **Jawaban**
  
  Dari file 1-5.pcapng, Website yang menggunakan *Basic Authentication Method* adalah [basic.ichimarumaru.tech](basic.ichimarumaru.tech)

  **Tata Cara:**
  
  1. Lakukan *display filtering* menggunakan filter ``http.authbasic``
  2. Akan ditampilkan seluruh paket yang menggunakan basic authentication method
  3. Setelah diitelaah terdapat satu website yang menggunakan metode tersebut, yaitu [basic.ichimarumaru.tech](basic.ichimarumaru.tech)
   
     <img src="https://user-images.githubusercontent.com/57520495/134288647-1af8dec9-01f4-49d7-8432-833cc4b43aaa.png" width="800">

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
  
  1.  Pada file 1-5.pcapng, Lakukan display filtering menggunakan filter ``http.host == basic.ichimaru.tech`` 
  2.  Lalu pilih paket dengan info GET
  3.  Pada Hypertext Transfer Protocol terdapat Authentication  yang berisikan credential:
     
     ``` 
     Username: kuncimenujulautan
     
     Password: tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN
     ```
      
   <img src= "https://user-images.githubusercontent.com/57520495/134288686-873714f1-75c7-4879-b000-296388c8673b.png" weight="700">
     
  4. Gunakan username dan password tersebut untuk mengakses [basic.ichimarumaru.tech](basic.ichimarumaru.tech) dan pertanyaan pada website dijawab.
     
     <img src= "https://user-images.githubusercontent.com/57520495/134288721-01769351-5268-4c66-a978-3f8920845424.png" weight="400">

## Nomor 04
   **Soal**
   
   Temukan paket mysql yang mengandung perintah query select!

  **Tata Cara dan Jawaban**
  
  1. Melakukan display filtering menggunakan 
     ```
     mysql.query
     ```
  2. Klik paket nomor 3 dan pada MySQL Protocol terdapat dropdown Request Command Query di mana menunjukkan statement ``SELECT DATABASE``
     
     ![image](https://user-images.githubusercontent.com/57520495/134288836-b3d1619b-02da-4429-aed7-c3a7fbfccd8a.png)
     
  4. Kami juga melakukan display filtering:
     ```
     mysql.query && frame contains “select”
     ```
     
     ![image](https://user-images.githubusercontent.com/57520495/134288862-f5d90c76-f02f-42c4-afe9-1976947fced2.png)
  
  ## Nomor 05
   **Soal**
   Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!

  **Jawaban**
  
  1. Username dan Password
     ```
     Username : akakanomi
     Password : pemisah4lautan
     ```
     
  2. Jawaban Pertanyaan
     ```
     Putih Oranye - Oranye -Putih Hijau - Biru - Putih Biru - Hijau - Putih Cokelat - Cokelat 
     ```
     
  **Tata Cara**
  
  1. Lakukan display filtering 
     ```
     Mysql.query && frame contains “users”
     ```
     
     ![image](https://user-images.githubusercontent.com/57520495/134288959-a8923d71-57a2-498d-a66d-8e47aa5e1d47.png)
     
  2. Didapatkan:
     ```
     Username : akakanomi
     Password : pemisah4lautan
     ```

  3. Jawab pertanyaan **Sebutkan Konfigurasi Pengkabelan T568B!**
     ```
     Putih Oranye - Oranye -Putih Hijau - Biru - Putih Biru - Hijau - Putih Cokelat - Cokelat 
     ```
     
     ![image](https://user-images.githubusercontent.com/57520495/134288978-2aa1abed-8806-4564-b6d6-40341d99b637.png)

  
## Nomor 06
   **Soal**

   Cari username dan password ketika melakukan login ke FTP Server!

  **Tata Cara dan Jawaban**
  
  1. Lakukan display filtering ```ftp.request.command == “USER” || ftp.request.command == “PASS”```
  2. Didapatkan: USER: ```secretuser``` dan PASS: ```aku.pengen.pw.aja```
  
  ![image](https://user-images.githubusercontent.com/57520495/134289004-a6d2abe2-6268-46b3-83f0-f91385721f71.png)
  
    
## Nomor 07
   **Soal**

   Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")

  **Tata Cara dan Jawaban**
  
  1. Lakukan filtering ```frame contains “.pdf” && frame contains “Real.pdf”```
  2. Follow TCP Stream
  3. Show as Raw
  4. Save as ```Real.pdf```
  
  ![image](https://user-images.githubusercontent.com/57520495/134289132-71f04e6e-d6bc-4f43-8112-4745296e77a9.png)
  ![image](https://user-images.githubusercontent.com/57520495/134289347-1dcbce40-025c-45de-b0f7-152238a51232.png)
  
  
## Nomor 08
  **Soal**

  Cari paket yang menunjukan pengambilan file dari FTP tersebut!

  **Jawaban**
  
  1. Lakukan display filtering ```frame contains “RETR”```
  2. Berdasarkan hasil yang didapat, tidak ada data/log yang menunjukkan pengambilan (download atau RETR dari FTP Server tsb)
  
  ![image](https://user-images.githubusercontent.com/57520495/134289470-0ec3a3b7-c561-40f2-8676-029227f01ecf.png)  
  
## Nomor 09
   **Soal**

   Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!


  **Jawaban**
  
  1. Lakukan display filtering ```frame contains “STOR” && frame contains “secret.zip”```
  2. Follow TCP Stream
  3. Increase stream number jadi 10, show as Raw
  4. Save as secret.zip
  
  ![image](https://user-images.githubusercontent.com/57520495/134289576-2cf8d937-80ca-4af0-9215-5b410c6fb215.png)  
  
## Nomor 10
   **Soal**

   Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!


  **Jawaban**
  
  1. Lakukan ```frame contains “.txt”``` atau ```frame contains “.txt”```
  2. Follow TCP Stream yang history.txt
  3. Increase Stream, show as ASCII
  
  ![image](https://user-images.githubusercontent.com/57520495/134289772-b68446fc-606b-482d-8c34-3f28801d2f2c.png)
  
  5. Berdasar isinya, dapat terlihat bahwa password file secret.zip merupakan baris ke-(-1) (tail -1) dari file bukanapapa.txt
  6. Follow TCP Stream yang bukanapapa.txt
  7. Increase Stream, show as ASCII
  
  ![image](https://user-images.githubusercontent.com/57520495/134289862-ad3cc7db-31c2-4378-bf74-22cbf75de1d2.png)
  
  9. Buka file ```Wanted.pdf``` dengan password yang didapatkan tadi
  
  ![image](https://user-images.githubusercontent.com/57520495/134289989-d02b40dc-eb95-4040-b64d-1130c4845a31.png)
  
## Nomor 11
   **Soal**

   Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

   **Jawaban**
  
   1. *Capture Filtering* menggunakan ``src port 80``
  
   ![image](https://i.imgur.com/Yv0VchJ.png)
  
   ![image](https://i.imgur.com/kREbOHf.png)
  
   2. *Display Filtering* menggunakan ``tcp.srcport == 80 || udp.srcport == 80``
  
   ![image](https://user-images.githubusercontent.com/57520495/134290038-c3e82129-8866-4e43-a40c-53aa68c180e6.png)

  
   **Tata Cara**
  
   1. Buka wireshark dan pilih jaringan Wifi
   2. Ketikan ``src port 80`` pada kolom filtering dan klik enter
   3. Wireshark akan menangkap paket-paket yang berasal dari port 80
   4. Pada soal ini, kami juga melakukan *display filtering* untuk memastikan bahwa semua paket berasal dari port 80  
  
## Nomor 12
   **Soal**

  Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

  **Jawaban**
  
  1. Jawab
     ![image](https://user-images.githubusercontent.com/57980125/134377458-55412df9-0b51-411e-b1a2-c4447b7b3d59.png)
  2. Jawab
     ![image](https://user-images.githubusercontent.com/57520495/134290063-25ddd11e-c06e-4af7-bd07-6918f3d9056f.png)

  
  **Tata Cara**
  1. Nyalakan Wireshark dan lakukan capturing packet menggunakan jaringan **Adapter for Loopback Traffic Capture** dengan capture filtering ``Port 21``
     
     ![image](![Wireshark_y0K6n6UwzF](https://user-images.githubusercontent.com/57980125/134377730-0a46e7b5-c600-431d-8476-58f16d49102e.png)
     
  2. Buka Xampp dan nyalakan FileZilla Server. Lalu klik admin. Pada admin akan muncul server address yang akan digunakan pada mesin filezilla client.
     
     ![image](https://user-images.githubusercontent.com/57980125/134377752-4909d67a-c6ad-408d-9ed3-e8ebb0761a2b.png)
     
     ![image](https://user-images.githubusercontent.com/57980125/134377916-744b7517-06e7-4b0f-8668-204d3d41a3c3.png)
     
  3. Pada filezilla server, klik users dan edit seperti gambar di bawah. Tetapkan username dan password yang akan digunakan. Di sini penulis menggunakan 
  
     ```username: indowebsite dan password: 123```
     
     ![image](https://user-images.githubusercontent.com/57980125/134378163-753abaf3-5e8f-4a7c-954a-0778dfabe8b4.png)
  
  4. Buka FileZilla Client dan isikan username, password, beserta mesin.
  
     ![image](https://user-images.githubusercontent.com/57980125/134378188-6d5a077e-e259-4eea-a137-0623b5fc0ffa.png)

  5. Cek kembali Wireshark dan akan didapatkan paket-paket yang mengandung port 21 di bawah ini
    
     ![image](https://user-images.githubusercontent.com/57980125/134377458-55412df9-0b51-411e-b1a2-c4447b7b3d59.png)
  
  6. Di sini Port 21 merupakan sebuah default port FTP
  
  
## Nomor 13
   **Soal**

   Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

  **Tata Cara dan Jawaban**
  
  1. Display Filtering
     
     Filter:
     

     ```tcp.dstport == 443 || udp.dstport == 443```
     

  
      ![image](https://user-images.githubusercontent.com/57520495/134290142-5b0cec1f-9d22-4700-a493-513d2fd25ac0.png)
  
  2. Capture Filtering
     

     ```dst port 443```
     

     
      ![image](https://user-images.githubusercontent.com/57520495/134290119-82b387a9-cf48-4f73-8868-fbf40be7096b.png)
     
## Nomor 14
   **Soal**

   Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!

  **Jawaban**
 
  ![image](https://user-images.githubusercontent.com/57520495/134290181-cae37dac-88a9-4793-bf00-600a9f274ce9.png)

  **Tata Cara**
  
  1. Ping [kemenag.go.id](kemenag.go.id) pada Command Prompt
 
      ![image](https://user-images.githubusercontent.com/57520495/134290168-8925cb1f-cdef-45aa-b57e-a88b0c10a54a.png)
      
  2. Pilih Wifi dan jalankan capturing paket
  
  4. Kunjungi website [kemenag.go.id](kemenag.go.id)
  
  6. Kembali ke wireshark dan stop capturing
  
  8. Lakukan display filtering ```http.host == kemenag.go.id```
  
## Nomor 15
   **Soal**

   Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

  **Jawaban**
  
  ![image](https://user-images.githubusercontent.com/57520495/134290217-f76b6760-f0dd-4bac-944e-50b029dd167f.png)
  
  **Tata Cara**
  1. Pertama-tama ketikkan ipconfig pada command prompt windows untuk mengetahui IP Address kami.
  
      <img src = "https://user-images.githubusercontent.com/57520495/134290202-4276d17c-d8ca-47cc-bd91-b054abe43843.png" weight = "300px">
      
  2. Setelah mendapatkan IP tersebut, buka wireshark dan ketikan ``src 192.168.43.1`` untuk melakukan *capture filter*.
  
     <img src = "https://user-images.githubusercontent.com/57520495/134290209-d5c79337-3657-4ae5-8cac-3eca9c3f384e.png" weight = "300px">
     
  3. Setelah itu jalankan wireshark dan stop capturing
     

## Kendala
  1.  ..
  2.  ..
  
  
  
