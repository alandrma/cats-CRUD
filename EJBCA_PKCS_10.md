# **Phoronix Test Suite**

### **The Phoronix Test Suite adalah platform pengujian dan benchmarking paling komprehensif yang tersedia yang menyediakan kerangka kerja yang dapat diperluas untuk pengujian baru yang dapat dengan mudah ditambahkan. Perangkat lunak ini dirancang untuk secara efektif melakukan benchmark kualitatif dan kuantitatif dengan cara yang bersih, dapat direproduksi, dan mudah digunakan. The Phoronix Test Suite dapat digunakan hanya untuk membandingkan kinerja komputer atau dapat digunakan dalam organisasi Anda untuk tujuan jaminan kualitas internal, validasi perangkat keras, dan integrasi berkelanjutan / manajemen kinerja.**

## *Requirements*
A working install of one of the supported distributions with root privileges and the latest graphics drivers installed.

## **Langkah Instalasi Phoronix Test Suite**
Ubuntu/Debian
Head over to the Phoronix Test Suite [download page](https://www.phoronix-test-suite.com/?k=downloads), and grab the latest .deb package.

When you have the package, install it with gdebi.

>`$ sudo apt install gdebi-core`

>`$ sudo gdebi phoronix-test-suite_*.deb`

Optionally, install Steam. If you’re on Debian, enable the non-free repos first.

>`$ sudo apt install steam`

## Penggunaan dasar Phoronix Test Suite
Rangkaian pengujian Phoronix memiliki banyak pengujian. Untuk melihat semua tes kita akan menjalankan perintah:

>`$ phoronix-test-suite`


Untuk mendapatkan list dari test
>`$ phoronix-test-suite list-tests`


Mendapatkan informasi tentang test atau suite tertentu
>` $ phoronix-test-suite info [test]`

View the included documentation or visit https://www.phoronix-test-suite.com/ for full details.


## Langkah Stress Test

Dalam pengujian kali ini akan melakukan sebuah uji terhadap OpenSSL dan juga SQlite. Pertama lakukan langkah instalasi terhadap test suite-nya. Dengan menambahkan perintah 

>phoronix-test-suite install [Test | Suite | OpenBenchmarking ID | Test Result]

Berikut perintah untuk menginstall paket test dari OpenSSL dan SQlite

>` $ phoronix-test-suite install pts/openssl`

>` $ phoronix-test-suite install pts/sqlite`

Selanjutnya perintah untuk menjalankan test yang sudah diinstall sebelumnya

>phoronix-test-suite run [Test | Suite | OpenBenchmarking ID | Test Result]

>` $ phoronix-test-suite run pts/openssl`

>` $ phoronix-test-suite run pts/sqlite`

Setelah-nya hasil dari benchmark yang dijalankan sebelumnya dapat diakses melalui website yang nantinya dapat di export 

Berikut hasil dari benchmark OpenSSl dan Sqlite

OpenSSL :

<a href="https://ibb.co/WcQnvjS"><img src="https://i.ibb.co/JzNnjgX/Screenshot-from-2022-04-04-12-10-28.png" alt="Screenshot-from-2022-04-04-12-10-28" border="0"></a>
<a href="https://ibb.co/hBgVNdP"><img src="https://i.ibb.co/jy8DYwc/Screenshot-from-2022-04-04-12-10-41.png" alt="Screenshot-from-2022-04-04-12-10-41" border="0"></a>
<a href="https://ibb.co/h7KTTLn"><img src="https://i.ibb.co/ZLhbbGw/Screenshot-from-2022-04-04-12-10-56.png" alt="Screenshot-from-2022-04-04-12-10-56" border="0"></a>

SQlite:

<a href="https://ibb.co/dg5PkL9"><img src="https://i.ibb.co/2Nkvcs2/Screenshot-from-2022-04-04-11-21-35.png" alt="Screenshot-from-2022-04-04-11-21-35" border="0"></a>
<a href="https://ibb.co/TcQC7n0"><img src="https://i.ibb.co/0q0w6W9/Screenshot-from-2022-04-04-11-21-48.png" alt="Screenshot-from-2022-04-04-11-21-48" border="0"></a>
<a href="https://ibb.co/LPmQfBv"><img src="https://i.ibb.co/dcFbyX7/Screenshot-from-2022-04-04-11-21-59.png" alt="Screenshot-from-2022-04-04-11-21-59" border="0"></a>
<a href="https://ibb.co/GvW7xpy"><img src="https://i.ibb.co/mC9JDTk/Screenshot-from-2022-04-04-11-22-10.png" alt="Screenshot-from-2022-04-04-11-22-10" border="0"></a>
<a href="https://ibb.co/dB2FXR7"><img src="https://i.ibb.co/H7z6RjX/Screenshot-from-2022-04-04-11-22-22.png" alt="Screenshot-from-2022-04-04-11-22-22" border="0"></a>




Jalankan start results viewer atau show results berdasarkan nama 
>phoronix-test-suite start-result-viewer

atau bisa juga dengan menjalankan

>phoronix-test-suite show-result [nama test yang telah disimpan sebelumnya]

>` $ phoronix-test-suite show-result openssl-test`

<a href="https://ibb.co/BBMPc3g"><img src="https://i.ibb.co/gJK7m9D/Screenshot-from-2022-04-04-11-29-49.png" alt="Screenshot-from-2022-04-04-11-29-49" border="0"></a>

Untuk menganalisa hasil test dapat dibuka dengan menjalankan perintah berikut 

>phoronix-test-suite [Nama Result Analysis] [Nama test result]

RESULT ANALYSIS

    analyze-run-times      [Test Result] 
    executive-summary      [Test Result] 
    result-file-confidence [Test Result] 
    result-file-stats      [Test Result] 
    wins-and-losses        [Test Result] 
    workload-topology      [Test Result]
    
Selain itu, hasil benchmark dapat di eksport melalui web ataupun command.

>phoronix-test-suite [Nama Result Eksport] [Nama test result]

RESULT EXPORT

    result-file-raw-to-csv [Test Result] 
    result-file-to-csv     [Test Result] 
    result-file-to-html    [Test Result] 
    result-file-to-json    [Test Result] 
    result-file-to-pdf     [Test Result] 
    result-file-to-suite   [Test Result] 
    result-file-to-text    [Test Result] 


Refrensi :
- https://linuxconfig.org/benchmark-your-graphics-card-on-linux
- https://github.com/phoronix-test-suite/phoronix-test-suite/blob/master/documentation/phoronix-test-suite.md
