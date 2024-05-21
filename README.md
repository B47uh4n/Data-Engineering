# Data-Engineering

# Azure Synapse: Veri Analitiği ve Büyük Veri Yönetimi

Büyük veri kütlesini yönetmek ve analiz etmek, geleneksel yöntemlerle giderek zorlaşmaktadır. Azure Synapse gibi çözümler bu noktada devreye giriyor.

## Azure Synapse Nedir?

Azure Synapse, Microsoft'un bulut tabanlı bir veri platformu hizmetidir. Büyük veri analitiği ve iş zekası için kapsamlı bir çözüm sunar. Veri ambarları, veri gölü ve büyük veri analitiği işlemlerini tek bir platformda birleştirerek veri yönetimini ve analizini kolaylaştırır.

## Ne İşe Yarar?

Azure Synapse, işletmelere veri toplama, depolama, işleme ve analiz etme imkanı sunar. Büyük veri kümelerini yönetmek için gerekli olan altyapıyı sağlar ve kullanıcıların verilerini hızlı ve güvenli bir şekilde analiz etmelerine olanak tanır. Aynı zamanda, gerçek zamanlı veri analitiği ve yapay zeka gibi gelişmiş analitik yetenekleri de destekler.

## Environment'leri Nelerdir?

Azure Synapse, veri analitiği işlemlerini gerçekleştirmek için farklı environment'ler sunar:

- **SQL Pool (Eski adıyla SQL Data Warehouse)**: Büyük veri depolama ve analiz için ölçeklenebilir bir SQL veritabanı hizmeti sunar.
- **Spark Pool**: Apache Spark tabanlı büyük veri işleme ve analizi için bir platform sağlar.
- **Data Lake**: Büyük veri depolama için kullanılan bir dosya sistemidir. Veri Lake ve Synapse Analytics arasında entegrasyon sağlar.

## Hangi Veri Yapılarını Oluşturabilir veya Geliştirebiliriz?

Azure Synapse, çeşitli veri yapıları oluşturabilir ve geliştirebilir:

- **Data Lake**: Büyük veri dosyalarını depolamak için kullanılır. Yapılandırılmamış ve yarı yapılandırılmış verileri destekler.
- **Data Warehouse**: Yapılandırılmış verileri depolamak için kullanılır. SQL tabanlı sorgularla analiz edilebilir.
- **Database**: Yapılandırılmış verileri depolamak ve yönetmek için kullanılır. İşletmelerin transaksiyonel verilerini saklamak için idealdir.

## Terimlerin Farkları

- **Data Lake**: Yapılandırılmamış ve yarı yapılandırılmış verilerin depolandığı geniş bir veri havuzu olarak düşünülebilir. Veri, genellikle orijinal biçiminde saklanır ve daha sonra analiz için işlenir.
- **Data Warehouse**: Yapılandırılmış ve işlenmiş verilerin depolandığı ve analiz edildiği bir veri deposudur. Veriler, genellikle işletmenin çeşitli kaynaklarından toplanır ve daha sonra analiz için optimize edilir.
- **Database**: Yapılandırılmış verilerin saklandığı ve yönetildiği bir veri deposudur. Veri bütünlüğü ve güvenliği gibi özelliklere odaklanır ve işletmenin günlük operasyonları için kullanılır.

Azure Synapse, bu farklı veri yapılarını tek bir platformda birleştirerek işletmelere esneklik ve performans sağlar. Bu sayede, işletmeler verilerini daha etkili bir şekilde yönetebilir ve rekabet avantajı elde edebilirler.

Azure Synapse, veri analitiği ve büyük veri yönetimi için birçok yenilikçi özellik sunar. İşletmeler, bu platformu kullanarak verilerini daha etkili bir şekilde analiz edebilir, rekabet avantajı elde edebilir ve daha iyi iş kararları alabilirler.


# Veri Türleri Açıklaması

Veri, genellikle yapılandırılmış, yarı yapılandırılmış veya yapılandırılmamış olarak sınıflandırılır. Her biri farklı özelliklere ve kullanım senaryolarına sahiptir.

## Yapılandırılmış Veri

Yapılandırılmış veri, geleneksel ilişkisel veritabanlarında bulunan ve sütunlar ve satırlar şeklinde düzenlenmiş veri türüdür. Her sütunun belirli bir veri tipi ve yapıya sahip olduğu bir düzeni vardır. Örnek olarak, bir müşteri veritabanında müşteri adı, soyadı, adresi gibi bilgileri içeren bir tablo yapısını düşünebiliriz. Yapılandırılmış veri, SQL tabanlı sorgularla kolayca işlenebilir ve analiz edilebilir.

