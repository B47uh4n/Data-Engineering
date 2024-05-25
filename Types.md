# Veritabanı Türleri ve Örnekleri (1 numaralı video linki)

## Satır Tabanlı Veri Tablosu (Row-Based Database)

Satır tabanlı veri tablolarında veriler satırlar halinde saklanır. Her bir satır, bir veri kaydını temsil eder ve tüm sütun değerleri bir arada tutulur. Bu yapı özellikle OLTP (Online Transaction Processing) uygulamaları için uygundur, çünkü veri ekleme, güncelleme ve silme işlemleri hızlıdır.

#### Örnek:

| ID  | İsim     | Yaş | Şehir     |
|-----|----------|-----|-----------|
| 1   | Ahmet    | 25  | İstanbul  |
| 2   | Ayşe     | 30  | Ankara    |
| 3   | Mehmet   | 22  | İzmir     |

Yukarıdaki tabloda, her satır bir kişinin bilgilerini içerir ve bir kaydı temsil eder.

## Sütun Tabanlı Veritabanı (Columnar Database)

**Açıklama:**
Sütun tabanlı veritabanları, verileri satırlar yerine sütunlar halinde depolar. Her bir sütun, aynı türdeki verileri bir arada tutar. Bu yapı, veri analitiği, OLAP (Online Analytical Processing) ve veri ambarı (data warehouse) uygulamaları için uygundur, çünkü belirli sütunlar üzerinde yapılan sorgulamalar daha hızlıdır. Her sütun, o sütunun tüm değerlerini içerir. Ancak, bunu tablodaki satırlar ve sütunlar şeklinde görselleştirmek biraz zor olabilir çünkü genellikle fiziksel depolama yapısını ifade eder.

#### Örnek:

Sütun tabanlı veriyi göstermek için, her sütunun ayrı ayrı saklandığını hayal edebiliriz:

**ID Sütunu:**
- 1, 2, 3

**İsim Sütunu:**
- Ahmet, Ayşe, Mehmet gibi.

Bu formatta, her sütun birbirinden bağımsız olarak saklanır. Bu yüzden belirli bir sütun üzerinde yapılan sorgulamalar daha hızlı olabilir çünkü sadece o sütun belleğe yüklenir ve işlenir. Örneğin, yaş ortalamasını hesaplamak istediğinizde, sadece "Yaş" sütununa erişmeniz yeterlidir.

### Kısa Karşılaştırma:

- **Satır Tabanlı:**
  - Avantaj: Hızlı veri ekleme, güncelleme ve silme.
  - Dezavantaj: Büyük veri setlerinde analiz ve raporlama performansı daha düşüktür.
- **Sütun Tabanlı:**
  - Avantaj: Veri analizi ve raporlama için daha hızlı sorgulama.
  - Dezavantaj: Veri ekleme ve güncelleme işlemleri daha karmaşık ve yavaştır.

Bu farklar, hangi veri tabanı modelinin kullanılacağına karar verirken önemli rol oynar ve uygulamanın ihtiyaçlarına göre seçilmelidir.


## 3. NoSQL Veritabanı

**Açıklama:**
NoSQL veritabanları, yapılandırılmamış veya yarı yapılandırılmış verileri depolamak için kullanılır. Genellikle büyük veri ve yüksek performans gerektiren uygulamalar için tercih edilir.

**Örnekler:**
- **MongoDB:** Belge tabanlı bir NoSQL veritabanıdır. JSON benzeri belgeler kullanarak esnek veri modeli sağlar.
- **Redis:** Anahtar-değer tabanlı bir NoSQL veritabanıdır. Yüksek hızlı veri erişimi gereksinimleri için kullanılır.
- **Neo4j:** Grafik tabanlı bir NoSQL veritabanıdır. Karmaşık ilişkileri ve bağlantıları yönetmek için optimize edilmiştir.

## 4. Grafik Veritabanı (Graph Database)

**Açıklama:**
Grafik veritabanları, verileri düğümler ve kenarlar olarak temsil eder. Bu yapı, özellikle ilişkisel verilerin yönetimi ve analizi için uygundur.

