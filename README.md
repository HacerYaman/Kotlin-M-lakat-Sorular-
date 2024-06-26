# Kotlin Mulakat Sorulari

1-Kotlin nedir ve Java'dan farklılıkları nelerdir?
-> Kotlin Jetbrains tarafından geliştirilen statik tipli JVM üzerinde çalışan bir programlama dilidir. Java ile tam uyumlu değildir. Kotlin, Java'ya göre daha kısa ve rahat okunabilirdir kod yazmayı sağlar. Aralarındaki farklılıklardan bazıları şunlardır; Kotlin null safety, extension function ve higher order function özelliklerini sağlar.

2- Kotlin'de null safety nasıl sağlanır?
-> Kotlinde değişkenler varsayılan olarak null olamaz. Null olabilen değişkenler ? ile tanımlanır. Null safety sağlamak için : ?. (safe call), ?: (elvis operatörü), !! (not null assertion) operatörleri kullanılır.

3- Type inference nedir? (tip çıkarımı)
-> IDE'nin türü belirtilmemiş değişkenin türü bilmesidir.

4- val ve var anahtar kelimelerinin farkı nedir?
-> val ile tanımlanan değişkenler değiştirilemezken var ile tanımlanan değişkenler yeniden atanabilir.

5- "==" ve "===" neleri kontrol eder?
-> "==" nesneleri ve içindeki değişkenleri karşılaştırır. "===" ise nesnelerin tutulduğu memory adresini yani referans bilgisini karşılaştırır.

6- var hangi durumda val gibi davranır?
-> Kotlin'de bir fonksiyon içinde tanımlanan değerler variable bir classa üye olarak tanımlanan değerler propertydir ve arka planda get ve set fonksiyonları vardır. Bu durumda set fonksiyonunu private yaparsak bu var property, val gibi davranacaktır.

7- Nothing? nedir?
-> Eğer bir değişkene değer atanmamışsa ve null ise IDE bunu "Nothing?" olarak işaretler. Hiçbir değeri temsil etmeyen ve hiçbir zaman başarılı bir şekilde bir değere dönüşmeyen bir türdür.

8- val ve const arasındaki fark nedir?
-> Her ikisi de immutable değişkenler için kullanılır fakat val run time constant olarak kullanılır. const ise compile time constant olarak kullanılır.

9- null safety hangi durumda karşımıza çıkabilir?
-> Elimizde nullable bir değişken varsa, bunun methodlarından birini ya da direkt kendisini kullanacaksak IDE'ye null olmayacak garantisini vermeli ya da null değilse çalışsın demeliyiz. NULL POINTER EXCEPTION ile karşılaşabiliriz.

10- Bir primitive tipteki değişken null yapılırsa ve === ile kontrol edilirse nasıl bir sonuç alırız? 
-> Bir değişkeni null yapmak onu primitive tipten obje referanslı tipe dönüştürür. byte aralığı -128 ve +127 arasında değilse false verir yani artık adresi değişmiştir. Aksi durumda true verir. Bu byte aralığında olan değişkenler obje referanslı hale gelmiş olsa bile bellekteki adresi değişmez. Adresinin değişmesi performans farkı yaratır. 

11- Boxed ve unboxed nedir?
-> boxed değişkenin obje referanslı olarak tutulmasıdır. unboxed değişkenin obje tipli tutulmasıdır.

12- Lazy çalışma mekanizması nedir?
-> || ve && lazy çalışma mekanizmasına sahiptir. || operatörünün sol tarafı true ise sağ taraf kontrol edilmez. && operatörünün solu false ise sağ taraf kontrol edilmez.

13- Operatörlerin ne zaman operatör hali ne zaman fonksiyon hali kullanılır?
-> Karşılaştırdığımız değerler nullable olduğu zaman operatör halini kullanamayız. Fonksiyon hali kullanılmalı.

14- Destructuring declaration nedir?
-> Bir veri yapısının (örneğin bir veri sınıfı, liste veya harita) bileşenlerini tek bir ifadeyle birden fazla değişkene atama yöntemidir.

