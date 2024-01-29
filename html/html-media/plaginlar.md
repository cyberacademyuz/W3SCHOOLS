# Plaginlar

Plaginlar brauzerning standart funksiyalarini kengaytiradigan kompyuter dasturlari hisoblanadi.

### Plaginlar

Plaginlar turli maqsadlarda foydalanish uchun mo'ljallangan:

* Java ilovalarini ishga tushirish uchun
* Microsoft ActiveX boshqaruvlarini ishga tushirish uchun
* Flash filmlarni ko'rsatish uchun
* Xaritalarni ko'rsatish uchun
* Viruslarni tekshirish uchun
* Bank identifikatorini tekshirish uchun

{% hint style="danger" %}
Ogohlantirish!

Ko'pgina brauzerlar endi Java appletlarini va plaginlarini qo'llab-quvvatlamaydi.

ActiveX boshqaruvlari endi hech qanday brauzerda qo'llab-quvvatlanmaydi.

Shockwave Flash-ni qo'llab-quvvatlash ham zamonaviy brauzerlarda o'chirilgan.
{% endhint %}

### \<object> elementi

`<object>` elementi barcha brauzerlar tomonidan qo'llab-quvvatlanadi.

`<object>` elementi HTML hujjatiga o'rnatilgan obyektni belgilaydi.

U veb-sahifalarga plaginlarni (masalan, Java appletlari, PDF readerlarni va Flash Playerlar) joylashtirish uchun mo'ljallangan, ammo HTML-ni HTML-ga kiritish uchun ham foydalanish mumkin:

```
<object width="100%" height="500px" data="snippet.html"></object>
```

Yoki hohlasangiz rasmlarni:

```
<object data="audi.jpeg"></object>
```

### \<embed>  elementi

`<embed>` elementi barcha asosiy brauzerlarda qo'llab-quvvatlanadi.

`<embed>` elementi, HTML hujjatiga o'rnatilgan obyektni ham belgilaydi.

Veb-brauzerlar \<embed> elementini uzoq vaqt davomida qo'llab-quvvatlab keladi. Biroq, u HTML5 dan oldin HTML spetsifikatsiyasining bir qismi bo'lmagan.

```
<embed src="audi.jpeg">
```

{% hint style="warning" %}
E'tibor bering, \<embed> elementida yopiluvchi teg yo'q. Unda muqobil matn bo‘lishi mumkin emas.
{% endhint %}

`<embed>` elementi HTML-ni HTML-ga kiritish uchun ham ishlatilishi mumkin:

```
<embed width="100%" height="500px" src="snippet.html">
```
