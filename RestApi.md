# REST API Nedir?

REST, client-server arasındaki haberleşmeyi sağlayan ,web servislerinin nasıl oluşturulmasu gerektiğini tanımlayan bir mimari tarzıdır .REST mimarisi HTTP protokolü üzerine kuruludur. İstemci ve sunucu arasında XML ve JSON verilerini taşıyarak uygulamanın haberleşmesini sağlar.

## REST API’nin Temel Özellikleri

- Daha az bant genişliği ve kaynak tükettikleri için hızlı web servisleridir.  
- REST herhangi bir programlama dilinde yazılabilir ve herhangi bir plartformada yürütülebilir.   
- REST mimarisi üzerine kurulmuş ölçeklenebilir bir hizmettir.  
- CRUD işlemleri, web servislerinde POST, GET, PUT, PATCH ve DELETE gibi HTTP yöntemleriyle yapılır.
- İnternet üzerindeki veri iletişimini şifreliyerek koruyan bir güvenlik protokolü olan TLS ile şifreleme sağlar. 
- Geliştirmek daha basittir.

 CRUD işlemleri veri tabanlı sistemlerde gerçekleştirilen dört temel işlemi ifade eder. 

 – Create (Oluştur): Yeni veri eklemek için kullanılır.
 
 – Read (Oku): Var olan verileri okumak için kullanılır.
 
 – Update (Güncelle): Var olan verileri güncellemek için kullanılır.
 
 – Delete (Sil): Var olan verileri silmek için kullanılır.   

REST mimarisi kaynak odaklı, basit ve HTTP protokolü üzerine kurulu bir yapıdır. REST API'ler bu mimarinin kurallarına göre oluşturulur.

##HTTP Nedir
Sunucu ve İstemci arasında internet adresi üzerinden bağlantı kurmak ve veri alışverişi için kullanılan bir TCP/IP protokolüdür.

### REST'in Temel Özellikleri:

- **İstemci-Sunucu Ayrımı:**  
  Kullanıcı arayüzü ile veri saklama ve işleme birbirindn ayrıdır. Bu sayede sistem bileşenleri bağımsız şekilde geliştirilebilir.

- **Stateless:**  
  Sunucu, her gelen isteği birbirinden bağımsız değerlendirir. Yani önceki isteklerin bilgisini tutmaz. Her istek, gerekli tüm bilgileri içermelidir.

- **Önbellekleme:**  
  Veriler önbelleğe alınabilir. Bu sayede aynı verilere tekrar erişilmesi gerektiğinde sunucuya yük binmeden hızlı cevap alınabilir.

- **Tekdüzen Arayüz:**  
  Tüm kaynaklara erişim standart yollarla yapılır. Bu sistemi daha basit ve anlaşılır kılar.


## SOAP Nedir

Basit Nesne Erişim Protokolü dağıtık yapıda bulunan web servislerinin iletişimi gerçekleştirmek üzere kullanılır. Sunucu – İstemci mantığında çalışan bir protokoldür.RPC (Remote Procedure Call) modelini 
kullananır.Veri iletimlerinde ise XML formatı kullanılır


## HTTP Protokolü ve REST API İlişkisi

REST API, HTTP protokolü üzerinde çalışan bir mimaridir. HTTP istemci ile sunucu arasında veri iletişimini sağlayan temel protokoldür ve REST mimarisi bu protokolün sunduğu kuralları kullanır.

REST API’ler HTTP’nin aşağıdaki temel bileşenlerini kullanarak çalışır:

- **HTTP Yöntemleri:** REST, HTTP’nin GET, POST, PUT, DELETE, PATCH gibi metodlarını kullanır. Bu yöntemler sayesinde CRUD işlemleri gerçekleştirilir.

- **URI:** Her kaynak benzersiz bir URI ile tanımlanır.

- **HTTP Durum Kodları:** REST API işlemlerin sonucunu belirtmek için HTTP durum kodlarını kullanır.Bu kodlar 200 Başarılı, 401 Hatalı veri gönderildi ,404 Bulunamadı ,500 Sunucu hatası gibidir. Bu kodlar istemciye yapılan işlemin başarılı mı başarısız mı olduğunu belirtir.

- **Veri Formatları:** REST API’de veri formatı olarak JSON veya XML kullanılır. JSON kullanımı daha yaygındır çünkü daha hafif ve okunması kolaydır.

