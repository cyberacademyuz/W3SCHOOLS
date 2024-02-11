---
description: >-
  Havolalar deyarli barcha veb-sahifalarda mavjud. Havolalar foydalanuvchilarga
  havolani bosish orqali bir sahifadan boshqa sahifaga o'tish imkonini beradi.
---

# Linklar

## <mark style="color:green;">HTML havolalar - Giperhavola</mark>

HTML havolalari giperhavolalardir

Siz havolani bosishingiz va boshqa sahifaga o'tishingiz mumkin.

Sichqonchani havola ustiga olib borganingizda, sichqoncha kursori kichik qo'lga aylanadi.

{% hint style="warning" %}
**Eslatma:** havola matn bo'lishi shart emas. Havola rasm yoki boshqa HTML elementi bo'lishi ham mumkin!
{% endhint %}

## HTML Havolalar - Sintaksis

HTMLda <mark style="color:red;">`<a>`</mark> tegi giperhavolani ifodalaydi. Uning sintaksisi quyidagicha.

```html
<a href="url">link text</a>
```

<mark style="color:red;">`<a>`</mark> elementining eng muhim atributi `href` atributi bo'lib, unga havolaning manzili kiritiladi.

_Link text_ qismi esa foydalanuvchiga ko'rinadigan qismdir.

Havola matnini bosish foydalanuvchini kiritilgan URL manzilga o'tkazadi.

{% code title="Bu misolda w3school.com saytiga o'tkazuvchi havolani qanday yaratish ko'rsatilgan:" %}
```html
<a href="https://www.w3schools.com/">Visit W3Schools.com!</a>
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_w3schools" %}

Standart tarzda, havolalar barcha brauzerlarda quyidagicha ko'rinadi:

* Kirilmagan havola ranggi ko'k va tagida chizilgan
* Kirilgan havola ranggi binafsha rang va tagida chizilgan
* Havola ustiga bosilganda ranggi qizil va tagida chizilgan

{% hint style="warning" %}
**Eslatma:** Havolalar boshqacha ko'rinishda bo'lishi uchun albatta ularni CSS orqali o'zgartirishingiz mumkin!
{% endhint %}

## <mark style="color:green;">HTML Havolalar - Target attributi</mark>

Odatda, havolani bosganingizda u aynan siz turgan brauzer oynasida ochiladi. Buni o'zgartirish uchun havolaga `target` atributini berishingiz kerak.

<mark style="color:red;">`target`</mark> atributi havola sahifasi qayerda ochilshi kerakligini belgilab beradi.

<mark style="color:red;">`target`</mark> attributi quyidagi qiymatlardan biriga ega bo'lishi mumkin:

* <mark style="color:red;">`_self`</mark> - Standart qiymat. Sahifani bosilgan oynada/tabda ochadi
* <mark style="color:red;">`_blank`</mark> - Sahifani yangi oyna yoki yangi tabda ochadi
* <mark style="color:red;">`_parent`</mark> - Sahifa asosiy ramkada ochiladi.
* <mark style="color:red;">`_top`</mark> - Sahifa brauzer oynasining to'liq qismida ochiladi.

{% code title="Sahifa brauzerning yangi oynasida yoki yangi tabda ochilishi uchun  target="_blank" dan foydalaning" %}
```html
<a href="https://www.w3schools.com/" target="_blank">Visit W3Schools!</a>
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_target" %}

## <mark style="color:green;">Absolute URLlar va Relative URLlar</mark>

Yuqoridagi ikkala misolda ham <mark style="color:red;">`href`</mark> attributida **absolute URL** (to'liq manzil) ishlatilgan.

Lokal havola (xuddi shu veb-saytdagi sahifaga havola) **relative URL** bilan ko'rsatiladi ("https://www" qismisiz):

```html
<h2>Absolute URLs</h2>
<p><a href="https://www.w3.org/">W3C</a></p>
<p><a href="https://www.google.com/">Google</a></p>

<h2>Relative URLs</h2>
<p><a href="html_images.asp">HTML Images</a></p>
<p><a href="/css/default.asp">CSS Tutorial</a></p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links" %}

## <mark style="color:green;">HTML havolalar - Rasmdan havola sifatida foydalaning</mark>

Rasmdan havola sifatida foydalanish uchun <mark style="color:red;">`<img>`</mark> tegni <mark style="color:red;">`<i>`</mark> tegining ichiga qo'yish kifoya:

```html
<a href="default.asp">
<img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_image" %}

## <mark style="color:green;">Elektron pochta manziliga havola</mark>

Foydalanuvchining elektron pochta dasturini ochadigan havola yaratish uchun <mark style="color:red;">`href`</mark> atributining ichida <mark style="color:red;">`mailto:`</mark> dan foydalaning.

```html
<a href="mailto:someone@example.com">Send email</a>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_email" %}

## <mark style="color:green;">Havola sifatidagi tugma</mark>

HTML tugmalaridan havola sifatida foydalanish uchun Javascriptga tegishli ba'zi kodlar qo'shishingiz kerak.

JavaScript tugmani bosish kabi hodisalarda nima sodir bo'lishini belgilash imkonini beradi:

```html
<button onclick="document.location='default.asp'">HTML Tutorial</button>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_button_element" %}

## <mark style="color:green;">Havola nomlari</mark>

<mark style="color:red;">`title`</mark> attributi element haqida qo'shimcha ma'lumotni bildiradi. Ma'lumot ko'pincha sichqonchani element ustida olib borganda tooltip sifatida ko'rsatiladi.

```html
<a href="https://www.w3schools.com/html/" title="Go to W3Schools HTML section">Visit our HTML Tutorial</a>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_title" %}

## <mark style="color:green;">Relative URL va Absolute URL haqida batafsil</mark>

> Boshqa Veb-saytga o'tkazish uchun to'liq URL manzilidan foydalanish:
>
> ```html
> <a href="https://www.w3schools.com/html/default.asp">HTML tutorial</a>
> ```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_external_url" %}

> Joriy veb-saytdagi html jildda joylashgan sahifaga havola yaratish:
>
> ```html
> <a href="/html/default.asp">HTML tutorial</a>
> ```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_external_relative" %}

> Joriy sahifa bilan bir xil papkada joylashgan sahifaga havola yaratish:
>
> {% code title="Boshqa Veb-saytga o'tkazish uchun to'liq URL manzilidan foydalanish: " %}
> ```
> <a href="default.asp">HTML tutorial</a>
> ```
> {% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_external" %}

## <mark style="color:green;">Bo'lim xulosasi</mark>

Havola yratish uchun <mark style="color:red;">`<a>`</mark> elementidan foydalaning

Havola manzilini belgilashda <mark style="color:red;">`href`</mark> attributidan foydalaning

Havola sahifasi qayerda ochilishini belgilashda <mark style="color:red;">`target`</mark> attributidan foydalaning

Rasmdan havola sifatida foydalanish uchun (<mark style="color:red;">`<a>`</mark> ichida) <mark style="color:red;">`<img>`</mark> elementidan foydalaning

Foydalanuvchining pochta dasturini ochish uchn <mark style="color:red;">`href`</mark> attributi ichida <mark style="color:red;">`mailto:`</mark>dan foydalaning

## HTML havola teglari

| Teg  | Tavsif               |
| ---- | -------------------- |
| \<a> | Giperhavola yaratish |
