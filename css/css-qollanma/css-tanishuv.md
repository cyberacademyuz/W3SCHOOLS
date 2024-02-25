---
description: CSS - bu veb-sahifani bezash uchun foydalanadigan til.
---

# CSS Tanishuv

## <mark style="color:green;">CSS nima ?</mark> <a href="#css-nima" id="css-nima"></a>

* CSS qisqartmasi Cascading Style Sheets degan ma'noni anglatadi
* CSS HTML elementlarini ekranda, hujjatda yoki boshqa mediada qanday ko'rsatilishini tavsiflaydi.
* CSS ko'p ishlarni tejaydi. U bir vaqtning o'zida bir nechta veb-sahifalar joylashuvini boshqarishi mumkin
* Tashqi stylesheetlar CSS fayllarda saqlanadi.

## <mark style="color:green;">CSS DEMO - Bitta HTML sahifa - Birqancha stillar!</mark> <a href="#css-demo-bitta-html-sahifa-koplab-bezaklar-bilan" id="css-demo-bitta-html-sahifa-koplab-bezaklar-bilan"></a>

Bu yerda 4 xil stil bilan tasvirlangan HTML sahifani ko'rsatganmiz. Turlicha still berilgan sahifalarni ko'rish uchun "Stylesheet 1", "Stylesheet 2", "Srylesheet 3", "Stylesheet 4" havolalarini bosing.

<figure><img src="../../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:green;">Nima uchun CSS dan foydalanish kerak ?</mark>

CSS web sahifalarni bezaklarini, dizaynini, ko'rinishini va har xil qurilmalarda qanday ko'rsatilishi kerakligini belgilaydi.

{% tabs %}
{% tab title="CSS" %}
```css
body {
  background-color: lightblue;
}

h1 {
  color: white;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_intro" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">CSS katta muammoni hal qildi</mark> <a href="#css-katta-muammoni-hal-qilgan" id="css-katta-muammoni-hal-qilgan"></a>

HTML da HECH QACHON web sahifani bezaydigan teglar bo'lmagan!

HTML web sahifadagi kontentni belgilash uchun yaratilgan:

<mark style="color:red;">`<h1>`</mark> This is a heading <mark style="color:red;">`</h1>`</mark>

<mark style="color:red;">`<p>`</mark> This is a paragraph. <mark style="color:red;">`</p>`</mark>

HTML ning 3.2 spetsifikatsiyasidan <mark style="color:red;">`<font>`</mark> tegiga o'xshash teglar va ranglarni bildiriuvchi attributlar qo'shilgandan so'ng, web dasturchilar uchun haqiqiy azob boshlandi. Har bir sahifasiga shriftlar va ranglar beriladigan katta veb-saytlarni yaratish uzoq va qimmat jarayonga aylandi.

Bu muammoni hal qilish maqsadida, World Wide Web Consortium (W3C) - CSS ni yaratishdi.

CSS yaratilgandan keyin HTML dagi bezak beruvchi teglar olib tashlandi!

{% hint style="warning" %}
Agar HTML nima ekanligini bilmasangiz unda bizning HTML darsligimizni ko'rib chiqing.
{% endhint %}

## <mark style="color:green;">CSS ko'p ishni tejaydi!</mark>

Still kodlari .css fayllarda saqlanadi.

Tashqi CSS fayl yordamida bitta faylni o'zgartirish orqali butun sayt dizaynini o'zgartirishingiz mumkin!
