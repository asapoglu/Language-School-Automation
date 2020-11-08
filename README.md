# Language School Automation

## 1. İÇİNDEKİLER

- 1. İÇİNDEKİLER
- 2. GİRİŞ
  * 2.1 Sistemin Amacı
  * 2.2 Sistemin Kapsamı
  * 2.3 Kabul ve Kısıtlar
  * 2.4 Varsayımlar
  * 2.5 Hedefler ve Başarı Kriterleri
- 3. YAZILIM GELİŞTİRME SÜRECİ
- 4. PROJE PLANI
  - 4.1 Ekip Organizasyon Şeması
  - 4.2 Görev Dağılım
  - 4.3 Gantt Diyagramı
  - 4.4 Risk Analizi
- 5. MODELLEME
  - 5.1 E-R Diyagramı
  - 5.2 Veri Akış Diyagramı Taslak
  - 5.3 Birinci Düzey Veri Akış Diyagramı
  - 5.4 İkinci Düzey Veri Akış Diyagramı
- 6. GERÇEKLEŞTİRME
  * 6.1 Veri Tabanı Tasarımı
   + 6.1.1Tablolar
   + 6.1.2Veriler
 - 6.2 Arayüz Tasarımı
   - 6.2.1Giriş Ekranı
   - 6.2.2Admin Panel
   - 6.2.3Şube Panel
- 7. TEST
  - 7.1 Test
   - 7.1.1Kodlama Aşaması
   - 7.1.2Kodlama Sonrası Aşama
   - 7.1.3Son Kullanıcı
- 8. Değerlendirme
 - 8.1 Müşteri Değerlendirmesi


## 2. GİRİŞ

### 2.1 Sistemin Amacı

Dil Kursu Otomasyon Yazılımının amacı özellikle çok şubeli ve dil eğitimi üzerine
yoğunlaşmış işletmelerin ders planlaması, öğretmen ve sınıf organizasyonu, öğrenci kaydı ve
takibi gibi temel operasyonlarını planlı ve eşgüdümlü olarak yönetmelerini ve takip
etmelerini sağlamaktır.

### 2.2 Sistemin Kapsamı

Yazılım temelde 2 tip kullanıcı için hazırlanmıştır. Sistem yöneticisi, öğretmen işe alımları,
mevcut dile ve seviyeleri dışında yeni tip kurs açılması ve ihtiyaç duyulduğunda yeni şube
açılması işlemlerini yapmaktadır.
Şube Kullanıcısı ise öğrenci kaydı ve ödeme takibi işlemlerini yapmaktadır.

### 2.3 Kabul ve Kısıtlar

- Yazılım dil kursu yetkililerince kullanılacaktır. Öğretmen ve öğrenci erişimi
    bulunmamaktadır.
- Şubelerde en fazla 10 derslik bulunmaktadır.
- Sistem yöneticisi kullanıcısı halihazırda tanımlı gelmektedir. Sonradan bir sistem
    yöneticisi oluşturmak mümkün değildir.
- Sistem yöneticisi ve şubeler için sistem giriş parola bilgisi otomatik olarak 0
    atanmaktadır.
- Tüm dillere ait eğitimlerin 6 kurdan oluşmaktadır.
- Öğrencilerin taksitli ödeme istediklerinde taksit sayısı 5’tir.

### 2.4 Varsayımlar

Yazılımın sağlıklı test edilmesi için işleyen şubelerinin mevcut olduğu ve bu sebeple
öğretmen ve kurslarının bazılarının hazır olduğu varsayılmıştır.

### 2.5 Hedefler ve Başarı Kriterleri

Merkez yönetiminin öğretmen alımı, yeni tip kurs açılması, yeni şube açılımı gibi
operasyonları rahatça yönetebilecekleri bir sistem yapılması ve bu sayede merkezin eşgüdüm
ve planlama gibi süreçlere yardımcı olunması;
Şubelerin kendi organizasyonları, öğrenci kaydı ve ödeme takibi gibi şube işlemlerini
diğer şubeler ve merkezle eşgüdüm içerisinde takip etmeleri;
Yazılımda temel hedefler olarak konulmuş ve çalışma bu yönde yapılmıştır.


