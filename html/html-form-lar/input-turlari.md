---
description: Ushbu bo'limda <input> elementining har xil turlari tushuntirilgan.
---

# Input turlari

## Input turlari

HTMLda foydalanishingiz mumkin bo'lgan turli xil input turlari:

* `<input type="button">`
* `<input type="checkbox">`
* `<input type="color">`
* `<input type="date">`
* `<input type="datetime-local">`
* `<input type="email">`
* `<input type="file">`
* `<input type="hidden">`
* `<input type="image">`
* `<input type="month">`
* `<input type="number">`
* `<input type="password">`
* `<input type="radio">`
* `<input type="range">`
* `<input type="reset">`
* `<input type="search">`
* `<input type="submit">`
* `<input type="tel">`
* `<input type="text">`
* `<input type="time">`
* `<input type="url">`
* `<input type="week">`

{% hint style="warning" %}
**Ma'lumot:** `type` atributining standart qiymati matn.
{% endhint %}

## Mant turidagi input

`<input type="text">` matn kiritish uchun bir qatorli matn maydonini yaratadi.

```
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form> 
```

Yuqoridagi kod brauzerda mana bunday ko'rinadi:

![](<../../.gitbook/assets/image (25).png>)

## Password turidagi input

`<input type="password">` parol kiritish maydonini yaratadi.

```
<form>
  <label for="username">Username:</label><br>
  <input type="text" id="username" name="username"><br>
  <label for="pwd">Password:</label><br>
  <input type="password" id="pwd" name="pwd">
</form> 
```

Yuqoridagi kod brauzerda mana bunday ko'rinadi:

![](<../../.gitbook/assets/image (57).png>)

{% hint style="warning" %}
Parol maydonidagi ma'lumot yulduzcha yoki doira shaklida ko'rsatiladi.
{% endhint %}

## Submit turidagi input

`<input type="submit">` ma'lumotlarni forma ma'lumotlarini qabul qiluvchiga yuborish tugmachasini yaratadi.

Forma ma'lumotlarini qabul qiluvchi odatda foydalanuvchi ma'lumotlarini saqlash va qayta foydalanish uchun tuzilgan serverdagi fayl hisoblanadi.

Formani qabul qiluvchi form elementining action atributida ko'rsatiladi.

{% code title="Yuborish tugmasi bo'lgan forma:" %}
```
<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form> 
```
{% endcode %}

Yuqoridagi HTML kod brauzerda quyidagidek ko'rinadi:

![](<../../.gitbook/assets/image (455).png>)

Submit tugmasining value atributini unutib qoldirsangiz tugma standart matnni oladi:

```
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit">
</form> 
```

## Reset turidagi input

`<input type="reset">` formaga kiritilgan barcha ma'lumotlarni standart qiymatlariga qaytaradigan **tiklash tugmasi**ni ifodalaydi:

```
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
  <input type="reset">
</form> 
```

Yuqoridagi HTML kod brauzerda quyidagidek ko'rinadi:

![](<../../.gitbook/assets/image (70).png>)

{% hint style="warning" %}
Agar siz kiritilgan ma'lumotlarni o'zgartirsangiz va keyin "Qayta tiklash" tugmasini bossangiz, forma-ma'lumotlar eskl holatiga qaytariladi.
{% endhint %}

## Radio turidagi input

`<input type="radio">` radio tugmalar yaratadi.

Radio tugmalari foydalanuvchiga bir nechta variyantlardan bittasini tanlash imkonini beradi.

```
<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form> 
```

Yuqoridagi HTML kod brauzerda quyidagicha ko'rinadi:

Sevimli veb-tilingizni tanlang:

HTML\
CSS\
JavaScript

## Checkbox turidagi input

`<input type="checkbox">` checkbox katakchalarini yaratadi.

Checkbox katakchalari turli tanlov variantlaridan bir nechtasini tanlash yoki hech qaysini tanlamaslik imkonini beradi.

{% code title="Checkbox katakchali forma" %}
```
 <form>
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label>
</form>
```
{% endcode %}

Yuqoridagi HTML kod brauzerda quyidagidek ko'rinadi:

* [ ] &#x20;Mening velosipedim bor
* [ ] &#x20;Mening mashinam bor
* [ ] Menda qayiq bor

## Button turidagi input

`<input type="button">` tugma yaratadi

```
<input type="button" onclick="alert('Hello World!')" value="Click Me!"> 
```

Yuqoridagi HTML kod brauzerda quyidagidek ko'rinadi:

