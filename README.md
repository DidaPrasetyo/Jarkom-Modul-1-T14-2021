# Jarkom-Modul-1-T14-2021

Anggota Kelompok :
- Dida Prasetyo Rahmat - 05311940000019 
- Revina Rahmanisa Harjanto - 05311940000046 

# 1. Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
command yang digunakan adalah `http.host contains "ichimarumaru.tech"` untuk melakukan capture ke http host yang mengandung "ichimaru.tech" untuk mendapatkan data dari webserver tersebut  
![soal 1 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889488432458518538/unknown.png)  
setelah mendapatkan datanya, lalu melakukan follow TCP Stream untuk mendapatkan informasi mengenai webservernya  
![soal 1 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/889487918043901952/unknown.png)  

# 2. Temukan paket dari web-web yang menggunakan basic authentication method!
disini kami menggunakan website `http://basic.ichimarumaru.tech` sebagai contohnya, dengan menggunakan command `http.authbasic` dan melakukan proses login makan akan didapatkan data basic authenticationnya  
![soal 2 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889498208848453693/unknown.png)  

# 3. Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
pada soal ke 3, pertama kami mencari username dan password terlebih dahulu yang bisa didapatkan menggunakan command `http.authbasic` dan mengecek credentialsnya untuk mendapatkan username dan password  
![soal 3 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889499574933278730/unknown.png)  
dapat dilihat pada gambar bahwa usernamenya adalah `kuncimenujulautan` dan setelah tanda `:` merupakan passwordnya, lalu kami login menggunakan username dan password tersebut untuk melaksanakan perintah yang ada pada `basic.ichimarumaru.tech`.  
![soal 3 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/890920764172283994/unknown.png)  
perintahnya adalah untuk menyebutkan urutan konfigurasi kabel T568A yang jawabannya adalah `putih hijau - hijau - putih orange - biru - putih biru - orange - putih coklat - coklat`  

# 4. Temukan paket mysql yang mengandung perintah query select!

# 5. Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!

# 6. Cari username dan password ketika melakukan login ke FTP Server!

# 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")

# 8. Cari paket yang menunjukan pengambilan file dari FTP tersebut!

# 9. Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!

# 10. Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!

# 11. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
menggunakan command `tcp.port == 80` sehingga wireshark hanya mengambil paket pada port 80  
![soal 11 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/890921561526251580/unknown.png)  

# 12. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
menggunakan command `tcp.port == 21` sehingga wireshark hanya mengambil paket pada port 21  
![soal 12 - screenshot 1](https://cdn.discordapp.com/attachments/889487853267083274/890921957619548180/unknown.png)  

# 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
menggunakan command `tcp.dstport == 443` sehingga wireshark hanya mengambil paket yang menuju ke port 443  
![soal 13 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/890922245491413052/unknown.png)  

# 14. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
command yang digunakan adalah `dst host kemenag.go.id` pada capture filter untuk menambil paket yang tujuannya `kemenag.go.id`  
![soal 14 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/890922524605579314/unknown.png)  

# 15. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
berikut adalah ip komputer yang digunakan untuk menjalankan wireshark  
![soal 15 - screenshot 1](https://cdn.discordapp.com/attachments/889487853267083274/890922701013811210/unknown.png)  
lalu dengan command `src host 192.168.62.181` pada capture filter, maka wireshark akan menangkap paket yang berasal dari ip yang dicantumkan  
![soal 15 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/890923087107850291/unknown.png)  