15- Fonksiyonlarda default argument ne demek?
-> Fonksiyon çağırılırken parametre değişkenine bir değer gönderilmemişse derleyici argüman olarak daha önce belirlenen ifadeyi kullanır. Bu default argumenttir.

16- Fist class citizen şartları nelerdir?
-> Bir yapı değişkenlere değer olarak atanabilirse, başka fonksiyonlara parametre olarak verilebilirse, fonksiyonun return değeri olabilirse first class citizendir.

17- Elvis operatörü nedir?
-> Null değeri kontrol etmek ve alternatif bir değer belirlemek için kullanılan operatördür. Null değerse solu, null değilse sağı geçerli kılar.

18- Visibility modifierlar nelerdir?
->  public: her yerden erişilebilir.
    internal: aynı modül içindeki tüm yerel paketler erişebilir.
    private: sadece tanımlandığı sınıfla erişilebilir.
    protected: private ile aynıdır ama ayrıca alt sınıflar tarafından da erişilebilir.

19- OOP'nin dört prensibi ve açıklamaları nedir?
-> inheritance: Bir sınıfın başka bir sınıfın özelliklerini ve davranışlarını miras almasını ifade eder. Alt sınıf üst sınıfın property ve methodlarını kullanabilir ve gerektiğinde override edebilir. Kodun yeniden kullanılabilirliğini arttırır. Sınıflar arasında hiyerarşi oluşmasını sağlar.
    encapsulation: Verileri ve ilgili methodları bir sınıf içinde bir araya getirme ve sınıfın dışındaki kodun doğrudan erişimini kısıtlama prensibidir. Sınıf içindeli uygulama   ayrıntılarını gizleyerek sınıfın güvenli olmasını sağlar.
    polymorphism: Aynı isimle fakat farklı davranışlara sahip methodların kullanılmasını ifade eder. 
    abstraction: Bir nesnenin duruma göre önemli özelliklerini vurgulayarak gereksiz ayrıntıları soyutlama prensibidir. Karmaşıklığı azaltır.

20- Unit fonksiyon nedir?
-> Unit, Java'daki void e karşılık gelir. Eğer bir fonksiyonun dönüş değeri belirtilmemişse varsayılan olarak tipi unit kabul edilir.

21- vararg nedir?
-> vararg, "variable number of argument" demektir. Argümanlar listesidir. Fonksiyona parametre olarak verildiğinde tek parametre gibi görünse de birden fazla parametre  verilmiş olur.

22- infix fonksiyon nedir neden kullanılır?
-> infix fonksiyonlar iki öğe arasındaki bir işlemi daha doğal ve okunabilir hale getirmek için kullanılan özel türdeki fonksiyonlardır. Nokta ve parantez kullanılmadan çağırılabilirler. Bu sayede daha rahat bir okunma sağlar. Örneği or ve and fonksiyonları olabilir. Şartları şunlardır: Sadece 1 parametre alabilirler (vararg olamaz), üye fonksiyon ya da extension olmalıdır, parametresi default değer alamaz.

23- Üye fonksiyon nedir?
-> Bir sınıfın içindeki fonksiyonlara üye fonksiyon denir.

25- Top-level function nedir?
-> Bir fonksiyon bir sınıfın içinde değil de bir dosyanın içinde boşlukta tanımlanırsa top level function adını alır.

26- Bir fonksiyona hiçbir şeyin erişmesini istemiyorsam ne yapmalıyım?
-> Fonksiyon içinde fonksiyon olarak yazarsak erişimi tamamen engelleriz.

27- Extension fonksiyon nedir?
-> Mevcut sınıflara yeni fonksiyonlar eklememizi sağlayan bir özelliktir. Classın kaynak kodunu değiştirmeden ya da alt sınıf oluşturmadan yapılabilir. Kodu daha esnek ve yeniden kullanılabilir yapar. O classa ait gerçek bir fonksiyon olmaz. 

28- Receiver nedir?
-> Extension yazacağımız sınıfı ifade eder.

