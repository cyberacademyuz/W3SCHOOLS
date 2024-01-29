---
description: XHTML - bu HTMLning XML-ga asoslangan talabchan versiyasidir.
---

# HTML va XHTML

## XHTML nima?

* XHTML qisqartmasi E**X**tensible **H**yper **T**ext **M**arkup **L**anguage ni bildiradi
* XHTML - bu HTMLning XML-ga asoslangan talabchan versiyasidir
* XHTML - XML kodlari sifatida ifodalanadigan HTML
* XHTML barcha asosiy brauzerlar tomonidan qo'llab-quvvatlanadi

## Nima uchun XHTML?

XML bu belgilash tili bo'lib, unda barcha kodlar to'g'ri ifodalanishi kerak.

XHTML HTMLni yanada kengaytiriladigan va boshqa ma'lumotlar formatlari (masalan, XML) bilan ishlash uchun moslashuvchan qilish uchun ishlab chiqilgan. Bundan tashqari, brauzerlar HTML-sahifalaridagi xatolarni e'tiborsiz qoldiradilar va veb-sayt kodlarida  ba'zi xatolar bo'lsa ham uni ko'rsatishga harakat qilishadi. Shunday qilib, XHTML hatolarga to'g'irlashga talabchanroq qilib yaratildi.

## HTML dan eng muhim farqlari

* **\<!DOCTYPE>** ni yozish majburiy
* \<html> da **xmlns** atributidan foydalanish majburiy
* \<html>, \<head>, \<title> va \<body> ham majburiy
* Elementlar har doim to'g'ri joylashtirilgan bo'lishi kerak
* Elementlar har doim yopilishi kerak
* Elementlar har doim kichik harflarda bo'lishi kerak
* Atribut nomlari har doim kichik harf bilan yozilishi kerak
* Atribut qiymatlari har doim qo'shtirnoq yoki birtirnoqga olinishi qilinishi kerak
* Atributni minimallashtirish taqiqlanadi

## XHTML - \<!DOCTYPE ....> majburiy

XHTML da \<!DOCTYPE> deklaratsiyasi bo'lishi kerak.

\<html>, \<head>, \<title> va \<body> elementlari ham yozilishi kerak va \<html>-ning **xmlns** atributi xml nom maydonini ko'rsatishi kerak.

{% code title="Bu minimal darajadagi eng kerakli teglarga ega XHTML kodi: " %}
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN"
"http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
  <title>Title of document</title>
</head>
<body>

  some content here...

</body>
</html> 
```
{% endcode %}

### XHTML elementlari to'g'ri joylashtirilgan bo'lishi kerak

XHTMLda elementlar har doim bir-birining ichiga to'g'ri joylashtirilishi kerak, masalan:

{% code title="To'g'ri" %}
```
<b><i>Some text</i></b> 
```
{% endcode %}

{% code title="Noto'g'ri" %}
```
<b><i>Some text</b></i> 
```
{% endcode %}

### XHTML elementlari har doim yopilishi kerak

XHTMLda elementlar har doim yopiq bo'lishi kerak, masalan:

{% code title="To'g'ri" %}
```
<p>This is a paragraph</p>
<p>This is another paragraph</p> 
```
{% endcode %}

{% code title="Noto'g'ri" %}
```
<p>This is a paragraph
<p>This is another paragraph 
```
{% endcode %}

### XHTMLda toq elementlar ham har doim yopilishi kerak

XHTMLda toq elementlar har doim yopilishi kerak, masalan:

{% code title="To'g'ri" %}
```
A break: <br />
A horizontal rule: <hr />
An image: <img src="happy.gif" alt="Happy face" />
```
{% endcode %}

{% code title="Noto'g'ri" %}
```
A break: <br>
A horizontal rule: <hr>
An image: <img src="happy.gif" alt="Happy face">
```
{% endcode %}

### XHTML elementlari kichik harflarda bo'lishi kerak

XHTMLda element nomlari har doim kichik harflarda yozilishi kerak, masalan:

{% code title="To'g'ri" %}
```
<body>
<p>This is a paragraph</p>
</body> 
```
{% endcode %}

{% code title="Noto'g'ri" %}
```
<BODY>
<P>This is a paragraph</P>
</BODY>
```
{% endcode %}

### XHTML-da atribut nomlari kichik harfda bo'lishi kerak

XHTMLda atribut nomlari har doim kichik harfda yozilishi kerak, masalan:

{% code title="To'g'ri" %}
```
<a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a> 
```
{% endcode %}

{% code title="Noto'g'ri" %}
```
<a HREF="https://www.w3schools.com/html/">Visit our HTML tutorial</a> 
```
{% endcode %}

### XHTML-da atribut qiymatlari tirnoqlar orasida bo'lishi kerak

XHTMLda atribut qiymatlari har doim quyidagicha qo'shtirnoq yoki birtirnoq ichida yozislishi kerak:

{% code title="To'g'ri" %}
```
<a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a> 
```
{% endcode %}

{% code title="Noto'g'ri" %}
```
<a href=https://www.w3schools.com/html/>Visit our HTML tutorial</a> 
```
{% endcode %}

### XHTML-da atributni qisqa berish taqiqlangan

XHTMLda atributni minimallashtirish taqiqlanadi:

{% code title="To'g'ri" %}
```
<input type="checkbox" name="vehicle" value="car" checked="checked" />
<input type="text" name="lastname" disabled="disabled" /> 
```
{% endcode %}

{% code title="Noto'g'ri" %}
```
<input type="checkbox" name="vehicle" value="car" checked />
<input type="text" name="lastname" disabled />
```
{% endcode %}
