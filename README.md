# NAMA : Muhammad Shean Elliora Ribah
# NIM : 235150307111045
# Sistem Automasi: Model Matematika Motor DC

Repositori ini berisi kode Python menggunakan library SymPy untuk memodelkan dan menganalisis sistem motor DC. Kode ini mencakup tiga bagian utama:

# 1. Model Matematika Motor DC
Kode ini mendefinisikan persamaan listrik dan mekanik yang menggambarkan dinamika motor DC. Persamaan listrik menghubungkan tegangan input, arus, dan kecepatan sudut, sedangkan persamaan mekanik menghubungkan torsi, kecepatan sudut, dan parameter fisik motor.

## > Persamaan Listrik
Persamaan listrik motor DC dinyatakan sebagai:
# ![image](https://github.com/user-attachments/assets/8050cec9-4903-4d89-abc4-58718f445065)

Penjelasan:
* V(t): Tegangan input sebagai fungsi waktu
* R: Resistansi armature
* L: Induktansi armature
* i(t): Arus armature sebagai fungsi waktu
* Ke: Konstanta gaya gerak listrik
* ω(t): Kecepatan sudut motor sebagai fungsi waktu

## > Persamaan Mekanik
Persamaan mekanik motor DC dinyatakan sebagai:
# ![image](https://github.com/user-attachments/assets/72fab6a8-f433-4f8f-9beb-79fab34a3f95)

Penjelasan:
* J: Momen inersia rotor
* B: Koefisien gesekan viscous
* Kt: Konstanta torsi motor
* ω(t): Kecepatan sudut motor sebagai fungsi waktu
* i(t): Arus armature sebagai fungsi waktu


# Transformasi Laplace pada Motor DC
Bagian ini melakukan transformasi Laplace pada persamaan listrik dan mekanik untuk menganalisis sistem dalam domain frekuensi. Transformasi Laplace memungkinkan kita untuk mempelajari respons sistem terhadap input yang bervariasi terhadap waktu.

Transformasi Laplace digunakan untuk mengubah persamaan diferensial dalam domain waktu ke domain frekuensi (domain s).

## > Persamaan Listrik dalam Domain Laplace
# ![image](https://github.com/user-attachments/assets/779dd2d5-ba56-4f67-9c12-f6a816776b83)

Penjelasan:
* V(s): Transformasi Laplace dari tegangan input
* I(s): Transformasi Laplace dari arus armature
* Ω(s): Transformasi Laplace dari kecepatan sudut

## > Persamaan Mekanik dalam Domain Laplace
# ![image](https://github.com/user-attachments/assets/6806e957-27f3-483b-b7b0-36bebf8015c8)

Penjelasan:
* Ω(s): Transformasi Laplace dari kecepatan sudut
* I(s): Transformasi Laplace dari arus armature

# Fungsi Alih Hubungan antara Kecepatan Sudut (ω) terhadap Tegangan (V)
Kode ini menghitung fungsi alih yang menghubungkan kecepatan sudut motor (ω) dengan tegangan input (V). Fungsi alih ini berguna untuk merancang kontroler dan menganalisis stabilitas sistem.

Fungsi alih Ω(s) / V(s) menggambarkan hubungan antara kecepatan sudut motor (ω) dan tegangan input (V) dalam domain Laplace. Fungsi alih ini dihitung dengan menyelesaikan persamaan listrik dan mekanik dalam domain Laplace

Fungsi Alih:
# ![image](https://github.com/user-attachments/assets/cfdfc299-ddba-44f1-b83d-1ad20106612a)

Penjelasan:
* Ω(s): Transformasi Laplace dari kecepatan sudut
* V(s): Transformasi Laplace dari tegangan input
* Kt: Konstanta torsi motor
* R: Resistansi armature
* L: Induktansi armature
* J: Momen inersia rotor
* B: Koefisien gesekan viscous
* Ke: Konstanta gaya gerak listrik
