<div align="center">

# Laporan Resmi Praktikum 1 Jaringan Komputer

| Nama | Muhammad Ersya Vinorian |
| ---- | ----------------------- |
| NRP  | 5025211045              |

</div>

<div align="justify">

## **Soal 1**

> User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

Mengunggah file pada FTP menggunakan kode request STOR. Dapat digunakan filter kueri menggunakan `ftp contains “STOR”`.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/e6e7e54e-eec1-4fbc-9549-8e1b8b913da4)

> a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/d2b04149-08c9-4be7-afee-07555f0e2e7b)

> b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/7159ea2b-3100-4d6a-af08-77e9b5fa5602)

> c.	Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

Klik kanan pada paket tersebut kemudian _follow TCP stream_ akan muncul kueri filter `tcp.stream eq 4` kemudian tambahkan kueri filter menjadi `tcp.stream eq 4 and ftp` dan klik paket response dari request pada subsoal sebelumnya menjadi berikut.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/06dc8cc8-4888-4576-b180-de6b814d557e)

> d.	Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/b469d9eb-1485-4879-8a80-997f2c89399c)

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/192af6a0-ce5e-4f0d-91bc-9dc1359483af)

`Jarkom2023{y0u_r_g00d_4t_4dr3ssing_LpDvGrM91196149}`

## **Soal 2**

> Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

Dapat dilakukan kueri filter `http` kemudian _follow HTTP stream_ pada paket http pertama yang ditemukan untuk mengetahui _header_ dari salah satu http _request_.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/5fd77d90-69d0-46c5-a044-9cd27a29498d)

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/e89f24a2-0e58-4ec2-968a-f06500e6e5b3)

`Jarkom2023{9unic0rn_1s_6u077k6sdtM2UVH_c00l}`

## **Soal 3**

> Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
> a.	Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

Dapat menggunakan kueri filter `ip.addr == 239.255.255.250 and udp.port == 3703` untuk menampilkan hasil paket yang sesuai dengan soal.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/1aa3b875-4a44-44b4-97a8-23b519c96c0f)

Terdapat 21 paket.

> b.	Protokol layer transport apa yang digunakan?

Terlihat bahwa protokol yang digunakan adalah UDP.

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/d48badff-4016-488f-805e-3228a8f0ae53)

`Jarkom2023{4nalyz3_is_1910_DvEmQvPvElA_gr3at}`

## **Soal 4**

> Berapa nilai checksum yang didapat dari header pada paket nomor 130?

Pilih pada paket nomor 130 dan lihat pada panel detail checksum.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/1f1c1df8-a666-4a3b-9cc1-b11a072e024a)

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/bcf0f44b-63c5-4ed1-b0ac-a2eece98b7a3)

`Jarkom2023{ch3cksum_is_u5eful_0xs47m}`

## **Soal 5**

> Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.

Dapat dilakukan filter kueri `smtp` untuk mendapatkan _service_ SMTP.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/3f511db2-2444-4176-9343-c6ddd0d8af92)

Kemudian _follow TCP stream_ untuk melihat kontennya.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/a977ade5-7b2d-4642-bb53-aef3edfc5664)

_Decode_ password menggunakan base64 menggunakan kakas seperti CyberChef.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/d047a9df-7531-4b0b-8b58-2903b10c64fe)

Masukkan password untuk membuka file connect.txt pada zip.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/39627427-8df2-4c47-a2ed-42f944a2f9c7)

Hubungkan ke netcat _instance_ untuk menjawab soal.

> a.	Berapa banyak paket yang berhasil di capture dari file pcap tersebut?

Klik pada No. untuk melakukan pengurutan terbalik pada nomor paket.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/651ab56b-ee7c-4c0f-b809-5c6f87cfebff)

> b.	Port berapakah pada server yang digunakan untuk service SMTP?

Klik pada salah satu paket _service_ SMTP dan lihat pada bagian panel detail.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/da0f9e3e-a828-4192-b5b3-3d490a58ebca)

> c.	Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

Alamat IP public adalah selain yang dimulai dengan 10.x.x.x.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/a46a4b42-be0f-40b4-8f1d-a662da6ef7c9)

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/fd20c07a-d2a2-45e7-b1ab-0ddb647dafa9)

`Jarkom2023{k0w4lski_0274_SmCyNPvmADv_4nalys1s}`

## **Soal 6**

>	Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

Dapat dilihat di soal bahwa terdapat keanehan dalam kapitalisasi huruf. Jika dilihat huruf kapital saja maka akan didapatkan kalimat “SUBSTITUSI SOURCE ADDRESS 7812”. Kemudian terdapat klue selanjutnya yaitu “a1 e5 u21” yang merupakan enkripsi “a1z26”. Untuk melihat _source address_ dari paket dengan nomor 7812 dapat menggunakan _go to packet_ (Ctrl + G) dan memasukkan nomor 7812.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/a19af6bb-d75b-4fd8-a458-fe0b6faadc6c)

Kemudian dengan menggunakan kakas bantuan seperti CyberChef untuk melakukan dekripsi pada _source address_.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/683b400c-8bf6-4474-a4fa-e9972626ecd6)

Setelah itu, akan dicoba memasukkan hasil dekripsi pada netcat _instance_.

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/c883545b-4665-43c0-8887-c96dd50057e3)

`Jarkom2023{h3h3_ctf_d1k1t_a0KQ02DJ314FY5Q2I4kx}`

## **Soal 7**

>	Berapa jumlah packet yang menuju IP 184.87.193.88?

Dapat menggunakan kueri filter `ip.dst == 184.87.193.88`.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/5ce26de2-5703-4203-83c2-843ee3963750)

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/10fcc452-6b17-4b2a-b128-eacb20a7e3df)

`Jarkom2023{8mIImHW15HGJ3z2zR4_4n0th3r_f1lt3ring}`

## **Soal 8**

> Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

Dapat menggunakan kueri filter `tcp.port == 80 || udp.port == 80`.

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/5d79bcbf-8f36-4df1-93df-bacd62af0af8)

`Jarkom2023{qu3ryyyyying_863911_QkBgQzAjCwR_15_fun}`

## **Soal 9**

> Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

Dapat menggunakan kueri filter `ip.src == 10.51.40.1 && ip.dst != 10.39.55.34`.

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/0811d0d6-9a99-4a18-8ab4-f17f4ad0e8ca)

`Jarkom2023{y3s_its_OlSlNiPjPlQ_qu3ry1ng}`

## **Soal 10**

> Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

Dapat kueri filter dengan menggunakan beberapa wordlist yang mengindikasikan kredensial, seperti `username`, `password`, `login`. Di sini ditemukan ketika menggunakan kueri filter `telnet contains “Login”`.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/11f3ab27-b992-4820-9124-b4a801245212)

Kemudian _follow TCP stream_ dan lihat kredensial username dan password nya.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/be226dbf-47a8-466f-9520-8f01fd5b98cc)

Agar lebih jelas dapat dipisah percakapan dari 172.16.0.254:43964 ke 172.16.0.4:23.

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/5dcb68e7-b188-43fe-b79d-403abd6d7646)

> Flag

![image](https://github.com/mvinorian/Jarkom-Modul-1-A01-2023/assets/54766683/b8be70a7-a032-4054-8b3b-987128cf2b23)

`Jarkom2023{t3lnet_is_CBA4ByCyy54Cz6z18_N0tSecu2e}`

</div>
