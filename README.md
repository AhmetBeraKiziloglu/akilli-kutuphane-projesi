# akilli-kutuphane-projesi
BÖZ405u02a02_Ödev
# Akıllı Kütüphane: Fiziksel Kaosu Dijital Düzenle Çözmek

Bu proje, Mayıs 2024 tarihinde Ege Güney tarafından BÖZ405 Proje Geliştirme dersi kapsamında Tasarım Odaklı Düşünme (Design Thinking) metodolojisi kullanılarak geliştirilmiş bir vaka çalışmasıdır.

## Problem Tanımı
Kütüphanelerde özellikle vize ve final gibi sınav dönemlerinde yaşanan temel sorun, sadece fiziksel kapasitenin yetersiz olması değildir. Asıl problem, masalara sadece çanta bırakılarak saatlerce geri dönülmeyen "Hayalet Rezervasyonlar" ve eşya ile yapılan haksız işgal durumudur. Bu durumun kullanıcı üzerindeki etkileri şu şekildedir:
* **Ne Görüyor:** Çantayla rezerve edilmiş ancak aslında boş olan koltuklar ve katlar arasında yer arayan yorgun kalabalıklar görüyor.
* **Ne Duyuyor:** Etrafından "Kütüphane tıklım tıklım, hiç gelme" veya "Yarım saattir yer arıyorum, bulamayıp eve döndüm" gibi cümleler duyuyor.
* **Ne Düşünüyor ve Hissediyor:** Sınav stresi yaşarken bir de yer aramak zorunda kaldığı için sinirleniyor, zamanının boşa gittiğini ve motivasyonunun düştüğünü hissediyor.
* **Ne Yapıyor:** Tüm katları tek tek geziyor ve kütüphane içindeki arkadaşlarına "Bana da yer tutar mısın?" şeklinde mesajlar atarak mevcut kaosu artırıyor.
* **Acı (Pain):** Yer aramak için enerji ve zaman harcıyor, odaklanma sorunları yaşıyor.

## Çözüm: QR Kodlu Rezervasyon Sistemi
Pahalı koltuk sensörleri veya akıllı kameralar yerine, çok düşük maliyetli ve adil bir zaman yönetimi kuralı sunan QR Kodlu Rezervasyon Sistemi geliştirilmiştir[cite: 16]. Bu sistem, masaların eşyalar tarafından limitsizce işgal edilmesini engellemeyi amaçlar.

### Sistemin Çalışma Adımları
1. **Canlı Harita:** Öğrenci mobil uygulamayı açar ve kuşbakışı kütüphane planı üzerinden açık yeşil (boş) ve kırmızı/mercan (dolu veya rezerve) masaları anlık olarak görüntüler.
2. **Masaya Yönelme:** Uygulama üzerinden belirlediği boş masaya vakit kaybetmeden doğrudan gider.
3. **QR Okutma:** Öğrenci, masada yer alan fiziki QR kodu kendi mobil cihazına okutur.
4. **Süre Başlangıcı:** QR kod okutulduğunda masa maksimum 3 saatliğine rezerve edilir ve ekranda bir geri sayım sayacı (örneğin "02:59:45") başlar.

## Kullanıcı Testleri ve İterasyon Süreci
Prototip, kütüphanede ders çalışan öğrencilere senaryo bazlı olarak test ettirilmiş ve alınan geri bildirimlere göre iki ana iterasyon gerçekleştirilmiştir:

* **İterasyon 1 (Geçici Rezerve Mantığı):** Test sırasında öğrencilerin "kütüphaneye varana kadar o 10 dakikalık sürede başkası gelip masayı kapabilir" endişesi üzerine geliştirilmiştir. Arayüze "15 Dk Yoldayım" butonu eklenerek öğrencinin uzaktayken masayı sarı renge (beklemede) çevirmesi sağlanmıştır. Öğrenci 15 dakika içinde QR kodu okutmazsa masa tekrar yeşile dönmektedir.
* **İterasyon 2 (Dinamik Süre Uzatma):** Öğrencilerin "Sınavım var ve daha çok çalışmam gerekiyor, sıra bekleyen yoksa neden kalkayım?" şeklindeki esneklik talebi doğrultusunda eklenmiştir. Kütüphane kuyruğunda bekleyen başka bir öğrenci yoksa, süre bitimine 15 dakika kala ekranda "+1 Saat Uzat" butonu aktif hale gelmektedir.

## Bireysel Öğrenim Yansıtması
Proje sonucunda, "kütüphanede yer yok" sorununun temelinde yatan asıl nedenin kapasite eksikliği değil, belirsizlik ve adaletsiz yer tutma alışkanlıkları olduğu Empati Haritası sayesinde tespit edilmiştir[cite: 21]. Masa başında tasarlanan sistemin gerçek kullanıcı testlerinde yürüme süresi hesaba katılmadığı için eksik kalması, tasarım süreçlerinde iterasyonun ve sahada gerçek ihtiyaçlara göre şekillenmenin önemini kanıtlamıştır.
