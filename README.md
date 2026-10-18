# Ziyaretçi Araç Giriş Yönetim Sistemi

**Web Programlama Dönem Projesi | 2026–2027 Güz Dönemi**

> **Proje durumu:** Analiz ve planlama aşaması. Bu depo henüz çalışan bir web uygulaması içermez. Kullanıcı görüşmeleri ve proje konusu onayı tamamlandığında kapsam güncellenecektir.

## 1. Projenin Amacı

Ziyaretçi araçlarının kurum ve işletme girişlerinde kaydedilmesi, onaylanması, giriş-çıkış zamanlarının izlenmesi ve geçmiş kayıtlara erişilmesi için web tabanlı bir yönetim sistemi geliştirmek amaçlanmaktadır.

Bazı işletmelerde bu tür işlemler defter, Excel, telefon veya mesajlaşma araçlarıyla yürütülebilir. Projemiz, farklı araçlarda tutulan kayıtların tek bir yerde yönetilebilmesi ve ilgili personelin aynı güncel bilgiye erişebilmesi ihtiyacına odaklanır. Bu sorunların hedef kurumda gerçekten yaşandığı, görüşmelerle doğrulanmalıdır.

## 2. Hedef Kullanıcılar

| Rol | Beklenen işlem |
| --- | --- |
| Güvenlik görevlisi | Araç ve ziyaretçi kaydı oluşturma, giriş/çıkış işlemi yapma, durum görüntüleme |
| Ziyaret edilen birimdeki yetkili | Ziyaret talebini inceleme, onaylama veya reddetme |
| Sistem yöneticisi | Kullanıcı ve yetki yönetimi, kayıt geçmişi ve raporları inceleme |

Roller ve yetkiler gerçek kullanıcı görüşmelerine göre yeniden düzenlenebilir.

## 3. Planlanan İş Akışı

1. Yetkili bir kullanıcı ziyaret talebi oluşturur veya güvenlik görevlisi gelen aracı kaydeder.
2. Plaka, ziyaretçi adı, ziyaret amacı, ziyaret edilecek kişi/birim ve zaman bilgisi sisteme işlenir.
3. Gerekli ise ilgili yetkili talebi onaylar veya reddeder.
4. Güvenlik görevlisi araç geldiğinde kaydı kontrol ederek giriş zamanını kaydeder.
5. Araç ayrılırken çıkış kaydı tamamlanır.
6. Yetkili kullanıcılar geçmiş kayıtları arayıp filtreleyebilir, özet raporları görüntüleyebilir.

## 4. Temel Fonksiyonlar (Hedef)

- Kullanıcı kaydı ve oturum açma
- Rol tabanlı erişim kontrolü
- Ziyaretçi ve araç bilgisi kaydı
- Ziyaret onay/red ve durum takibi
- Araç giriş/çıkış zamanlarının kaydedilmesi
- Tarih, plaka ve durum bazında kayıt arama/filtreleme
- Yetkili kullanıcı için özet raporlar

## 5. Dersin Teknik Gereksinimlerine Uyum Planı

| Gereksinim | Plan |
| --- | --- |
| Frontend | React + Vite |
| Backend | Node.js + Express |
| Veritabanı | MySQL |
| Kimlik doğrulama | Kullanıcı kaydı ve giriş işlemleri |
| Canlı yayın | 6. hafta itibarıyla erişilebilir bir dağıtım hedefi |

Ek teknik özelliklerden **en az üçünün** uygulanması hedeflenmektedir:

1. **Rol tabanlı yetkilendirme:** Güvenlik / yetkili / yönetici için farklı işlemler.
2. **Gerçek zamanlı güncelleme:** Onay ve giriş durumunu SSE veya WebSocket ile sayfa yenilenmeden göstermek.
3. **Raporlama / grafik:** Veritabanındaki ziyaret kayıtlarından günlük ve dönemsel özetler üretmek.

Bunlar planlanan özelliklerdir; henüz geliştirilmiş veya test edilmiş değildir.

## 6. Özgün Yaklaşım

Proje yalnızca ziyaretçi listesi tutmak yerine **talep → onay → giriş → çıkış → raporlama** sürecini birlikte ele almayı hedefler. Amaç, gerçek bir kurumun iş akışına uyarlanabilecek, yetkilere ayrılmış operasyonel bir uygulama geliştirmektir. Konunun özgünlüğü ve kapsamı görüşmeler ve ders onayıyla netleştirilecektir.

## 7. Depo Dosyaları

- **PROBLEM.md:** Problem kartı, görüşme şablonları, mevcut iş akışı ve çözüm önerisi.
- **AI_LOG.md:** Yapay zekâ desteğiyle hazırlanan kısımlar ve gözden geçirilmesi gereken noktalar.
- **.env.example:** Gerçek şifre içermeyen örnek ortam değişkenleri.
- **.gitignore:** Gizli veya gereksiz yerel dosyaların Git'e eklenmesini engelleyen kurallar.

## 8. İlk Hafta / Sonraki Adımlar

- [x] GitHub deposunun oluşturulması
- [x] İlk problem ve kapsam taslağının yazılması
- [x] Temel repo dokümantasyonunun hazırlanması
- [ ] Gerçek problemi yaşayan en az üç kişiyle görüşme yapılması
- [ ] PROBLEM.md içindeki görüşme bilgilerinin doldurulması
- [ ] Konunun 2. hafta sunumunda onaylanması
- [ ] React uygulama iskeletinin oluşturulması
- [ ] Backend ve veritabanı tasarımının başlatılması

**Not:** Yönergede depo açılışı için belirtilen tarih 6 Ekim 2026'dır. GitHub'a yapılan işlemlerin gerçek tarihleri esas alınır; geç yapılmış işlem geçmiş tarihli gibi gösterilmez.

## 9. Gizlilik ve Veri Güvenliği

Gerçek kişilere ait telefon, plaka veya benzeri kişisel veriler izinsiz olarak herkese açık depoya eklenmeyecektir. Parolalar, API anahtarları ve veritabanı bağlantı bilgileri .env içinde tutulur; repoda sadece .env.example bulunur. Uygulama geliştirilirken yetkilendirme, gerekli minimum veri toplama ve erişim kontrolü dikkate alınacaktır.
