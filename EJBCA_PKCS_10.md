# **Phoronix Test Suite**

### **The Phoronix Test Suite adalah platform pengujian dan benchmarking paling komprehensif yang tersedia yang menyediakan kerangka kerja yang dapat diperluas untuk pengujian baru yang dapat dengan mudah ditambahkan. Perangkat lunak ini dirancang untuk secara efektif melakukan benchmark kualitatif dan kuantitatif dengan cara yang bersih, dapat direproduksi, dan mudah digunakan. The Phoronix Test Suite dapat digunakan hanya untuk membandingkan kinerja komputer atau dapat digunakan dalam organisasi Anda untuk tujuan jaminan kualitas internal, validasi perangkat keras, dan integrasi berkelanjutan / manajemen kinerja.**

### *Requirements*
A working install of one of the supported distributions with root privileges and the latest graphics drivers installed.

### **Installation Step Phoronix Test Suite**
Ubuntu/Debian
Head over to the Phoronix Test Suite [download page](https://www.phoronix-test-suite.com/?k=downloads), and grab the latest .deb package.

When you have the package, install it with gdebi.

>`$ sudo apt install gdebi-core`

>`$ sudo gdebi phoronix-test-suite_*.deb`

Optionally, install Steam. If you’re on Debian, enable the non-free repos first.

>`$ sudo apt install steam`

### Penggunaan dasar Phoronix Test Suite
Rangkaian pengujian Phoronix memiliki banyak pengujian. Untuk melihat semua tes kita akan menjalankan perintah:

>`$ phoronix-test-suite

Untuk mendapatkan keseluruhan informasi yang tersedia

>`$ phoronix-test-suite list-tests`
Untuk mendapatkan list dari test

Mendapatkan informasi tentang test atau suite tertentu:

>$ phoronix-test-suite info [test]

### Langkah Stress Test

Dalam pengujian kali ini akan melakukan sebuah uji terhadap OpenSSL dan juga SQlite. Pertama lakukan langkah instalasi terhadap test suite-nya. Dengan menambahkan perintah 

` phoronix-test-suite install [Test | Suite | OpenBenchmarking ID | Test Result]

>` $ phoronix-test-suite install pts/openssl
>` $ phoronix-test-suite install pts/sqlite

` phoronix-test-suite run [Test | Suite | OpenBenchmarking ID | Test Result]

>` $ phoronix-test-suite run pts/openssl
>` $ phoronix-test-suite run pts/sqlite