## Yarı Yapılandırılmış Veri

Yarı yapılandırılmış veri, yapısal olarak düzenlenmiş olmasına rağmen her kayıtın aynı sütunlara sahip olmadığı veri türüdür. JSON veya XML gibi formatlarda sıklıkla karşılaşılır. Her kayıt, farklı bir yapıya sahip olabilir, ancak genel bir şemaya uyar. Örneğin, bir e-ticaret platformundaki ürünlerin JSON formatında depolanması yarı yapılandırılmış veriye bir örnektir. Ürünlerin her biri farklı özelliklere (renk, boyut, fiyat vb.) sahip olabilir, ancak genel olarak aynı şemaya uyarlar.

## Yapılandırılmamış Veri

Yapılandırılmamış veri, herhangi bir yapıya veya düzene sahip olmayan veri türüdür. Metin dosyaları, log dosyaları, ses dosyaları gibi formatlarda bulunabilir. Bu tür veri genellikle doğrudan kaynaktan alınır ve daha sonra analiz için yapılandırılmış veya yarı yapılandırılmış formata dönüştürülür. Örneğin, bir web sitesinin günlük dosyaları yapılandırılmamış veriye bir örnektir. Bu dosyalarda herhangi bir belirli bir düzen veya yapı olmayabilir, ancak bu veriler daha sonra işlenerek yapılandırılmış veya yarı yapılandırılmış bir veri formatına dönüştürülebilir.

Azure Synapse, bu farklı veri türlerini yönetmek ve analiz etmek için esnek bir platform sağlar. Bu sayede, işletmeler farklı kaynaklardan gelen yapılandırılmış, yarı yapılandırılmış ve yapılandırılmamış verileri tek bir platformda birleştirerek kapsamlı bir veri analizi yapabilirler.

# Data Pipelines

Veri akışı veya veri boruları olarak da bilinen veri boruları, veri işleme süreçlerinin adım adım yürütüldüğü bir dizi otomatik veya manuel işlemi ifade eder. Veri boruları, farklı veri kaynakları arasında veri aktarımını, dönüşümünü ve işlenmesini kolaylaştırır. Veri boruları, ETL (Extract, Transform, Load) süreçlerinin bir parçası olarak kullanılabilir ve genellikle büyük veri analitiği ve iş zekası projelerinde yaygın olarak kullanılır.

## ETL Pipelines

ETL, Extract, Transform, Load kelimelerinin kısaltmasıdır ve veri boruları sürecinin üç ana aşamasını tanımlar:

- **Extract (Çıkarma)**: Verinin kaynak sistemlerden çıkarılması veya alınması.
- **Transform (Dönüştürme)**: Verinin temizlenmesi, standartlaştırılması ve hedef veri modeline uygun hale getirilmesi.
- **Load (Yükleme)**: Dönüştürülmüş verinin hedef sistemlere veya veritabanlarına yüklenmesi.

ETL, veri analitiği ve iş zekası projelerinde veri hazırlama ve işleme süreçlerini yönetmek için yaygın olarak kullanılır.

## Apache Spark Pool

Apache Spark Pool, büyük veri işleme ve analizi için Apache Spark tabanlı bir hesaplama ortamı sağlar. Bu havuz, Apache Spark iş yüklerini çalıştırmak için kullanılır ve büyük veri setlerini paralel olarak işleyebilir.

Örneğin, Azure Synapse Studio içindeki Apache Spark Pool kullanarak aşağıdaki gibi bir senaryo gerçekleştirilebilir:

- **Veri İşleme ve Analiz**: Büyük bir veri setini Apache Spark kullanarak işlemek ve analiz etmek istiyorsunuz. Azure Synapse Studio'da yeni bir Apache Spark not defteri oluşturabilirsiniz.
- **Veri Okuma ve Yazma**: Apache Spark Pool, farklı veri kaynaklarından (örneğin, Azure Blob Storage veya Azure SQL veritabanı) veri okuyabilir ve sonuçlarını çeşitli hedeflere yazabilir. Örneğin, Blob Storage'dan veri okuyup işleyerek sonuçları SQL veritabanına yazabilirsiniz.
- **Makine Öğrenimi ve Veri Madenciliği**: Apache Spark, büyük veri kümeleri üzerinde makine öğrenimi ve veri madenciliği algoritmalarını uygulamak için kullanılabilir. Örneğin, Synapse Studio'da bir Apache Spark not defteri oluşturarak bir sınıflandırma veya kümeleme modeli eğitebilirsiniz.
- **Gerçek Zamanlı Veri İşleme**: Apache Spark, gerçek zamanlı veri işleme işlemleri için de kullanılabilir. Kafka gibi gerçek zamanlı veri kaynaklarından gelen verileri işleyebilir ve sonuçları hemen alabilirsiniz.







