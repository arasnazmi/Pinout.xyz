<!--
---
name: PCM
page_url: pcm
description: T3 Gemstone O1 PCM/I2S uyumlu başlık sinyalleri
url: https://docs.t3gemstone.org/tr/boards/o1/peripherals/introduction
pin:
  '38':
    name: DATA0
  '40':
    name: DATA1
-->
# PCM - Darbe Kod Modülasyonu

Dört pin dijital ses taşır ve bunlar Raspberry Pi'nin I2S için kullandığı konumlarla aynıdır; yani bir ses HAT'i fiziksel olarak yerine oturur:

| Pin | Ne taşır |
| --: | :-- |
| 12 | bit saati |
| 35 | çerçeve eşzamanlaması |
| 38 | ses verisi, Pi'de giriş olan hat |
| 40 | ses verisi, Pi'de çıkış olan hat |

Bilmeye değer bir fark var. Raspberry Pi'de Physical Pin 38 her zaman giriş, Physical Pin 40 her zaman çıkıştır. Burada ise her iki veri pini yazılımda giriş ya da çıkış olarak ayarlanabilir; hangisinin ne olduğunu kablolama değil, ses yapılandırması belirler.
