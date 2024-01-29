# Sass o'zgaruvchilar

### Sass o'zgaruvchilar <a href="#sass-ozgaruvchilar" id="sass-ozgaruvchilar"></a>

O'zgaruvchilar keyinchalik qayta ishlatishingiz mumkin bo'lgan ma'lumotlarni saqlash usuli hisoblanadi.

Sass yordamida ma'lumotlarni o'zgaruvchilarda saqlashingiz mumkin, masalan:

* Stringlarni
* Raqamlarni
* Ranglarni
* Booleanlarni
* Ro'yhatlarni
* Null-larni

Sass o'zgaruvchilarini e'lon qilish uchun, $ belgisidan keyin, uning nomi yozilishi kerak:

{% code title="Sassda o'zgaruvchi sintaksisi:" %}
```
$variablename: value;
```
{% endcode %}

Quyidagi misolda `myFont`, `myColor`, `myFontSize` va `myWidth` nomli 4 ta o'zgaruvchi e'lon qilinadi. O'zgaruvchilar e'lon qilingandan keyin, ulardan xohlagan joyda foydalanishingiz mumkin:

```
$myFont: Helvetica, sans-serif;
$myColor: red;
$myFontSize: 18px;
$myWidth: 680px;

body {
  font-family: $myFont;
  font-size: $myFontSize;
  color: $myColor;
}

#container {
  width: $myWidth;
}
```

Sass fayli CSS ga tarjima qilinganda, u o'zgaruvchilarni (`myFont`, `myColor` va boshqalarni) oladi va CSS-ga joylashtirilgan o'zgaruvchi qiymatlarini oddiy CSS-da ko'rsatadi, masalan:

```
body {
  font-family: Helvetica, sans-serif;
  font-size: 18px;
  color: red;
}

#container {
  width: 680px;
}
```

### Sass o'zgaruvchi scopi <a href="#sass-ozgaruvchan-doirasi" id="sass-ozgaruvchan-doirasi"></a>

Sass o'zgaruvchilari faqat ular e'lon qilingan joyda foydalanish scopiga ega.

Quyidagi misolga qarang:

```
$myColor: red;

h1 {
  $myColor: green;
  color: $myColor;
}

p {
  color: $myColor;
}
```

`<p>` tegidagi matnning rangi qizil bo'ladimi yoki yashil ? Qizil bo'ladi!

Boshqa misol, $myColor: yashil; `<h1>` qoidasi ichida joylashgan va faqat o'sha yerda mavjud bo'ladi!

CSSga o'girish natijasi quyidagicha bo'ladi:

```
h1 {
  color: green;
}

p {
  color: red;
}
```

Bu o'zgaruvchi scopi uchun standart xatti-harakatdir.

### Sassda !global dan foydalanish <a href="#sass-global-dan-foydalanish" id="sass-global-dan-foydalanish"></a>

O'zgaruvchilar scopining standart xatti-harakatini `!global` kalit so'zi yordamida bekor qilish mumkin.

`!global` kalit so'zi o'zgaruvchining global o'zgaruvchi ekanligini ko'rsatadi, ya'ni unga barcha scopelarda murojaat qilish mumkin.

Quyidagi misolga qarang (yuqoridagi kabi; lekin `!global` kalit so'zi qo'shilgan):

```
$myColor: red;

h1 {
  $myColor: green !global;
  color: $myColor;
}

p {
  color: $myColor;
}
```

Endi `<p>` tegi ichidagi matn rangi yashil bo'ladi!

Shunday qilib, CSS ga o'girilgan natija quyidagicha bo'ladi:

```
h1 {
  color: green;
}

p {
  color: green;
}
```

{% hint style="warning" %}
**Maslahat**: Global o'zgaruvchilar har qanday kodlardan tashqari elon qilinishi kerak. Barcha global o'zgaruvchilarni "\_globals.scss" deb nomlangan faylda saqlash va faylni `@include` kalit so'zi bilan ulash oqilona yo'l bo'ladi.
{% endhint %}
