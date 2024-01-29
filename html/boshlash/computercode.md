---
description: >-
  HTML foydalanuvchi bosishi kerak bo'lgan tugmalarni va kompyuter kodlarini
  ko'rsatishi uchun bir nechta elementlarni o'z ichiga oladi.
---

# Computercode

```
<code>
x = 5;
y = 6;
z = x + y;
</code> 
```

Klaviatura tugmalarini ko'rsatish uchun \<kbd> elementi

HTMLning `<kbd>` elementi klaviaturada bosiladigan tugmalarni ko'rsatish uchun ishlatiladi. Element ichidagi matn brauzerning standart monospace shriftida ko'rsatiladi.

{% code title="HTML faylda klaviatura tugmalarini ko'rsatuvchi matn yarating: " overflow="wrap" %}
```
<p>Save the document by pressing <kbd>Ctrl + S</kbd></p>
```
{% endcode %}

{% code title="Natija" %}
```
Save the document by pressing Ctrl + S
```
{% endcode %}

## Dastur habarlari uchun \<samp> elementi

HTMLning `<samp>` elementi kompyuter dasturining xabarlarini ko'rsatish uchun ishlatiladi. Element ichidagi matn brauzerning standart monospace shriftida ko'rsatiladi.

{% code title="HTML faylda dastur xabarlarini ko'rsatuvchi matn yarating: " %}
```
<p>Message from my computer:</p>
<p><samp>File not found.<br>Press F1 to continue</samp></p> 
```
{% endcode %}

{% code title="Natija" %}
```
Message from my computer:

File not found.
Press F1 to continue
```
{% endcode %}

## Kompyuter kodlari uchun \<code> elementi

HTMLning `<code>` elementi kompyuter kodining bir qismini ko'rsatish uchun ishlatiladi. Element ichidagi matn brauzerning standart monospace shriftida ko'rsatiladi.

{% code title="HTML fayldagi ba'zi matnlarni kompyuter kodi sifatida ko'rsating:" %}
```
<code>
x = 5;
y = 6;
z = x + y;
</code> 
```
{% endcode %}

{% code title="Natija" %}
```
x = 5; y = 6; z = x + y; 
```
{% endcode %}

E'tibor bering, `<code>` elementi qo'shimcha bo'sh joylarni va yangi qatorlarni qabul qilmaydi.

Buni to'g'irlash uchun \<code> elementini \<pre> elementining ichida foydalaning.

```
<pre>
<code>
x = 5;
y = 6;
z = x + y;
</code>
</pre> 
```

```
x = 5;
y = 6;
z = x + y;
```

## O'zgaruvchilar uchun \<var> elementi

HTML `<var>` elementi dasturlashda yoki matematik amallarda o'zgaruvchini ko'rsatish uchun ishlatiladi. Element ichidagi matn odatda kursiv shaklda ko'rsatiladi.

{% code title="HTMLdagi ba'zi matnlarni o'zgaruvchilar sifatida belgilang:" overflow="wrap" %}
```
<p>The area of a triangle is: 1/2 x <var>b</var> x <var>h</var>, where <var>b</var> is the base, and <var>h</var> is the vertical height.</p> 
```
{% endcode %}

{% code title="Natija:" %}
```
The area of a triangle is: 1/2 x b x h, where b is the base, and h is the vertical height. 
```
{% endcode %}

## Xulosa

