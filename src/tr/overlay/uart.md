<!--
---
page_url: uart
description: T3 Gemstone O1 UART-MAIN1 başlık pinleri ve isteğe bağlı UART yönlendirmeleri
pin:
  '11':
    name: UART-MAIN1 RTS
  '36':
    name: UART-MAIN1 CTS
-->
# UART

Physical Pin 8 gönderir, Physical Pin 10 alır. Linux'ta bu seri port `/dev/ttyS3` olarak görünür. Cihazınızın alma pinini Physical Pin 8'e, gönderme pinini Physical Pin 10'a bağlayın ve toprağı ortaklayın.

Physical Pin 11 ile Physical Pin 36, ihtiyaç duyan cihazlar için akış kontrolü (RTS ve CTS) ekler. Basit seri cihazların çoğu buna ihtiyaç duymaz; bu iki pini boş bırakabilirsiniz.

> **Yalnızca 3,3 V:** Bu portu asla bir RS-232 portuna veya 5 V'luk bir seri dönüştürücüye bağlamayın; ikisi de kartı bozar. 3,3 V'luk bir USB-seri dönüştürücü ya da uygun bir RS-232 seviye dönüştürücü kullanın.

Kartın üzerindeki üç pinli konnektör, açılış konsolu için kullanılan ayrı bir seri porttur. Bu pinlerle aynı şey değildir.