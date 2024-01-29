---
description: Ushbu bo'limda <input> elementi uchun turli atributlar tushuntirilgan.
---

# Input attributlari

## Value atributi

Inputning `value` atributi input maydoni uchun boshlang'ich qiymatni beradi:

{% code title="Dastlabki qiymatlarga ega bo'lgan input maydonlari:" %}
```
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe">
</form> 
```
{% endcode %}

## Readonly atributi

Inputning `readonly` atributi input maydoni faqat o'qish uchun ekanligini bildiradi.

Readonly hisoblangan input maydonini o'zgartirib bo'lmaydi (lekin foydalanuvchi uni tanlashi, belgilashi va undagi matnni nusxalashi mumkin).

Formani yuborishda readonly input maydonidagi qiymat yuboriladi!

{% code title="Readonly atributiga ega input maydon" %}
```
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John" readonly><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe">
</form>
```
{% endcode %}

## Disabled atributi

Inputning `disabled` atributi input maydonini o'chirib qo'yish kerakligini bildiradi.

O'chirilgan input maydonidan foydalanib ham va bosib ham bo'lmaydi,

Formani yuborishda disabled input maydonining qiymati yuborilmaydi!

{% code title="Disabled atributiga ega input maydon" %}
```
 <form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John" disabled><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe">
</form> 
```
{% endcode %}

## Size atributi

Inputning `size` atributi input maydonining gorizontal uzunligini belgilaydi.

`size`-ning standart qiymati 20.

**Eslatma:** `size` atributi text, search, tel, url, email va password nomli input turlari bilan ishlaydi

{% code title="Input maydonining kengligini belgilash" %}
```
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" size="50"><br>
  <label for="pin">PIN:</label><br>
  <input type="text" id="pin" name="pin" size="4">
</form> 
```
{% endcode %}

## Maxlength atributi

Inputning `maxlength` atributi input maydonida kiritiladigan belgilarning maksimal sonini belgilaydi.

**Eslatma:** `maxlength` berilgan  bo'lsa, input maydoni berilgan belgilar sonidan ortig'ini qabul qilmaydi. Biroq, bu atribut foydalanuvchini bu haqida ogohlantirmayd. Shuning uchun agar siz foydalanuvchini ogohlantirmoqchi bo'lsangiz, JavaScriptdan foydalanishingiz kerak.

{% code title="Input maydoni uchun maksimal uzunlikni belgilang::" %}
```
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" size="50"><br>
  <label for="pin">PIN:</label><br>
  <input type="text" id="pin" name="pin" maxlength="4" size="4">
</form> 
```
{% endcode %}

## Min va max atributlari

Inputning `min`va `max`atributlari inputga kiritiladigan eng kam va eng ko'p belgilar sonini o'rnatadi.

`min` va `max` atributlari number, range, data, datetime-local, month, time va wekk nomli input turlari bilan ishlaydi.

**Maslahat:** Minimal va maksimum qiymatlar oralig'ini yaratish uchun min va max atributlaridan birgalikda foydalaning.

{% code title="Maksimal sana, minimal sana va checklangan qiymatlar diapazonini belgilang:" %}
```
<form>
  <label for="datemax">Enter a date before 1980-01-01:</label>
  <input type="date" id="datemax" name="datemax" max="1979-12-31"><br><br>

  <label for="datemin">Enter a date after 2000-01-01:</label>
  <input type="date" id="datemin" name="datemin" min="2000-01-02"><br><br>

  <label for="quantity">Quantity (between 1 and 5):</label>
  <input type="number" id="quantity" name="quantity" min="1" max="5">
</form>
```
{% endcode %}

## Multiple atributi

Inputning `multiple` atributi foydalanuvchiga input maydonida bir nechta qiymat kiritishga imkon beradi.

`multiple` atributi email va file input turlari bilan ishlaydi.

{% code title="Bir nechta qiymatlarni qabul qiladigan fayl yuklash maydoni:" %}
```
<form>
  <label for="files">Select files:</label>
  <input type="file" id="files" name="files" multiple>
</form> 
```
{% endcode %}

## Pattern atributi

Inputning `pattern` atributi forma yuborilganda input  maydonining qiymatini tekshiriladigan regex-ni qabul qiladi.

`pattern` atributi text, date, search, url, tel, email va password input turlari bilan ishlaydi.

**Maslahat:** Foydalanuvchiga nima kritishi kerakligini ko'rsatib yordam berish uchun tittle atributidan foydalaning.

{% code title="Faqat uchta harfdan iborat bo'lgan input maydoni (raqamlar yoki maxsus belgilarsiz):" %}
```
<form>
  <label for="country_code">Country code:</label>
  <input type="text" id="country_code" name="country_code"
  pattern="[A-Za-z]{3}" title="Three letter country code">
</form>
```
{% endcode %}

## Placeholder atributi

Inputning `placeholder` atributi input maydoniga qanday ma'lumot kiritish kerakligi haqida ko'rsatmani ifodalaydi.

Foydalanuvchi inputga qiymat kiritishidan oldin placeholderga berilgan ko'rsatma input maydonida ko'rsatiladi.