29- Higher order function nedir?
-> Diğer fonksiyonları parametre olarak alan veya fonksiyon döndüren fonksiyonlardır.

30- inline fonksiyonlar neden default değer alamazlar?
-> Temel nedeni, derleyicinin inline fonksiyonları optimize etme ve performans artırma şekliyle ilgilidir. Default parametreler bu optimizasyonlarla uyumlu olmadığı için inline fonksiyonlarda kullanılmaz.

31- Bir property nasıl extend edebiliyoruz?
-> Bunun sebebi propertylerin aslında get ve set methodu olan fonksiyonlar olmasıdır. Field tanımlanmaz. Gerçek anlamda bir propert extension olmaz.

32- HOFların interfacelere göre performans farkı nedendir?
-> Lambda ifadelerinin HOFta kullanılması performans farkı yaratır. Her lambda ifadesi için ek nesne yaratılması gerekir.

33- non-local return nedir?
-> Bir lambda ifadesi içerisinden, kapsayıcı fonksiyona dönmeyi sağlar. Bu davranış, lambda ifadesinin içinde çağırıldığı fonksiyonun da çalışmasını durdurur. Sadece inline fonksiyonlarda mümkündür.

34- Kotlinde constructor yapısı nasıldır?
-> kotlinde 2 tip constructor vardır: primary ve secondary. Bir constructor yazmasak bile default olarak primary constructor oluşur.

35- init bloğu nedir?
-> Bir sınıfın bir örneği oluşturulduğunda ilk başlatma işlemlerini gerçekleştirmek için kullanılır. init bloğu constructora ait olan tüm kod parçaları çağırıldıktan sonra otomatik olarak çağırılır. Birden fazla init bloğu olabilir ve yazıldığı sırayla çağırılır.  Constructorun bodysidir.

36- Kotlinde data classını neden kullanmak isteriz?
-> IDE kendisi default olarak fonksiyonlar oluşturur ve bu fonksiyonlar sadece constructordaki variable için geçerlidir. Data classlar destructuring declaration desteği sunar. 

37- invoke nedir?
-> Bir sınıfın nesnesi doğrudan bir fonksiyon gibi çağırıldığında çalışmasını sağlayan özel bir fonksiyondur. Nesneyi fonksiyon gibi kullanmamıza olanak tanır. 

38- Data classta neden val - var zorunludur?
-> Değişkenlerin üye değişken gibi olması sağlanır.

39- inline fonksiyon nedir? Neden kullanılır?
-> Kotlinde inline fonksiyonu özel olarak HOF'un performansını artırmak amacıyla kullanbiliriz. Bir fonksiyon inline olarak işaretlendiğinde bu fonksiyon gövdesi çağırıldığı her yere yeleştirilir. Bu özellikle lamda ifadeleri ile kullanıldığında ek nesne oluşturma maliyetinden kurtarmış olur.

40- Kotlinde neden her şey publictir?
-> Kotlinde Java tarafında aslında her şey değişmez biçimde privatedir ama get ve setleri vardır. Bir öğeyi private ya da public yapmak sadece onun get ve set methodlarına sahip olup olmamasını değiştirir.

41- const val nedir?
-> Sabit değerler tanımlamak içim kullanılan bir anahar kelimedir. Bu anahtar kelime ile tanımlanan değerler, derleme zamanında belirlenir ve çalışma zamanında değiştirilemezler. Bu performans artışına ve sabitlerin daha etkin kullanılmasına olanak tanır.

42- string interpolasyonu nasıl çalışır?
-> bir string içinde değişken yerleştirmek için $ sembolü kullanılır.

43- open anahar kelimesi neyi ifade eder?
->  Kullanımı bir propery ya da methodun miras alınabileceğini ya da override edilebileceğini ifade eder.

44- Kotlinde classların varsayılan davranışı hangi yöndedir?
-> Kotlinde tüm sınıflar varsayılan olarak finaldir. Developerin miras alınacak classları open ile işaretlemesi gerekmektedir.

45-Abstract class ile interface farkı nedir?
-> Interfaceler state tutmazlar.

