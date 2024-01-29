# Grid Element

<figure><img src="../../.gitbook/assets/image (435).png" alt=""><figcaption></figcaption></figure>

### Child elementlar

Grid _konteyneri_ grid _elementlarini_ o'z ichiga oladi.

Standart tarzda, konteynerning har bir qatorida har bir ustun uchun bitta grid elementi bo'ladi, biroq grid elementlarini bir nechta ustun va/yoki qatorlarlarni qamrab oladigan tarzda o'zgartirishingiz mumkin.

### grid-column xususiyati:

`grid-column` xususiyati elementni qaysi ustun(lar)ga joylashtirishni belgilaydi.

Element qayerdan boshlanishini va qayerda tugashini belgilaysiz.

<figure><img src="../../.gitbook/assets/image (366).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma**: `grid-column` xususiyati `grid-column-start` va `grid-column-end` xususiyatlari uchun qisqartma xususiyat hisoblanadi.
{% endhint %}

Elementni joylashtirish uchun _qator raqamlariga_ murojaat qilishingiz mumkin yoki element qancha ustunni qamrab olishini belgilash uchun "span" kalit so'zidan foydalaning.

{% code title="“item1” 1-ustundan boshlanib, 5-ustundan oldin tugaydi:" %}
```
.item1 {
  grid-column: 1 / 5;
}
```
{% endcode %}

{% code title=""Item1" 1-ustundan boshlanib, 3 ta ustunni qamrab oladi:" %}
```
.item1 {
  grid-column: 1 / span 3;
}
```
{% endcode %}

{% code title=""Item2" 2-ustundan boshlanib, 3 ta ustunni qamrab oladi:" %}
```
.item2 {
  grid-column: 2 / span 3;
}
```
{% endcode %}

### grid-row xususiyati:

`grid-row` xususiyati elementni qaysi qatorga joylashtirishni belgilaydi.

Element qayerdan boshlanishini va qayerda tugashini belgilaysiz.

<figure><img src="../../.gitbook/assets/image (410).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Eslatma**: `grid-row` xususiyati `grid-row-start` va `grid-row-end` xususiyatlari uchun qisqartma xususiyat hisoblanadi.
{% endhint %}

Elementni joylashtirish uchun _qator raqamlariga_ murojaat qilishingiz yoki element qancha qatorni qamrab olishini belgilash uchun "span" kalit so'zidan foydalanishingiz mumkin:

{% code title=""Item1" ni 1-qatorda boshlang va 4-qatorda tugating:" %}
```
.item1 {
  grid-row: 1 / 4;
}
```
{% endcode %}

{% code title=""Item1" ni 1-qatordan boshlangg va 2 qatorni qamrab oling:" %}
```
.item1 {
  grid-row: 1 / span 2;
}
```
{% endcode %}

### grid-area xususiyati

`grid-area` xususiyati `grid-row-start`, `grid-column-start`, `grid-row-end` va `grid-column-end` xususiyatlari uchun qisqartma xususiyat sifatida ishlatilishi mumkin.

<figure><img src="../../.gitbook/assets/image (384).png" alt=""><figcaption></figcaption></figure>

{% code title=""element8" ni 1-qator va 2-ustun qatorida boshlang va 5-qator hamda 6-ustun qatorida tugating:" %}
```
.item8 {
  grid-area: 1 / 2 / 5 / 6;
}
```
{% endcode %}

{% code title=""element8" ni 2-qator va 1-ustun qatoridan boshlang va 2-qator hamda 3-ustunni egallab olsin:" %}
```
.item8 {
  grid-area: 2 / 1 / span 2 / span 3;
}
```
{% endcode %}

### Grid elementlarini nomlash

`grid-area` xususiyatdan grid elementlariga nom berish uchun ham foydalanish mumkin.

<figure><img src="../../.gitbook/assets/image (401).png" alt=""><figcaption></figcaption></figure>

Nom berilgan grid obyektlari grid konteynerining `grid-template-areas` xususiyati bilan bog'liq bo'lishi mumkin.

{% code title="Item1 "myArea" nomini oladi va besh ustunli grid layoutidagi barcha besh ustunni qamrab oladi:" %}
```
.item1 {
  grid-area: myArea;
}
.grid-container {
  grid-template-areas: 'myArea myArea myArea myArea myArea';
}
```
{% endcode %}

Har bir qator apostrof ('') bilan belgilanadi.

Har bir qatordagi ustunlar bo'sh joy bilan ajratilgan apostroflar ichida yoziladi.

{% hint style="warning" %}
**Eslatma**: Nuqta belgisi nomsiz grid elementini ifodalaydi.
{% endhint %}

{% code title=" "myArea" besh ustunli grid layoutida ikkita ustunni qamrab olsin." %}
```
.item1 {
  grid-area: myArea;
}
.grid-container {
  grid-template-areas: 'myArea myArea . . .';
}
```
{% endcode %}

Ikki qatorni belgilash uchun boshqa apostroflar to'plami ichida ikkinchi qatorning ustunini belgilang:

{% code title=""Item1" ni ikkita ustun va ikkita qatorga aylantiring:" %}
```
.grid-container {
  grid-template-areas: 'myArea myArea . . .' 'myArea myArea . . .';
}
```
{% endcode %}

{% code title="Barcha elementlarga nom bering va foydalanishga tayyor veb-sahifa shablonini yarating:" %}
```
.item1 { grid-area: header; }
.item2 { grid-area: menu; }
.item3 { grid-area: main; }
.item4 { grid-area: right; }
.item5 { grid-area: footer; }

.grid-container {
  grid-template-areas:
    'header header header header header header'
    'menu main main main right right'
    'menu footer footer footer footer footer';
}
```
{% endcode %}

### Elementlarning tartibi

Grid Layout elementlarni istalgan joyga joylashtirish imkonini beradi.

{% hint style="warning" %}
HTML kodidagi birinchi element griddagi birinchi element sifatida ko'rsatilishi shart emas.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

```
.item1 { grid-area: 1 / 3 / 2 / 4; }
.item2 { grid-area: 2 / 3 / 3 / 4; }
.item3 { grid-area: 1 / 1 / 2 / 2; }
.item4 { grid-area: 1 / 2 / 2 / 3; }
.item5 { grid-area: 2 / 1 / 3 / 2; }
.item6 { grid-area: 2 / 2 / 3 / 3; }
```

Media querylardan foydalanib, ma'lum bir ekran o'lchamlari uchun joylashuv tartibini qaytadan tartibga solishingiz mumkin:

```
@media only screen and (max-width: 500px) {
  .item1 { grid-area: 1 / span 3 / 2 / 4; }
  .item2 { grid-area: 3 / 3 / 4 / 4; }
  .item3 { grid-area: 2 / 1 / 3 / 2; }
  .item4 { grid-area: 2 / 2 / span 2 / 3; }
  .item5 { grid-area: 3 / 1 / 4 / 2; }
  .item6 { grid-area: 2 / 3 / 3 / 4; }
}
```
