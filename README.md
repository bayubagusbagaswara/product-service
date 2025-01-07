# Product Service

# Perintah run Docker Compose

- docker compose up -d

# Notes
1. Nimbus JWK: Library Nimbus digunakan untuk menangani kunci RSA dan JSON Web Keys (JWK). Spring Authorization Server mendukungnya secara default.
2. Endpoint JWKS: Setelah konfigurasi, endpoint JWKS dapat diakses di: `http://localhost:8080/.well-known/jwks.json`

# Authorization Server
Authorization Server bertanggung jawab untuk mengelola otentikasi, pembuatan token, dan endpoint terkait OAuth2.

# Integrasi Antar Microservices
Setiap microservice berinteraksi dengan microservices lain sesuai kebutuhan. Untuk menghubungkan service-service ini:
1. Event-Driven Architecture: Menggunakan Kafka atau RabbitMQ untuk komunikasi asynchronous.
2. RESTful API: Menggunakan HTTP untuk komunikasi langsung antar microservices.
3. Service Registry: Dengan tools seperti Eureka atau Consul, untuk menemukan dan menghubungkan microservices.

# User Service
Fungsi: Mengelola data pengguna, seperti informasi profil, hak akses, dan preferensi. Memberikan API untuk mengatur pengguna, misalnya registrasi, penghapusan, atau pembaruan profil.

# Notification Service
Fungsi: Mengirimkan notifikasi kepada pengguna melalui email, SMS, atau push notifications. Memberikan API untuk mengatur atau mengirim notifikasi.
Integrasi: order-service dapat memanggil notification-service untuk mengirimkan konfirmasi pesanan.

# Payment Service
Fungsi: Mengelola pembayaran dari pengguna, termasuk integrasi dengan penyedia pembayaran pihak ketiga. Melakukan validasi transaksi dan pencatatan pembayaran.

# Analytics Service
Fungsi: Mengelola data analitik, seperti perilaku pengguna, laporan penjualan, dan performa sistem. Memberikan wawasan kepada tim bisnis untuk pengambilan keputusan.
