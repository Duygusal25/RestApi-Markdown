# REST API Nedir?

REST, client-server arasındaki haberleşmeyi sağlayan ,web servislerinin nasıl oluşturulmasu gerektiğini tanımlayan bir mimari tarzıdır .REST mimarisi HTTP protokolü üzerine kuruludur. İstemci ve sunucu arasında XML ve JSON verilerini taşıyarak uygulamanın haberleşmesini sağlar.

Amazon, Google, Facebook, LinkedIn ve Twitter gibi web siteleri, kullanıcıların bu bulut hizmetleriyle iletişim kurmasını sağlayan REST tabanlı API’leri kullanır.


## REST API’nin Temel Özellikleri

- Daha az bant genişliği ve kaynak tükettikleri için hızlı web servisleridir.  
- REST herhangi bir programlama dilinde yazılabilir.  
- Bu servisler herhangi bir platformda yürütülebilir.  
- REST mimarisi üzerine kurulmuş hafif ve ölçeklenebilir bir hizmettir.  
- CRUD (Create, Read, Update, Delete) yani oluştur, oku, güncelle ve sil işlemleri için GET, POST, DELETE, PUT ve PATCH gibi HTTP fiillerini kullanır.  
- TLS (Transport Layer Security) yani taşıma katmanı güvenliği aracılığıyla temel iletişim şifrelemelerini destekler, bu nedenle SOAP’tan daha az güvenlidir.  
- Geliştirmek daha basittir.  
- SOAP ile karşılaştırıldığında daha az bant genişliği gerektirir.  

 ## REST Mimarisi ve Temel İlkeleri

REST mimarisi; kaynak odaklı, basit ve HTTP protokolü üzerine kurulu bir yapıdır. REST API'ler bu mimarinin belirli ilkelerine uyarak geliştirilir.

### REST'in Temel İlkeleri:

- **İstemci-Sunucu (Client-Server) Ayrımı:**  
  Kullanıcı arayüzü (istemci) ile veri saklama ve işleme (sunucu) birbirinden ayrıdır. Bu sayede sistem bileşenleri bağımsız şekilde geliştirilebilir.

- **Durumsuzluk (Stateless):**  
  Sunucu, her gelen isteği birbirinden bağımsız değerlendirir. Yani önceki isteklerin bilgisini tutmaz. Her istek, gerekli tüm bilgileri içermelidir.

- **Önbellekleme (Caching):**  
  Veriler önbelleğe alınabilir. Bu sayede aynı verilere tekrar erişilmesi gerektiğinde sunucuya yük binmeden hızlı cevap alınabilir.

- **Tekdüzen Arayüz (Uniform Interface):**  
  Tüm kaynaklara erişim standart ve tutarlı yollarla yapılır. Bu, sistemi daha basit ve anlaşılır kılar.

- **Katmanlı Sistem (Layered System):**  
  Sistemin bileşenleri katmanlara ayrılabilir (örneğin: güvenlik katmanı, yük dengeleme katmanı vb.). İstemci, sunucuya doğrudan mı yoksa ara katmanlar aracılığıyla mı eriştiğini bilmez.

## HTTP Protokolü ve REST API İlişkisi

REST API, HTTP protokolü üzerinde çalışan bir mimaridir. HTTP, istemci (client) ile sunucu (server) arasında veri iletişimini sağlayan temel protokoldür ve REST mimarisi bu protokolün sunduğu standartları kullanır.

REST API’ler, HTTP’nin aşağıdaki temel bileşenlerini kullanarak çalışır:

- **HTTP Yöntemleri:** REST, HTTP’nin GET, POST, PUT, DELETE, PATCH gibi metodlarını kullanarak kaynaklar üzerinde işlem yapar. Bu yöntemler sayesinde CRUD işlemleri gerçekleştirilir.

- **URI (Uniform Resource Identifier):** Her kaynak benzersiz bir URI ile tanımlanır. Örneğin, bir kullanıcı bilgisine erişmek için `/users/123` gibi bir adres kullanılır.

- **HTTP Durum Kodları:** REST API, işlemlerin sonucunu belirtmek için HTTP durum kodlarını (200 BAşarılı, 201 Hatalı veri gönderildi, 404 Bulunamadı, 500 Sunucu hatası vb.) kullanır. Bu, istemciye yapılan işlemin başarılı mı, başarısız mı olduğunu bildirir.

- **Veri Formatları:** REST API’lerde genellikle veri formatı olarak JSON veya XML kullanılır. Ancak günümüzde JSON daha yaygındır çünkü daha hafif ve okunması kolaydır.

REST API ile HTTP protokolü birlikte çalışarak web servislerinde basit, anlaşılır ve platformlar arası uyumlu bir iletişim modeli sunar.

## REST API Nasıl Çalışır?

REST API, istemci (client) ile sunucu (server) arasında HTTP protokolü aracılığıyla veri alışverişi yaparak çalışır. Bu yapıdaki temel amaç, kaynaklara (örneğin kullanıcılar, ürünler, siparişler) erişim sağlamaktır.

Çalışma mantığı genel olarak şu adımlarla gerçekleşir:

1. **İstemci isteği gönderir:**  
   Kullanıcı bir uygulama aracılığıyla bir işlem yapmak istediğinde (örneğin bir ürün listesini görmek), istemci belirli bir HTTP isteği oluşturur. Bu istek genellikle bir URI adresine yöneltilir.

2. **HTTP yöntemi belirlenir:**  
   Yapılacak işleme göre uygun HTTP yöntemi (GET, POST, PUT, DELETE vb.) kullanılır:
   - `GET` → Veri okuma  
   - `POST` → Yeni veri oluşturma  
   - `PUT` → Mevcut veriyi güncelleme  
   - `DELETE` → Veriyi silme  

3. **Sunucu isteği işler:**  
   Sunucu, gelen isteği alır, işler ve istenilen kaynağı veritabanından alır, günceller ya da siler.

4. **Cevap döner:**  
   Sunucu, işlenen verinin sonucunu istemciye genellikle JSON formatında geri gönderir. Ayrıca işlem sonucu hakkında bilgi veren bir HTTP durum kodu da iletilir (örneğin: `200 OK`, `404 Not Found`, `201 Created`).

5. **İstemci gelen veriyi işler:**  
   İstemci, sunucudan dönen yanıtı kullanıcıya sunar ya da arka planda kullanır.

Bu yapı sayesinde REST API’ler, basit, anlaşılır ve platformdan bağımsız olarak çalışabilir hale gelir.







