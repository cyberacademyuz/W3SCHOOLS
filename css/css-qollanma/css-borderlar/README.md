# CSS Borderlar

CSSning `border` xususiyati element chegarasining kstillarini, uzunligini va rangini o'zgartirishga imkon beradi.

<figure><img src="../../../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

### CSS Border stili <a href="#css-border-style" id="css-border-style"></a>

`border-style` xususiyati chegara dizayni qanday ko'rinishda bo'lishini belgilaydi.

Quyidagi qiymatlardan foydalanish mumkin:

* `dotted` - nuqtali chegara yaratadi
* `dashed` - chiziqchali chegara yaratadi
* `solid` - tekish chegara yaratadi
* `double` - ikkitali chegara yaratadi
* `groove` - 3D groove chegara yaratadi. Effekt border-color qiymatiga bog'liq.
* `ridge` - 3D ridge chegara yaratadi. Effekt border-color qiymatiga bog'liq.
* `inset` - 3D inset chegara yaratadi. Effekt border-color qiymatiga bog'liq.
* `outset` - 3D outset chegara yaratadi. Effekt border-color qiymatiga bog'liq.
* `none` - Chegara yo'qligini bildiradi.
* `hidden` - ko'rinmas chegara yaratadi.

`border-style` xususiyati birdan to'rttagacha qiymat qabul qilishi mumkun (tepa chegara uchun, o'ng chegara uchun, pastki chegara uchun va chap chegara uchun)

{% code title="Chegaraning stillarini har xil ko'rinishlari:" %}
```
p.dotted {border-style: dotted;}
p.dashed {border-style: dashed;}
p.solid {border-style: solid;}
p.double {border-style: double;}
p.groove {border-style: groove;}
p.ridge {border-style: ridge;}
p.inset {border-style: inset;}
p.outset {border-style: outset;}
p.none {border-style: none;}
p.hidden {border-style: hidden;}
p.mix {border-style: dotted dashed solid double;}
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (296).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma**: `border-style` xususiyatidan foydalanmaguncha chegara xususiyatlarining hech biri hech qanday tasirga ega bo'lmaydi.
{% endhint %}
