---
description: HTML-da <, @, % kabi belgilar, belgi obyeklariga almashtirilishi kerak
---

# Belgi obyektlari

## HTML obyektlari

Ba'zi belgilar HTMLga avvaldan kiritib kiritib qo'yilgan.

Agar siz matnlaringizda < yoki > belgilaridan foydalansangiz, HTML uni teglar bilan aralashtirib yuborishi mumkin.

Belgi obyektlari <, @, % kabi turli belgilarni ifodlash uchun foydalaniladi.

Belgi obyektlari quyidagicha ko'rinadi:

```
&obyekt_nomi;
yoki
&#obyekt_raqami; 
```

Ekranda < belgisini ko'rsatish uchun **\&lt;** yoki **\&#60** ni yozishimiz kerak.

{% hint style="warning" %}
**Obyekt nomlardan foydalanishning afzalligi:** Obyekt nomlarini eslab qolish oson

**Obyekt nomlaridan foydalanishning noqulayligi:** Brauzerlar barcha obyekt nomlarini qo'llab quvvatlamaydi, ammo obyekt raqamlarini yaxshi qo'llab quvvatlaydi.
{% endhint %}

## Non-breaking Space

HTMLda tez-tez ishlatiladigan obyekt bu **non-breaking space** hisoblanadi.

Non-breaking space - bu brauzer tomonidan o'chirib tashlanmaydigan bo'sh joylardir.

Non-breaking space bilan ajratilgan ikkita so'z bir-biri bilan yopishib turadi.

Misollar:

* § 10
* 10 km/h
* 10 PM

**Non-breaking space** dan foydalanishning yana bir keng tarqalgan usuli brauzerlarning HTML-sahifalardagi bir nechta ketma ket bo'sh joylarni o'chirib tashlashini oldini olishdir.

Agar matningizda 10 ta ketma ket bo'sh joy qoldirsangiz, brauzer ulardan 9 tasini olib tashlaydi. Matningizga keraklicha bo'sh joylar qoʻshish uchun **\&nbsp;** dan foydalana olasiz.

{% hint style="warning" %}
**Maslahat:** Non-breaking hyphen ([\&#8209;](https://www.w3schools.com/charsets/ref\_utf\_punctuation.asp)) yangi chiziq - belgisi uchun ishlatiladi.
{% endhint %}

## HTMLning ba'zi foydali belgi obyektlari

<table><thead><tr><th width="126">Natija</th><th width="210">Ta'rif</th><th>Obyekt nomi</th><th>Obyekt raqami</th></tr></thead><tbody><tr><td></td><td>non-breaking space</td><td>&#x26;nbsp;</td><td>&#x26;#160;</td></tr><tr><td>&#x3C;</td><td>dan kichik</td><td>&#x26;lt;</td><td>&#x26;#60;</td></tr><tr><td>></td><td>dan katta</td><td>&#x26;gt;</td><td>&#x26;#62;</td></tr><tr><td>&#x26;</td><td>ampersand</td><td>&#x26;amp;</td><td>&#x26;#38;</td></tr><tr><td>"</td><td>Qo'shtirnoq</td><td>&#x26;quot;</td><td>&#x26;#34;</td></tr><tr><td>'</td><td>Birtirnoq (apostro</td><td>&#x26;apos;</td><td>&#x26;#39;</td></tr><tr><td>¢</td><td>sent</td><td>&#x26;cent;</td><td>&#x26;#162;</td></tr><tr><td>£</td><td>funt</td><td>&#x26;pound;</td><td>&#x26;#163;</td></tr><tr><td>¥</td><td>yen</td><td>&#x26;yen;</td><td>&#x26;#165;</td></tr><tr><td>€</td><td>yevro</td><td>&#x26;euro;</td><td>&#x26;#8364;</td></tr><tr><td>©</td><td>copyright (mualliflik huquqi)</td><td>&#x26;copy;</td><td>&#x26;#169;</td></tr><tr><td>®</td><td>ro'yxatga olingan tovar belgisi</td><td>&#x26;reg;</td><td>&#x26;#174;</td></tr></tbody></table>

{% hint style="warning" %}
**Eslatma**: Obyekt nomlari katta kichik harflarga qarab farq qiladi
{% endhint %}

## Diakritik belgilar

Diakritik belgi - bu harfga qo'shiladigan "glif"dir.

&#x20; ̀ va  ́ kabi ba’zi belgilar diakritik belgi hisoblanadi.

Diakritik belgilar harfning tepasida ham, ostida ham, harf ichida ham, ikki harf orasida ham bo'lishi mumkin.

Diakritik belgilar, sahifada ishlatiladigan charset encodida mavjud bo'lmagan belgini yaratish uchun alfanumerik belgilar bilan birgalikda ishlatilishi mumkin.

Quyida bunga bir nechta misollar keltirilgan:

| ́Belgi | Harf | Konstruktor | Natija |
| ------ | ---- | ----------- | ------ |
| ̀      | a    | a\&#768;    | à     |
| ́      | a    | a\&#769;    | á     |
| ̂      | a    | a\&#770;    | â     |
|  ̃     | a    | a\&#771;    | ã     |
|  ̀     | O    | O\&#768;    | Ò     |
|  ́     | O    | O\&#769;    | Ó     |
| ̂      | O    | O\&#770;    | Ô     |
|  ̃     | O    | O\&#771;    | Õ     |

Ushbu qo'llanmaning keyingi bobida ko'proq HTML belgilari bilan tanishasiz.
