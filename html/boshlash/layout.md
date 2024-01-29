---
description: Veb-saytlar kontentni ko'pincha bir nechta ustunlarda ko'rsatadi
---

# Layout

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

## Layout elementlar

HTML veb-sahifaning turli qismlarini o'rab turuvchi bir nechta semantik elementlarga ega:

<img src="../../.gitbook/assets/image (63).png" alt="" data-size="original">

* `<header>` - sahifa yoki bo'lim uchun bosh qism
* `<nav>` - Navigatsiya havolalari uchun qism
* `<section>` - Sahifaning biror bir bo'limi
* `<article>` - Sahifa tarkibidagi mustaqil qism
* `<aside>` - Sahifa tarkibidan tashqari tarkibni ifodalaydi (yon panel kabi)
* `<footer>` - sahifa yoki bo'lim uchun pastki qism
* `<details>` - Foydalanuvchi talabiga binoan ochilshi va yopilshi mumkin bo'lgan qo'shimcha tafsilotlarni o'z ichiga oladi.
* `<summary>` - elementi uchun sarlavhani ifodalaydi.

Semantik elementlar haqida bizning [HTML semantikalar ](semantikalar.md)bo'limimizda batafsilriq ma'lumot olishingiz mumkin.

## Layout texnikalari

turli qismlarini o'rab turuvchi layoutlar yaratishning to'rt xil usuli mavjud. Har bir texnikaning ijobiy va salbiy tomonlari bor:

* CSS freymework
* CSSning float xususiyati
* CSS flexbox
* CSS grid

## CSS freymworklari

Agar layoutlaringizni tezroq yaratmoqchi bo'lsangiz w3.css va bootstrap kabi CSS freymworklaridan foydalaning.

## CSS float layouti

Barcha layoutlarni CSSning float xususiyatidan foydalangan holda tuzish odatiy holga aylangan. Floatni o'rganish oson - faqat float va `clear` xususiyatlari qanday ishlashini eslab qolishingiz kerak.&#x20;

**Kamchiliklari:** Float elementlar html oqimiga bog'langan, bu esa sahifaning moslashuvchanligiga zarar yetkazishi mumkin.

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

## Flexbox layouti

Flexbox-dan foydalanish, sahifa tartibi turli ekran o'lchamlari va turli xil displey qurilmalariga mos kelishi kerak bo'lganda, elementlarni moslashuvchan qilishni ta'minlaydi.

<figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

CSS Grid Layout moduli qatorlar va ustunlar bilan gridga asoslangan layout tizimini taklif etadi, bu esa float va moshlashuvchanlikdan foydalanilmagan veb-sahifalar tuzishni osonlashtiradi.
