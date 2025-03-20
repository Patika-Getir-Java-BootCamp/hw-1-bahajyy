Soru 1:

OOP kullanmamızın ana sebebi, kodu daha modüler, reusable ve yönetilebilir, daha kolay bakım yapılabilir hale getirmektir. Gerçek dünyadaki nesneleri modelleyerek, kodu daha anlaşılır ve esnek yapmamızı sağlar.Java, C#,Python,C++ dilleri örnek olarak verilebilir.

Soru 2:

Interface:
Sadece method imzaları içerir, body içermez(abstract method sadece)
Multiple inheritance destekler.
Constructor tanımlanamaz.
“implements” keywordu ile implement ederiz.

Abstract Class:
Hem abstract hem concrete methodlar olabilir.
Sadece single inheritance destekler.
Instance variablelar olabilir.
Constructor tanımlanabilir.
“extends” keywordü ile extend ederiz.

Soru 3:

equals() methodu, iki object’in içeriğinin eşit olup olmadığını kontrol eder.
Varsayılan olarak Object class’ından gelir ve == operatörü gibi referansları karşılaştırır.
Eğer içerik bazlı karşılaştırma yapmak istiyorsak, equals() methodunu override etmeliyiz.

hashCode() methodu, bir object’in integer tipinde bir hash değeri döndürmesini sağlar.
Özellikle hash bazlı collection'lar (HashMap, HashSet, HashTable gibi) performanslı çalışması için kullanılır.Aynı içeriğe sahip object’lerin aynı hash değerine sahip olması gerekir, bu yüzden equals() ile birlikte override edilmelidir.

Eğer equals metodunu override ediyorsak, hashCode metodunu da override etmeliyiz.

Soru 4:

Diamond Problem, bir class’ın aynı method veya field’e sahip iki veya daha fazla parent class’tan inherit etmesi durumunda ortaya çıkar. Bu durum bir conflicte neden olur, çünkü compliler subclass’ın hangi parent class’taki method veya field’i kullanacağını belirleyemez.Çözüm olarak  "super" keyword’ünü kullanarak belirli bir parent class’ın method veya field’ini çağırabiliriz veya abstract class yerine interface kullanabiliriz çünkü Java interface’ler aracılığıyla multiple inheritance’ı destekler.

Soru 5:

Garbage Collector, kullanılmayan object’leri bellekten temizlemek için kullanılır. Eğer garbage collector olmasaydı, manuel olarak memory management yapmak zorunda kalırdık, bu da memory leak’lere yol açardı ayrıca  code complexitysini  arttırıdı ve bu da performans sorunlarına yol açardı.Garbage Collector JVM tarafından otomatik olarak çalıştırılır,Mark and Sweep algoritması kullanarak hangi object’lerin kullanılmadığını belirler ve siler.

Soru 6:

Static keywordü javada genellikle memory management amacıyla kullanılır.Variable, method, block, ve nested classlar için kullanılabilir.Bellek üzerinde tek bir kopya oluşturacak şekilde tanımlanmasını sağlar.Yani classın instancesına değil classa bağlıdır ve class seviyesinde memory management sağlar.Her object için bir kopya oluşturmaktansa class düzeyinde bir değer saklamamızı sağlar.

Soru 7:

Immutability, bir nesnenin oluşturulduktan sonra içeriğinin değiştirilememesi anlamına gelir. Yani, bir nesne ilk kez oluşturulduğunda, ona atanan değerler sonrasında değiştirilemez.Örneğin String sınıfı immutable bir sınıftır.Ayrıca final keywordu ile bir değişkeni immutable yapabiliriz, construsctorda değer atama ile class seviyesinde immutable yapabiliriz.Güvenlik, hata azaltma, işlem güvenliği için kullanılır.

Soru 8:

Composition: Güçlü bir "has-a" (sahiplik) ilişkisidir. Child object, parent object olmadan var olamaz. Parent object yok olduğunda, ona bağlı olan child object de yok olur.
Aggregation: Daha zayıf bir "has-a" ilişkisidir. Child object, parent object  olmadan var olmaya devam edebilir. 

