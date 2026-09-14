<!--
---
page_url: i2c
description: T3 Gemstone O1 I2C-MCU0 ve paylaşımlı I2C-WKUP0 başlık pinleri
-->
# I2C

Physical Pin 3 (veri) ve Physical Pin 5 (saat), kendi cihazlarınız için ayrılmış I2C veri yoludur. Kart üzerinde bu hattı kullanan başka bir şey yok, yani hat tamamen size ait. Bir I2C veri yolunun ihtiyaç duyduğu pull-up dirençleri kartta hazır takılıdır; ayrıca direnç eklemeniz gerekmez.

Farklı yazılım imajları veri yolunu farklı numaralandırır; bu yüzden hat `/dev/i2c-1` veya `/dev/i2c-2` olarak görünebilir. Hangi veri yollarının mevcut olduğunu görmek için `ls /dev/i2c-*`, bağlı cihazları görmek için de o hat üzerinde `i2cdetect` komutunu çalıştırın.

> **Bağlamadan önce:** Yalnızca 3,3 V cihaz kullanın. Hattaki her cihaza farklı bir adres verin, aksi halde birbirleriyle çakışırlar. Pull-up direnci ekleyecekseniz kartta zaten mevcut olduğunu unutmayın.

## 27 ve 28 numaralı pinler paylaşımlı bir hat

Bu iki pin, çalışan ikinci bir I2C veri yoludur; pull-up dirençleri de ilki gibi kartta takılıdır. Kartın gücünü yöneten çip, gerçek zaman saati ve EEPROM bu hatta bağlıdır.

Yani bu pinleri kullanabilirsiniz, sadece paylaşmanız gerekir. Bir cihaz seçmeden önce bu hat üzerinde `i2cdetect` çalıştırıp hangi adreslerin dolu olduğunu görün ve çakışmayan bir adres seçin.

> **Burada 3 ve 5 numaralı pinlerden daha dikkatli olun:** Güç yönetim çipi bu hatta olduğu için bir kısa devre, yanlış gerilim ya da hattı kilitleyen bir cihaz yalnızca aksesuarınızı değil kartın tamamını durdurabilir. Hatta halihazırda bulunan cihazların ayarlarını değiştirmeyin. Günlük sensör ve eklentiler için Physical Pin 3 ile Physical Pin 5 daha kolay seçimdir, çünkü o hat tamamen size aittir.
