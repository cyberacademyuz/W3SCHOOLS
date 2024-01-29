# Sass @mixin

### Sass mixin lar <a href="#sass-mixin-lar" id="sass-mixin-lar"></a>

`@mixin` direktivasi butun veb-saytda qayta ishlatilishi kerak bo'lgan CSS kodini yaratishga imkon beradi.

`@include` direktivasi `mixin`dan foydalanish (qo'shish) uchun yaratilgan.

### Mixin ni e'lon qilish <a href="#mixin-ni-bildirish" id="mixin-ni-bildirish"></a>

Mixin `@mixin` direktivasi orqali e'lon qilinadi:

{% code title="Sass @mixin sintaksisi:" %}
```
@mixin name {
  property: value;
  property: value;
  ...
}
```
{% endcode %}

Quyidagi misol "important-text" nomli mixin yaratadi:

```
@mixin muhim-matn {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid blue;
}
```

{% hint style="warning" %}
**Maslahat**: Sassda chiziqcha va pastki chiziq bo'yicha maslahat: chiziqcha va pastki chiziq bir xil hisoblanadi. Bu **@mixin important-text { }** va **@mixin important\_text { }** bir xil miksin sifatida qabul qilinishini anglatadi!
{% endhint %}

### Mixin dan foydalanish <a href="#mixin-dan-foydalanish" id="mixin-dan-foydalanish"></a>

`@include` direktivasi mixin kiritish uchun ishlatiladi.

{% code title="Sass @include mixin sintaksisi:" %}
```
selector {
  @include mixin-name;
}
```
{% endcode %}

Shunday qilib, yuqorida yaratilgan important text mixinini kiritish uchun:

```
.danger {
  @include important-text;
  background-color: green;
}
```

Sass transpileri yuqoridagi kodni oddiy CSS ga o'giradi:

```
.danger {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid blue;
  background-color: green;
}
```

Mixin boshqa mixinlarni ham o'z ichiga olishi mumkin:

```
@mixin special-text {
  @include important-text;
  @include link;
  @include special-border;
}
```

### O'zgaruvchilarni Mixin ga kiritish <a href="#ozgaruvchilarni-mixin-ga-kiritish" id="ozgaruvchilarni-mixin-ga-kiritish"></a>

Mixinlar argumentlarni qabul qiladi. O'zgaruvchilarni shu tarzda mixinga kiritishingiz mumkin.

Argumentli mixinni quyidagicha ifodalash mumkin:

```
/* Define mixin with two arguments */
@mixin bordered($color, $width) {
  border: $width solid $color;
}

.myArticle {
  @include bordered(blue, 1px);  // Call mixin with two values
}

.myNotes {
  @include bordered(red, 2px); // Call mixin with two values
}
```

E'tibor bering, argumentlar o'zgaruvchilar sifatida o'rnatiladi va keyin `border` xususiyatining qiymatlari (rangi va kengligi) sifatida ishlatiladi.

Kompilyatsiyadan so'ng CSS kod quyidagicha ko'rinadi:

```
.myArticle {
  border: 1px solid blue;
}

.myNotes {
  border: 2px solid red;
}
```

## Mixin uchun standart qiymatlar <a href="#mixin-uchun-standart-qiymatlar" id="mixin-uchun-standart-qiymatlar"></a>

Bundan tashqari, mixindagi o'zgaruvchilar uchun standart qiymatlar berish mumkin:

```
@mixin bordered($color: blue, $width: 1px) {
  border: $width solid $color;
}
```

Keyin, faqat mixinni qo'shganingizda o'zgaradigan qiymatlarni ko'rsatishingiz kerak:

```
.myTips {
  @include bordered($color: orange);
}
```

### Vendor prefikslari uchun mixindan foydalanish <a href="#vendor-prefikslari-uchun-mixindan-foydalanish" id="vendor-prefikslari-uchun-mixindan-foydalanish"></a>

Vendor prefikslari uchu mixindan foydalanish mumkin.

{% code title="transformga misol:" %}
```
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}

.myBox {
  @include transform(rotate(20deg));
}
```
{% endcode %}

Kompilatsiyadan keyin CSS fayl quyidagicha bo'ladi:

```
.myBox {
  -webkit-transform: rotate(20deg);
  -ms-transform: rotate(20deg);
  transform: rotate(20deg);
}
```
