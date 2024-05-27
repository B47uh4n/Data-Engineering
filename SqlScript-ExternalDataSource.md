```sql
Use demoDB -- serverless sql pool'umuz ile oluşturduğumuz LDW'nin adı
GO
-- credentials'ı koruyacak master keyi oluşturuyoruz
CREATE MASTER KEY ENCRYPTION BY PASSWORD = 'Batuhan123+'

-- ADLS ile baglanti kurmak icin saglamamiz gereken credentials kısmı, 
-- ADLS içerisinde shared access signature sekmesinden allowed resource typesta bulunan tikleri işaretleyerek izin verip Generate SAS demeliyiz.
-- Buradan SAS Token'ı kopyalayıp ilk karakter olan ? silinir.
CREATE DATABASE SCOPED CREDENTIAL testCredential
WITH IDENTITY = 'SHARED ACCESS SIGNATURE',
SECRET = '(baglanacagimiz adlsın ? karakteri silinen SAS Tokenı )'

-- ADLS, Settings, Endpoints sekmesindeki primary DLS endpoint adresini kopyalariz
CREATE EXTERNAL DATA SOURCE testDataSource 
WITH (
    LOCATION = 'primary endpoint adresimiz',
    CREDENTIAL = testCredential
)
```
## CREATE DATABASE SCOPED CREDENTIAL için :
```sql
CREATE DATABASE SCOPED CREDENTIAL ManagedIdentity
WITH IDENTITY = 'Managed Identity'
GO
```
-- şeklinde bir kullanım da yapabilirdik. Eğer managed identitymizin data source oluşturmak istediğimiz lokasyondaki adsl'e erişimi varsa genelde bu yöntem kullanılıyormuş.