Composition, sahiplik ve yaşam döngüsü bağımlılığını ifade eder. Aggregation, sahiplik olmadan ilişkiyi ifade eder ve yaşam döngüsü bağımsızdır.

Soru 9:

Cohesion: Bir sınıf ya da modül içindeki elemanların (metotlar, özellikler vb.) ne kadar birbirine bağlı ve uyumlu olduğunu ifade eder. High cohesion, bir sınıfın veya modülün sadece tek bir sorumluluğa sahip olduğu ve tüm elemanlarının bu sorumluluğa odaklandığı anlamına gelir.

Coupling:Bir sınıf ya da modülün diğer sınıf ya da modüllere olan bağımlılığını ifade eder. Loose coupling, modüllerin birbirine daha az bağımlı olduğu ve daha bağımsız çalıştığı anlamına gelir.

Soru 10:

Heap:
Dynamic memory allocation için kullanılır.
Object’ler ve büyük veri yapıları burada depolanır.
Garbage Collector tarafından yönetilir.
Bellek büyüklüğü esnektir, yani runtime sırasında büyüyüp küçülebilir.

Stack:
Local variables ve method call’ları için kullanılır.
LIFO (Last In, First Out) düzenine göre çalışır.
Fixed size'da olup, stack overflow hatası verebilir.
Method çağrıldığında stack’e push edilir, method tamamlandığında pop edilir.

Soru 11:

Exception: 
Kodumuzun normal akışını bozan, beklenmedik durumlardır. Genellikle hataları yakalamak ve yönetmek için kullanırız. Kodumuzda bir hata oluştuğunda, try-catch blockları ile bir exception fırlatılır ve bu exception, hatayı handle eder.

Türleri:
Checked Exceptions: Bu tür exceptionlar compile zamanında kontrol edilir.Kodu yazarken, bu hataları handle etmek zorundayız. (örneğin, IOException, SQLException).
Unchecked Exceptions (Runtime Exceptions): Bu tür exceptionlar  run timeda oluşur. Genellikle kodun mantıksal hatalarından kaynaklanır (örneğin, NullPointerException, ArrayIndexOutOfBoundsException).
Error: Genellikle sistemin kendisindeki hatalardır.Bu hatalar, JVM seviyesinde oluşur ve genellikle uygulamanın çökmesine yol açar (örneğin, OutOfMemoryError, StackOverflowError).

Soru 12:

Clean code basit, readable, maintainable ve efficient kod yazmaktır.Best practiceları takip ederek,anlamlı değişken isimleri kullanarak,duplicate koddan uzak durarak anlaşılması ve değiştirilmesi kolay kod olarak özetleyebilirim.

Soru 13:

-Java’da hiding , bir alt sınıfın, üst sınıfında var olan bir özelliği veya metodu yeniden tanımlamasıyla gerçekleştirilir. Bu, method hiding olarak adlandırılır ve static metotlar için geçerlidir.Eğer bir alt sınıf, üst sınıfındaki static metodu aynı adla tanımlarsa, alt sınıftaki metod üst sınıfın metodunu gizler. Bu durum, polimorfizmle karıştırılmamalıdır çünkü polimorfizm dinamik metod çağrılarıyla ilgiliyken, method hiding static metodlar için geçerlidir ve compile timeda hangi metodun çağrılacağı belirlenir.

Soru 14:

Abstraction, sınıfların sadece gerekli bilgileri dışa sunarak, iç işleyişi gizler. Bu, karmaşıklığı azaltır ve sadece kullanıcıya gerekli olan özellikler gösterilir. Örneğin, bir interface veya abstract class kullanarak, detaylardan soyutlanmış bir yapı kurulur.
Polymorphism ise,  çok biçimlilik anlamına gelir.aynı metodun farklı şekillerde çalışabilmesi durumudur. Bu, aynı isme sahip bir metodun farklı sınıflarda farklı işlevler yerine getirmesini sağlar. Örneğin, method overriding ya da method overloading ile polymorphism elde edilir.

