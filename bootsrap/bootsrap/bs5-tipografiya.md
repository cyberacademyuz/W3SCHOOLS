# BS5 Tipografiya

### Bootstrap 5 standart sozlamalari

Bootstrap 5 default tarzda `font-size`  uchun 1rem (16px)-dan foydalanadi va u `line-height` da 1,5 bo'ladi.

Bundan tashqari, barcha `<p>` elementlarda `margin-top:0` va `margin-bottom:1rem`(standart 16px) mavjud.

### \<h1> - \<h6>

Bootstrap 5 stilidagi HTML sarlavhalari ( `<h1>dan` `<h6>`gacha) qalinroq font-weight va moslashuvchan font-size ga ega.

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

Xohlasangiz, boshqa elementlarda `.h1` dan `.h6` gacha bo'lgan classlarni sarlavha sifatida ishlatishingiz mumkin:

```
<p class="h1">h1 Bootstrap heading</p>
<p class="h2">h2 Bootstrap heading</p>
<p class="h3">h3 Bootstrap heading</p>
<p class="h4">h4 Bootstrap heading</p>
<p class="h5">h5 Bootstrap heading</p>
<p class="h6">h6 Bootstrap heading</p>
```

### Display sarlavhalar

Displey sarlavhalari oddiy sarlavhalardan ko'proq ajralib turish uchun ishlatiladi (kattaroq font-size va kichikriq font-weight) va tanlash uchun oltita sinf mavjud:  `.display-1` dan `.display-6` gacha&#x20;

<figure><img src="../../.gitbook/assets/image (611).png" alt=""><figcaption></figcaption></figure>

### \<small>

Bootstrap 5 da HTMLning `<small>` elementi (va `.small` classi) har qanday sarlavhada kichikroq va ikkinchi darajali matn yaratish uchun ishlatiladi:

<figure><img src="../../.gitbook/assets/image (615).png" alt=""><figcaption></figcaption></figure>

### \<mark>

Bootstrap 5 sariq fon rangi va biroz paddingli \<mark>  va .mark stilini yaratadi:

<figure><img src="../../.gitbook/assets/image (564).png" alt=""><figcaption></figcaption></figure>

### \<abbr>

Bootstrap 5 HTMLning `<abbr>` elementiga nuqtali pastki hoshiya va kursor ustida so'roq belgisi ko'rinishdia stil beradi:

<figure><img src="../../.gitbook/assets/image (581).png" alt=""><figcaption></figcaption></figure>

### \<blockquote>

Boshqa manbaning kontentini ko'rsatishda `.blockquote` classini  `<blockquote>` elementiga qo'shing. Va manbaga nom berishda, masalan, "WWF veb-saytidan" `.blockquote-footer` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (613).png" alt=""><figcaption></figcaption></figure>

### \<dl>

Bootstrap 5  `<dl>` elementiga quyidagi tarzda  still beradi:

<figure><img src="../../.gitbook/assets/image (626).png" alt=""><figcaption></figcaption></figure>

### \<code>

Bootstrap 5 `<code>` elementiga quyidagi tarzda still beradi:

<figure><img src="../../.gitbook/assets/image (574).png" alt=""><figcaption></figcaption></figure>

### \<kbd>

Bootstrap 5 `<kbd>` elementiga quyidagi tarzda still beradi:

<figure><img src="../../.gitbook/assets/image (623).png" alt=""><figcaption></figcaption></figure>

### \<pre>

Bootstrap 5 `<pre>` elementiga quyidagi tarzda still beradi:

<figure><img src="../../.gitbook/assets/image (593).png" alt=""><figcaption></figcaption></figure>

### Qo'shimcha tipografik classlar

Quyidagi Bootstrap 5 classlari HTML elementlarining stillariga qo'shilishi mumkin:

| Class                   | Ta'rif                                                                                                                                                                                                                                                                                                            |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `.lead`                 | Paragrafni alohida ajratib turadi                                                                                                                                                                                                                                                                                 |
| `.text-start`           | Chapga taqalgan matnni bildiradi                                                                                                                                                                                                                                                                                  |
| `.text-break`           | Uzun matn joylashuvni buzishini oldini oladi                                                                                                                                                                                                                                                                      |
| `.text-center`          | Markazga qo'yilgan matnni bildiradi                                                                                                                                                                                                                                                                               |
| `.text-decoration-none` | Havoladan pastki chiziqni olib tashlaydi                                                                                                                                                                                                                                                                          |
| `.text-end`             | O'ngga taqalgan matnni bildiradi                                                                                                                                                                                                                                                                                  |
| `.text-nowrap`          | Matnga no wrap xususiyatini beradi                                                                                                                                                                                                                                                                                |
| `.text-lowercase`       | Kichik harflar bilan yozilgan matnni bildiradi                                                                                                                                                                                                                                                                    |
| `.text-uppercase`       | Katta harflar bilan yozilgan matnni bildiradi                                                                                                                                                                                                                                                                     |
| `.text-capitalize`      | Bosh harflar bilan yozilgan matnni bildiradi                                                                                                                                                                                                                                                                      |
| `.initialism`           | \<abbr> elementi ichidagi matnni biroz kichikroq shrift o'lchamida ko'rsatadi                                                                                                                                                                                                                                     |
| `.list-unstyled`        | Roʻyxat elementlarining standart list-style va margin left stilini olib tashlaydi (ikkala \<ul> va \<ol> da ishlaydi). Bu classf faqat bevosita ichki ro'yhat elementlariga taalluqlidir (har qanday ichki roʻyxatlardan standart list-styleni olib tashlash uchun ushbu classni ichki roʻyxatlarga ham qoʻllang) |
| `.list-inline`          | Biarcha roʻyxat elementlarini bitta qatorga joylashtiradi (har bir \<li> elementda .list-inline-item bilan birga ishlatiladi)                                                                                                                                                                                     |
