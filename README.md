# AB-Testing

Kasus yang akan digunakan adalah membuka akun deposit untuk nasabah bank. Pada kesempatan kali ini data scientist diminta tolong untuk menganalisa hasil ab-testing suatu perusahaan bank. Apakah jumlah campaign mampu meningkatkan keinginan user untuk membuka akun deposit atau tidak?

Data yang digunakan berasal dari folder bank.zip file yang digunakan 
adalah bank-full.csv

1. Untuk variabel jumlah campaign bisa dicek untuk kolom campaign 
2. untuk variabel apakah akhirnya user membuka akun atau tidak bisa menggunakan variabel y

### 1. Pemahaman konsep A/B Testing
#### a. Apa nama experimentnya? [![paypal.me/anuraghazra]
menganalisis dengan AB Testing mengenai pengaruh jumlah campaign terhadap keinginan user untuk membuka akun deposit atau tidak.

#### b. Definisikan Hipotesis
semakin banyak campaign yang dilakukan terhadap user maka kemungkinan user akan membuka akun semakin tinggi.

#### c. Siapa participant-nya?
User (nasabah bank)

#### d. Variabel yang akan diuji apa?
Jumlah campaign 

#### e. Metrics apa yang akan digunakan?
**Macroconversions:** jumlah campaign per nasabah
**Microconversions:** jumlah nasabah yang diberi campaign

#### f. Berapa sample size dan durasi experiment?
Jumlah **sample size** yang dibutuhkan ada **400 sample**, dengan 200 untuk group yang yes dan 200 untuk gruop yang no. Sedangkan untuk **durasi experiment akan dilakukan selama 7 hari**

### 2. Pengujian Hipotesis
#### a. Penentuan hipotesis
Apakah jumlah campaign mampu meningkatkan keinginan user untuk membuka akun deposit atau tidak?

H0: rata-rata jumlah campaign user/nasabah yang membuka akun **sama** dengan yang tidak membuka akun  <br>
H1: rata-rata jumlah campaign user/nasabah yang membuka akun **berbeda** dengan yang tidak membuka akun

#### b. Pengujian yang digunakan
menggunakan T-test untuk kategori **membuka akun (yes)** dan **tidak membuka akun (no)**. 

#### c. Deteksi asumsi beserta cara penanganannya
rata-rata untuk kategori yang membuka akun: 2.1410474569861977
rata-rata untuk kategori yang tidak membuka akun: 2.8463503832473322

#### d. Hasil pengujian hipotesis
P-Value : 9.742452436952554e-72
Tidak cukup bukti jumlah campaign bisa bedakan user untuk membuka akun atau tidak membuka akun

#### e. Kesimpulan dan interpretasi
Hasil uji hipotesis menunjukkan bahwa **p-value < alpha**, sehingga jumlah campaign dapat berpengaruh terhadap user/nasabah untuk membuka akun atau tidak membuka akun. akan tetapi jika dilihat dari **rata-rata grafik distribusi campaign per kategori** ternyata semakin banyak campaign yang diberikan user akan semakin menolak membuka akun. sehingga jumlah campaign memiliki hubungan yang berbanding terbalik dengan user yang ingin membuka akun (semakin sedikit campaign maka user yang ingin membuka akun banyak begitu juga jika banyak campaign maka user sedikt yang ingin membuka akun).