REST API ile HTTP protokolü birlikte çalışarak web servislerinde basit, anlaşılır ve platformlar arası uyumlu bir iletişim modeli sunar.

## REST API Nasıl Çalışır?

REST API, istemci ile sunucu arasında HTTP protokolü kullanarak veri alışverişi yapar. Bu yapıdaki temel amaç, kaynaklara erişim sağlamaktır.

1. **İstemci isteği göndermesi:**  
   Kullanıcı bir uygulama aracılığıyla bir işlem yapmak istediğinde istemci bir HTTP isteği oluşturur. Bu istek bir URI adresine yöneltilir.

2. **HTTP yöntemi belirlenmesi:**  
   Yapılacak işleme göre uygun HTTP yöntemi kullanılır:
   - `GET` → Veri okuma  
   - `POST` → Yeni veri oluşturma  
   - `PUT` → Var olan veriyi güncelleme  
   - `DELETE` → Veriyi silmek için kullanılır  

3. **Sunucu isteği işler:**  
   Sunucu, gelen isteği alır, işler ve istenileni veritabanından alır, günceller ya da siler.

4. **Cevap döner:**  
   Sunucu işlenen veriyi istemciye genellikle JSON formatında gönderir. Ayrıca işlem sonucu hakkında bilgi veren bir HTTP durum kodu da iletilir.

5. **İstemci gelen veriyi işler:**  
   İstemci, sunucudan dönen yanıtı kullanıcıya sunar.

Bu yapı sayesinde REST API’ler, basit, anlaşılır ve platformdan bağımsız olarak çalışabilir hale gelir.

  <img width="643" height="351" alt="Image" src="https://github.com/user-attachments/assets/2b5d3899-7ee4-4db6-93b1-a2f147598ef6" />

  ## REST API’nin Avantajları ve Dezavantajları

### Avantajları

- **Basit ve Hafif:** REST, HTTP protokolünün standartlarını kullanır bu da öğrenmesini ve uygulanmasını kolaylaştırır.  
- **Platform Bağımsızlığı:** REST API’ler herhangi bir programlama dili ve platformda çalışabilir.  
- **Ölçeklenebilirlik:** Ölçeklendirmesi kolaydır.  
- **Performans:** HTTP önbellekleme desteği sayesinde performansı artırır.  
- **Esneklik:** Farklı veri formatlarını destekler.  

  
### Dezavantajları

- **Durumsuzluk Sınırlaması:** Sunucu önceki isteklerin bilgisini tutmadığı için bazı durumlarda istemcinin daha fazla veri göndermesi gerekir.  
- **Standart Eksikliği:** REST için resmi standart yoktur; bu da uygulamalar arasında uyumsuzluklara yol açabilir.  
- **Güvenlik:** TLS gibi güvenlik katmanları eklenmezse, temel iletişim güvenliği SOAP’a göre daha zayıf olabilir.  
- **Yüksek Karmaşıklık:** Büyük ve karmaşık işlemler için REST bazen yetersiz kalabilir.

  # REST API'de Content-Type Kullanımı

## Content-Type Nedir?

`Content-Type`  sunucuya veya istemciye gönderilen verinin **hangi formatta** olduğunu belirtir. REST API'de veri gönderimi sırasında sıklıkla kullanılır.

## Yaygın Content-Type Değerleri

| Content-Type                         | Açıklama                                             |  
|-------------------------------------|-------------------------------------------------------|
| `application/json`                  | JSON formatında veri                                  | 
| `application/xml`                   | XML formatında veri                                   |       
                                                   
##Accept Nedir?

`Accept` istemcinin sunucudan **hangi formatta veri almak istediğini** belirtir.  

## Yaygın Accept Başlıkları

| Accept Değeri            | Açıklama                                 |
|--------------------------|------------------------------------------|
| `application/json`       | JSON formatında yanıt beklenir           |
| `application/xml`        | XML formatında yanıt beklenir            |



  ## Gerçek Hayatta REST API Kullanım Alanları

- **Sosyal Medya Platformları**  

- **Bulut Hizmetleri**  
 
- **E-Ticaret Siteleri**  

- **Harita ve Konum Servisleri**  
  
- **Ödeme Sistemleri**  

##Kaynakça

[https://medium.com/mobillium/rest-api-restful-api-nedir-b45b32ab4a12]

[https://www.geeksforgeeks.org/node-js/rest-api-introduction/]

[https://www.hosting.com.tr/bilgi-bankasi/rest-api/]






