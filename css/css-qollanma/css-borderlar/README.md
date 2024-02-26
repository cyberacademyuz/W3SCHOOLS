# CSS Borderlar

CSSning <mark style="color:red;">`border`</mark> xususiyati element chegarasining kstillarini, uzunligini va rangini o'zgartirishga imkon beradi.

<figure><img src="../../../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

## CSS Border stili <a href="#css-border-style" id="css-border-style"></a>

<mark style="color:red;">`border-style`</mark> xususiyati chegara dizayni qanday ko'rinishda bo'lishini belgilaydi.

Quyidagi qiymatlardan foydalanish mumkin:

* <mark style="color:red;">`dotted`</mark> - nuqtali chegara yaratadi
* <mark style="color:red;">`dashed`</mark> - chiziqchali chegara yaratadi
* <mark style="color:red;">`solid`</mark> - tekish chegara yaratadi
* <mark style="color:red;">`double`</mark> - ikkitali chegara yaratadi
* <mark style="color:red;">`groove`</mark> - 3D groove chegara yaratadi. Effekt border-color qiymatiga bog'liq.
* <mark style="color:red;">`ridge`</mark> - 3D ridge chegara yaratadi. Effekt border-color qiymatiga bog'liq.
* <mark style="color:red;">`inset`</mark> - 3D inset chegara yaratadi. Effekt border-color qiymatiga bog'liq.
* <mark style="color:red;">`outset`</mark> - 3D outset chegara yaratadi. Effekt border-color qiymatiga bog'liq.
* <mark style="color:red;">`none`</mark> - Chegara yo'qligini bildiradi.
* <mark style="color:red;">`hidden`</mark> - ko'rinmas chegara yaratadi.

<mark style="color:red;">`border-style`</mark> xususiyati birdan to'rttagacha qiymat qabul qilishi mumkun (tepa chegara uchun, o'ng chegara uchun, pastki chegara uchun va chap chegara uchun)

{% tabs %}
{% tab title="CSS" %}
Chegaraning stillarini har xil ko'rinishlari:

```css
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

Natija:

<figure><img src="../../../.gitbook/assets/image (296).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_border-style" %}
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
**Eslatma**: <mark style="color:red;">`border-style`</mark> xususiyatidan foydalanmaguncha chegara xususiyatlarining hech biri hech qanday tasirga ega bo'lmaydi.
{% endhint %}
