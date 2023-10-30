
## Intro 
- 

## Latar Belakang 
Dalam era modern, orang tua menghadapi tantangan besar dalam memantau dan memahami perkembangan anak-anak mereka. Dengan gaya hidup yang sibuk, komunikasi yang kurang dan perjalanan harian yang sering tidak terawasi, muncul kebutuhan akan solusi yang dapat memberikan pemantauan yang lebih efektif terhadap anak-anak. Dalam konteks ini, saya mengusulkan Inovasi SecureKids Aplikasi Mobile Pemantau Anak yang akan membantu orang tua memantau anak-anak mereka dengan lebih efisien dan efektif.

## Branding 
Pada tahap ini kita mengeksplorasi *branding* dari produk UbiCom yang dibuat. Contoh:
- Merk: **SecureKids** 
- Inspirasi merk: SecureKids merujuk pada keselamatan dan keamanan anak-anak. Ini mencerminkan fokus produk pada melindungi anak-anak dan memberikan rasa aman kepada orang tua.
- Tagline: Pemantau Anak Cerdas, Keselamatan Prioritas
- Campaign: 
- Target user:
  - Seorang ayah/ ibu
  - Sibuk dan tidak punya waktu memantau anak
  - Khawatir dengan tumbuh kembang anak
  - Ingin mengawasi seluruh perkembangan anak
- User experience theme:
  - Aplikasi Mobile Android

## User Story
Pada tahap ini kita mengeksplorasi kebutuhan prioritas dari para pengguna untuk kita wujudkan sebagai fitur pada sistem atau aplikasi yang akan dibuat.
User story [[1]](https://www.mountaingoatsoftware.com/agile/user-stories) memudahkan kita membuat prioritas fitur-fitur untuk dikerjakan untuk jangka waktu tertentu.

|Sebagai|Saya ingin bisa|Sehingga|Prioritas
|---|---|---|---|
|Sebagai pengembang sistem|saya ingin memastikan bahwa sistem dapat melakukan pemrosesan data suara|sehingga sistem dapat mendeteksi kata-kata kunci yang mencurigakan dalam percakapan anak.|⭐⭐⭐⭐⭐|
|Sebagai pengembang sistem|&raquo; saya ingin mengintegrasikan sensor GPS ke dalam perangkat pemantauan anak |sehingga saya dapat melacak lokasi anak dengan akurat.|⭐⭐⭐⭐⭐|
|Sebagai pengembang sistem|&raquo; saya ingin memastikan sistem dapat mengirim data lokasi anak ke server cloud secara real-time melalui koneksi yang aman|sehingga saya dapat menampilkan data response dan diproses menggunakan algoritma/AI lalu ditampilkan dalam bentuk laporan difront-end|⭐⭐⭐|
|Sebagai pengembang sistem|&raquo; Mengatur Lock Aplikasi, Artinya orang tua bisa mengunci aplikasi dalam kurun waktu tertentu |Anak bisa kurang dalam bermain game/aplikasi yang tidak berguna|⭐⭐⭐⭐|
|Sebagai pengembang sistem|&raquo; Menampilkan banyaknya waktu bermain sebuah aplikasi |Bisa memantau waktu bermain anak|⭐⭐⭐⭐⭐|
|Sebagai pengembang sistem|menampilkan kata kunci atau apa saja yang anak ketik pada search engine seperti google atau yang lainnya |Orang tua  bisa lebih terbantu dalam memonitoring anak|⭐⭐⭐⭐⭐|

## Metode dan Algoritma 
- Pemrosesan Data Suara: Untuk mendeteksi kata-kata kunci yang mencurigakan dalam percakapan anak, menggunakan metode pemrosesan data suara dan algoritma pemrosesan bahasa alami (Natural Language Processing - NLP). Data suara diperoleh dari sensor mic pada hp android, ini akan memungkinkan sistem untuk menganalisis dan mengenali kata-kata yang tidak sesuai atau berpotensi berbahaya yang diucapkan oleh anak.
- Pelacakan Lokasi: Untuk melacak lokasi anak dengan akurat, saya akan menggunakan GPS (Global Positioning System) pada perangkat anak. Algoritma pelacakan akan memungkinkan saya untuk mendapatkan data lokasi secara real-time dan mengirimkannya ke server pusat.
- Report lokasi harian, menampilkan rekapan lokasi anak kemana saja
- Report Kata-kata anak yang diucapkan, menampilkan rekapan kata2 anak dari algortima NLP
- Pengaturan Lock Aplikasi: Untuk mengatur waktu akses dan pembatasan aplikasi, sistem akan menggunakan algoritma manajemen waktu dan akses. Orang tua akan dapat mengunci akses ke aplikasi dalam kurun waktu tertentu.
- Pemantauan Aktivitas Anak: Kami akan menggunakan algoritma pemantauan waktu bermain dan aktivitas anak. Ini akan memungkinkan sistem untuk melacak berapa lama anak bermain aplikasi tertentu dan memberikan laporan kepada orang tua.
- Analisis Pencarian dan Aktivitas Online: Untuk menganalisis kata kunci dan apa yang anak ketik pada mesin pencarian seperti Google

## Database Design

## Arsitektur Sistem 
![Untitled Diagram drawio (2)](https://github.com/romijatmiko/romijatmiko.github.io/assets/71611488/35082c71-6f3d-4298-bdf8-f94a4f65808d)
## Deskripsi Teknologi 
Pada tahap ini kita menjelaskan setiap teknologi hardware dan software yang digunakan dalam pembangunan sistem. Contoh:
- Mesin komputasi
  - Cloud server: AWS EC2 Debian.
  - Smart phone: Android Only
- Database
  - PostgreSQL
- Software development
  - Mobile Front End: Kotlin.
  - Backend stack: Belum Fix, tapi pastinya menggunakan bahasa python.
- Sensor 
  - Mic: Default dari hp
  - GPS: Default dari hp
- Responder 

## User Experience (UX) Design 
[figma](https://www.figma.com/file/25X3nEDWY43rm7T8f03P2c/Untitled?type=design&node-id=0%3A1&mode=design&t=tARznfszltsGoiyb-1)
