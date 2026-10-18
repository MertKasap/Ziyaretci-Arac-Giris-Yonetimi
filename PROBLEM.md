# Problem Kartı — Ziyaretçi Araç Giriş Yönetimi

**Durum:** Görüşmelerle doğrulanması ve ders kapsamında onaylanması gereken taslak.

## 1. Problemi Kim Yaşıyor?

**Hedef kurum/işletme:** [Gerçek kurum ya da işletme adı — izin varsa yazılacak]

**Birincil kullanıcılar:** Güvenlik personeli, ziyaret edilen birimin yetkilileri ve giriş-çıkış kayıtlarından sorumlu yöneticiler.

**İletişim kişisi:** [Görüşme yapılacak gerçek yetkili adı / görevi / iletişim yöntemi — yalnızca paylaşım izni varsa]

## 2. Problemin Tanımı

Ziyaretçi araçlarının giriş-çıkış kayıtlarının farklı kanallarda veya manuel tutulduğu ortamlarda plaka ve ziyaret bilgilerini doğrulama, onay takibi, giriş/çıkış saatlerini eşleştirme ve geçmişi araştırma işlemleri zaman alabilir. Bilgi akışının parçalı olması güvenlik personeli ile ilgili birimler arasında iletişim gecikmelerine yol açabilir.

**Önemli:** Bu paragraf, araştırılacak bir problem hipotezidir; hedef kurumun mevcut durumu olarak doğrulanmış bilgi değildir.

## 3. İş Bugün Nasıl Yapılıyor?

**Doğrulama bekleyen mevcut akış:**
1. Ziyaret öncesinde veya kapıda bilgi güvenlik birimine ulaşır.
2. Ziyaretçinin araç bilgisi manuel olarak kaydedilebilir.
3. Ziyaret edilecek yetkiliden telefon/mesaj yoluyla onay alınabilir.
4. Araç çıkışı ayrı bir kayıt üzerinden takip edilebilir.
5. Geçmiş kayıtlar defter veya tablo içinden aranabilir.

**Gerçek kullanımın anlatımı:** [Görüşmelerden sonra kullanılan araçlar, mevcut adımlar, sorun sıklığı ve örnek olaylar yazılacak.]

## 4. En Az Üç Gerçek Kullanıcı Görüşmesi

> Bu bölüm öğretim elemanının talep ettiği gerçek görüşme kayıtları için hazırlanmıştır. Henüz görüşme yapıldığına dair bilgi bulunmadığı için aşağıdaki alanlar bilinçli olarak boş bırakılmıştır. İzin alınmadan kişisel iletişim bilgilerini herkese açık repoya koymayın.

### Görüşme 1 — Güvenlik personeli

- **Tarih:** [Doldurulacak]
- **Kişi / görev:** [Doldurulacak]
- **İletişim bilgisi veya izinli iletişim kanalı:** [Doldurulacak]
- **Mevcut işleyiş:** [Gerçek yanıt]
- **En sık yaşanan sorun:** [Gerçek yanıt]
- **İhtiyaç / öneri:** [Gerçek yanıt]

### Görüşme 2 — Ziyaret kabul eden birim yetkilisi

- **Tarih:** [Doldurulacak]
- **Kişi / görev:** [Doldurulacak]
- **İletişim bilgisi veya izinli iletişim kanalı:** [Doldurulacak]
- **Mevcut işleyiş:** [Gerçek yanıt]
- **En sık yaşanan sorun:** [Gerçek yanıt]
- **İhtiyaç / öneri:** [Gerçek yanıt]

### Görüşme 3 — Yönetici / idari personel

- **Tarih:** [Doldurulacak]
- **Kişi / görev:** [Doldurulacak]
- **İletişim bilgisi veya izinli iletişim kanalı:** [Doldurulacak]
- **Mevcut işleyiş:** [Gerçek yanıt]
- **En sık yaşanan sorun:** [Gerçek yanıt]
- **İhtiyaç / öneri:** [Gerçek yanıt]

## 5. Önerilen Çözüm

Güvenlik personeli ve yetkililerin oturum açarak kullanacağı, ziyaret talebi, onay, araç giriş-çıkış kaydı ve geçmiş sorgulama işlemlerini tek bir web uygulamasında toplayan sistem.

### En Önemli Üç Özellik

1. **Ziyaret ve araç kaydı:** Plaka, ziyaret nedeni, ilgili birim, tarih ve saat bilgilerinin yönetilmesi.
2. **Onay ve giriş/çıkış takibi:** Yetkili onayı ile güvenlik giriş-çıkış işlemlerinin aynı kayıtta izlenmesi.
3. **Yetkili geçmiş arama ve raporlama:** Kullanıcının yetkisine göre kayıt filtreleme ve özet bilgilere erişim.

Bu öncelikler gerçek görüşme bulgularına göre değiştirilebilir.

## 6. Seçilen Teknik Özellikler

**Yönergedeki en az üç özellik koşulunu karşılamak üzere hedeflenenler:**

- **Rol tabanlı yetkilendirme:** Güvenlik, birim yetkilisi, yönetici
- **Gerçek zamanlı güncelleme:** Onay/durum değişikliği için SSE veya WebSocket
- **Raporlama / grafik:** Ziyaret kayıtlarından tarih ve durum bazlı özetler

**Temel teknoloji planı:** React (Vite), Node.js/Express, MySQL; kullanıcı kaydı/girişi ve canlı yayına alma.

## 7. Özgünlük ve Kapsam

Genel amaçlı bir site veya liste kopyası yerine, ziyaretçi aracının kuruma kabulünden çıkışına kadar birden çok görevlinin rol aldığı somut iş akışına odaklanılır. Gerçek kurumda süreç bu şekilde işlemiyorsa iş akışı görüşmelerden sonra uyarlanacaktır.

## 8. Onay ve Görüşme Kontrol Listesi

- [ ] Problemi gerçekten yaşayan bir kurum / kişi belirlendi
- [ ] En az üç farklı gerçek kullanıcı ile görüşüldü
- [ ] Görüşmelerin özetleri ve izinli iletişim bilgileri eklendi
- [ ] Mevcut manuel iş akışı doğrulandı
- [ ] En önemli üç özellik kullanıcı ihtiyacına göre revize edildi
- [ ] Konu sunumu yapıldı
- [ ] Öğretim elemanından onay alındı

**Not:** Konu sunumundan önce bu dosyanın gerçek bulgularla güncellenmesi gerekmektedir.