![](<../../.gitbook/assets/image (14).png>)

## Color turidagi input

`<input type="color">` ranglardan tashkil topgan maydonlar uchun ishlatiladi .

Brauzer qo'llab-quvvatlashiga qarab, input maydonida rang tanlash vositasi paydo bo'lishi mumkin.

```
<form>
  <label for="favcolor">Select your favorite color:</label>
  <input type="color" id="favcolor" name="favcolor">
</form> 
```

## Date turidagi input

`<input type="date">` sanani tanlash imkonini beruvchi maydonlar uchun ishlatiladi.

Brauzer qo'llab-quvvatlashiga qarab, sana tanlagich input maydonida ko'rinishi mumkin.

```
<form>
  <label for="birthday">Birthday:</label>
  <input type="date" id="birthday" name="birthday">
</form> 
```

Shuningdek, sanalarga cheklovlar qo'shish uchun `min`va `max` atributlaridan foydalanishingiz mumkin:

```
<form>
  <label for="datemax">Enter a date before 1980-01-01:</label>
  <input type="date" id="datemax" name="datemax" max="1979-12-31"><br><br>
  <label for="datemin">Enter a date after 2000-01-01:</label>
  <input type="date" id="datemin" name="datemin" min="2000-01-02">
</form> 
```

## Datetime-local input turi

`<input type="datetime-local">` sana va vaqtni vaqt mintaqasisiz kiritish maydonini yaratadi.

Brauzer qo'llab-quvvatlashiga qarab, sana tanlagich input maydonida paydo bo'lishi mumkin.

```
<form>
  <label for="birthdaytime">Birthday (date and time):</label>
  <input type="datetime-local" id="birthdaytime" name="birthdaytime">
</form> 
```

## Email turidagi input

`<input type="email">` elektron pochta manzilini qabul qiladigan input maydonlari uchun ishlatiladi.

Brauzer qo'llab-quvvatlashiga qarab, elektron pochta manzili yuborilganda avtomatik tarzda tasdiqlanishi mumkin.

Ba'zi smartfonlar elektron pochta turini taniydi va elektron pochta inputiga mos kelish uchun klaviaturaga ".com" tugmasini qo'shadi.

```
<form>
  <label for="email">Enter your email:</label>
  <input type="email" id="email" name="email">
</form> 
```

## Image turidagi input

`<input type="image">` rasmni submit tugma sifatida qabul qiladi.

Rasm joylashuvi `src` atributida ko'rsatiladi.

```
<form>
<input type="image" src="img_submit.gif" alt="Submit" width="48" height="48">
</form> 
```

## File turidagi input

`<input type="file">` fayl tanlash va fayl yuklash uchun "Browse" tugmasini yaratadi.

```
<form>
  <label for="myfile">Select a file:</label>
  <input type="file" id="myfile" name="myfile">
</form> 
```

## Hidden turidagi input

