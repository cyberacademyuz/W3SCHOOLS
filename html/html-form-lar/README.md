---
description: >-
  HTML formasi foydalanuvchi ma'lumotlarini qabul qilish uchun ishlatiladi.
  Foydalanuvchi ma'lumotlari ko'pincha saqlash va qayta foydalanish uchun
  serverga yuboriladi.
---

# HTML form-lar

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

## \<form> elementi

Foydalannuvchidan ma'lumotlarni qabul qilish uchun HTMLning \<form> elementidan foydalaning.

```
<form>
.
form elements
.
</form>
```

`<form>` elementi har xil turga ega input elementlari uchun konteyner hisoblanadi, masalan: matn kiritish maydonlari, checkboxlar, radio tugmalari, ma'lumotni yuboruvchi tugmalar va hokazo.

### \<input> elementi

HTMLning `<input>` elementi eng ko'p ishlatiladigan forma elementidir.

`<input>` elementi type atributiga qarab turlicha ko'rinishi mumkin.

Mana bunga bir nechta misollar:

| Input turi               | Ta'rifi                                                                                                |
| ------------------------ | ------------------------------------------------------------------------------------------------------ |
| \<input type="text">     | Bir qatorli matn kiritish maydoni                                                                      |
| \<input type="radio">    | Radio tugmachasi  (ko'p variantlardan birini tanlash uchun)                                            |
| \<input type="checkbox"> | Checkbox katakchalari (turli variantlardan bir nechtasini tanlash yoki hech qaysini tanlamaslik uchun) |
| \<input type="submit">   | Yuborish tugmachasi (formani yuborish uchun)                                                           |
| \<input type="button">   | Bosiladigan tugma                                                                                      |

### Matn maydonlari

`<input type="text">` matn kiritish uchun bir qatorli matn maydonini yaratdi.

{% code title="Matn kiritish uchun input maydonlariga ega forma:" %}
```
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form> 
```
{% endcode %}

Yuqoridagi HTML kod brauzerda mana bunday ko'rsatiladi:

![](<../../.gitbook/assets/image (40).png>)

{% hint style="warning" %}
**Eslatma:** Formaning o'zi ko'rinmaydi. Shuni ham yodda tutingki, input maydonining standart kengligi 20 belgidan iborat.
{% endhint %}

## \<label> elementi

Yuqoridagi misolda `<label>` elementidan qanday foydalanilganiga e'tibor bering.

`<label>` tegi forma elementlarini bir biriga bog'lash vazifasini bajradi.

`<label>` elementi ekranni o'quvchi dasturdan foydalanadigan foydalanuvchilar uchun foydali hisoblanadi, chunki foydalanuvchi input maydonini bosganida ekranni o'quvchi dastur labelga kiritilgan matnni baland ovozda o'qiydi.

Shuningdek  `<label>` elementi radio tugmalari yoki checkbox kataklari kabi kichik maydonlarni bosishga qiynalayotgan foydalanuvchilarga yordam beradi - chunki foydalanuvchi `<label>` elementi ichidagi matnni bosganida, u radio tugmani/checkbox katakchasini tanlaydi.

`<label>` tegining `for` atributi ularni bir-biriga bog'lashi uchun `<input>` elementning `id` atributiga berilgan qiymat bilan bir xil bo'lishi kerak.

## Radio tugmalar

`<input type="radio">` radio tugmalar yaratadi.

Radio tugmalari foydalanuvchiga bir nechta variyantlardan bittasini tanlash imkonini beradi.

{% code title="Radio tugmali forma:" %}
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

Yuqoridagi HTML kod brauzerda quyidagicha ko'rinadi:

Sevimli veb-tilingizni tanlang:

HTML\
CSS\
JavaScript

## Checkbox katakchalari

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

## Yuborish tugmasi

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

## \<input> uchun name atributi

&#x20;E'tibor bering, har bir input maydonida yuboriladigan `name` atributi bo'lishi kerak.

Agar `name` atributi unutib qoldirilsa input maydonidagi qiymat umuman yuborilmaydi.

{% code title="Ushbu misolda "Ism" kiritish maydoniniga kiritilgan qiymat yuborilmaydi: " %}
```
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" value="John"><br><br>
  <input type="submit" value="Submit">
</form> 
```
{% endcode %}