# View Yapısı

Veritabanında birden fazla tabloyu JOIN yapısı ile birleştirip, istediğimiz kolonları getirmek için sorgular yazarız. Ancak elde ettiğimiz sorgu sonucunu ilerde tekrar kullanmak istediğimizde, aynı SQL sorgusunu tekrar yazmamız gerekmektedir. Bu nedenle, her ihtiyacımız olduğunda aynı SQL sorgusunu yazmamak için, View (sanal tablo) yapısı kullanılır.

- View oluşturuken, sorgumuz doğru çalışıyor mu diye ilk defasında derlenir ve sonrasında sadece çağrılır.
- Oluşturduğumuz View’lar veriyi içinde tutmaz. Her çağrıldığında sorguyu yeniden çalıştırır.
- Oluşturulan View’lar normal SQL tablosu gibi çağrılır.
- View oluştururken OrdeyBy kullanmak istersek, SELECT ifadesi ile birlikte TOP ifadesinin de kullanılması gerekir.

## Nerelerde Kullanılır:

- Birden fazla tablodan bilgi görmek istediğimizde, karmaşık sorguları basitleştirmek için;
- Göstermek istemediğimiz (Maaş, Kredi Kartı, Adres.. gibi) bilgiler için, erişimi engelleyip güvenlik sağlayabiliriz;
- Karmaşık sorguyu bir defa yazıp, sonrasında normal tablo çağırır gibi sorgu süresini kısaltma gibi yerlerde kullanılmaktadır.

## View Oluşturma (Create View)

Yeni bir view oluşturmak istediğimizde, `CREATE VIEW` komutu ve View ismi yazılıp, sonrasında `AS` ifadesiyle View’da çalışmasını istediğimiz sorgu belirlenir. Böylece sorguyu çalıştırdığımızda yeni bir view oluşturmuş oluruz. Örneğin:

```sql
CREATE VIEW OrderDetails
AS
SELECT PO, Sku, BOM, Date, Country FROM Orders
```
Yukarıdaki örnekte Orders tablosundan istediğimiz kolonları seçip OrderDetails isminde yeni view oluşturduk.

`SELECT * FROM OrderDetails` şeklinde ise View'u çağırabiliriz.

## Şifreli View Oluşturma (With Encryption)

View’ımızın düzenlenebilirliğini kapatmak için şifreleme işlemi uygulanır. Şifrelenen View’lar üzerinde, artık kendimiz dahi değişiklik yapamayız. Bunun için şifreli view oluştururken view kodlarının da yedeğini bir yerde saklamamız, ilerde değişiklik yapmak istediğimizde gerekli olabilir. Şifreli View, normal view oluşturur gibi View isminden sonra `WITH ENCRYPTION` ifadesi eklenerek oluşturulur.

# External Table

External table (harici tablo), veri ambarı veya veritabanı içinde fiziksel olarak depolanmayan, dış kaynaklardaki verilere erişim sağlayan bir veritabanı nesnesidir. Örneğin, Azure Blob Storage veya Azure Data Lake Storage gibi dış veri depolama sistemlerindeki verilere erişmek için external table'lar kullanılabilir. Bu, veri entegrasyonu ve veri analitiği işlemlerinde farklı veri kaynaklarını birleştirmek için yaygın olarak kullanılır.







# Azure Data Factory

Azure Data Factory (ADF), bulut tabanlı bir veri entegrasyonu hizmetidir. Veri hareketi ve veri dönüşüm işlemlerini yönetmek için kullanılır. Farklı veri kaynakları arasında veri aktarımı sağlar, veri işleme süreçlerini otomatikleştirir ve veri akışlarını izler. ADF, karmaşık veri entegrasyon senaryolarını yönetmek için kullanıcı dostu bir arayüz sunar.

# Azure Synapse Dedicated ve Serverless

Azure Synapse Analytics, büyük veri analitiği ve iş zekası için kapsamlı bir çözüm sunan bir bulut veri platformudur. Synapse, iki farklı dağıtım modeli sunar: Dedicated ve Serverless.

