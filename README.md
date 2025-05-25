# Data-Cleaning [Veri Temizleme Temel Pratikleri (Pandas ile)]

Bu projede, bir e-ticaret şirketine ait örnek sipariş verileri üzerinden veri temizleme işlemleri adım adım uygulanmaktadır. Amaç, ham veriyi analiz edilebilir hale getirmek için Pandas kütüphanesi ile çeşitli veri ön işleme tekniklerini göstermektir.

## Kullanılan Teknolojiler
- Python 3.x
- Pandas
- NumPy

## Senaryo
Bir e-ticaret şirketinin sipariş kayıtları incelenmek isteniyor. Ancak elimizdeki veri seti:
- Eksik veriler (NaN),
- Yanlış formatlanmış tarihler,
- Sayısal olmayan fiyatlar,
- Yinelenen satırlar,
- Tutarsız yazılmış müşteri adları

içermektedir. Bu projede bu sorunlar çözüme kavuşturulmaktadır.

## Temizleme Adımları
1. **Eksik Değerlerin Düzenlenmesi**  
   `Ürün` sütunundaki boş değerler `"Bilinmiyor"` ile dolduruldu.

2. **Veri Tipi Dönüşümleri ve Format Temizliği**  
   `Fiyat (TL)` sütunundaki `"TL"` ifadeleri kaldırıldı ve değerler float veri tipine dönüştürüldü.

3. **Yinelenen Kayıtların Silinmesi**  
   `SiparişID` ve `MüşteriAdı` alanlarına göre yinelenen satırlar tespit edilip kaldırıldı.

4. **Metin Standardizasyonu**  
   `MüşteriAdı` sütunundaki isimler baş harfi büyük, diğer harfler küçük olacak şekilde düzenlendi.

5. **Tarih Formatlarının Standardizasyonu**  
   `SiparişTarihi` sütunu, `pd.to_datetime()` kullanılarak ortak bir tarih formatına çevrildi.

