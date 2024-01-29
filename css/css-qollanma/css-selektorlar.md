# CSS Selektorlar

CSS Selektori nomi bilan ham aytib turibdi, siz bezak bermoqchi bo'lgan HTML elementlarini belgilaydi.

#### CSS Selektorlari <a href="#css-selektorlari-2" id="css-selektorlari-2"></a>

CSS Selektorlar siz still bermoqchi bo'lgan HTML elementlarini "topish" (yoki tanlash) uchun ishlatiladi.

Biz CSS selektorlarini beshta kategoriyaga bo'la olamiz:

* Oddiy selektorlar (elementlarni teg nomi, id-si va classiga qarab topadi)
* [Kombinator](css-kombinatorlar.md) selektorlar (elementlarni ular orasidagi ma'lum munosabatiga qarab tanlaydi)
* [Pseudo-class selektorlar](css-pseudo-class.md) (elementlarni ma'lum bir holatga qarab tanlaydi)
* [Pseudo-elementlar selektorlari](css-pseudo-element.md) (elementni ma'lum bir qismini tanlaydi va still beradi)
* [Attribut selektorlari](css-atrr-selektorlari.md) (elementlarni attribut nomiga yoki attribut qiymatiga qarab belgilaydi)

Ushbu sahifada asosan boshlang'ich CSS selektorlar tushuntirilgan.

### CSS element selektori <a href="#css-element-selektori" id="css-element-selektori"></a>

Element selektori HTML elementlarini nomiga qarab tanlaydi.

{% code title="Ushbu misolda barcha <p> elementlari o'rtada turadi va qizil rangda bo'ladi:" %}
```
p {
  text-align: center;
  color: red;
}
```
{% endcode %}

### CSS id selektori <a href="#css-id-selektori" id="css-id-selektori"></a>

Id selektori elementni tanlash uchun HTML elementining `id` atributidan foydalanadi.

Elementning id-si sahifada bitta bo'ladi, shuning uchun `id` selektori bitta unikal elementni tanlash uchun ishlatiladi!

id-ga ega elementni tanlash uchun xesh (#) belgisini va undan keyin elementning id nomini yozing.

{% code title="Ushbu misoldagi css kod id="para1" attributiga ega elementga qo'llaniladi:" %}
```
#para1 {
  text-align: center;
  color: red;
}
```
{% endcode %}

{% hint style="warning" %}
**Note:** id hech qachon raqam bilan boshlanmaydi!
{% endhint %}

### CSS class selektori <a href="#css-klass-selektori" id="css-klass-selektori"></a>

Class selektori HTML elemntlarini `class` attributiga qarab tanlaydi.

Class attributiga ega elementlarni tanlash uchun nuqta (.) belgisini va undan keyin class nomini yozing.

{% code title="Ushbu misoldagi css kod class="center" ga ega barcha HTML elementlarining rangizni qizil qiladi va uni markazga to'g'irlaydi:" %}
```
.center {
  text-align: center;
  color: red;
}
```
{% endcode %}

Bundan tashqari, classni faqat maxsus HTML elementlariga ta'sir qilishi kerakligini belgilashingiz mumkin.

{% code title="Ushbu misolda faqatgina class="center" ga ega <p> elementlari tanlangan va stil qiymatlari qizil va joylashuvi o'rtaga o'zgartirilgan:" %}
```
p.center {
  text-align: center;
  color: red;
}
```
{% endcode %}

HTML elementlari bittadan ortiq klasslarni o'z ichiga olishi mumkin.

{% code title="Ushbu misolda <p> elementi bir vaqtni o'zida class="center" va class="large" larni jamlamoqda:" %}
```
<p class="center large">This paragraph refers to two classes.</p>
```
{% endcode %}

{% hint style="warning" %}
**Note:** Class nomi raqam bilan boshlanmaydi!
{% endhint %}

### CSS Universal selektor <a href="#css-universal-selektori" id="css-universal-selektori"></a>

Universal selektor sahifadagi barcha HTML elementlarini belgilaydi.

{% code title="CSS qoidasiga ko'ra quyidagi misolda barcha HTML elementlari tanlanadi:" %}
```
* {
  text-align: center;
  color: blue;
}
```
{% endcode %}

### CSS Guruhlash selektorlari <a href="#css-guruhlash-selektorlari" id="css-guruhlash-selektorlari"></a>

Guruhlash selektori bir xil css kodlari bilan berilgan barcha HTML elementlarini tanlaydi.

Quyidagi CSS kodga e'tiboringizni qarating (h1, h2 va p elementlariga bir xil still qiymatlari berilgan):

```
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```

Bunday uzun kodni  guruhlash selektorlari yordamida qisqartirishingiz mumkin.

Guruh selektorlaridan foydalanish uchun har bir element nomidan keyin vergul orqali ajratish kerak.

{% code title="Ushbu misolda yuqoridagi elementlarni guruhlash selektori bilan minimallashtirdik:" %}
```
h1, h2, p {
  text-align: center;
  color: red;
}
```
{% endcode %}

### Barcha oddiy CSS selektorlari <a href="#barcha-oddiy-css-selektorlari" id="barcha-oddiy-css-selektorlari"></a>

| Selektor              | Misol      | Ta'rif                                                      |
| --------------------- | ---------- | ----------------------------------------------------------- |
| _#id_                 | #firstname | id-"firstname" attributiga ega elementni tanlaydi           |
| _.class_              | .intro     | class="intro" ga ega elementlarni tanlaydi                  |
| _element.class_       | p.intro    |  Faqatgina class="intro" ga ega \<p> elementlarini tanlaydi |
| \*                    | \*         | Barcha elementlarni tanlaydi                                |
| _element_             | p          | Barcha \<p> elementlarini tanlaydi                          |
| _element,element,..._ | div, p     | Barcha \<div> va \<p> elementlarini tanlaydi                |
