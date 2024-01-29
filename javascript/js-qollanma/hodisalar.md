# Hodisalar

HTML hodisalari HTML elementlari bilan sodir bo'ladigan **"holatlar"**dir.

HTML sahifalarda JavaScriptdan foydalanilganda, JavaScript bu hodisalarga **“**javob qaytara**”** oladi.

### HTML hodisalari

HTMLda yuz beradigan biror hodisa brauzer yoki foydalanuvchi bajaradigan amal bo'lishi mumkin.

Quyida HTMLda yuz berishi mumkin bo'lgan hodisalarga ba'zi misollar keltirilgan:

* HTML veb-sahifa yuklanishi tugashi
* HTMLdagi input maydoning o'zgartirilishi
* HTML tugmasi bosilishi

Ko'pincha, biror hodisa yuz berganda, boshqa biror narsa qilishni xohlashingiz mumkin.

JavaScript hodisa sodir bo'lganida biror kodni amalga oshirishga imkon beradi.

HTML, HTML elementlariga JavaScript yordamida hodisani boshqaruvchi atributlar qo'shish imkonini beradi.

Bir tirnoq bilan:

```html
<element event='JavaScript kod'>
```

Qo'shtirnoq bilan:

```html
<element event="JavaScript kod">
```

Quyidagi misolda `onclick` atributi `<button>` elementiga) qo'shilgan:

```html
<button onclick="document.getElementById('demo').innerHTML = Date()">The time is?</button>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_event_onclick1" %}

Yuqoridagi misoldagi kod id="demo" yordamida elementning tarkibini o'zgartiradi.

Keyingi misoldagi kod o'z elementining tarkibini o'zgartiradi (**`this`**`.innerHTML` dan foydalanib):

```html
<button onclick="this.innerHTML = Date()">The time is?</button>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_event_onclick" %}

{% hint style="warning" %}
JavaScript kodlar odatda bir necha qatordan iborat bo'ladi. Funksiyalarni chaqiruvchi hodisa atributlarini uchratish sohada ko'p kuzatiladi.
{% endhint %}

```html
<button onclick="displayDate()">The time is?</button>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_events1" %}

### Umumiy HTML hodisalari

Quyida ba'zi umumiy HTML hodisalari ro'yxati keltirilgan:

| Hodisa      | Ta'rif                                                         |
| ----------- | -------------------------------------------------------------- |
| onchange    | HTML elementi o'zgarganda                                      |
| onclick     | Foydalanuvchi HTML elementini bosganida                        |
| onmouseover | Foydalanuvchi sichqonchani HTML elementi ustiga olib kelganida |
| onmouseout  | Foydalanuvchi sichqonchani elementdan tashqariga chiqarganida  |
| onkeydown   | Foydalanuvchi klaviatura tugmachasini bosganida                |
| onload      | Brauzer sahifani yuklab bo'lganida                             |

Hodisalar ro'yhati juda uzun: [W3Schoolsning JavaScriptda HTML DOM hodisalar ma'lumotnomasi](https://www.w3schools.com/jsref/dom\_obj\_event.asp).

## Hodisa boshqaruvchilar

Hodisalarni boshqaruvchilar foydalanuvchi va brauzer harakatlarini boshqarish va tekshirish uchun  ishlatiladi:

* Har safar sahifa yuklanganda bajarilishi kerak bo'lgan ishlar
* Sahifa yopilganda bajarilishi kerak bo'lgan ishlar
* Foydalanuvchi tugmani bosganida bajarilishi kerak bo'lgan harakat
* Foydalanuvchi ma'lumotlarni kiritganda tekshirish va tasdiqlash
* Va boshqalar...

JavaScriptni hodisalar bilan ishlashiga imkon berish uchun turli xil usullardan foydalanish mumkin:

* HTMLning hodisa atributlari JavaScript kodni to'g'ridan to'g'ri bajara oladi
* HTMLning  hodisa atributlari JavaScript funksiyalarini chaqira oladi
* HTML elementlariga o'zingizning hodisani boshqaruvchi funksiyalaringizni berishingiz mumkin
* Hodisalar yuborilishini yoki boshqarilishini oldini olishingiz mumkin
* Va boshqalar ...

{% hint style="warning" %}
HTML DOM bo'limlarida hodisalar va hodisalarni boshqaruvchilar haqida batafsil bilib olasiz.
{% endhint %}
