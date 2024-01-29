---
description: Ushbu bo'lim forma elementlarining barchasini tushuntirib beradi.
---

# Form elementlari

## \<form> elementi

HTMLning `<form>` elementi quyidagi forma elementlaridan bittasini yoki bir nechtasini o'z ichiga olishi mumkin:

* `<input>`
* `<label>`
* `<select>`
* `<textarea>`
* `<button>`
* `<fieldset>`
* `<legend>`
* `<datalist>`
* `<output>`
* `<option>`
* `<optgroup>`

## \<input> elementi

Eng ko'p ishlatiladigan forma elementlaridan biri `<input>` elementidir.

`<input>` element `type` atributiga qarab bir necha xil shaklda bo'lishi mumkin.

```
<label for="fname">First name:</label>
<input type="text" id="fname" name="fname"> 
```

## \<label> elementi

`<label>` tegi forma elementlarini bir biriga bog'lash vazifasini bajradi.

`<label>` elementi ekranni o'quvchi dasturdan foydalanadigan foydalanuvchilar uchun foydali hisoblanadi, chunki foydalanuvchi input maydonini bosganida ekranni o'quvchi dastur labelga kiritilgan matnni baland ovozda o'qiydi.

Shuningdek  `<label>` elementi radio tugmalari yoki checkbox kataklari kabi kichik maydonlarni bosishga qiynalayotgan foydalanuvchilarga yordam beradi - chunki foydalanuvchi `<label>` elementi ichidagi matnni bosganida, u radio tugmani/checkbox katakchasini tanlaydi.

`<label>` tegining `for` atributi ularni bir-biriga bog'lashi uchun `<input>` elementning `id` atributiga berilgan qiymat bilan bir xil bo'lishi kerak.

## \<select> elementi

`<select>` elementi drop-down ro'yxat yaratadi.

```
<label for="cars">Choose a car:</label>
<select id="cars" name="cars">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select> 
```

`<option>` elementlari tanlanishi kerak bo'lgan variantni ifodlaydi.

Standart tarzda, drop-down ro'yxatdagi birinchi element tanlangan holatda turadi.

Variantlar orasida tanlangan sifatida turishi kerak bo'lgan boshqa variantni berish uchun uning \<option> elementiga `selected`  atributni parametr sifatida qo'shing:

```
<option value="fiat" selected>Fiat</option> 
```

## Ko'rinib turuvchi qiymatlar:

Ko'rinib turishi kerak bo'lgan qiymatlar sonini belgilash uchun `size` atributidan foydalaning:

```
<label for="cars">Choose a car:</label>
<select id="cars" name="cars" size="3">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select> 
```

## Bir nechtasini tanlashga ruxsat berish:

Foydalanuvchiga bir nechta qiymatlarni tanlashga ruxsat berish uchun `multiple` atributdan foydalaning:

```
<label for="cars">Choose a car:</label>
<select id="cars" name="cars" size="4" multiple>
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select> 
```

## \<textarea> elementi

`<textarea>` elementi bir necha qatorga ega matn kiritish maydonini belgilaydi:

```
<textarea name="message" rows="10" cols="30">
The cat was playing in the garden.
</textarea> 
```

`rows` atributi matn maydonidagi qatorlar sonini belgilaydi.

`cols` atributi matn maydonining kengligi (eni) ni belgilaydi.

Yuqoridagi kod brauzerda mana bunday ko'rinadi:

![](<../../.gitbook/assets/image (443).png>)

CSS-dan foydalanib, matn maydonining o'lchamini o'zgartirishngiz mumkin:

```
<textarea name="message" style="width:200px; height:600px;">
The cat was playing in the garden.
</textarea> 
```

## \<button> elementi

`<button>` elementi bosiladigan tugmani yaratadi:

```
<button type="button" onclick="alert('Hello World!')">Click Me!</button> 
```

Yuqoridagi kod brauzerda mana bunday ko'rinadi:

![](<../../.gitbook/assets/image (39).png>)

{% hint style="info" %}
**Eslatma:** Button elementi uchun har doim `type` atributini bering. Brauzerlar button elementi uchun har xil standart turlaridan foydalanadi.
{% endhint %}

## \<fieldset> va \<legend> elementlari

`<fieldset>` elementi formadagi bir biriga bo'g'liq ma'lumotlarni guruhlash uchun ishlatiladi.

`<legend>` elementi esa `<fieldset>` elementi uchun sarlavhani ifodalaydi.

```
<form action="/action_page.php">
  <fieldset>
    <legend>Personalia:</legend>
    <label for="fname">First name:</label><br>
    <input type="text" id="fname" name="fname" value="John"><br>
    <label for="lname">Last name:</label><br>
    <input type="text" id="lname" name="lname" value="Doe"><br><br>
    <input type="submit" value="Submit">
  </fieldset>
</form> 
```

Yuqoridagi kod brauzerda mana bunday ko'rinadi:

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

## \<datalist> elementi

`<datalist>` elementi `<input>` elementi uchun avvaldan tayyorlab qo'yilgan variantlar ro'yxatini ko'rsatadi.

Foydalanuvchilar ma'lumotlarni kiritishda avvaldan tayyorlab qo'yilgan variantlarning drop-down ro'yxatini ko'rishadi.

`<input>` elementining `list` atributi `<datalist>` elementining `id` atributiga murojaat qilishi kerak.

```
<form action="/action_page.php">
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

## \<output> elementi

`<output>` elementi dasturlash tili orqali bajarilgan arifmetik amallar natijalarini ifodalaydi.

{% code title="Hisoblash amalini bajaring va natijani <output> elementda ko'rsating:" %}
```
<form action="/action_page.php"
  oninput="x.value=parseInt(a.value)+parseInt(b.value)">
  0
  <input type="range"  id="a" name="a" value="50">
  100 +
  <input type="number" id="b" name="b" value="50">
  =
  <output name="x" for="a b"></output>
  <br><br>
  <input type="submit">
</form> 
```
{% endcode %}

| Tag                                                                                                                                       | Description                                                |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| \<form>                                                                                                                                   | Defines an HTML form for user input                        |
| \<input>                                                                                                                                  | Defines an input control                                   |
| \<textarea>                                                                                                                               | Defines a multiline input control (text area)              |
| \<label>                                                                                                                                  | Defines a label for an \<input> element                    |
| \<fieldset>                                                                                                                               | Groups related elements in a form                          |
| \<legend>                                                                                                                                 | Defines a caption for a \<fieldset> element                |
| \<select>                                                                                                                                 | Defines a drop-down list                                   |
| \<optgroup>                                                                                                                               | Defines a group of related options in a drop-down list     |
| \<option>                                                                                                                                 | Defines an option in a drop-down list                      |
| \<button>                                                                                                                                 | Defines a clickable button                                 |
| \<datalist>                                                                                                                               | Specifies a list of pre-defined options for input controls |
| [\<output>](https://www-w3schools-com.translate.goog/tags/tag\_output.asp?\_x\_tr\_sl=en&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Defines the result of a calculation                        |
