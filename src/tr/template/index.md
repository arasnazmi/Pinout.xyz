# T3 Gemstone O1 Pinout

T3 Gemstone Pinout, T3-GEM-O1 geliştirme kartının fiziksel pinlerini, uyumluluk GPIO numaralarını ve varsayılan arayüzlerini belgeler. Başlık, bilinen Raspberry Pi 40 pin fiziksel dizilimini kullanır; ancak işlemci, pin çoklama seçenekleri ve yazılım altyapısı Texas Instruments AM67A platformuna özgüdür.

## Başlık arayüzleri

Başlık size I2C, SPI, akış kontrollü bir seri port, dört dijital ses sinyali ve 3,3 V GPIO sunar; buna ek olarak Physical Pin 29, Physical Pin 31, Physical Pin 32 ve Physical Pin 33 üzerinde donanımsal PWM vardır. Bunların bir kısmı ancak ilgili overlay `/boot/uEnv.txt` içinde etkinleştirildiğinde çalışır; bir şey bağlamadan önce açılış yapılandırmasını kontrol edin.

## Uyumlu HAT ve eklentiler

Fiziksel olarak takılabilmek, elektriksel veya yazılımsal uyumluluk anlamına gelmez. [Uyumlu kartlar kataloğunda](/tr/boards) yalnızca T3-GEM-O1 pin dizilimi, gerilim gereksinimleri, pin yönleri, device-tree yapılandırması ve Linux sürücüleri incelenen kartlar yer alır.

Bir eklenti, katalogda **Doğrulandı** veya **Koşullu uyumlu** durumu gösterilmedikçe uyumlu kabul edilmez.

Uyumluluk durumları:

* **Doğrulandı:** donanım ve yazılım çalışması teyit edilmiştir.
* **Koşullu uyumlu:** belgelenen sınırlamalar veya yapılandırmayla çalışabilir.
* **Uyumsuz:** kart kullanılmamalıdır veya gerekli bir özellik mevcut değildir.

## Yetkili kaynaklar

* [T3 Gemstone O1 dokümantasyonu](https://docs.t3gemstone.org/tr/boards/o1/introduction)
* [GPIO kılavuzu](https://docs.t3gemstone.org/tr/boards/o1/peripherals/gpio)
* [PWM kılavuzu](https://docs.t3gemstone.org/tr/boards/o1/peripherals/pwm)
* [Açık donanım tasarım dosyaları](https://github.com/t3gemstone/hardware)
