# PatiGo – Sokak Hayvanları İçin Yardımlaşma Platformu

## 1. Proje Hakkında
Bu proje, sokak hayvanlarının beslenme, barınma ve tedavi ihtiyaçlarının karşılanması amacıyla gönüllüler ile yetkilileri bir araya getiren sosyal sorumluluk odaklı bir web uygulamasıdır. **Python Django** web çatısı kullanılarak geliştirilmiştir. Temel amaç, harita tabanlı takip ve görev sistemi ile sokak hayvanlarına ulaşımı kolaylaştırmak ve yardımlaşmayı teşvik etmektir.

## 2. Özellikler
*   **Kimlik Doğrulama & Yetkilendirme:** E-posta doğrulama özellikli güvenli giriş ve kayıt sistemi.
*   **Kullanıcı Rolleri:**
    *   **Gönüllü (User):** Harita üzerindeki görev noktalarını görebilir, görev alabilir, tamamladığı görevler karşılığında rozet kazanabilir.
    *   **Yetkili (Admin/Official):** Yeni görevler oluşturabilir, yemek noktaları bildirebilir ve sistemi yönetebilir.
*   **Harita Entegrasyonu:** Yemek ve su ihtiyacı olan noktaların harita üzerinde görüntülenmesi (Geopy entegrasyonu).
*   **Görev Yönetimi:** Acil, orta ve normal öncelikli görevlerin atanması ve takibi.
*   **Oyunlaştırma (Gamification):** Tamamlanan görevlere göre "Su Kahramanı", "Mama Dağıtıcısı" gibi rozetlerin kazanılması.
*   **Stok/Durum Takibi:** Mama noktalarının doluluk oranlarının bildirimi.
*   **Dashboard:** Sistem istatistiklerinin (aktif noktalar, gönüllü sayısı vb.) görüntülendiği anasayfa.

## 3. Teknoloji Yığını

| Kategori | Teknoloji | Açıklama |
| :--- | :--- | :--- |
| **Frontend** | HTML5 / CSS3 | Kullanıcı arayüzü yapısı ve stilizasyonu |
| | JavaScript | Dinamik arayüz etkileşimleri ve harita yönetimi |
| **Backend** | Python 3.9+ | Ana programlama dili |
| | Django 4.2+ | Web framework ve ORM |
| | Geopy | Konum ve harita servisleri için kütüphane |
| **Veritabanı** | SQLite (Geliştirme) | Varsayılan dosya tabanlı veritabanı |
| | PostgreSQL (Prodüksiyon) | İlişkisel veritabanı yönetim sistemi (Desteklenir) |
| **Araçlar** | Pip / Venv | Paket ve sanal ortam yönetimi |
| | Pillow | Görsel işleme kütüphanesi |

## 4. Proje Yapısı ve Mantığı
*   **MVT Mimarisi:** Django'nun Model-View-Template yapısına uygun olarak tasarlanmıştır.
*   **Modeller:** `UserProfile` (Kullanıcı profilleri), `Task` (Görevler), `FoodSource` (Besleme noktaları), `Badge` (Rozet sistemi).
*   **Servis Yönetimi:** E-posta gönderimi (SMTP) ve Konum servisi (Nominatim) entegrasyonları.
*   **Güvenlik:** Django'nun dahili güvenlik önlemleri (CSRF, XSS koruması, güvenli parola saklama) kullanılmaktadır.

## 5. Proje Nasıl Çalıştırılır?

### Ön Gereksinimler
*   Python 3.9 veya üzeri kurulu olmalı
*   Pip paket yöneticisi kurulu olmalı

### Kurulum

1.  **Depoyu İndirin:**
    Proje dosyalarını bilgisayarınıza indirin veya klonlayın.

2.  **Sanal Ortam Oluşturun ve Aktif Edin:**
    ```bash
    # MacOS/Linux
    python3 -m venv .venv
    source .venv/bin/activate
    
    # Windows
    python -m venv .venv
    .venv\Scripts\activate
    ```

3.  **Bağımlılıkları Yükleyin:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Veritabanı Migrasyonlarını Uygulayın:**
    ```bash
    python manage.py migrate
    ```

5.  **Uygulamayı Çalıştırın:**
    ```bash
    python manage.py runserver
    ```
    Uygulama varsayılan olarak `http://127.0.0.1:8000` adresinde çalışacaktır.

## 6. Proje Demo Videosu
Uygulamanın temel özelliklerini ve genel işleyişini görmek için aşağıdaki demo videosunu izleyebilirsiniz:

https://github.com/user-attachments/assets/7c382c21-564a-468b-a6e3-7980ae01cbc1
](https://github.com/user-attachments/assets/84f14ee7-ca9f-4a05-a472-22ca99e3696d)
