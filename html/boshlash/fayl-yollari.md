---
description: Fayl yo'li - websayt papkalari ichidagi fayllarning joylashishini bildiradi.
---

# Fayl yo'llari

## Fayl yo'llariga misollar

| Yo'l                             | Ta'rif                                                                     |
| -------------------------------- | -------------------------------------------------------------------------- |
| \<img src="picture.jpg">         | "picture.jpg" fayli joriy sahifa bilan bir papkada joylashga               |
| \<img src="images/picture.jpg">  | "picture.jpg" fayli shu joydagi **images** papkasida joylashgan            |
| \<img src="/images/picture.jpg"> | "picture.jpg" vebsayt tizimining root qimidagi images papkasida joylashgan |
| \<img src="../picture.jpg">      | "picture.jpg" fayli shu papkadan bitta yuqoridagi papkada joylashgan       |

## HTML fayl yo'llari

Fayl yo'llari quyidagilar kabi tashqi fayllarni ulash uchun foydalaniladi:

* Veb sahifalar
* Rasmlar
* Css fayllar
* Javascriptlar

## Absolyut fayl yo'li

Absolyut fayl yo'li faylning to'liq URL manzilidir:

```
<img src="https://www.w3schools.com/images/picture.jpg" alt="Mountain"> 
```

Relative fayl yo'li

Relative fayl yo'llari joriy sahifaga nisbatan beriladigan faylning joylashuvini bildiradi:

```
<img src="/images/picture.jpg" alt="Mountain"> 
```

Quyidagi misolda fayl joylashuvi, joriy papkada joylashgan images pakpasidagi faylni bildiradi:

```
<img src="images/picture.jpg" alt="Mountain"> 
```

Quyidagi misolda faylning joylashuvi joriy jilddan bitta tepada joylashgan images papkasidagi faylni bildiradi:

```
<img src="../images/picture.jpg" alt="Mountain"> 
```

## Best Practice

Relative fayl yo'llaridan foydalanish best practice hisoblanadi.

Relative fayl yo'llaridan foydalanganda, veb-sahifalaringizning URL manzili bilan bog'lanmaydi. Barcha havolalar sizning shaxsiy kompyuteringizda ishlaydi.
