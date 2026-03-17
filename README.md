Simple LMS — Django Docker Project

📌 Deskripsi Project



Project ini merupakan setup environment development untuk aplikasi Simple Learning Management System (LMS) menggunakan Django Framework yang dijalankan dengan Docker Compose.



Tujuan dari project ini adalah memahami konsep:



Containerization menggunakan Docker



Multi-service architecture (Web + Database)



Konfigurasi PostgreSQL pada aplikasi Django



Penggunaan environment variables



Deployment development environment yang portable



🧱 Arsitektur Sistem



Project terdiri dari 2 service utama:



🖥️ Django Web Application



Framework: Django



Port akses: http://localhost:8000



Berfungsi sebagai backend aplikasi LMS



🗄️ PostgreSQL Database



Image: postgres:15



Digunakan sebagai database penyimpanan data aplikasi



Semua service berjalan dalam Docker Network sehingga dapat saling terhubung menggunakan hostname service.



⚙️ Cara Menjalankan Project



Masuk ke folder project



cd simple-lms



Jalankan container menggunakan Docker Compose



docker compose up --build



Akses aplikasi melalui browser



http://localhost:8000



👤 Membuat Superuser Django



Untuk mengakses halaman admin jalankan perintah:



docker compose exec web python manage.py createsuperuser



Setelah berhasil login admin dapat diakses di:



http://localhost:8000/admin



🗄️ Konfigurasi Database



Django dikonfigurasi menggunakan PostgreSQL container.



Hostname database menggunakan nama service docker yaitu:



db



Sehingga komunikasi antar container berjalan otomatis melalui docker network.



🔐 Environment Variables



Konfigurasi database disimpan dalam file .env.



Contoh konfigurasi:



POSTGRES\_DB=lms\_db

POSTGRES\_USER=lms\_user

POSTGRES\_PASSWORD=lms\_password

POSTGRES\_HOST=db

POSTGRES\_PORT=5432



📷 Screenshot Aplikasi

Django Welcome Page



Django Login Admin



Django Admin Dashboard



🧪 Hasil Pengujian



Pengujian yang telah dilakukan:



Docker Compose berhasil menjalankan semua service



Django dapat diakses melalui browser



PostgreSQL berhasil terkoneksi



Migration database berhasil dijalankan



Superuser berhasil dibuat



Halaman admin dapat diakses



👨‍💻 Author



Nama: GEDE PRADISTYA EVAN ARYAPUTRA

NIM: A11.2023.14886

Mata Kuliah: Pemrograman Sisi Server