- **Azure Synapse Dedicated**: Bu modelde, bir veri ambarı (data warehouse) ve büyük veri analitiği için ölçeklenebilir bir hesaplama kaynağı ayrılmış bir küme üzerinde çalışır. Bu, yüksek performanslı ve özel bir ortam sağlar, ancak sürekli olarak kaynakları kullanır ve maliyetlidir.

- **Azure Synapse Serverless**: Bu modelde, altyapıyı yönetmekle uğraşmadan büyük veri analitiği işlemlerini gerçekleştirebilirsiniz. Sunulan kaynaklar ihtiyaca göre otomatik olarak ölçeklenir ve kullanılan işlem ve depolama miktarına göre ücretlendirilir.

Her iki model de veri gölü (data lake) ile entegre çalışabilir ve veri ambarı, büyük veri analitiği ve iş zekası projeleri için kapsamlı bir çözüm sunar.

# Data Lake ile İlgisi

Azure Synapse, Data Lake ile entegre çalışabilir. Veri gölü (data lake), yapılandırılmamış ve yarı yapılandırılmış verileri depolamak için kullanılan bir depolama sistemidir. Azure Synapse Analytics içindeki Synapse Studio üzerinden Data Lake'e bağlanabilir, verileri okuyabilir ve işleyebilirsiniz. Bu, büyük veri analitiği ve iş zekası projelerinde veri kaynaklarını genişletmek ve çeşitli veri yapılarını bir arada kullanmak için önemlidir.


# Azure Blob Storage Nedir?
**Tanım:**
- Azure Blob Storage, yapılandırılmamış veri depolamak için optimize edilmiş bir bulut depolama hizmetidir.
- Temelde üç tür blob vardır: blok blobları (genel amaçlı veri depolama), append blobları (log verileri için) ve page blobları (sanal diskler için).
- Blob, Binary Large Object'ın kısaltmasıdır ve genellikle büyük dosyaları veya veri kümelerini ifade eder.

## Ne İşe Yarar?

Azure Blob Storage, aşağıdaki gibi çeşitli kullanım senaryoları için idealdir:

1. **Veri Depolama**: Büyük veri dosyalarını, medya dosyalarını, yedekleri ve diğer nesneleri güvenli ve ölçeklenebilir bir şekilde depolamak için kullanılabilir.
   
2. **Büyük Veri Analitiği**: Büyük veri kümelerini depolayarak ve Azure Synapse veya diğer büyük veri analitiği araçları ile entegre ederek veri analitiği ve iş zekası işlemlerini gerçekleştirmek için kullanılabilir.
   
3. **Medya İşleme**: Resimler, videolar ve diğer medya dosyalarını depolamak ve işlemek için kullanılabilir. Azure Blob Storage, medya dosyalarını depolamak ve küresel olarak dağıtılan içerik dağıtım ağları (CDN) aracılığıyla sunmak için de idealdir.

## Özellikler

Azure Blob Storage, şu özellikleri sağlar:

- **Yüksek Ölçeklenebilirlik**: Azure Blob Storage, büyük miktarda veriyi güvenli ve ölçeklenebilir bir şekilde depolamak için tasarlanmıştır. Verilerinizin depolanma kapasitesini ihtiyacınıza göre kolayca genişletebilirsiniz.
  
- **Güvenlik**: Blob Storage, verilerinizi şifreleme ve erişim kontrolleri gibi güvenlik önlemleriyle korur. Verileriniz, Microsoft'un güvenlik standartlarına uygun olarak korunur.
  
- **Yüksek Dayanıklılık**: Azure Blob Storage, verilerinizi çoğaltarak depolar ve birden fazla bölgede yedekler. Bu sayede, veri kaybı riskini en aza indirir ve iş sürekliliğini sağlar.
  
- **Uygun Maliyet**: Azure Blob Storage, kullanılan depolama miktarına göre ölçeklenebilir fiyatlandırma modeli sunar. Yalnızca kullandığınız depolama miktarı için ödersiniz, gereksiz maliyetlerden kaçınarak maliyetleri optimize edebilirsiniz.

Azure Blob Storage, bulut tabanlı veri depolama ihtiyaçlarınızı karşılamak için güvenilir, ölçeklenebilir ve uygun maliyetli bir çözümdür. Bu sayede, verilerinizi güvenli bir şekilde depolayabilir, işleyebilir ve analiz edebilirsiniz.

# Azure Blob Storage ve Azure Data Lake Arasındaki Farklar

Azure Blob Storage ve Azure Data Lake, Microsoft Azure tarafından sunulan iki farklı bulut depolama çözümüdür. Her ikisi de büyük miktarda veri depolamak ve yönetmek için tasarlanmıştır, ancak kullanım amaçları ve sundukları özellikler açısından belirgin farklılıklar vardır.

