<!--
---
name: GPIO
page_url: gpio
description: T3 Gemstone O1 genel amaçlı 3,3 V GPIO pinleri
-->
# GPIO - Genel Amaçlı Giriş/Çıkış

T3-GEM-O1 üzerindeki 40 pin başlık size 3,3 V'luk dijital pinler sunar. Her pin bir girişi okuyabilir, bir çıkışı sürebilir veya seri port, SPI, I2C, ses ve PWM gibi özel bir işleve geçirilebilir.

Bir pini Linux'tan kontrol etmek için `libgpiod`, pinleri listelemek için `gpioinfo`, okuma ve yazma için `gpioget` ve `gpioset` araçlarını kullanabilirsiniz. Raspberry Pi'nin GPIO kütüphaneleri burada çalışmaz. Pini numarasıyla değil sistem adıyla arayın; numaralar yazılım sürümleri arasında değişebilir.

> **3,3 V'ta kalın:** Her pin doğrudan işlemciye bağlıdır, arada koruma sağlayan hiçbir şey yoktur. Herhangi bir pine uygulanan 5 V kartı bozabilir. Pinler güç değil sinyal için tasarlanmıştır: LED, buzzer, röle veya motor çalıştıracaksanız pini tek başına kullanmayın, bir sürücü, transistör ya da röle modülü kullanın.

Bazı işlevler ancak ilgili device tree overlay'i `/boot/uEnv.txt` içinde listelendiğinde etkinleşir, o zamana kadar pin düz bir GPIO olarak kalmaktadır.