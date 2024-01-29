# CSS Formalar

HTML formasining ko'rinishi CSS yordamida sezilarli darajada yaxshilanishi mumkin:

<figure><img src="../../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>

### Input maydonlariga stil berish <a href="#input-maydonlariga-stil-berish" id="input-maydonlariga-stil-berish"></a>

Input maydonining uzunligini belgilash uchun `width` xususiyatidan foydalaning.

<figure><img src="../../.gitbook/assets/image (789).png" alt=""><figcaption></figcaption></figure>

```
input {
  width: 100%;
}
```

Yuqoridagi misol barcha \<input> elementlarida ishlaydi. Agar ma'lum bir input turiga still bermoqchi bo'lsangiz unda atribut selektorlaridan foydalanishingiz mumkin:

* `input[type=text]` - faqatgina matn kiritiladigan maydonlarini tanlaydi.
* `input[type=password]` - faqatgina parol kiritiladigan maydonlarni tanlaydi.
* `input[type=number]` - faqatgina raqam kiritiladigan maydonlarni tanlaydi
* va hokazolar

### Padding berilgan inputlar <a href="#padding-berilgan-inputlar" id="padding-berilgan-inputlar"></a>

`padding` xususiyatidan foydalanish orqali input ichidagi bo'sh joyni yana biroz ko'paytirib olsangiz bo'ladi.

**Maslahat:** Agar sizda ketma ket kelgan bir qancha inputlar bo'lsa, ularning tashqarisiga ko'proq joy qo'shish uchun margindan foydalanishingiz mumkin.

<figure><img src="../../.gitbook/assets/image (783).png" alt=""><figcaption></figcaption></figure>

```
input[type=text] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
}
```

{% hint style="warning" %}
E'tibor bering, `box-sizing` xususiyatini `border-box` qildik. Bu padding va chegaralarni elementlarning umumiy kengligi va balandligiga kiritilishiga imkon beradi.

`box-sizing` xususiyati haqida bizning <mark style="color:green;">CSS Box Sizing</mark> bo'limimizda batafsil o'qing.
{% endhint %}

### Xoshiyaga ega inputlar <a href="#borderga-ega-inputlar" id="borderga-ega-inputlar"></a>

`border` xususiyatidan foydalanib inputlarning xoshiya o'lchamini va rangini o'zgartirish mumkin. Undan tashqari `border-radius` xususyati orqali dumoloqsimon burchaklar qo'shish mumkin

<figure><img src="../../.gitbook/assets/image (757).png" alt=""><figcaption></figcaption></figure>

```
 input[type=text] {
  border: 2px solid red;
  border-radius: 4px;
}
```

Agar faqat pastki qismga chegara bermoqchi bo'lsangiz `border-bottom` xususiyatidan foydalaning

<figure><img src="../../.gitbook/assets/image (770).png" alt=""><figcaption></figcaption></figure>

```
 input[type=text] {
  border: none;
  border-bottom: 2px solid red;
}
```

### Rangli inputlar <a href="#rangli-inputlar" id="rangli-inputlar"></a>

Inputning background rangini berish uchun `background-color` xususiyatidan va matn rangini o'zgartirish uchun `color` xususiyatidan foydalaning:

<figure><img src="../../.gitbook/assets/image (799).png" alt=""><figcaption></figcaption></figure>

```
 input[type=text] {
  background-color: #3CBC8D;
  color: white;
}
```

### Fokus holatidagi inputlar <a href="#fokusdagi-inputlar" id="fokusdagi-inputlar"></a>

Default holatda ba'zi brauzerlar input fokus bo'lganida uning atrofiga ko'k outline qo'shadi. Uni `outline: none;` qilish orqali olib tashlasangiz bo'ladi

Ularning ustiga bosilganda nimalar bo'lishi keraklgiini ifodalash uchun `:focus` selektoridan foydalaning.

<figure><img src="../../.gitbook/assets/image (828).png" alt=""><figcaption></figcaption></figure>

```
 input[type=text]:focus {
  background-color: lightblue;
}
```

```
input[type=text]:focus {
  border: 3px solid #555;
}
```

### Rasm/iconli input <a href="#rasmikonkaga-ega-input" id="rasmikonkaga-ega-input"></a>

Agar input ichiga icon yoki rasm qo'yishni xohlasangiz `background-image` dan va uni joylashuvini belgilash uchun `background-position` xususiyatlaridan foydalaning. Shuni ham unitmangki, iconning atrofida bo'sh joy qoldirish uchun chap tomoniga kattaroq padding beridik.

<figure><img src="../../.gitbook/assets/image (279).png" alt=""><figcaption></figcaption></figure>

```
input[type=text] {
  background-color: white;
  background-image: url('searchicon.png');
  background-position: 10px 10px;
  background-repeat: no-repeat;
  padding-left: 40px;
}
```

### Animatsiyali input <a href="#animatsiyali-input" id="animatsiyali-input"></a>

Ushbu misolda input fokus bo'lganida qidiruv inputining kengligini animatsion tarzda kattalashtirish uchun CSSning `transition` xususiyatidan foydalanamiz. `transition`lar haqida keyigi bo'limlarda bilib olasiz.

![](<../../.gitbook/assets/image (802).png>)

```
 input[type=text] {
  transition: width 0.4s ease-in-out;
}

input[type=text]:focus {
  width: 100%;
}
```

### Textarea-larga still berish <a href="#textarea-larga-stil-berish" id="textarea-larga-stil-berish"></a>

**Maslahat:** Textarea-larining oʻlchamlarini oʻzgartirishni taqiqlash uchun `resize` xususiyatidan foydalaning (pastki oʻng burchakdagi “grabber”ni oʻchirish):

<figure><img src="../../.gitbook/assets/image (632).png" alt=""><figcaption></figcaption></figure>

```
textarea {
  width: 100%;
  height: 150px;
  padding: 12px 20px;
  box-sizing: border-box;
  border: 2px solid #ccc;
  border-radius: 4px;
  background-color: #f8f8f8;
  resize: none;
}
```

### Tanlanadigan menyularga still berish <a href="#menularni-selekt-qilish-va-ularga-chiroy-berishmasada" id="menularni-selekt-qilish-va-ularga-chiroy-berishmasada"></a>

<figure><img src="../../.gitbook/assets/image (758).png" alt=""><figcaption></figcaption></figure>

```
 select {
  width: 100%;
  padding: 16px 20px;
  border: none;
  border-radius: 4px;
  background-color: #f1f1f1;
}
```

### Input tugma-larga still berish <a href="#input-button-larga-stil-berish" id="input-button-larga-stil-berish"></a>

<figure><img src="../../.gitbook/assets/image (796).png" alt=""><figcaption></figcaption></figure>

```
 select {
  width: 100%;
  padding: 16px 20px;
  border: none;
  border-radius: 4px;
  background-color: #f1f1f1;
}
```

CSS yordamida tugmalarga still berish haqida ko'proq ma'lumot olish uchun <mark style="color:green;">CSS tugmalar</mark> bo'yicha qo'llanmamizni o'qing.

### Responsiv forma <a href="#responsive-form" id="responsive-form"></a>

Brauzer oynasini kichiklashtirsangiz effektni ko'rasiz. Ekran 600px dan kichiklashganda Ustunlarni yonma yon emas, balki bir-biriga ustma ust holatda joylashtiring.

{% hint style="warning" %}
**Advanced:** Quyidagi misolda bu effekt <mark style="color:green;">media querielar</mark> yordamida amalga oshirilgan. Media querielar haqida keyingi bo'limlarda bilib olasiz.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (825).png" alt=""><figcaption></figcaption></figure>