## Azure Blob Storage

**Özellikler:**
- Azure Blob Storage, yapılandırılmamış veri depolamak için optimize edilmiş bir bulut depolama hizmetidir.
- Basit depolama çözümleri için idealdir.
- Düşük maliyetli ve yüksek performanslıdır.
- REST API ve çeşitli SDK'lar aracılığıyla erişilebilir.
- Hot, Cool ve Archive gibi erişim katmanları sunar, bu da verinin erişim sıklığına göre maliyet optimizasyonu sağlar.

**Kullanım Örneği:**
- Web uygulamalarında resim, video gibi büyük medya dosyalarının depolanması.
- Yedekleme ve arşivleme çözümleri.
- Log verilerinin saklanması.

## Azure Data Lake Storage (ADLS)

**Tanım:**
- Azure Data Lake Storage, büyük veri analitiği iş yüklerini desteklemek için optimize edilmiş bir bulut depolama hizmetidir.
- Hadoop dağıtık dosya sistemi (HDFS) uyumlu bir dosya sistemi sağlar.

**Özellikler:**
- Büyük ölçekli analiz ve veri işleme iş yükleri için idealdir.
- Hiyerarşik dosya sistemi (HFS) sunar, bu da dizinler ve dosyalar üzerinde daha ayrıntılı yönetim ve erişim kontrolü sağlar.
- Azure Synapse Analytics, Azure Databricks ve diğer büyük veri analitik araçlarıyla sıkı entegrasyon.
- Yüksek performanslı veri aktarımı ve yönetimi.

**Kullanım Örneği:**
- Büyük veri analitiği ve makine öğrenimi projeleri.
- Kurumsal veri ambarı çözümleri.
- IoT verilerinin toplanması ve analizi.

## Farklar ve Kullanım Senaryoları

### Yapılandırılmamış Veriler
- **Blob Storage:** Büyük dosyaların (resim, video, yedekleme dosyaları) depolanması.
  - **Örnek:** Bir e-ticaret sitesinin kullanıcı fotoğraflarını ve videolarını depolamak.

### Büyük Veri Analitiği
- **Data Lake Storage:** Büyük veri setlerinin analizi ve işlenmesi.
  - **Örnek:** Bir telekom şirketinin günlük ağ trafiği verilerini analiz edip performans ve kullanıcı davranışlarını değerlendirmesi.

### Dosya Sistemi Yönetimi
- **Blob Storage:** Basit dosya depolama ve erişim.
  - **Örnek:** Bir uygulama günlük dosyalarının saklanması.
- **Data Lake Storage:** Hiyerarşik dosya sistemi ve ileri düzey erişim kontrolleri.
  - **Örnek:** Büyük ölçekli bir finans kurumunun günlük işlem verilerini organize etmesi ve analiz etmesi.

### Entegrasyon ve Performans
- **Blob Storage:** Genel veri depolama ve çeşitli Azure hizmetleri ile entegrasyon.
  - **Örnek:** Bir medya şirketinin video içeriklerini depolayıp dünya çapında kullanıcılarına sunması.
- **Data Lake Storage:** Büyük veri işleme araçlarıyla entegrasyon ve yüksek performanslı veri işleme.
  - **Örnek:** Bir sağlık kurumunun hastane verilerini analiz edip sağlık trendlerini değerlendirmesi.

## Sonuç

Azure Blob Storage ve Azure Data Lake Storage, farklı kullanım senaryolarına hitap eden iki depolama çözümüdür. Blob Storage, genel veri depolama için daha basit ve maliyet etkin bir çözümken, Data Lake Storage, büyük veri analitiği ve ileri düzey veri yönetimi gereksinimleri, data warehousing için daha uygun bir seçenektir. Detay olarak ise ADLS Gen2 Actual hierarchy folder structure kullanırken blob storage logical hiyerarşi kullanır yani
ADLS aynı windows gibi explorer'a sahiptir ama blob storage logicaldır. ADLS Fine grained access controls sağlarken Blob storage resource level access control yapar. yani blob storage bir bütün gibi davranır.




# Faydalı Bağlantılar:
- https://awesomedataengineering.com/
- https://furkanalaybeg.medium.com/sqlde-view-yap%C4%B1s%C4%B1-50e3d90d4760
- https://www.youtube.com/watch?v=DZneFEqH-H4&list=PLMWaZteqtEaIZxPCw_0AO1GsqESq3hZc6&index=3