## 3. YAZILIM GELİŞTİRME SÜRECİ

Proje başlangıcında klasik yaklaşımla ilerleneceği düşünüldüğü için Şelale (Waterfall)
Süreç Modeli seçildi. Şelale Süreç Modeli analiz, tasarım, gerçekleştirme ve test olarak 4
süreçten oluşur ve süreçler bu sırayla ilerler.

- Analiz
- Tasarım
- Gerçekleme
- Test

![NicePng_water-fall-png_863932](https://user-images.githubusercontent.com/72756431/98467287-88b93a80-21e5-11eb-93cc-c93b86e93e9f.png)

Öte yandan henüz tasarım aşamasında, temelde projenin 2 tip kullanıcı için tasarlanması
kararı alınınca Hızlı Uygulama Geliştirme (RAD Rapid Application Develeopment) Süreç Modeli
öne çıktı. Bu sayede 2 farklı kullanıcının her biri için farklı bir ekibin çalışmasının
projeye hızı kazandıracağı düşünüldü.
Hızlı Uygulama Geliştirme Modeli’de temelde Şelale Modeli gibi klasik modellerden
biridir. Şelale Modeli’nden farkı ise analiz ve planlamanın ardından gerçekleştirme kısmında
işin ekiplere bölünmesine olanak vermesidir. Bu yazılımın geliştirilmesi bakımından avantaj
sağlarken, analiz ve tasarım aşamalarında yapılacak hataların düzeltilmesi Şelale Modeli’ne
göre zordur ve bu sebeple dezavantaj içerir.
Oluşturulmak istenilen programa uyumlu ve bu projede Şelale Modeli’nden zaman ve işleyiş
olarak daha uygun olan Hızlı Uygulama Geliştirme Süreci tercih edildi. Analiz ve tasarım
aşamaları üzerinde yoğunlaşılarak ilerleyen süreçte çıkacak sorunlar önlendi.

## 4. PROJE PLANI

Proje başlangıcında öncelikle çok şubeli ve farklı dillerde eğitim veren bir dil kursu
yapısı üzerinde analiz başladı. Benzer dil kursları internet siteleri üzerinden incelendi.
Çeşitli forum sitelerinde buraya giden öğretmen ve öğrencilerin yorumlarından veya daha önce
bu kurslarda eğitim almış kişilerle yapılan görüşmelerle kursların yapısı ve işleyişi
incelendi. Anlaşılmayan konular hakkında farklı dile kursları aranarak bilgi alındı.


Analiz aşamasının ardından tasarım aşamasına başlandı. Toplanıp değerlendirme imkanı
olmadığı için bu aşamada mesajlaşma ve online görüşme kanallarıyla grup toplantıları
yapılarak model oluşturuldu. Modele dair prototip çalışmaları yine benzer kanallarla grup
içerisinde paylaşılarak değerlendirildi. Olumlu görülen tasarım ileride bir hata ile
karşılaşılmaması için kontrol edildi. Risk analizi oluşturuldu.
Ardından görev dağılımı ve iş planlaması yapılarak gerçekleştirme süreci başladı.
Öncelikle veri tabanı oluşturuldu. Sonrasında proje iki tip kullanıcı için iki modülde
ilerledi. Düzenli toplantılar, bilgilendirme mesajları ve test ile eşgüdüm sağlandı.
Proje bitişinde yazılım test aşamasına geçildi. Önceki aşamaların düzgün yürütülmesi
sebebiyle büyük problemlerle karşılaşılmadı. Karşılaşılan ufak problemler giderilerek
yazılım nihai haline ulaştı.

### 4.1 Ekip Organizasyon Şeması

Ekip yapısı demokratiktir tüm ekip üyelerinin ağırlıkları eşittir. Kararlar oylama ile
alınmaktadır.

### 4.2 Görev Dağılım

- **Abdurrahman ŞAPOĞLU** : ERD, VAD, veri tabanı işlemleri, kodun oluşturulması, Gantt
    diyagramı, ERD, VAD, kodun oluşturulması, Prototipleme, rapor hazırlama, risk analizi,
    kodun oluşturulması
    
Projenin analiz kısmı fikir alışverişi ve araştırmalarla beraber yapılmıştır. Tasarım
aşamasında herkesin katılımı, alternatif görüşlerin paylaşımı ve incelenmesiyle ortak karar
doğrultusunda ilerlenmiştir.

### 4.3 Gantt Diyagramı
![giant](https://user-images.githubusercontent.com/72756431/98467325-bd2cf680-21e5-11eb-8611-dc0c2a96430e.png)

### 4.4 Risk Analizi
![risk](https://user-images.githubusercontent.com/72756431/98467336-ccac3f80-21e5-11eb-854a-121313d098f1.png)

Risk yönetimi, potansiyel riskleri sistematik olarak belirleyip takip ederek,
gerçekleşme olasılığını ya da etkisini azaltarak riskin projenin gerçekleşme sürecine
vereceği zararı minimuma indirmeyi hedefler. Risk yönetimi ayrıca her bir risk için, risk
gerçekleştiğinde devreye alınacak bir “B” planını da içermelidir

## 5. MODELLEME

### 5.1 E-R Diyagramı

![diagram](https://user-images.githubusercontent.com/72756431/98467343-d7ff6b00-21e5-11eb-8fa5-cde6ae004477.png)

### 5.2 Veri Akış Diyagramı Taslak

![veri akış diyagramı taslak](https://user-images.githubusercontent.com/72756431/98467357-e483c380-21e5-11eb-8b48-f7f2f7a0ed4d.jpg)
### 5.3 Birinci Düzey Veri Akış Diyagramı

![Birinci Düzey veri akış diyagramı](https://user-images.githubusercontent.com/72756431/98467367-f2394900-21e5-11eb-9c84-cb755133da16.png)

### 5.4 İkinci Düzey Veri Akış Diyagramı

![2 SEVIYE](https://user-images.githubusercontent.com/72756431/98467387-0a10cd00-21e6-11eb-8810-a25aa615ce95.png)

## 6. GERÇEKLEŞTİRME

### 6.1 Veri Tabanı Tasarımı

Veritabanımızı gerçekleştirirken ilişkisel veritabanı modelini kullandık. Bu model
verileri her bir satırı tanımlayan benzersiz bir anahtarla sütunların ve satırların bir veya
daha fazla tabloya ilişkilenmesini sağlar.

#### 6.1.1Tablolar
![Resim1](https://user-images.githubusercontent.com/72756431/98467463-81def780-21e6-11eb-9d3f-d776c8d8021d.png)

Veritabanında birbirlerine bağlı 11 tane tablo vardır. Her tablonun kendi otomatik artan
benzersiz id numarası vardır. Tablolar birbirlerine id’leri üzerine foreign keyler ile
bağlanmışlardır. Örneğin öğretmenler ile kurs tabloları arasında çok’a çok bir ilişki olduğu
için öğretmenbeceri isminde bir tablo üzerinden bağlantıları sağlanmaktadır.


#### 6.1.2Veriler
![Resim3](https://user-images.githubusercontent.com/72756431/98467482-9de29900-21e6-11eb-89ab-d48ee3bc8dae.png)

Örnekte görüldüğü gibi açılankurslar tablosu kurs_id ile kurslar tablosuna, öğretmen_id
ile öğretmenler tablosuna, derslik_id ile derslik tablosuna bağlıdır.

### 6.2 Arayüz Tasarımı

Programımızın arayüzünü geliştirirken Java programlama dili ve Swing arayüz geliştirme
aracı kullanılmıştır.

#### 6.2.1Giriş Ekranı
![loginGirisHatası](https://user-images.githubusercontent.com/72756431/98467508-c4083900-21e6-11eb-9fb7-8c52a88a6b6c.png)

Yazılım çalıştırıldığında Kullanıcı ID ve şifreyi ister. Hatalı girişte hata mesajı
verir. 2 tür kullanıcı tipi vardır ve program bu noktada admin ve şube arayüzü şeklinde
otomatik olarak dallanır. Kullanıcı id bilgisine “admin” şifre olarak “0” girdiğimizde admin
panel “Şube Adı” ve şifre olarak “0” girdiğimizde şube paneli açılır.


#### 6.2.2Admin Panel

Admin panelinde şube, öğretmen ve dersler listesi ile birlikte gerçekleştirebileceğimiz
6 seçenek karşılar.
![adminpanel](https://user-images.githubusercontent.com/72756431/98467518-d1bdbe80-21e6-11eb-95bd-f44ea0ae6565.png)

**6.2.2.1 Yeni Şube Oluştur**
Mevcudun yetmediği durumlarda yeni şube oluşturur. Yeni oluşturulan şube arka planda
sisteme giriş için veritabanında da hem users hem şube tablolarında oluşturulur. Default
olarak yeni oluşturulan şubelerin derslikleri yoktur şube düzenleme ekranından şubeye
derslik sonradan eklenebilir.

![Resim5](https://user-images.githubusercontent.com/72756431/98467557-0df11f00-21e7-11eb-879a-727388136bac.png)


**6.2.2.2 Şube Düzenle**
Şube listesinden seçtiğimiz şubenin adını, adresini ve ulaşım bilgilerini
düzenleyebilir şubelere yeni derslikler ekleyebiliriz. Şube listesinden Mouse ile şube
seçmediğimiz zaman bu modüle ulaşmaktayız.

![Resim6](https://user-images.githubusercontent.com/72756431/98467615-66282100-21e7-11eb-9584-90ce7ebc3f34.png)

**6.2.2.3 Yeni Öğretmen Oluştur**
Yeni öğretmen kaydı yapılır. Başlangıçta kaydı yapılan öğretmenin şubesi ve verebileceği
dersler yoktur. Bu bilgiler sonradan öğretmen düzenle modülü ile oluşturulur.

![Resim7](https://user-images.githubusercontent.com/72756431/98467617-67594e00-21e7-11eb-910a-9cacf9e610ba.png)


**6.2.2.4 Öğretmen Düzenle**
Öğretmenler listesinden seçtiğimiz öğretmenlerin iletişim bilgileri, verebileceği dersleri,
öğretmenin hangi şubede ders vereceğini düzenleyebileceğimiz bir modüldür. Bu modül
veritabanında ogretmen ve ogretmenbeceri tablolarını eşzamanlı olarak günceller.

![Resim8](https://user-images.githubusercontent.com/72756431/98467618-67594e00-21e7-11eb-9221-bd59f4a353af.png)

**6.2.2.5 Yeni Ders Oluştur**
Bu modül ile dil kursumuzda eğitimini verebileceğimiz yeni dilleri ve bu dillerin
taksitli ve peşin fiyatlarını belirleyebilmekteyiz.

![Resim9](https://user-images.githubusercontent.com/72756431/98467619-67f1e480-21e7-11eb-8a52-9b2a13a1db3f.png)


**6.2.2.6 Yeni Kurs Tanımla**
Bu modül ile şubelerimizdeki halihazırda verilen derslerin gün, saat, öğretmen, dil ve
seviye bilgilerini anlık olarak görebilir boş olan gün ve saatlere yeni dersler
ekleyebilmekteyiz. Bu ekranda kurs oluşturmak istediğimiz alanı seçtiğimizde bize
oluşturulacak kursun detaylarını gireceğimiz yeni bir modül açılmaktadır.

![Resim10](https://user-images.githubusercontent.com/72756431/98467620-67f1e480-21e7-11eb-81a5-ed5c694b7cde.png)

Açılan bu ekranda seçtiğimiz şubedeki öğretmenleri görüp yine seçtiğimiz öğretmenin
verebileceği dersler listesinden ders seçebilmekteyiz.

![Resim11](https://user-images.githubusercontent.com/72756431/98467621-688a7b00-21e7-11eb-9730-ded0b3da0ef5.png)



#### 6.2.3Şube Panel

Şube panelinde yeni öğrenci kaydet, ödeme al, şube ders programlarını ile ilgili işlemler yapabileceğimiz 3 seçenek karşımıza çıkmaktadır.

![Resim12](https://user-images.githubusercontent.com/72756431/98467622-688a7b00-21e7-11eb-8990-a17dbcd61ce4.png)

**6.2.3.1 Yeni Öğrenci Kaydet**
Bu menüde şube yetkilisi bağlı bulunduğu şubeye veya başka bir şubeye öğrenci kaydı
yapar. Şube listesi ve ders bilgileri ile filtreleme yapıp istenilen şubenin istenilen
kursuna öğrenci kaydı yapılmaktadır. Anlık olarak kursların peşin ve taksitli fiyat bilgileri yine bu listede gözükmektedir. Taksitli bilgileri seçilen kursun fiyatına göre otomatik olarak belirlenmekte ve elle değiştirilebilmektedir.

![Resim13](https://user-images.githubusercontent.com/72756431/98467623-688a7b00-21e7-11eb-98ae-ca1e8a78dd77.png)

Peşin ödemede taksit sütunları yerine tek bir giriş seçeneği gelir, bu sebeple kurs
ücretinin tamamı ödenmediği takdirde öğrencinin kaydı yapılamaz.

![Resim14](https://user-images.githubusercontent.com/72756431/98467624-69231180-21e7-11eb-873a-bb48ccbbb27a.png)


**6.2.3.2 Ödeme Al**
Bu modülde sadece taksitli ödeme yapan öğrenciler ve ödedikleri ödemedikleri taksit
bilgileri gözükür. Ödenmeyen taksitler kırmızı olarak gözükür ve ödeme al butonuna
tıklandığında ödenmemiş ilk taksit otomatik olarak ödenir.

![Resim15](https://user-images.githubusercontent.com/72756431/98467625-69231180-21e7-11eb-96cf-926e9fff4844.png)

**6.2.3.3 Şube Ders Programı**
Bu menüde kendi şubesi ve diğer şubelerde olan ders programlarını görebilir.

![Resim16](https://user-images.githubusercontent.com/72756431/98467627-69bba800-21e7-11eb-97e7-5d64efad778e.png)



## 7. TEST

### 7.1 Test

#### 7.1.1Kodlama Aşaması

Yazılım programlama esnasında test edilerek denendi. Bu kısımda karşılaşılan problemler
analiz edilerek çözüldü.

#### 7.1.2Kodlama Sonrası Aşama

Yazılım son haline geldikten sonra ekip tarafından tüm işlevler test edildi. Özellikle
aynı veri tablosundan veri çeken kısımların veri değişikliklerinin düzgün işlenip işlenmediği
incelendi. Karşılaşılan problemler çözüldü, tüm kısımların ve fonksiyonların düzgün
çalıştığı görüldü.

#### 7.1.3Son Kullanıcı

Yazılım kullanıcılar tarafından denendi. Programın çalışmasında sorun olmayan fakat son
kullanıcının çalışmasına etki eden hata mesajları, uyarı veya görsel ayrıntılar vb.
kısımlarda ufak değişiklikler yapıldı.

## 8. Değerlendirme

### 8.1 Müşteri Değerlendirmesi

Test aşamasından sonra son halini alan yazılım kullanıcılara sunuldu. Kullanım sonrası
programın istenilene uygun, işlevlerini hatasız yerine getiren, kullanımı kolay ve bir dil
kursunun tüm ihtiyaçlarını karşıladığı müşteri tarafından bildirildi.
