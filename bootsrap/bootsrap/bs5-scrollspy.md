# BS5 Scrollspy

### Scrollspy

Scrollspy navigatsiya ro'yxatidagi havolalarni sahifaning scroll holatiga qarab avtomatik tarda yangilash uchun ishlatiladi.

<figure><img src="../../.gitbook/assets/image (551).png" alt=""><figcaption></figcaption></figure>

### Scrollspy qanday yaratiladi

Quyidagi misolda scrollspyni qanday yaratish ko'rsatilgan:

```
<!-- The scrollable area -->
<body data-bs-spy="scroll" data-bs-target=".navbar" data-bs-offset="50">

<!-- The navbar - The <a> elements are used to jump to a section in the scrollable area -->
<nav class="navbar navbar-expand-sm bg-dark navbar-dark fixed-top">
...
  <ul class="navbar-nav">
    <li><a href="#section1">Section 1</a></li>
    ...
</nav>

<!-- Section 1 -->
<div id="section1">
  <h1>Section 1</h1>
  <p>Try to scroll this page and look at the navigation bar while scrolling!</p>
</div>
...

</body>
```

#### Misolni tushuntirish

Scroll bo'ladigan maydon sifatida ishlatilishi kerak bo'lgan elementga `data-bs-spy="scroll"` ni qo'shing (ko'pincha bu `<body>`element).

Keyin id qiymati yoki navbar (`.navbar`) class nomi bilan `data-bs-target` atributini qo'shing. Bu navbarning scroll bo'ladigan maydon bilan bog'langanligiga ishonch hosil qilish uchun kerak.

Scroll bo'ladigan elementlar navbardagi ro'yxat elementlarining ichidagi havolalar id-siga mos kelishi kerakligini eslab qoling ( `<div id="section1">` `<a href="#section1">`ga mos keladi).

Ixtiyoriy `data-bs-offset` atributi scroll bo'ladigan joyni hisoblashda tepadan surilishi kerak bo'lgan piksellar sonini belgilaydi. Bu scroll eilementlarga oʻtishda navbardagi havolalar aktiv holatni tez yoki erta oʻzgartirayotganini sezganingizda foyda beradi. Standart 10px.

{% hint style="warning" %}
**Reletive position talab qiladi:** data-bs-spy="scroll" elementi to'g'ri ishlashi uchun CSSning **position** xususiyati, "**relative**" qiymatini talab qiladi.
{% endhint %}