**Örnekler:**
- **Neo4j:** Popüler bir grafik veritabanıdır. Sosyal ağ analizleri, öneri sistemleri ve dolandırıcılık tespiti gibi uygulamalarda kullanılır.
- **Amazon Neptune:** AWS tarafından sunulan yönetilen bir grafik veritabanı hizmetidir. İlişkisel veri modelleri ve sorguları için optimize edilmiştir.
- **ArangoDB:** Çok model destekli bir veritabanıdır. Hem grafik hem de diğer veri modellerini destekler.

## Özet

- **Sütun tabanlı veritabanları**, veri analitiği ve raporlama iş yükleri için optimize edilmiştir ve genellikle veri ambarı çözümlerinde kullanılır.
- **Satır tabanlı veritabanları**, OLTP uygulamaları için uygundur ve geleneksel iş uygulamalarında yaygın olarak kullanılır.
- **NoSQL veritabanları**, esneklik ve ölçeklenebilirlik gerektiren büyük veri uygulamaları için idealdir.
- **Grafik veritabanları**, karmaşık ilişkisel verileri yönetmek ve analiz etmek için kullanılır.

# Apache Parquet Nedir?

Parquet, özellikle büyük veri analitiği için optimize edilmiş bir sütun tabanlı depolama formatıdır. Apache Parquet, Apache Hadoop ekosisteminde yaygın olarak kullanılır ve birçok büyük veri işleme araçları ve platformları tarafından desteklenir.

## Parquet'in Özellikleri

1. **Sütun Tabanlı Depolama:**
   - Parquet, verileri sütunlar halinde depolar. Bu, özellikle belirli sütunlar üzerinde sorgulama yaparken performans avantajı sağlar.

2. **Yüksek Sıkıştırma:**
   - Sütun tabanlı depolama, benzer türdeki verilerin birlikte depolanmasına olanak tanır, bu da verinin sıkıştırılmasını daha etkili hale getirir.

3. **Verimli Okuma:**
   - Sadece ihtiyaç duyulan sütunlar okunur, bu da I/O maliyetlerini azaltır ve sorgu performansını artırır.

4. **Veri Tipi Desteği:**
   - Parquet, kompleks veri türlerini (nested data) destekler, yani iç içe geçmiş veri yapılarıyla çalışmak mümkündür.

## Neden Parquet Kullanılır?

- **Büyük Veri İşlemleri:**
  - Parquet, büyük veri setlerini verimli bir şekilde depolamak ve işlemek için idealdir.
- **Analitik Sorgular:**
  - Analitik iş yükleri genellikle belirli sütunlar üzerinde yoğunlaşır. Parquet, bu tür sorgular için optimize edilmiştir.
- **Sıkıştırma ve Depolama Verimliliği:**
  - Parquet, yüksek sıkıştırma oranları sağlar, bu da depolama maliyetlerini düşürür.

## Parquet Kullanım Alanları

- **Veri Ambarları:**
  - Veri ambarlarında büyük veri setlerinin depolanması ve analizi için yaygın olarak kullanılır.
- **ETL (Extract, Transform, Load) İşlemleri:**
  - Parquet dosyaları, veri entegrasyon süreçlerinde (ETL) yaygın olarak kullanılır.
- **Apache Hadoop ve Apache Spark:**
  - Hadoop ve Spark gibi büyük veri işleme araçları, Parquet formatını doğal olarak destekler.

## Parquet ile Çalışmak

Parquet dosyalarıyla çalışmak için birçok araç ve platform mevcuttur. Örneğin:

- **Apache Spark:**
  - `spark.read.parquet("path/to/parquet/file")` komutuyla Parquet dosyaları okunabilir.
- **Pandas (Python Kütüphanesi):**
  - `pandas.read_parquet("path/to/parquet/file")` komutuyla Parquet dosyaları okunabilir.
- **Azure Synapse:**
  - Azure Synapse Analytics, Parquet dosyalarını destekler ve bunları işlemek için kullanılabilir.

## Özet

Apache Parquet, sütun tabanlı bir depolama formatı olup, büyük veri analitiği ve işleme iş yükleri için optimize edilmiştir. Sütun tabanlı yapısı, yüksek sıkıştırma oranları ve verimli okuma performansı sunar. Parquet, veri ambarları, ETL işlemleri ve büyük veri işleme araçları tarafından yaygın olarak kullanılır.

## Faydalı Bağlantılar
https://www.youtube.com/watch?v=8KGVFB3kVHQ (1)
