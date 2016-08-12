**image** kullanıcak imaj adı ya da ID’si belirtilir.
<br>**build** Dockerfile’ın bulunduğu dizin belirtilir.(çalıştığımız dizin ile aynı konumda ise "." ile belirtilir.)
<br>**dockerfile** default değeri Dockerfile ‘dır. Dosya ismi farklı ise ya da farklı bir dizinde ise bu anahtar kelime kullanılır.
<br>**ports** yönlendirme yapılacak portları belirtmek için kullanılır.
<br>**volumes** dosya dizinlerini ilişkilendirmek için kullanılır. Erişim modu da belirtilebilir. (ro: read only gibi)
<br>**volumes_from** diğer bir servisin veya konteynerin dosya dizinini eklemek için kullanılır.
<br>**links** bağlantı yapılacak konteynerleri belirtmek için kullanılır.
<br>**command** çalıştırılacak komutu belirtmek için kullanılır.
