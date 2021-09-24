# Jarkom-Modul-1-T14-2021

Anggota Kelompok :
- Dida Prasetyo Rahmat - 05311940000019 
- Revina Rahmanisa Harjanto - 05311940000046 

## 1. Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
command yang digunakan adalah `http.host contains "ichimarumaru.tech"` untuk melakukan capture ke http host yang mengandung "ichimaru.tech" untuk mendapatkan data dari webserver tersebut  
![soal 1 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889488432458518538/unknown.png)  
setelah mendapatkan datanya, lalu melakukan follow TCP Stream untuk mendapatkan informasi mengenai webservernya  
![soal 1 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/889487918043901952/unknown.png)  

## 2. Temukan paket dari web-web yang menggunakan basic authentication method!
disini kami menggunakan website `http://basic.ichimarumaru.tech` sebagai contohnya, dengan menggunakan command `http.authbasic` dan melakukan proses login makan akan didapatkan data basic authenticationnya  
![soal 2 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889498208848453693/unknown.png)  

## 3. Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
pada soal ke 3, pertama kami mencari username dan password terlebih dahulu yang bisa didapatkan menggunakan command `http.authbasic` dan mengecek credentialsnya untuk mendapatkan username dan password  
![soal 3 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889499574933278730/unknown.png)  
dapat dilihat pada gambar bahwa usernamenya adalah `kuncimenujulautan` dan setelah tanda `:` merupakan passwordnya, lalu kami login menggunakan username dan password tersebut untuk melaksanakan perintah yang ada pada `basic.ichimarumaru.tech`.  
![soal 3 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/890920764172283994/unknown.png)  
perintahnya adalah untuk menyebutkan urutan konfigurasi kabel T568A yang jawabannya adalah `putih hijau - hijau - putih orange - biru - putih biru - orange - putih coklat - coklat`  

