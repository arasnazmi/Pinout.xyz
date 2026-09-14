<!--
---
page_url: spi
description: T3 Gemstone O1 SPI-MCU0 başlık pinleri
url: https://docs.t3gemstone.org/tr/boards/o1/peripherals/introduction
-->
# SPI

SPI beş pin kullanır: Physical Pin 19 cihazınıza veri gönderir, Physical Pin 21 cihazdan veri alır, Physical Pin 23 ise saat hattıdır. Physical Pin 24 ve Physical Pin 26, hangi cihazla konuşulduğunu seçen iki chip-select hattıdır. Bu bağlantılar Linux'ta `/dev/spidev0.0` ve `/dev/spidev0.2` olarak görünür.

Her birine kendi chip-select hattını verdiğiniz ve chip-select'i etkin olmayan cihaz sessiz kaldığı sürece aynı veri ve saat pinlerine birden fazla cihaz bağlayabilirsiniz.

## Kartın kendi sensörleri de bu hatta

Kartın içindeki basınç sensörü ile hareket sensörü bu veri ve saat pinlerini sizinle paylaşır. Kendi chip-select hatları vardır ve bunlar başlığa çıkarılmamıştır; dolayısıyla cihazınız onlarla karışmaz.

> **Dikkat edilecekler:** 3,3 V sinyal kullanın. Cihazınızın, chip-select'i etkin değilken veri giriş pinini sürmeyi bıraktığından emin olun; konuşmaya devam ederse kartın kendi sensör okumaları yanlış çıkar, tersi de geçerlidir.

> **26 numaralı pinin ikinci bir görevi var:** Bu pin, ek bir seri portun alma hattı olarak da kullanılabilir. Onu etkinleştirirseniz tek chip-select hattınız Physical Pin 24 olur.
