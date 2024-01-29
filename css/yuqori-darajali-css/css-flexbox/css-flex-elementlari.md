# CSS Flex elementlari

### Child elementlar (elementlar)

Moslashuvchan konteynerning bola elementlari to'g'ridan-to'g'ri avtomatik tarzda moslashuvchan elementlarga aylanadi.

<figure><img src="../../../.gitbook/assets/image (409).png" alt=""><figcaption></figcaption></figure>

Yuqoridagi element kulrangli moslashuvchan konteyner ichidagi to'rtta ko'k rangli moslashuvchan elementni o'z ichiga oladi.

```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>
```

Moslashuvchan elementning xususiyatlari:

* <mark style="color:red;">`order`</mark>
* <mark style="color:red;">`flex-grow`</mark>
* <mark style="color:red;">`flex-shrink`</mark>
* <mark style="color:red;">`flex-basis`</mark>
* <mark style="color:red;">`flex`</mark>
* <mark style="color:red;">`align-self`</mark>

### order xususiyati&#x20;

`order` xususiyati moslashuvchan elementlarning tartibini belgilaydi.

<figure><img src="../../../.gitbook/assets/image (308).png" alt=""><figcaption></figcaption></figure>

Koddagi birinchi flex element tartibdagi birinchi element sifatida paydo bo'lishi shart emas.

order qiymati raqam bo'lishi kerak, standart qiymat 0.

{% code title="order xususiyati moslashuvchan elementlarning tartibini o'zgartirishi mumkin :" %}
```
<div class="flex-container">
  <div style="order: 3">1</div>
  <div style="order: 2">2</div>
  <div style="order: 4">3</div>
  <div style="order: 1">4</div>
</div>
```
{% endcode %}

### flex-grow xususiyati

`flex-grow` xususiyati moslashuvchan elementning qolgan moslashuvchan elementlarga nisbatan qanchalik cho'zilishini belgilaydi.

<figure><img src="../../../.gitbook/assets/image (365).png" alt=""><figcaption></figcaption></figure>

Uning qiymati ham raqam bo'lishi kerak, standart qiymat 0.

{% code title="Uchinchi flex elementni boshqa flexx elementlarga qaraganda sakkiz baravar uzunroq cho'zish:" %}
```
<div class="flex-container">
  <div style="flex-grow: 1">1</div>
  <div style="flex-grow: 1">2</div>
  <div style="flex-grow: 8">3</div>
</div>
```
{% endcode %}

### Flex-shrink xususiyati

`flex-shrink` xususiyati flex elementning qolgan flex elementlariga nisbatan qanchalik qisqarishini belgilaydi.

<figure><img src="../../../.gitbook/assets/image (291).png" alt=""><figcaption></figcaption></figure>

Uning qiymati raqam bo'lishi kerak, standart qiymat 1.

{% code title="Uchinchi flex element boshqa flex elementlar kabi qisqarishiga yo'l qo'ymaslik:" %}
```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex-shrink: 0">3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
  <div>7</div>
  <div>8</div>
  <div>9</div>
  <div>10</div>
</div>
```
{% endcode %}

### flex-basis xususiyati

`flex-basis` xususiyati flex elementning dastlabki uzunligini belgilaydi.

<figure><img src="../../../.gitbook/assets/image (521).png" alt=""><figcaption></figcaption></figure>

{% code title="Uchinchi flex elementning dastlabki uzunligini 200px qilish:" %}
```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex-basis: 200px">3</div>
  <div>4</div>
</div>
```
{% endcode %}

### felx xususiyati

`flex` xususiyati `flex-grow`, `flex-shrink` va `flex-basis` xususiyatlarining qisqartma shakli hisoblanadi.

{% code title="Uchinchi flex elementni grow bo'lmaydigan (0), shrink bo'lmaydigan (0) va boshlang'ich uzunligini 200px qiling:" %}
```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="flex: 0 0 200px">3</div>
  <div>4</div>
</div>
```
{% endcode %}

### align-self xususiyati

`align-self` xususiyati flex konteyner ichidagi tanlangan element uchun joylashuvni belgilaydi.

`align-self` xususiyati konteynerning `align-items` xususiyati tomonidan o'rnatilgan standart joylashuvni bekor qiladi.

<figure><img src="../../../.gitbook/assets/image (404).png" alt=""><figcaption></figcaption></figure>

Ushbu misollar orqali `align-self` xususiyatini yaxshiroq ko'rsatib berish uchun 200px balandlikdagi konteynerdan foydalanamiz.

{% code title="Uchinchi f;ex elementni konteynerning o'rtasiga to'g'irlash:" %}
```
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div style="align-self: center">3</div>
  <div>4</div>
</div>
```
{% endcode %}

{% code title="Ikkinchi flex elementni konteynerning yuqori qismiga va uchinchi flex elementni konteynerning pastki qismiga to'g'irlash:" %}
```
<div class="flex-container">
  <div>1</div>
  <div style="align-self: flex-start">2</div>
  <div style="align-self: flex-end">3</div>
  <div>4</div>
</div>
```
{% endcode %}

### CSS Flexbox elementlarining xususiyatlari

Quyidagi jadvalda Flexbox Itemsning barcha xususiyatlari keltirilgan:

| Xususiyat                                                                                                                                                 | Ta'rif                                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| [align-self](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_align-self.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Specifies the alignment for a flex item (overrides the flex container's align-items property)               |
| [flex](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_flex.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | A shorthand property for the flex-grow, flex-shrink, and the flex-basis properties                          |
| [flex-basis](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_flex-basis.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Specifies the initial length of a flex item                                                                 |
| [flex-grow](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_flex-grow.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Specifies how much a flex item will grow relative to the rest of the flex items inside the same container   |
| [flex-shrink](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_flex-shrink.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Specifies how much a flex item will shrink relative to the rest of the flex items inside the same container |
| [order](https://www-w3schools-com.translate.goog/cssref/css3\_pr\_order.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | Specifies the order of the flex items inside the same container                                             |