46- abstract ile open classın farkı nedir?
-> Abstract classlar override etme zorunluyken open classlar zorunlu değiller.

47- classlarda constructor kısmındaki değişkenlerin var veya val ile işaretlenmesi ne fayda sağlar?
-> Bu değişkenlere classın herhangi bir yerinden erişim sağlayabiliriz. Üye değişken gibi davranırlar. Aksi durumda sadece init bloğundan erişebiliriz.

48- Smart cast (akıllı tür dönüşümü) nedir?
-> Derleyicinin belirli koşullar altında bir nesnenin türünü otomatik olarak dönüştürme yeteneğini ifade eder.

49- String nedir?
-> String metinleri sakladığımız veri türüdür. Immutabledir. Char dizisidir.

50- Type conversion nedir?
-> Tür dönüşümü bir veri türündeki bir değeri başka bir veri türüne dönüştürme işlemidir.

51- Abstrack classların nesnesi oluşturulamadığı halde constructoru olabiliyor. Bu durumda constructor ne işe yarar?
->

52- Stack ve heap nedir?
-> memory 2 bölüme ayırılır: stack __ küçük sabit boyutlu bellek alanı, hızlı, yerel değişkenler tutulur ,,, heap __ büyük bellek alanı, yavaş, uzun ömürlü veriler ve nesneler tutulur.

53- Escape karakterler nelerdir?
-> belirli karakterleri, sembolleri veya kontrol dizilerini temsil etmek için kullanılır. \n \r \t \\ \' \" gibi 

54- Unicode karakter nedir?
-> Unicode, her bir karaktere benzersiz bir sayı (kod noktası) atayarak, farklı dillerdeki metinlerin tutarlı bir şekilde işlenmesini sağlar.

55- Null değerler memoryde yer kaplamaz mı?
-> Kaplar 

56- Fonksiyonları neden kullanırız?
-> Kodun tekrar kullanılabilirliğini, okunabilirliğini artırır.

57- overload nedir?
-> Aynı isimde birden fazla fonksiyon tanımlanması işlemidir.

58- Local function nedir?
-> bir fonksiyonun bir başka fonksiyonun içinde tanımlanmasıdır. Yani, bir fonksiyonun sadece belirli bir başka fonksiyonun içinde erişilebilir ve kullanılabilir olmasını sağlar. 

59- Expression ve state kullanımları nelerdir?
-> Expression kullanımı: İfadeler, genellikle bir değeri hesaplamak, bir işlem gerçekleştirmek veya bir sonuç üretmek için kullanılır. TEK SATIR State kullanımı: programın mevcut durumunu izlemek, değiştirmek ve yönetmek için kullanılır BLOK

60- Bir classın sahip olabileceği elemanlar nelerdir?
-> 

61- Method overriding nedir?
-> alt sınıfın üst sınıftaki bir methodu kendi ihtiyaçlarına göre yeniden tanımlamasıdır.

62- Overriding property açıklaması nedir?
-> Hem fonksiyonlar hem propertyler open olmak şartıyla override edilebilir.

63- Property nedir? (özellik)
-> Kotlinde property bir sınıfın verilerini kapsülleyen ve bunlara erişimi kontrol eden mekanizmadır. var  veya var olabilir.

64- Backing field nedir?
-> Propertylerin değerlerinin saklandığı alan.

-----------------------------
65- Polimorfizm nedir?
-> Polimorfizm "birçok form" anlamına gelir. Polimorfizm, aynı arayüz veya temel sınıf kullanılarak farklı nesnelerin farklı şekillerde davranabilme yeteneğini ifade eder. Başka bir deyişle, polimorfizm sayesinde aynı işlemi farklı nesneler üzerinde gerçekleştirebiliriz ve bu nesneler, kendi özel uygulamalarını kullanarak bu işlemi yerine getirirler.

66- Enum classların sabitleri arka planda nasıl bulunur?
->

67- "ANKARA" stringindeki k harfini nasıl elde ederiz?
->  [2] . indexe giderek