## 4. Temukan paket mysql yang mengandung perintah query select!
dengan menggunakan command `mysql` untuk menampilkan semua paket yang berhubungan dengan mysql, lalu memilih paket yang memiliki informasi request query dan mengecek pada kolom `request command query` pada informasi dibawah list paketnya  
- `SELECT DATABASE()`  
![soal 4 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889503029370437642/unknown.png)  
- `select username from users`
![soal 4 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/889502882985033748/unknown.png)  
- `select count(*) from users`
![soal 4 - screenshot 3](https://media.discordapp.net/attachments/889487853267083274/889502974852870174/unknown.png)  

## 5. Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
masih menggunakan command `mysql` kami mengecek paket yang memiliki informasi request query dan menemukan username dan password pada query insert table
![soal 5 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889503325379244032/unknown.png)  
username yang didapat adalah `akakanomi` dan passwordnya `pemisah4lautan` yang digunakan untuk login ke `portal.ichimarumaru.tech` dan mengerjakan soal yang diperintahkan pada web tersebut  
![soal 5 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/889504209303662602/unknown.png?width=1002&height=676)  
perintah pada web tersebut adalah untuk menyebutkan urutan dari configurasi kabel T568B yang jawabannya adalah putih orange - orange - putih hijau - biru - putih biru - hijau - putih coklat - coklat  

## 6. Cari username dan password ketika melakukan login ke FTP Server!
untuk mendapatkan informasi username dan password yang digunakan untuk login ke FTP Server, kami menggunakan command `ftp.request.command`  
![soal 6 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889506652192120892/unknown.png)  
didapatkan usernamenya adalah `secretuser` dan passwordnya `aku.pengen.pw.aja`  

## 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
command yang digunakan untuk mencari pdfnya adalah `ftp-data contains "Real.pdf"`, lalu akan didapatkan paket yang mengandung file tersebut
![soal 7 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889508821561638912/unknown.png)  
selanjutkan kami melakukan Follow TCP Stream pada paket tersebut dan menampilkan data dalam bentuk raw, lalu menyimpannya dalam format zip dan mengekstraknya, sehingga didapatkanlah file `Real.pdf` yang tersimpan di zip tersebut  
![soal 7 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/889509654068068402/unknown.png)  
![soal 7 - screenshot 3](https://media.discordapp.net/attachments/889487853267083274/889509792282980352/unknown.png?width=1202&height=676)  

## 8. Cari paket yang menunjukan pengambilan file dari FTP tersebut!
kami menggunakan command `ftp` dan `ftp-data contains "RETR"` untuk melihat informasi paket yang menunjukan pengambilan file dari FTP, namun paket tersebut tidak ditemukan
![soal 8 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/890930909866491924/unknown.png)  
![soal 8 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/889513519937118259/unknown.png)  

## 9. Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!
kami menggunakan command `ftp-data contains "STOR secret.zip"` untuk mengambil paket yang memiliki informasi mengenai file zip tersebut
![soal 9 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889517318932168774/unknown.png)  
setelah ditemukan paket tersebut, kami memilih paket di list bawah dan melakukan Follow TCP Stream, menampilkan data dengan metode raw dan menyimpannya sebagai file zip

## 10. Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!
dengan command `ftp-data contains "STOR history.txt"` kami dapat melihat paket yang mengandung file `history.txt`  
![soal 10 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/889516155885195324/unknown.png)  
lalu kami membuka paket tersebut untuk mengecek isinya dengan perintah Follow TCP Stream  
![soal 10 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/889516255709626378/unknown.png)  
pada `history.txt` terlihat bahwa `secret.zip` dipassword menggunakan password yang disimpan pada `bukanapaapa.txt` sehingga kami melakukan pencarian paket yang mengandung file tersebut. Command yang kami gunakan adalah `ftp-data contains "bukanapaapa"`  
![soal 10 - screenshot 3](https://media.discordapp.net/attachments/889487853267083274/889516442364563466/unknown.png)  
setelah kami buka file tersebut, didapatkan bawah password zipnya adalah `dibilangbukanapaapajugagapercaya`  
![soal 10 - screenshot 4](https://media.discordapp.net/attachments/889487853267083274/889516538841927740/unknown.png)  
![soal 10 - screenshot 5](https://media.discordapp.net/attachments/889487853267083274/889517989362303056/unknown.png)  
setelah berhasil melakuan unzip pada file `secret.zip`, berikut adalah isi dari `wanted.pdf` yang tersimpan didalamnya  
![soal 10 - screenshot 6](https://media.discordapp.net/attachments/889487853267083274/889518201124302898/unknown.png?width=1202&height=676)  

## 11. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
menggunakan command `tcp.port == 80` sehingga wireshark hanya mengambil paket pada port 80  
![soal 11 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/890921561526251580/unknown.png)  

## 12. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
menggunakan command `tcp.port == 21` sehingga wireshark hanya mengambil paket pada port 21. Dikarenakan port 21 sedang tidak terpakai sehingga wireshark tidak mengcapture paket apapun. 
![soal 12 - screenshot 1](https://cdn.discordapp.com/attachments/889487853267083274/890921957619548180/unknown.png)  

## 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
menggunakan command `tcp.dstport == 443` sehingga wireshark hanya mengambil paket yang menuju ke port 443  
![soal 13 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/890922245491413052/unknown.png)  

## 14. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
command yang digunakan adalah `dst host kemenag.go.id` pada capture filter untuk menambil paket yang tujuannya `kemenag.go.id`  
![soal 14 - screenshot 1](https://media.discordapp.net/attachments/889487853267083274/890922524605579314/unknown.png)  

## 15. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
berikut adalah ip komputer yang digunakan untuk menjalankan wireshark  
![soal 15 - screenshot 1](https://cdn.discordapp.com/attachments/889487853267083274/890922701013811210/unknown.png)  
lalu dengan command `src host 192.168.62.181` pada capture filter, maka wireshark akan menangkap paket yang berasal dari ip yang dicantumkan  
![soal 15 - screenshot 2](https://media.discordapp.net/attachments/889487853267083274/890923087107850291/unknown.png)  
