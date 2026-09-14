<!--
---
name: 5 V Güç
page_url: 5v_power
description: T3 Gemstone O1 5 V başlık besleme pinleri
url: https://docs.t3gemstone.org/tr/boards/o1/peripherals/introduction
-->
# 5 V Güç

Physical Pin 2 ve Physical Pin 4, 3,3 V'tan fazlasına ihtiyaç duyan eklentiler için 5 V verir. Sinyal pinlerinin hala yalnızca 3,3 V olduğunu unutmayın: bir kartı 5 V ile beslemek, bir GPIO pinine 5 V geri gönderebileceğiniz anlamına gelmez.

Bu 5 V, taktığınız kaynaktan doğrudan gelmez; karttaki bir regülatörden üretilir ve kart bu hattı kapatabilir.

> **Buradan güç vermeyin:** Bu pinler çıkıştır. Buraya 5 V uygulamak kartın regülatörüne karşı çalışır ve kartın kendi güç girişindeki korumayı atlar; bir şeyleri bozmanın kolay yolu budur.
