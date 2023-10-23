
## Intro 
- Artikel ini membahas contoh dokumen pembangunan teknologi UbiCom dengan tema Automatic Mental and Physical Refreshment using Smart Home Technologies 

## Latar Belakang 
Dalam era modern, orang tua menghadapi tantangan besar dalam memantau dan memahami perkembangan anak-anak mereka. Dengan gaya hidup yang sibuk, komunikasi yang kurang dan perjalanan harian yang sering tidak terawasi, muncul kebutuhan akan solusi yang dapat memberikan pemantauan yang lebih efektif terhadap anak-anak. Dalam konteks ini, saya mengusulkan Inovasi SecureKids Aplikasi Mobile Pemantau Anak yang akan membantu orang tua memantau anak-anak mereka dengan lebih efisien dan efektif.

## Branding 
Pada tahap ini kita mengeksplorasi *branding* dari produk UbiCom yang dibuat. Contoh:
- Merk: **SecureKids** 
- Inspirasi merk: SecureKids merujuk pada keselamatan dan keamanan anak-anak. Ini mencerminkan fokus produk pada melindungi anak-anak dan memberikan rasa aman kepada orang tua.
- Tagline: Pemantau Anak Cerdas, Keselamatan Prioritas
- Campaign: Bagaimana menjadikan rumah / kostan / kontrakan dan perangkat wearable yang dimiliki sebagai pendukung penyegaran kondisi mental dan fisik
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
Pada tahap ini kita menjelaskan metode dan algoritma yang digunakan pada setiap komponen teknologi UbiCom. Contoh:
- Sensor:
  - Face recognition: MobileNet. penjelasan . . .
  - Expression recognition: MobileNet. penjelasan . . .
  - Gesture recognition: YOLOv7. penjelasan . . .
  - Speech recognition: PANN. penjelasan . . .
  - Fuzzy logic
- Responder:
  - Speech synthesis: ASGAN
  - Fuzzy logic
- Mobile software development
- Edge software development

## Struktur Data 
Pada tahap ini kita mengeksplorasi struktur data yang digunakan pada teknologi UbiCom. Contoh:

<pre class="mermaid">
erDiagram
  PENGGUNA {
    int id_pengguna
    string username
    string email
    string password
    string nama_lengkap
    vector model_wajah
  }
  PENGGUNA ||--o{ KONDISI : dideteksi 
  KONDISI {
    int id_kondisi
    int id_pengguna
    int id_tipe_kondisi
    datetime waktu_deteksi
  }
  KONDISI ||--o{ RESPON : diberikan 
  RESPON {
    int id_respon
    int id_kondisi
    int id_tipe_respon
    json konten_respon
    datetime waktu_respon
  }
</pre>
- Pada tahap ini kita mengeksplorasi dan menganalisis bentuk struktur data yang mampu memfasilitasi *user story* yang ada, maupun yang kemungkinan besar dibutuhkan di kemudian hari
- Kita akan merepresentasikan Entitas pada aplikasi dalam bentuk tabel Entitas dan Atribut

## Arsitektur Sistem 
<pre class="mermaid">
flowchart BT 
  subgraph cloud server
    WS1[Web service: Python] <--> BE1[Database: PostgreSQL]
  end

  subgraph edge server: Raspberry Pi
    BE2[Program Deteksi: Python] 
    BE3[Program Respon: Python] 
    BE2 --> BE4[Broker: NATS]
    BE3 <--> BE4
    BE4 <--> BE5[Cloud communicator: Python]
    BE5 --> WS1
  end

  subgraph mobile phone 
    MA1[Mobile app: Flutter] <--> WS1
  end

  subgraph sensors 
    S1[CCTV] --> BE2 
    S2[Mic] --> BE2 
    S3[Sensor] --> BE2 
  end
  subgraph responders 

    BE3 --> R1[Speaker] 
    BE3 --> R2[Lampu] 
  end
</pre>
Pada tahap ini kita merancang arsitektur berikut teknologi yang terdapat pada setiap komponen pembentuk aplikasi.

## Deskripsi Teknologi 
Pada tahap ini kita menjelaskan setiap teknologi hardware dan software yang digunakan dalam pembangunan sistem. Contoh:
- Mesin komputasi
  - Edge server: Raspberry Pi. Penjelasan . . .
  - Cloud server: AWS EC2 Debian. Penjelasan . . . 
  - Smart phone: Android & iPhone. Penjelasan . . .
- Software development
  - Mobile development: Flutter. Penjelasan . . .
  - Backend developer: FastAPI. Penjelasan . . .
  - PubSub: NATS. Penjelasan . . .
- Sensor 
  - CCTV: Merk. Penjelasan . . .
  - Mic: Merk. Penjelasan . . .
  - Sensor temperature: Merk. Penjelasan . . .
  - Web service cuaca: URL. Penjelasan . . .
- Responder 
  - Mic: Merk. Penjelasan . . .
  - Lampu: Merk. Penjelasan . . .

## User Experience (UX) Design 
[figma](https://www.figma.com/file/25X3nEDWY43rm7T8f03P2c/Untitled?type=design&node-id=0%3A1&mode=design&t=tARznfszltsGoiyb-1)
