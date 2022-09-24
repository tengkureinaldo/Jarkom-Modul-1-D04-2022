# soal-jarkom-modul-1-D04-2022 

## Anggota Kelompok
| **Nama** | **NRP** |
| ------ | ------ |
| Muhammad Ghani Taufiqurrahman Atmaja | 5025201110 |
| Tengku Fredly Reinaldo | 5025201198 |
| Shaula Aljauhara Riyadi | 5025201265 |

## Soal 1
Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 
### Jawab
* #### Filter yang digunakan
```http.host eq monta.if.its.ac.id```
* #### Penjelasan
Menggunakan display filter ```http.host == "monta.if.its.ac.id"``` yang befungsing untuk menampilkan paket http yang memiliki host ```monta.if.its.ac.id```

![messageImage_1664028387464](https://user-images.githubusercontent.com/77779184/192102458-97365586-d422-4c36-b182-2bfaadc59563.jpg)

Lalu klik kanan salah satu paket memilih ```follow -> tcp stream```

![messageImage_1664028368648](https://user-images.githubusercontent.com/77779184/192102412-252a0f6e-db8c-4f1d-9a88-5942c1948f85.jpg)

Lalu didapatkan web server yang digunakan yaitu ```nginx/1.10.3```

![messageImage_1664028406851](https://user-images.githubusercontent.com/77779184/192102559-6067eb51-153a-43f5-9be6-435615bc50e3.jpg)

## Soal 2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ? 
### Jawab
* #### Filter yang digunakan
```http.host contains monta.if.its.ac.id```
* #### Penjelasan

Sama seperti sebelumnya akan tetapi menggunakan ```contains``` untuk menampikan nilai tertentu.

![messageImage_1664028886873](https://user-images.githubusercontent.com/77779184/192102862-d761567c-f76c-41e1-bc61-9f7639e71ed9.jpg)

Setelah mendapatkan paket yang dari filter tersebut kita dapat melihat paket yang memiliki info ```detail topik```.

![messageImage_1664028924391](https://user-images.githubusercontent.com/77779184/192102920-de0666f9-31d3-43e1-909f-c3c4a7c8844a.jpg)

Lalu melihat detail dari paket tersebut yang nantinya terdapat link yang di tuju oleh mas ishaq.

![messageImage_1664028954650](https://user-images.githubusercontent.com/77779184/192102962-3fbd8cdf-1fb4-4186-9688-2163624a9fd3.jpg)


3. Filter sehingga wireshark hanya menampilkan paket yang menuju port 80! <br /> <br />
![3](https://user-images.githubusercontent.com/56400536/192100261-9088baab-3e90-4f89-b26b-2745c5faedeb.jpg)
> Karena port 80 menggunakan protokol TCP, maka masukkan *filter expression* seperti pada gambar di
atas dan hasilnya adalah daftar paket yang menuju port 80, ditandai dengan “... -> 80” di
bagian Info

4. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21! <br /> <br />
![4](https://user-images.githubusercontent.com/56400536/192100495-967fc92a-c882-44f4-80ee-e97627181016.jpg)
> Karena port 21 menggunakan port TCP, maka masukkan *filter expression* seperti pada gambar di
atas dan hasilnya adalah daftar paket yang berasal dari port 21, ditandai dengan “21 -> …” di
bagian Info

5. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443! <br /> <br />
![5](https://user-images.githubusercontent.com/56400536/192100506-c59be7d7-ef6e-46bb-8acd-eb7ec8798146.jpg)
> Karena port 443 menggunakan protokol TCP, maka masukkan *filter expression* seperti pada gambar di
atas dan hasilnya adalah daftar paket yang berasal dari port 443, ditandai dengan “443 -> …”
di bagian Info

6. Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id ! <br /> <br />
![6 1](https://user-images.githubusercontent.com/56400536/192100523-218349c9-6dcf-41f6-a5da-d2ba0596039f.jpg)
> Carilah terlebih dahulu *IP Address* dari website lipi.go.id menggunakan “ping
lipi.go.id”

![6 2](https://user-images.githubusercontent.com/56400536/192100528-7f694c36-1730-48e5-bfd0-72a558f06d37.jpg)

> Setelah mendapatkan *IP Address*-nya, tuliskan *filter expression* seperti pada gambar di
atas beserta *IP Address* yang telah didapat tadi

## Soal 7
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
### Jawab
* #### Filter yang digunakan
```ip.src == 192.168.0.100``` atau ```ip.src == ip.adress kalian```
* #### Penjelasan
Untuk mendapatkan paket dari ip kalian bisa dimulai dari mencari ip kalian dari cmd dengan menggunakan command ```ipconfig```.

![messageImage_1664029194702](https://user-images.githubusercontent.com/77779184/192103114-a6344670-7c55-4946-aa9a-f6a796aa71a0.jpg)

Setelah mendapatkan ip kalian bisa menggunakan display filter sesuai ip kalian.

![messageImage_1664029370981](https://user-images.githubusercontent.com/77779184/192103151-d4434af4-313f-4326-9c2e-f6e8cc4977be.jpg)

## Soal 8
Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut. 
### Jawab
* #### Filter yang digunakan
```(ip.src == 127.0.0.1 || ip.dst == 127.0.0.1) && (tcp.port == 65432 || tcp.port == 60236)```
* #### Penjelasan
Untuk mendapatkan percakapan dari dua mahasiswa tersebut kita mesti menentukan ip atau port mereka yang mana.

![messageImage_1664029725089](https://user-images.githubusercontent.com/77779184/192103534-386b75c1-4112-41d3-91a4-268cd034aa17.jpg)

Setelah mendapatkan ip atau port mereka kita bisa meng-filter berdasarkan ip dan port mereka.

![messageImage_1664029539002](https://user-images.githubusercontent.com/77779184/192103585-32c6fccf-c71d-4f98-902c-2b4b610b88a2.jpg)

Setelah menfilter paket berdasarkan ip dan port mereka, kita bisa melihat percakapan mereka dengan menggunakan ```tcp stream```.

![messageImage_1664029559592](https://user-images.githubusercontent.com/77779184/192103643-fdec3088-7ea1-40d7-82d0-4dfd8fb24270.jpg)

## Soal 9
Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”. 
### Jawab
* #### Filter yang digunakan
```(ip.src == 127.0.0.1 || ip.dst == 127.0.0.1) && tcp.port == 9002```
* #### Penjelasan
Untuk mendapatkan filenya kita dapat menggukan port ```9002``` sesuai yang terdapat pada clue.

![messageImage_1664029919264](https://user-images.githubusercontent.com/77779184/192103776-cb1bde2f-07be-425b-9716-75a24b9db2ca.jpg)
![messageImage_1664030055068](https://user-images.githubusercontent.com/77779184/192103888-f2828143-a3e3-4672-9886-1313d83bac8b.jpg)

Lalu kita bisa melihat filenya dengan ```tcp stream``` salah satu pake dan untuk mendapatkan paketnya kita dapat mendownload file dengan menggunakan output sebagai ```raw```.

![10](https://user-images.githubusercontent.com/77779184/192104062-393648da-2554-4bc9-8912-df40b6645f1e.png)
![11](https://user-images.githubusercontent.com/77779184/192104083-bdc98eae-f713-4ae8-b18f-78e1e3b537cf.png)
![12](https://user-images.githubusercontent.com/77779184/192104099-ee189e1d-5575-48d7-9b06-cf3b5b4f8566.png)

Setelah mendapatkan filenya kita dapat men-decrypt dengan menggunakan syntax ```openssl des3 -d -in D04.des3 -out flag.txt``` yang dapat dilakukan di ubuntu.

![14](https://user-images.githubusercontent.com/77779184/192104842-915ec011-020d-47c6-b34e-7933221c0357.png)
![15](https://user-images.githubusercontent.com/77779184/192104872-1f193fc5-de7f-408e-b8b5-5ec162d2ee6d.png)

Didapatkan text file seperti ini.

![messageImage_1664031735195](https://user-images.githubusercontent.com/77779184/192105015-491d9653-2f94-4dc1-9aa8-930626051c96.jpg)

## Soal 10
Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas! 
### Jawab
* #### Jawaban
Password = ```nakano```
* #### Penjelasan
Untuk mendapatkan password kita bisa menggunakan clue yang terdapat pada percakapan di soal no 8.

![messageImage_1664031861676](https://user-images.githubusercontent.com/77779184/192105104-b013f402-45c9-48aa-9e7e-447ea7abce90.jpg)

Dengan mencoba setiap kata pada nama karakter-karakter tersebut didapatkan kata ```nakano``` sebagai password untuk men-decrypt file no 9.

## Kendala
- Untuk nomer 10 agak ambigu untuk mereka yang tidak menonton anime tersebut
- Untuk nomer 9, kesulitan untuk decrypt filenya dikarenakan mesti didownload dalam raw baru bisa dipake dengan syntax openssl
- Untuk nomer 8, sempat kebingungan bagaimana cara untuk mendapatkan percakapan secara bersih tanpa ada paket-paket yang lain