`placeholder` atributi text, search, url, tel, email, va password input turlari bilan ishlaydi.

{% code title="Placeholder matnli input maydon:" %}
```
<form>
  <label for="phone">Enter a phone number:</label>
  <input type="tel" id="phone" name="phone"
  placeholder="123-45-678"
  pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}">
</form> 
```
{% endcode %}

## Required atributi

Inputning `required` atributi formani yuborishdan oldin to'ldirilmagan input maydonini toʻldirish shart ekanligini bildiradi.

`required` atributi text, search, url, tel, email, password, date, number, checkbox, radio, and file input turlari bilan ishlaydi.

{% code title="To'ldirilishi shart bo'lgan input maydon" %}
```
<form>
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" required>
</form>
```
{% endcode %}

## Step atributi

Inputning `step` atributi input maydoni uchun ma'lum bir raqamlar oralig'ini belgilaydi.

**Misol:** agar atribut step="3" qilib berilgan bo'lsa, raqamlar ketma ketligi -3, 0, 3, 6 va hokazo tartibda bo'lishi mumkin.

**Maslahat**: Bu atributdan max va min atributlari bilan birgalikda bir qator ma'lum bir qiymatlarni yaratish uchun foydalanish mumkin.

`step` atributi number, range, date, datetime-local, month, time and week bilan ishlaydi.

{% code title="" %}
```
<form>
  <label for="points">Points:</label>
  <input type="number" id="points" name="points" step="3">
</form>
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Input cheklovlariga ishonib bo'lmaydi va JavaScript inputga kiritish mumkin bo'lmagan ma'lumotlarni kiritishning ko'plab usullarini taqdim qiladi. Inputga to'g'ri qiymatlar kiritilganligini tekshirish uchun uni qabul qiluvchi (server) ham tekshirishi kerak!
{% endhint %}

## Autofocus elementi

Inputning `autofocus` atributi sahifaga kirilganda avtomatik tarzda tanlanishi kerak bo'lgan input maydonini bildiradi.

{% code title="Sahifaga kirilganda "Name" input maydoni tanlangan bo'lshiga ruxsat berish:" %}
```
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" autofocus><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form> 
```
{% endcode %}

## Height va width atributi

Inputning `height` va `width` atributlari `<input type="image">` elementining balandligi va kengligini belgilaydi.

{% hint style="warning" %}
**Maslahat:** Rasmlar uchun har doim width va height atributlarini bering. Agar width va height berilgan bo'lsa, sahifa yuklanganda rasm uchun zarur bo'sh joy ajratiladi. Ushbu atributlarsiz brauzer rasm hajmini bilmaydi va unga tegishli joy ajrata olmaydi. Buning natijasida sahifani yuklash paytida sahifa tartibi o'zgaradi.
{% endhint %}

{% code title="Rasmnni width va height atributlari bilan submit tugmasi sifatida ifodalang:" overflow="wrap" %}
```
<form>
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="image" src="img_submit.gif" alt="Submit" width="48" height="48">
</form> 
```
{% endcode %}

## List atributi

Inputning `list` atributi \<input> elementi uchun oldindan belgilangan variantlarni o'z ichiga olgan `<datalist>` elementiga bo'g'laydi.

{% code title="<datalist>da oldindan kiritilgan qiymatlarga ega  <input>elementi:" %}
```
<form>
  <input list="browsers">
  <datalist id="browsers">
    <option value="Internet Explorer">
    <option value="Firefox">
    <option value="Chrome">
    <option value="Opera">
    <option value="Safari">
  </datalist>
</form> 
```
{% endcode %}

## Autocomplete atributi

Inputning `autocomplete` atributi forma yoki input maydonida avtomatik toʻldiruv xususiyatini yoqish yoki oʻchirish kerakligini belgilaydi.

Autocomplete brauzerga kiritiladigan ma'lumotni taxmin qilish imkonini beradi. Agar foydalanuvchi input maydoniga yozishni boshlasa, brauzer oldingi kiritilgan qiymatlar asosida maydonni to'ldirish uchun variantlar ko'rsatadi:

`autocomplete` atributi `<form>` va `<input>`-ning text, search, url, tel, email, password, date, range, and color turlari bilan ishlaydi.

{% code title="Input maydoni uchun autocomplete yoqilgan va oʻchirilgan HTML formasi:" %}
```
<form action="/action_page.php" autocomplete="on">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" autocomplete="off"><br><br>
  <input type="submit" value="Submit">
</form> 
```
{% endcode %}

**Maslahat:** Bu ba'zi brauzerlarda ishlashi uchun brauzerning autocomplete funksiyasini yoqib qo'yishingiz kerak bo'lishi mumkin (brauzer menyusidagi "Sozlamalar" bo'limiga qarang).

## Forma va input elementlari

| Teg      | Ta'rif                                               |
| -------- | ---------------------------------------------------- |
| \<form>  | Foydalanuvchi ma'lumot kiritish uchun forma yaratadi |
| \<input> | Input maydonini yaratish                             |
