# Laravel ve PHP En İyi Uygulamaları Rehberi

---

## 🧭 Temel İlkeler
- Kısa, teknik ve doğru PHP örnekleriyle yanıt ver.  
- Laravel’in en iyi uygulama ve konvansiyonlarını takip et.  
- SOLID prensiplerine odaklanarak nesne yönelimli programlama kullan.  
- Kod tekrarı yerine iterasyon ve modüler yapıyı tercih et.  
- Açıklayıcı değişken ve metod isimleri kullan.  
- Klasör adlarında küçük harf ve tire kullan (örn. `app/Http/Controllers`).  
- Dependency injection ve servis container’larını tercih et.

---

## 🐘 PHP / Laravel

### Genel Kurallar
- PHP 8.2+ özelliklerini uygunsa kullan (örn. typed properties, match expressions).  
- PSR-12 kodlama standartlarını uygula.  
- Laravel’in built-in özelliklerini ve helper’larını mümkün olduğunca kullan.  
- Dosya yapısında Laravel dizin ve isimlendirme konvansiyonlarını takip et.  

### Hata Yönetimi ve Logging
- Laravel’in exception handling ve logging özelliklerini kullan.  
- Gerekirse custom exception oluştur.  
- Beklenen hatalar için `try-catch` blokları kullan.  

### Validasyon ve Middleware
- Form ve request validasyonu için Laravel validation kullan.  
- Request filtreleme ve değişiklik için middleware uygula.  

### Veritabanı
- Eloquent ORM ile database işlemlerini gerçekleştir.  
- Karmaşık sorgular için Laravel query builder kullan.  
- Doğru database migration ve seeder’ları uygula.

---

## 🔗 Bağımlılıklar
- Laravel (en son stabil sürüm)  
- Composer ile dependency yönetimi

---
## 🔗 Artisan
-Çalıştırmam için artisan kodlarını vermeyi unutma.
## 🔑 Temel Konvansiyonlar
1. Laravel’in **MVC** mimarisini takip et.  
2. Application endpoint’leri için Laravel routing sistemini kullan.  
3. Request validasyonu için Form Requests kullan.  
4. Görünümler için Laravel **Blade** template engine kullan.  
5. Database ilişkilerini Eloquent ile uygula.  
6. Laravel’in built-in authentication scaffolding’ini kullan.  
7. API resource dönüşümlerini doğru uygula.  
8. Ayrık (decoupled) kod için event ve listener sistemini kullan.  
9. Veri bütünlüğü için database transaction uygula.  
10. Tekrarlayan görevler için Laravel’in built-in scheduling özelliklerini kullan.

## 🏆 Laravel En İyi Uygulamaları
- Mümkün olduğunda raw SQL yerine Eloquent ORM kullan.  
- Data access için Repository pattern uygula.  
- Laravel’in built-in authentication ve authorization özelliklerini kullan.  
- Performans için caching mekanizmalarını uygula.  
- Uzun süren görevler için job queue kullan.  
- Unit ve feature testler için Laravel’in built-in testing araçlarını kullan (PHPUnit, Dusk).  
- Public API’ler için API versioning uygula.  
- Çoklu dil desteği için localization özelliklerini kullan.  
- CSRF koruması ve diğer güvenlik önlemlerini uygula.  
- Asset compilation için Laravel Mix kullan.  
- Query performansı için database indexing uygula.  
- Built-in pagination özelliklerini kullan.  
- Hata loglama ve monitoring’i doğru uygula.

---


