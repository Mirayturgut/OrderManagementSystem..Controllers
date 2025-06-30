# Order Management System 🧾

C# ve Entity Framework Core kullanılarak geliştirilen bu uygulama, rol bazlı sipariş yönetimini sağlayan bir **konsol tabanlı back-end projesidir**. Uygulama, SQL Server veritabanı ile entegre edilmiştir.

## 🚀 Proje Özellikleri

- SQL Server destekli veritabanı bağlantısı (EF Core ile)
- Rol bazlı kullanıcı yönetimi: `Admin`, `Kitchen`, `User`
- Giriş yapma ve kayıt olma işlemleri (şifreleme destekli)
- Ürün yönetimi (Ekleme, Listeleme, Güncelleme)
- Sipariş oluşturma ve geçmiş sipariş görüntüleme
- Sipariş durumlarını güncelleme (Hazırlanıyor, Hazır, Teslim Edildi)
- Konsol üzerinden kullanıcı dostu menü sistemi

## 🧑‍💻 Kullanıcı Rolleri

- **Admin**: Ürünleri yönetebilir, tüm kullanıcı ve siparişleri görüntüleyebilir.
- **Kitchen**: Hazırlanacak siparişleri listeler ve durumlarını güncelleyebilir.
- **User**: Ürünleri görüp sipariş oluşturabilir, geçmiş siparişlerini görebilir.

## 🛠️ Kullanılan Teknolojiler

- .NET 9.0
- C#
- Entity Framework Core
- SQL Server
- Console UI (yardımcı sınıflar ve menüler)
- LINQ, EF `Include()` ile ilişkili veri yönetimi

## 🏗️ Veritabanı Yapısı

- `Users`
- `Products`
- `Orders`
- `OrderItems`

Veritabanı oluşturulurken `EnsureCreated()` yöntemiyle yapılandırma sağlanır.

## 📌 Kurulum ve Çalıştırma

1. Bu repoyu klonlayın:
    ```bash
    git clone https://github.com/Mirayturgut/OrderManagementSystem.git
    ```
2. `appsettings.json` dosyasındaki **SQL Server bağlantı cümlesini** kendi veritabanınıza göre düzenleyin.
3. Konsol üzerinden aşağıdaki komutları sırasıyla çalıştırarak veritabanı migrasyonlarını uygulayın:
    ```bash
    dotnet ef migrations add InitialCreate
    dotnet ef database update
    ```
4. Projeyi başlatın:
    ```bash
    dotnet run
    ```

## ✍️ Geliştirici

**Miray Turgut**  
📫 [LinkedIn Profilim](https://www.linkedin.com/in/mirayturgut)

---

> Bu proje, konsol uygulamalarında Entity Framework kullanımı ve katmanlı mimari uygulamaları için bir örnek teşkil etmektedir.
