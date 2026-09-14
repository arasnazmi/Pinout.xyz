<!--
---
name: PWM
page_url: pwm
description: T3 Gemstone O1 donanımsal PWM destekli başlık pinleri
-->
# PWM - Darbe Genişlik Modülasyonu

Dört pin donanım üzerinden PWM üretebilir; yani zamanlama, işlemci uğraşmadan kararlı kalır. Bu pinler iki çift halinde gelir:

| Pinler | Kanallar |
| :-- | :-- |
| 29 ve 32 | PWM-0A ve PWM-0B |
| 31 ve 33 | PWM-1A ve PWM-1B |

Bir çiftteki iki pin aynı frekansı paylaşır, ancak her birinin görev döngüsü ayrı ayarlanabilir. Yani iki frekans üzerinde dört bağımsız görev döngüsü elde edersiniz.

Bunları `/sys/class/pwm` üzerinden kontrol edebilirsiniz.

> **PWM hiçbir şeyi beslemez:** Bu pinler yalnızca 3,3 V'luk bir sinyal verir, fazlası değil. Servo, motor veya LED şeridi kendi güç kaynağına, toprağının başlıktaki bir toprak pinine bağlanmasına ve araya bir sürücü kartı ya da transistöre ihtiyaç duyar.
