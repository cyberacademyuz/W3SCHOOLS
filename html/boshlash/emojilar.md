---
description: 'Emojilar UTF-8 belgilar to‘plamidagi belgilardir: 😄 😍 💗'
---

# Emojilar

## Emojilar nima ?

Emojilar rasm yoki piktogramma o'xshab ko'rinadi, lekin ular unday emas.

Ular UTF-8 (Unicode) belgilar to'plamidagi harflar(belgilar)dir.

{% hint style="warning" %}
UTF-8 dunyodagi deyarli barcha belgilar va symbollarni qamrab oladi.
{% endhint %}

## HTML charset atributi

HTML sahifani to'g'ri ko'rsatish uchun veb-brauzer sahifada ishlatiladigan belgilar to'plamini bilishi kerak.

U `<meta>` tegida ko'rsatiladi:

```
<meta charset="UTF-8">
```

{% hint style="warning" %}
Agar u ko'rsatilmagan bo'lsa ham UTF-8 HTML-dagi standart belgilar to'plami hisoblanadi.
{% endhint %}

## UTF-8 belgilari

Ko'pgina UTF-8 belgilarini klaviaturada yozib bo'lmaydi, lekin ular har doim raqamlar yordamida ko'rsatilishi mumkin (bu obyekt raqamlari deb ataladi):

* A - 65
* B - 66
* C - 67

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
</head>
<body>

<p>I will display A B C</p>
<p>I will display &#65; &#66; &#67;</p>

</body>
</html> 
```

## Misol orqali tushuntirish:

`<meta charset="UTF-8">` elementi belgilar to'plamini ifodalaydi.

A, B va C belgilar 65, 66 va 67 raqamlari orqali ko'rsatiladi.

Brauzer unga belgi ko'rsatayotganingizni tushunishi uchun ob'ekt raqamini \&# dan boshlashingiz va uni ; (nuqta vergul) bilan tugatishingiz kerak.

## Emoji belgilar

Emojilar ham UTF-8 alifbosidagi belgilar hisoblanadi:

* 😄 128516
* 😍 128525
* 💗 128151

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
</head>
<body>

<h1>My First Emoji</h1>

<p>&#128512;</p>

</body>
</html> 
```

Emojilar belgilar bo'lgani uchun ularni HTML-dagi boshqa belgilar kabi nusxalash, ekranda ko'rsatish va o'lchamini o'zgartirish mumkin.

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
</head>
<body>

<h1>Sized Emojis</h1>

<p style="font-size:48px">
&#128512; &#128516; &#128525; &#128151;
</p>

</body>
</html> 
```

## UTF-8-dagi ba'zi emoji belgilar

| Emoji | Qiymati    |
| ----- | ---------- |
| 🗻    | \&#128507  |
| 🗼    | \&#128508; |
| 🗽    | \&#128509; |
| 🗾    | \&#128510; |
| 🗿    | \&#128511; |
| 😀    | \&#128512; |
| 😁    | \&#128513; |
| 😂    | \&#128514; |
| 😃    | \&#128515; |
| 😄    | \&#128516; |
| 😅    | \&#128517; |
