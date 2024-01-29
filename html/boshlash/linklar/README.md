---
description: >-
  Havolalar deyarli barcha veb-sahifalarda mavjud. Havolalar foydalanuvchilarga
  havolani bosish orqali bir sahifadan boshqa sahifaga o'tish imkonini beradi.
---

# Linklar

## HTML havolalar - Giperhavola

HTML havolalari giperhavolalardir

Siz havolani bosishingiz va boshqa sahifaga o'tishingiz mumkin.

Sichqonchani havola ustiga olib borganingizda, sichqoncha kursori kichik qo'lga aylanadi.

{% hint style="warning" %}
**Eslatma:** havola matn bo'lishi shart emas. Havola rasm yoki boshqa HTML elementi bo'lishi ham mumkin!
{% endhint %}

## HTML Havolalar - Sintaksis

HTMLda `<a>` tegi giperhavolani ifodalaydi. Uning sintaksisi quyidagicha.

```
<a href="url">link text</a>
```

`<a>` elementining eng muhim atributi `href` atributi bo'lib, unga havolaning manzili kiritiladi.

_Link text_ qismi esa foydalanuvchiga ko'rinadigan qismdir.

Havola matnini bosish foydalanuvchini kiritilgan URL manzilga o'tkazadi.

{% code title="Bu misolda w3school.com saytiga o'tkazuvchi havolani qanday yaratish ko'rsatilgan:" %}
```
<a href="https://www.w3schools.com/">Visit W3Schools.com!</a>
```
{% endcode %}

Standart tarzda, havolalar barcha brauzerlarda quyidagicha ko'rinadi:

* Kirilmagan havola ranggi ko'k va tagida chizilgan
* Kirilgan havola ranggi binafsha rang va tagida chizilgan
* Havola ustiga bosilganda ranggi qizil va tagida chizilgan

{% hint style="warning" %}
**Eslatma:** Havolalar boshqacha ko'rinishda bo'lishi uchun albatta ularni CSS orqali o'zgartirishingiz mumkin!
{% endhint %}

## HTML Havolalar - Target attributi

Odatda, havolani bosganingizda u aynan siz turgan brauzer oynasida ochiladi. Buni o'zgartirish uchun havolaga `target` atributini berishingiz kerak.

`target` atributi havola sahifasi qayerda ochilshi kerakligini belgilab beradi.

`target` attributi quyidagi qiymatlardan biriga ega bo'lishi mumkin:

* `_self`- Standart qiymat. Sahifani bosilgan oynada/tabda ochadi
* `_blank`- Sahifani yangi oyna yoki yangi tabda ochadi
* `_parent`- Sahifa asosiy ramkada ochiladi.
* `_top`- Sahifa brauzer oynasining to'liq qismida ochiladi.

{% code title="Sahifa brauzerning yangi oynasida yoki yangi tabda ochilishi uchun  target="_blank" dan foydalaning" %}
```
<a href="https://www.w3schools.com/" target="_blank">Visit W3Schools!</a>
```
{% endcode %}

## Absolute URLlar va Relative URLlar

Yuqoridagi ikkala misolda ham `href` attributida **absolute URL** (to'liq manzil) ishlatilgan.

Lokal havola (xuddi shu veb-saytdagi sahifaga havola) **relative URL** bilan ko'rsatiladi ("https://www" qismisiz):

```
<h2>Absolute URLs</h2>
<p><a href="https://www.w3.org/">W3C</a></p>
<p><a href="https://www.google.com/">Google</a></p>

<h2>Relative URLs</h2>
<p><a href="html_images.asp">HTML Images</a></p>
<p><a href="/css/default.asp">CSS Tutorial</a></p>
```

## HTML havolalar - Rasmdan havola sifatida foydalaning

Rasmdan havola sifatida foydalanish uchun `<img>` tegni `<i>` tegining ichiga qo'yish kifoya:

```html
<a href="default.asp">
<img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a>
```

## Elektron pochta manziliga havola

Foydalanuvchining elektron pochta dasturini ochadigan havola yaratish uchun `href` atributining ichida `mailto:` dan foydalaning.

```
<a href="mailto:someone@example.com">Send email</a>
```

## Havola sifatidagi tugma

HTML tugmalaridan havola sifatida foydalanish uchun Javascriptga tegishli ba'zi kodlar qo'shishingiz kerak.

JavaScript tugmani bosish kabi hodisalarda nima sodir bo'lishini belgilash imkonini beradi:

```
<button onclick="document.location='default.asp'">HTML Tutorial</button>
```

## Havola nomlari

`title` attributi element haqida qo'shimcha ma'lumotni bildiradi. Ma'lumot ko'pincha sichqonchani element ustida olib borganda tooltip sifatida ko'rsatiladi.

```
<a href="https://www.w3schools.com/html/" title="Go to W3Schools HTML section">Visit our HTML Tutorial</a>
```

## Relative URL va Absolute URL haqida batafsil

{% code title="Boshqa Veb-saytga o'tkazish uchun to'liq URL manzilidan foydalanish: " %}
```
<a href="https://www.w3schools.com/html/default.asp">HTML tutorial</a>
```
{% endcode %}

{% code title="Joriy veb-saytdagi html jildda joylashgan sahifaga havola yaratish:" %}
```
<a href="/html/default.asp">HTML tutorial</a>
```
{% endcode %}

{% code title="Joriy sahifa bilan bir xil papkada joylashgan sahifaga havola yaratish: " %}
```
<a href="default.asp">HTML tutorial</a>
```
{% endcode %}

## Bo'lim xulosasi

Havola yratish uchun `<a>` elementidan foydalaning

Havola manzilini belgilashda `href` attributidan foydalaning

Havola sahifasi qayerda ochilishini belgilashda `target` attributidan foydalaning

Rasmdan havola sifatida foydalanish uchun (`<a>` ichida) `<img>` elementidan foydalaning

Foydalanuvchining pochta dasturini ochish uchn `href` attributi ichida `mailto:`dan foydalaning

## HTML havola teglari

| Teg  | Tavsif               |
| ---- | -------------------- |
| \<a> | Giperhavola yaratish |
