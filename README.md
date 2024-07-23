# Hisse Senedi Analiz Panosu
Bu proje, çeşitli hisse senetlerinin gerçek zamanlı fiyatlarını ve teknik göstergelerini (SMA ve RSI) görselleştiren bir Python uygulamasıdır. Uygulama, Tkinter tabanlı bir grafiksel kullanıcı arayüzü (GUI) kullanır ve hisse senedi verilerini her 5 saniyede bir günceller.

## Özellikler
Gerçek zamanlı hisse senedi fiyatları.
Simple Moving Average (SMA) ve Relative Strength Index (RSI) teknik göstergeleri.
Her 5 saniyede bir otomatik veri güncelleme.
Kullanıcı dostu Tkinter tabanlı grafiksel arayüz.
## Gereksinimler
Bu projeyi çalıştırmak için aşağıdaki Python kütüphanelerine ihtiyacınız olacak:

- tkinter
- yfinance
- matplotlib
- ta
- datetime
- threading

  ## Teknik Detaylar
### Ana Sınıf: StockApp
#### init Metodu
- Tkinter penceresi oluşturur ve başlığı ayarlar.
- Hisse senedi fiyatını ve son güncelleme zamanını göstermek için bir çerçeve oluşturur.
- 3x3 boyutunda grafikler oluşturur ve her biri bir hisse senedi için kullanılır.
- Hisse senetlerini güncelleme işlevini başlatır.
#### update_stock_data Metodu
- Her bir hisse senedi için verileri Yahoo Finance'ten çeker.
- Verileri çektiği her hisse senedi için plot_stock_data metodunu çağırır.
- Son güncelleme zamanını etikette gösterir ve güncellemeyi 5 saniye sonra tekrar çalıştırmak için zamanlayıcı başlatır.
#### plot_stock_data Metodu
- Hisse senedi verilerini çizer.
- Kapanış fiyatı, SMA ve RSI göstergelerini grafiklere ekler.
- İkinci bir y ekseni oluşturur ve RSI değerlerini bu eksende çizer.
- Eksen etiketlerini ve başlıkları ayarlar.
- Grafiği günceller.
#### on_close Metodu
- Zamanlayıcıyı iptal eder ve uygulama penceresini kapatır.
## Ana Program
Tkinter ana penceresini oluşturur ve StockApp sınıfını başlatır.
Pencere kapatma olayını on_close metoduna bağlar.
Tkinter ana döngüsünü başlatır.
## Katkıda Bulunma
Katkılarınızı memnuniyetle karşılıyoruz! Lütfen bir pull request göndermeden önce bir issue açarak ne üzerinde çalışmak istediğinizi belirtin.

## Lisans
Bu proje MIT Lisansı ile lisanslanmıştır. Daha fazla bilgi için LICENSE dosyasına bakabilirsiniz.