68- "2" ile "2.5" i == ile karşılaştırdığımda ne verir?
->

69- infix fonksiyonların performansa etkisi var mı?
-> 

70- data classlar ile data objeler arasında ne fark var?
->

71- sealed classların scoopu nedir yani nereden erişilir?
->

72- when yapıları içinde else casei hangi durumda gerekli olmaz?
->

73- iki arrayi kıyaslerken "==" kullanabilir miyiz? kullanırsak sonuç ne olur?
->

74- genericlerin in varyantı olması durumu nedir?
->

75- 10L ve 10UL olarak değer atarsak tipi ne olur?
->

76- companion object başka bir sınıfı miras alabilir mi ya da bir sınıfı implement edebilir mi?
->

77- bir enum class içine open fun yazarsak bunu nasıl override edebiliriz?
->

78- sealed classın ya da içindeki ondan miras alan sabitlerin nesnesi oluşturulabilir mi?
->

79- extension functionun bir dosya içinde top level olarak tanımlanması ile bir classın içinde tanımlanması arasında ne fark olur?
->

80- Bir interface içinde nasıl property tanımlıyoruz?
-> 

81- char tipi değişkenler boxed mıdır unboxed mıdır?
->

--------------------------

82- abstract class nedir? özellikleri nelerdir?
-> soyut sınıf olarak adlandırılır ve diğer sınıflar tarafından genişletilmesi amaçlanır. Nesnesi oluşturulamayan ve alt sınıflar tarafından genişletilerek kullanılabilen sınıflardır.
Detay bilgi içermemelidir. abstract fonksiyonlar bodye sahip olamaz. abstrack fonksiyonların override zorunluluğu vardır. 

83- interface nedir?
-> bir sınıfın belirli bir işlevselliği uygulamasını zorunlu kılmak için kullanılan bir yapıdır. interfaceler bir sınıfın belirli methodları ve özellikleri içermesi gerektiğini belirtir.
bir sınıf birden fazla interface implement edebilir
doğrudan nesnesi oluşturulamaz. interfaceleri uygulayan sınıflardan nesne oluşturulabilir

84- interfaceler hangi durumda class gibi davranır javada?
-> object expression kullanımında 

85- hangi durumda override zorunlu değildir?
-> fonksiyonun bodysi varsa override zorunlu değil

86- data classlarda constructorlar ne işe yarar?
-> classların taşıdığı verileri tanımlar

87- data classların şartları nelerdir?
-> en az 1 parametresi olmalı. parametreler val veya var olmalı, abstract open sealed veya inner olamazlar

88- enum class nedir neden kullanılır?
-> kullanım amacı veri kümelerini gruplanabilir yapmatır. yapısı gereği finaldır. nesnesi oluşturulamaz. her enum sabiti final name ve final ordinala sahip. miras alınamaz. içindeki sabitler bulunduğu classı miras olan başka classlardır.

89- sealed class nedir ve özellikleri nelerdir?
-> classların gruplandırılması için kullanılır. sınırlı bir hiyerarşi içinde belli türdeki alt sınıfları tanımlamak için kullanılan sınıf türü. özellikleri: alt sınıflar sadece aynı modul ya da dosya içinde olmalı, daha güçlü kapsülleme sağlar. hiyerarşiyi idenin kontrolünden alıp developera verir

90- enum classın sealed classtan farkı nedir?
-> enum classlara objesini üretmeden erişebilirim arka planda statiktir.

91- generics yerine neden any kullanmıyorum?
-> any type safety sağlamıyor.

92- spread operatörü nedir?
-> bir diziyi fonksiyona iletmek için * kullanılır.

93- contentEquals() ve contentDeepEquals() ne için kullanılır?
-> iki arrayin öğeleri tamamen aynı mı ve aynı sırada mı onu kontrol eder.

94- dizilerde "==" ne işlevdedir?
->  referans kontrolü yapar

95- is ve !is ne için kullanılır
-> type kontrolü

96- while aslında nedir?
-> for un içine if konulmasıdır
