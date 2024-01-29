# CSS qanday qo'shiladi

Browser CSS kodini o'qiganida HTML hujjatni shu ma'lumotlarga muvofiq formatlaydi.

### CSS ni qo'shishni 3 xil usuli <a href="#css-ni-qoshishni-3-xil-usuli" id="css-ni-qoshishni-3-xil-usuli"></a>

CSS ni qo'shishni 3 xil usuli mavjud:

* External CSS (Tashqi CSS)
* Internal CSS (Ichki CSS)
* Inline CSS (Bir qatordagi CSS)

### External CSS (Tashqi CSS) <a href="#external-css-tashqi-css" id="external-css-tashqi-css"></a>

Tashqi stillar yordamida butun sayt dizaynini bitta faylning o'zida o'zgartira olasiz!

Har bir HTML sahifasining head qismida tashqi CSS fayl `<link>` tegi orqali ulangan bo'lishi kerak.

{% code title="Tashqi stillar <head> tegining ichida <link> elementi bilan HTML sahifaga ulanadi:" %}
```
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
{% endcode %}

Tashqi CSS fayllar har qanday matn tahrirlovchi dastur orqali yozilishi va .css kengaytmasi bilan saqlanishi mumkin.

Tashqi CSS fayllar o'zida hech qanday HTML teglarini saqlamaydi.

Quyida "**mystyle.css**" fayli qanday ko'rinishi keltirilgan:

{% code title=""mystyle.css"" %}
```
body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}
```
{% endcode %}

{% hint style="danger" %}
**Note**: Xususiyat qiymati (20) va qisqarma (px) o'rtasida bo'sh joy qo'shmang:

Xato (bo'sh joy): margin-left: 20 px;

To'g'ri (bo'sh joysiz): margin-left: 20px;
{% endhint %}

#### Internal CSS (Ichki CSS) <a href="#internal-css-ichki-css" id="internal-css-ichki-css"></a>

Internal CSS (Ichki CSS) bitta HTML sahifasigagina bezak berish kerak bo'lganda ishlatiladi

Ichki CSS \<style> tegi ichida yoziladi va u ham head bo'limida joylashadi.

{% code title="Ichki CSS <style> tegi ichida yozib ketiladi va u ham head bo'limida joylashadi:" %}
```
<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
{% endcode %}

### Inline CSS (Bir qatordagi CSS) <a href="#inline-css-bir-qatordagi-css" id="inline-css-bir-qatordagi-css"></a>

Inline CSS bitta elementga unikal still berish uchun ishlatiladi.

Inline CSSdan foydalanish uchun kerakli elementga `style` attributini qo'shing. Style atributi har qanday CSS xususiyatini o'z ichiga olishi mumkin.

{% code title="Inline stillar tegishli elementning "style" atributida yoziladi:" %}
```
<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

</body>
</html>
```
{% endcode %}

{% hint style="warning" %}
**Maslahat:** Inline css stylesheetning ko'pgina afzalliklarini yo'qotadi. Ushbu usuldan kamdan kam holatda foydalaning.
{% endhint %}

### Bir nechta stylesheetlar <a href="#bir-nechta-ulanish-usullarini-birlashtirish" id="bir-nechta-ulanish-usullarini-birlashtirish"></a>

Agar bitta selektor (element) uchun ba'zi xususiyatlar turli stylesheetlarda berilgan bo'lsa, oxirgi o'qilgan stylesheetdagi qiymatdan foydalaniladi.

{% code title="Tasavvur qiling, quyidagi kod <h1> elementi uchun tashqi CSS faylida yozilgan:" %}
```
h1 {
  color: navy;
}
```
{% endcode %}

{% code title="Keyin, tasavvur qiling quyidagi kod ichki CSS orqali <h1> uchun yozilgan:" %}
```
h1 {
  color: orange;   
}
```
{% endcode %}

{% code title="Agarda Internal CSS, External CSS ulanishdian keyin yozilgan bo'lsa, unda <h1> "olovrang" bo'lib qoladi:" %}
```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
<style>
h1 {
  color: orange;
}
</style>
</head>
```
{% endcode %}

{% code title="Agarda Internal CSS <link> tegidan oldin yozilgan bo'lsa unda External CSS ning qiymatlari hisobga olinib <h1> elementlari "ko'k rang" bo'lib qoladi:" %}
```
<head>
<style>
h1 {
  color: orange;
}
</style>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```
{% endcode %}

### Kaskadlash tartibi

HTML element uchun bir nechta stil qiymatlari berilsa qaysi biri ishlatiladi ?

Barcha sahifadagi stillar quyidagi ketma-ketlikda ishlaydi:

1. Inline stil (HTML elementining ichidagi CSS qiymatlari)
2. External va Inline CSS (Head bo'limidagi)
3. Browser ni defolt holatidagi

Shunday qilib, inline still yuqori ustuvorlikka ega va tashqi va ichki stillarini hamda brauzerning standart sozlamalarini bekor qiladi.
