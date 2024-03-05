<p align="center">
  <img width="1000" height="450" src="[https://github.com/rifdanlabibah/MDS-7/assets/90300127/aa5a1493-5982-407c-a43f-8aad18ce62f5](https://github.com/rifdanl/MDS-Kelompok-7/assets/162286538/ca8bfc89-373f-4c3d-9ce5-c3c2021cdd53)">
</p>

<div align="center">

# Database Histori Pertandingan NBA

[Tentang](#scroll-tentang)
•
[Screenshot](#rice_scene-screenshot)
•
[Demo](#dvd-demo)
•
[Dokumentasi](#blue_book-dokumentasi)

</div>

**Halo Basketball Lovers! Selamat datang di "Hoops Historia"**
Sebuah platform bagi para basketball lovers yang haus akan informasi yang mendalam dan terperinci! Di sini, kami hadir untuk memberikan Anda akses eksklusif ke sejumlah informasi penting tentang sejarah pertandingan bola basket profesional Amerika.

**Apakah Anda penggemar setia NBA??** 
Hoops Historia menyediakan informasi lengkap tentang pertandingan-pertandingan yang tak terlupakan. Dari tanggal pertandingan hingga informasi tentang tim yang bertanding, kami menampilkan statistik yang lengkap, termasuk skor per quarter, serta informasi tentang arena tempat pertandingan berlangsung beserta kapasitasnya.

**Atau Anda baru ingin mengenal NBA?**
Bagi Anda yang ingin mengenal lebih dalam tentang tim-tim di NBA, Hoops Historia menawarkan gambaran lengkap tentang setiap tim yang bersaing di lapangan. Dari nama tim hingga kota asalnya, kami menyajikan informasi tentang sejarah berdirinya tim, lengkap dengan nama panggilan khas yang membuatnya ikonik. Tidak hanya itu, Anda juga dapat melihat detail tentang manajemen tim, termasuk nama general manager dan head coach yang bertanggung jawab atas strategi dan kinerja tim. Informasi tentang arena tempat tim bermain dan pemilik tim juga tersedia, memberikan Anda pemahaman yang lebih baik tentang identitas dan budaya di balik setiap tim.

Jadi, apakah Anda seorang penggemar setia yang ingin menggali lebih dalam tentang pertandingan atau penggemar baru yang ingin mengenal lebih dekat tim-tim yang berkompetisi, Hoops Historia hadir untuk memenuhi semua kebutuhan informasi Anda. Selamat menikmati perjalanan Anda dalam menjelajahi dunia basket melalui Hoops Historia

## :bookmark_tabs: Menu

- [Tentang](#scroll-tentang)
- [Screenshot](#rice_scene-screenshot)
- [Demo](#dvd-demo)
- [Dokumentasi](#blue_book-dokumentasi)
- [Requirements](#exclamation-requirements)
- [Skema Database](#floppy_disk-skema-database)
- [ERD](#rotating_light-erd)
- [Deskripsi Data](#heavy_check_mark-deskripsi-data)
- [Struktur Folder](#open_file_folder-struktur-folder)
- [Tim Pengembang](#smiley_cat-tim-pengembang)

## :scroll: Tentang
Hoops Historia akan memberikan penggemar basketball akses yang mudah dan terperinci ke sejarah dan statistik pertandingan NBA serta informasi lengkap tentang setiap tim dalam liga. Melalui penyajian data yang akurat dan terkini, dashboard ini bertujuan untuk memenuhi kebutuhan pengetahuan penggemar dalam menjelajahi perjalanan panjang dan dinamika kompetisi bola basket profesional Amerika. Dengan demikian, Hoops Historia berfungsi sebagai sumber informasi terpercaya dan komprehensif bagi mereka yang ingin memahami dengan lebih baik aspek-aspek kunci dalam dunia NBA.



## :rice_scene: Screenshot

<p align="center">
  <img width="900" height="500" src="https://github.com/rifdanl/MDS-Kelompok-7/assets/162286538/e4f29c53-8276-40da-9b5c-8ba6fd203127">
</p>

## :dvd: Demo

Berikut merupakan link untuk shinnyapps atau dashboard dari project kami:


## :blue_book: Dokumentasi 

Dokumentasi penggunaan aplikasi database. Anda dapat juga membuat dokumentasi lives menggunakan readthedocs.org (opsional).

## :exclamation: Requirements

- Data diperoleh dari dataset NBA Database dari (link https://ln.run/Xuahj) dengan mengambil data 65,000+ pertandingan sejak 1946  
- RDBMS yang digunakan adalah PostgreSQL dan ElephantSQL
- Dashboard menggunakan `shinny`, `shinnythemes`, `bs4Dash`, `DT`, dan `dplyr` dari package R

## :floppy_disk: Skema Database

Menggambarkan struktur *primary key* **line score**, **game**, **team details** dan **team** dengan masing-masing *foreign key* dalam membangun relasi antara tabel atau entitas.
<p align="center">
  <img width="600" height="400" src="https://github.com/rifdanlabibah/MDS-7/assets/90300127/6f84f676-b6bb-4810-8ab7-f69ebb231167">
</p>


## :rotating_light: ERD

ERD (Entity Relationship Diagram) menampilkan hubungan antara entitas dengan atribut. Pada project ini, entitas line score terdapat dua atribut yang berhubungan dengan atribut pada entitas lain, yaitu game_id berhubungan dengan entitas game, team_id berhubungan dengan entitas team.

Selanjutnya, entitas game terdapat dua atribut yang berhubungan dengan atribut pada entitas lain, yaitu game_id berhubungan dengan entitas line_score, team_id bergubungan dengan entitas team.

Selain itu, entitas team_details dan entitas team saling berhubungan pada team_id id_instansi.

<p align="center">
  <img width="600" height="400" src="https://github.com/rifdanlabibah/MDS-7/assets/90300127/d45cecd1-c842-4190-9691-4b68a5357db4">
</p>

## :heavy_check_mark: Deskripsi Data
Hoops Historia menyajikan informasi lengkap tentang setiap tim yang berkompetisi di liga. Dari tanggal pertandingan hingga skor per kuartal, detail matchup home dan arena tempat pertandingan berlangsung. Selain itu, kami juga menyediakan profil komprehensif tentang setiap tim, mencakup informasi tentang nama, singkatan, kota asal, tahun pendirian, manajemen tim, serta informasi tentang arena tempat tim bermain. 
Berisi tentang tabel-tabel yang digunakan berikut dengan sintaks SQL DDL (CREATE).

### Create Database
Databse Histori Pertandingan NBA menyimpan informasi yang mewakili atribut data yang saling berhubungan untuk kemudian dianalisis.
```sql
CREATE DATABASE kel.7-mds
    WITH
    OWNER = postgres
    ENCODING = 'UTF8'
    CONNECTION LIMIT = -1
    IS_TEMPLATE = False;
```
### Create Table line_score
Tabel "line_score" dalam Hoops Historia menyajikan rincian skor per kuartal dari setiap pertandingan NBA, termasuk game ID untuk mengidentifikasi setiap pertandingan, ID tim untuk menghubungkan dengan entitas tim terkait, singkatan tim, tanggal pertandingan, serta jumlah poin yang dicetak oleh tim tersebut pada setiap kuartal.  Berikut deskripsi untuk setiap tabel line_score.
| Attribute          | Type                  | Description                     |
|:-------------------|:----------------------|:--------------------------------|
| game_id            | VARCHAR(10)           | Game ID                         |
| team_id            | VARCHAR(10)           | Team ID                         |
| abbreviation       | VARCHAR(10)           | Singkatan Team                  |
| game_date          | DATE 	             | Tanggal Pertandingan            |
| pts_qtr1_home      | smallint		     | Skor pada quarter pertama       |
| pts_qtr2_home      | smallint		     | Skor pada quarter kedua         |
| pts_qtr3_home      | smallint		     | Skor pada quarter ketiga        |
| pts_qtr4_home      | smallint		     | Skor pada quarter keempat       |

dengan script SQL sebagai berikut:
```sql
CREATE TABLE IF NOT EXISTS line_score (
    game_id VARCHAR(10),
    team_id VARCHAR(10),
    abbreviation VARCHAR(10),
    game_date DATE,
    pts_qtr1_home SMALLINT,
    pts_qtr2_home SMALLINT,
    pts_qtr3_home SMALLINT,
    pts_qtr4_home SMALLINT,
    FOREIGN KEY (game_id) REFERENCES game(game_id),
    FOREIGN KEY (team_id) REFERENCES team(team_id)
);
```
### Create Table game
Tabel "Game" dalam Hoops Historia menyajikan informasi lengkap tentang setiap pertandingan NBA, termasuk detail matchup home, skor per kuartal, dan tanggal pertandingan.Berikut deskripsi untuk setiap tabel game.
| Attribute          | Type                  | Description                     |
|:-------------------|:----------------------|:--------------------------------|
| game_id            | VARCHAR(10)           | Game ID                         |
| team_id            | VARCHAR(10)           | Team ID                         |
| wl_home            | VARCHAR(10)           | Win-Loss Home                   |
| abbreviation       | VARCHAR(10)           | Singkatan Team                  |
| full_name          | VARCHAR(100)          | Nama Lengkap Team               |
| game_date          | DATE 	             | Tanggal Pertandingan            |
| matchup_home       | VARCHAR(50) 	     | Nama tim yang bertanding        |

dengan script SQL sebagai berikut:
```sql
CREATE TABLE IF NOT EXISTS Game (
    game_id VARCHAR(10) PRIMARY KEY,
    team_id VARCHAR(10),
    wl_home VARCHAR(10),
    abbreviation VARCHAR(10),
    full_name VARCHAR(100),
    game_date DATE,
    matchup_home VARCHAR(50),
    FOREIGN KEY (team_id) REFERENCES Team(team_id)
);
```
### Create Table team_details
Tabel "team_details" dalam database Hoops Historia menyimpan informasi rinci tentang setiap tim yang berpartisipasi dalam kompetisi NBA. Data yang disajikan termasuk detail tentang nama tim, singkatan, nama panggilan, kota asal, tahun pendirian, serta informasi tentang manajemen tim seperti general manager dan head coach. Selain itu, tabel ini juga mencakup detail tentang arena tempat tim bermain, termasuk kapasitasnya. Berikut deskripsi untuk setiap tabel team_details.
| Attribute          | Type                  | Description                                      |
|:-------------------|:----------------------|:-------------------------------------------------|
| team_id            | VARCHAR(10)           | Team ID                                          |
| nickname           | VARCHAR(50)           | Nama panggilan /julukan tim                      |
| arena              | VARCHAR(100)          | Nama arena tempat tim bermain                    |
| arenacapacity      | INT                   | Kapasitas maximum arena dalam menampung penonton |
| owner              | VARCHAR(100)          | Nama pemilik tim                                 |
| generalmanager     | VARCHAR(100)          | Nama general manager tim                         |
| headhcoach         | VARCHAR(100)          | Nama pelatih utama tim                           |

dengan script SQL sebagai berikut:
```sql
CREATE TABLE IF NOT EXISTS team_details (
    team_id VARCHAR(10) PRIMARY KEY,
    nickname VARCHAR(50),
    arena VARCHAR(100),
    arenacapacity INT,
    owner VARCHAR(100),
    generalmanager VARCHAR(100),
    headcoach VARCHAR(100),
    FOREIGN KEY (team_id) REFERENCES team(team_id)
);
```
### Create Table team
Tabel "Team" dalam Hoops Historia menyajikan informasi lengkap tentang setiap tim yang berkompetisi di NBA, mulai dari nama tim, singkatan, dan nama panggilan hingga detail tentang kota asal, tahun pendirian. Berikut deskripsi untuk setiap tabel team.
| Attribute          | Type                  | Description                                      |
|:-------------------|:----------------------|:-------------------------------------------------|
| team_id            | VARCHAR(10)           | Team ID                                          |
| full_name          | VARCHAR(100)          | Nama Lengkap Team                                |
| abbreviation       | VARCHAR(10)           | Singkatan Team                                   |  
| nickname           | VARCHAR(50)           | Nama panggilan /julukan tim                      |
| city               | VARCHAR(100)          | Kota asal tim                                    |
| state              | VARCHAR(50)           | Negara asal tim                                  |
| year_founded       | INT                   | Tahun pendirian tim                              |

dengan script SQL sebagai berikut:              
```sql
CREATE TABLE IF NOT EXISTS team (
    team_id VARCHAR(10) PRIMARY KEY,
    full_name VARCHAR(100),
    abbreviation VARCHAR(10),
    nickname VARCHAR(50),
    city VARCHAR(100),
    state VARCHAR(50),
    year_founded INT
    );
```

## :open_file_folder: Struktur Folder

```
.
├── app           # ShinyApps
│   ├── css
│   │   ├── **/*.css
│   ├── server.R
│   └── ui.R
├── data 
│   ├── csv
│   │   ├── **/*.css
│   └── sql
|       └── db.sql
├── src           # Project source code
├── doc           # Doc for the project
├── .gitignore
├── LICENSE
└── README.md
```

## :smiley_cat: Tim Pengembang

- Frontend Developer: [Kevin Alifviansyah](https://github.com/Alifviansyah) (G1501231018)
- Technical Writer: [Rifda Nida'ul Labibah](https://github.com/rifdanlabibah) (G1501231061)
- Database Manager: [Sean Marshelle](https://github.com/seanmarshelle) (G1501231012)