`<input type="hidden">` yashirin input maydonini yaratadi (foydalanuvchiga ko'rinmaydi).

Yashirin maydon forma yuborilganda dasturchilarga foydalanuvchilar uchun ko'rilmaydigan yoki o'zgartirilmaydigan ma'lumotlarni kiritish imkonini beradi.

Yashirin maydon ko'pincha forma yuborilgan payt yangilanishi kerak bo'lgan ma'lumotlar bazasining yozuvini saqlaydi.

**Eslatma:** Ushbu qiymatlar foydalanuvchiga sahifada ko'rsatilmasa ham, barcha brauzerlardagi devtools vositalari yoki "View source" funksiyasidan foydalanganda ko'rinadi (va o'zgartirilishi mumkin).

```
<form>
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="hidden" id="custId" name="custId" value="3487">
  <input type="submit" value="Submit">
</form> 
```

## Month turidagi input

`<input type="month">` bu foydalanuvchiga oy va yilni tanlash imkonini beradi.

Brauzer qo'llab-quvvatlashiga qarab, sana tanlagich input maydonida paydo bo'lishi mumkin.

```
<form>
  <label for="bdaymonth">Birthday (month and year):</label>
  <input type="month" id="bdaymonth" name="bdaymonth">
</form> 
```

## Number turidagi input

`<input type="number">`  raqam kiritilladigan input maydonini yaratadi.

Bundan tashqari, qanday raqamlar qabul qilinishiga cheklov qo'yishingiz ham mumkin.

Quyidagi misolda 1 dan 5 gacha qiymat kiritishingiz mumkin bo'lgan input maydoni ko'rsatilgan:

```
<form>
  <label for="quantity">Quantity (between 1 and 5):</label>
  <input type="number" id="quantity" name="quantity" min="1" max="5">
</form> 
```

## Input checklovlari

Quyida ba'zi umumiy input cheklovlarining ro'yxati keltirilgan:

| Atribut   | Ta'rif                                                                                                                  |
| --------- | ----------------------------------------------------------------------------------------------------------------------- |
| checked   | Sahifa yuklanganda input maydonida avvaldan tanlangan qiymatni ifodalaydi (type = "checkbox" yoki type = "radio" uchun) |
| disabled  | Input maydonini o'chirib qo'yish kerakligini bildiradi                                                                  |
| max       | Input maydoni uchun maksimal raqam qiymatini belgilaydi                                                                 |
| maxlength | Input maydoni uchun maksimal belgilar sonini belgilaydi                                                                 |
| min       | Input maydoni uchun minimal raqam qiymatini belgilaydi                                                                  |
| pattern   | Input qiymatini tekshirish uchun regex ni ifodalaydi                                                                    |
| readonly  | Input maydonini faqat oʻqish mumkinligini bildiradi (oʻzgartirib boʻlmaydi)                                             |
| required  | Input maydoni to'ldirish zarurligini bildiradi                                                                          |
| size      | Input maydonining kengligini belgilaydi                                                                                 |
| step      | Raqamli input maydon uchun kiritiladigan raqamlar oralig'ini belgilaydi                                                 |
| value     | Input maydoni uchun standart qiymatni ifodalaydi                                                                        |

Keyingi bo'limda input cheklovlari haqida ko'proq narsa o'rganasiz.

Quyidagi misol sizga 0 dan 100 gacha bo'lgan raqamlarni har 10talik intervalda kiritishingiz mumkin bo'lgan raqamli input maydonini ko'rsatadi. Standart qiymat 30:

```
<form>
  <label for="quantity">Quantity:</label>
  <input type="number" id="quantity" name="quantity" min="0" max="100" step="10" value="30">
</form> 
```

## Range turidagi input

`<input type="range">` ma'lum bir raqamdan boshqa bir raqamgacha bo'lgan oraliqdagi raqamni kiritish uchun ishlatiladi. Standart oraliq 0 dan 100 gacha bo'ladi. Biroq `min`, `max` va `step` atributlari orqali qanday raqamlar qabul qilinishini belgilash uchun cheklovlar o'rnatishingiz mumkin:

```
<form>
  <label for="vol">Volume (between 0 and 50):</label>
  <input type="range" id="vol" name="vol" min="0" max="50">
</form> 
```

## Search turidagi input

`<input type="search">` qidiruv maydonlari uchun ishlatiladi (qidiruv maydoni odatdagi matn maydonidek ishlaydi).

```
<form>
  <label for="gsearch">Search Google:</label>
  <input type="search" id="gsearch" name="gsearch">
</form>
```

## Tel turidagi input

`<input type="tel">` telefon raqam kiritilishi kerak bo'lgan input maydonlar uchun ishlatiladi.

```
<form>
  <label for="phone">Enter your phone number:</label>
  <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}">
</form> 
```

## Time turidagi input

`<input type="time">` foydalanuvchiga vaqtni tanlash imkonini beradi.

Brauzer qo'llab-quvvatlashiga qarab, vaqt tanlagich input maydonida paydo bo'lishi mumkin.

```
<form>
  <label for="appt">Select a time:</label>
  <input type="time" id="appt" name="appt">
</form> 
```

## URL turidagi input

`<input type="url">` URL manzilni qabul qilishi kerak bo'lgan input maydonlari uchun ishlatiladi.

Brauzer qo'llab-quvvatlashiga qarab, URL maydonidagi qiymat yuborilganda avtomatik tarzda tasdiqlanishi mumkin.

Ba'zi smartfonlar input URL turida ekanligini taniydi va url inputga mos kelish uchun klaviaturaga ".com" tugmasini qo'shadi.

```
<form>
  <label for="homepage">Add your homepage:</label>
  <input type="url" id="homepage" name="homepage">
</form> 
```

## Week turidagi input

`<input type="week">` foydalanuvchiga hafta va yilni tanlash imkonini beradi.

Brauzer qo'llab-quvvatlashiga qarab, input maydonida sana tanlagich paydo bo'lishi mumkin.

## Inputning type atributi

| Teg              | Ta'ri                                           |
| ---------------- | ----------------------------------------------- |
| \<input type=""> | Ekranda ko'rsatiladigan input turini belgilaydi |
