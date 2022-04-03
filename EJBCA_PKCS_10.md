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



Pertama yaitu buka aplikasi Postman _(aplikasi untuk melakukan Stress Test)_. Kemudian melakukan import file JSON _(file JSON yang sudah disediakan sebelumnya)_ ke dalam aplikasi Postman.

> Pilih **_File_** > **_Import_** > **_Upload Files_** > pilih **JSON file yang akan digunakan**

![Upload File](https://i.ibb.co/DrwXRYq/1.png "Upload file di aplikasi postman")


Setelah mengimport JSON file diatas, maka akan muncul tampilan seperti gambar dibawah ini dan kemudian dapat melanjutkan tahap berikut:

> Pilih **_Collections_** > **_Add User Direct_ EJBCA pkcs10** > **_Body_** > lalu **isi data-data sesuai dengan kebutuhan** > **_Save_**

![Upload File](https://i.ibb.co/WWdYn4q/2.png "Upload file di aplikasi postman")

Selanjutnya dapat melakukan tahap berikut:

> Pilih **_File_** > **_New Runner Tab_** > pilih **_Add User Direct_ EJBCA** > kemudian **_Drag Add User Direct_ EJBCA** ke bagian **_RUN ORDER_** > lalu hanya _checklist_ bagian **_Add User Direct_ EJBCA PKCS10 UAT** > **_Iterations_** _(sesuaikan dengan kebutuhan)_ > kemudian **_Run_ EJBCA UAT**

![Run EJBCA](https://i.ibb.co/BLdWN5q/3.png "Run EJBCA")

Setelah melakukan **_Run_ EJBCA UAT**, maka akan tampil hasil Stress Test dengan beberapa kali percobaan pada **“_Add User Direct_ EJBCA pkcs10 UAT”** dengan status **“200 OK”** yang berarti proses Stress Test selesai. 

![Proses Stress Test](https://i.ibb.co/hY2ds06/4.png "proses stress test selesai")


Kemudian tidak lupa _screenshoot_ hasil proses _Stress Test_ nya dan atau **_Export Results_** nya untuk bahan pengisian laporan **_Stress Test_**.

## **STRESS TEST REPORT**

### **STRESS TEST REPORT - 2 USER 22 CONCURENT**
> #### **PROSES INFORMATION**
> |                |                             |
> | -----          | --------------------------- |
> | Operation Name | Add User Direct EJBCA PKCS10 UAT |
>
> #### **STRESS TEST PARAMETER**
> |                                 |           |
> | -----                           | ---       |
> | Start Date	                    | 17 Desember 2021 |
> | Delay Request	                | 0 s       |
> | Number of Iterations	        |22         |
> | Duration	                    | 11,8 s |
> | Successful Inspection Rate	    | 100% (22/22) |
> | Unsuccessful Inspection Rate	|Transaction rolled back => (0/22) |
> #### **ITERATION DURATION**
> |         |           |         |
> | -----   | ---       | ---     |
> | Avg	    | Min	    | Max     |
> | 1,06 s	| 0,956 s	| 1,163 s |
> #### **DETAIL SCENARIO (STAGES)**
> |                 |          |
> | -----           | ---      |
> | Value	        | Duration |
> | 22 iterations	| 11,8 s   |
> #### **TPS Scenario**
> |         |            |    
> | -----   | ---        |
> | Value	| Iterations |
> | 2 TPS	| 22         |

![Stress Test Report](https://i.ibb.co/L1yBmgz/1.jpg "Stress Test Report - 2 User 22 Concurents")

### **STRESS TEST REPORT - 2 USER 200 CONCURENT**
> #### **PROSES INFORMATION**
> |                |                             |
> | -----          | --------------------------- |
> | Operation Name | Add User Direct EJBCA PKCS10 UAT |
>
> #### **STRESS TEST PARAMETER**
> |                                 |                        |
> | -----                           | ---                    |
> | Start Date	                    | 17 Desember 2021       |
> | Delay Request	                | 0 s                    |
> | Number of Iterations	        | 200                    |
> | Duration	                    | 106,9 s                |
> | Successful Inspection Rate	    | 100% (200/200)         |
> | Unsuccessful Inspection Rate	|Transaction rolled back => (0/200) |
> #### **ITERATION DURATION**
> |         |           |         |
> | -----   | ---       | ---     |
> | Avg	    | Min	    | Max     |
> | 1,06 s	| 0,784 s	| 1,382 s |
> #### **DETAIL SCENARIO (STAGES)**
> |                 |          |
> | -----           | ---      |
> | Value	        | Duration |
> | 200 iterations	| 106,9 s  |
> #### **TPS Scenario**
> |         |            |    
> | -----   | ---        |
> | Value	| Iterations |
> | 2 TPS	| 200        |

![Stress Test Report](https://i.ibb.co/HntsS70/2.jpg "Stress Test Report - 2 User 200 Concurents")

### **STRESS TEST REPORT - 2 USER 1800 CONCURENT**
> #### **PROSES INFORMATION**
> |                |                             |
> | -----          | --------------------------- |
> | Operation Name | Add User Direct EJBCA PKCS10 UAT |
>
> #### **STRESS TEST PARAMETER**
> |                                 |                        |
> | -----                           | ---                    |
> | Start Date	                    | 17 Desember 2021       |
> | Delay Request	                | 0 s                    |
> | Number of Iterations	        | 1400                   |
> | Duration	                    | 391,517 s              |
> | Successful Inspection Rate	    | 0,928% (13/1400)       |
> | Unsuccessful Inspection Rate	|Transaction rolled back => (1387/1400) |
> #### **ITERATION DURATION**
> |         |           |         |
> | -----   | ---       | ---     |
> | Avg	    | Min	    | Max     |
> | 3,785 s	| 0,432 s	| 7,814 s |
> #### **DETAIL SCENARIO (STAGES)**
> |                 |          |
> | -----           | ---      |
> | Value	        | Duration |
> | 1400 iterations	| 391,517 s|
> #### **TPS Scenario**
> |         |            |    
> | -----   | ---        |
> | Value	| Iterations |
> | 14 TPS	| 1400       |

![Stress Test Report](https://i.ibb.co/ckTRyKg/3.jpg "Stress Test Report - 2 User 1800 Concurents")

