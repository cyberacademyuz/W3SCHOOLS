# CSS Overflow

CSSning `overflow` xususiyati, agar kontent o'zi egallab turgan maydondan tashqariga chiqib ketsa nima qilish kerakligini belgilaydi.

<figure><img src="../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

### CSS overflow <a href="#css-overflow" id="css-overflow"></a>

CSSning `overflow` xususiyati, agar kontent o'zi egallab turgan maydondan tashqariga chiqib ketsa nima qilish kerakligini belgilaydi.

`overflow` xususiyatida quyidagi qiymatlar mavjud:

* `visible` - Default. Maydondan chiqib ketgan kontentga tegilmagan. Kontent element maydonidan tashqarida ko'rinadi.
* `hidden` - Overflow bo'lgan kontent kesilgan va qolgan kontent ko'rinmaydi
* `scroll` - overflow bo'lgan kontent kesilgan va qolgan kotnentni ko'rish uchun scrollbar qo'shilgan.
* `auto` - scrollga o'xshash, lekin scrollbarni faqat kerakli vaqtda qo'shadi

{% hint style="warning" %}
**Eslatma:** `overflow` xususiyati faqat block elementlariga ma'lum bir balandlik berilgandagina ishlaydi

**Eslatma:** OS X Lion-da (Mac-da) skroll barlar standart standart tarzda yashirin bo'ladi va faqat foydalanilganda ko'rsatiladi (garchi "`overflow: scroll`" berilgan bo'lsa ham).
{% endhint %}

### overflow: visible; <a href="#overflow-visible" id="overflow-visible"></a>

Standart tarzda overflow qiymayi `visible` bo'ladi. Maydondan chiqib ketgan kontentga tegilmagan. Kontent element maydonidan tashqarida ko'rinadi.

![](<../../.gitbook/assets/image (478).png>)

```
div {
  width: 200px;
  height: 65px;
  background-color: coral;
  overflow: visible;
}
```

### overflow: hidden; <a href="#overflow-hidden" id="overflow-hidden"></a>

`overflow: hidden;` da maydondan chiqib ketgan kontent kesiladi va kontentning qolgan qismi ko'rinmaydi.

![](<../../.gitbook/assets/image (303).png>)

```
div {
  overflow: hidden;
}
```

### overflow: scroll; <a href="#overflow-scroll" id="overflow-scroll"></a>

Xususiyat qiymayiga `scroll` berilganida o'rtib chiqgan kontent olib tashlanadi va kontentning qolgan qismini ko'rish uchun scroll qo'shiladi.  Scrollbar ham gorizontal, ham vertikal holatga qo'shiladi (hatto u qism kerak bo'lmasa ham)

![](<../../.gitbook/assets/image (486).png>)

```
div {
  overflow: scroll;
}
```

### overflow: auto; <a href="#overflow-auto" id="overflow-auto"></a>

`auto` qiymati ham `scroll` qiymatiga o'xshaydi ammo u scrollbarni faqat kerakli tarafga qo'shadi.

![](<../../.gitbook/assets/image (488).png>)

```
div {
  overflow: auto;
}
```

### overflow-x va overflow-y <a href="#overflow-x-va-overflow-y" id="overflow-x-va-overflow-y"></a>

`overflow-x` va `overflow-y` xususiyatlari gorizontal yoki vertikal holatdagi kontentning overflowini o'zgartiradi.

`overflow-x` kontentning o'ngdagi va chapdagi burchaklarni belgilaydi

`overflow-y` kontentning tepadagi va pastdagi burchaklarini belgilaydi

```
div {
  overflow-x: hidden; /* Hide horizontal scrollbar */
  overflow-y: scroll; /* Add vertical scrollbar */
}
```

### CSS ning barcha overflow xususiyatlari <a href="#barcha-css-overflow-xususiyatlari" id="barcha-css-overflow-xususiyatlari"></a>

| Xususiyat                                                                     | Ta'rif                                                                                                                   |
| ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [overflow](https://www.w3schools.com/cssref/pr\_pos\_overflow.asp)            | Element kontent qutisidan chiqib ketganda nima qilish kerakligini belgilaydi                                             |
| [overflow-wrap](https://www.w3schools.com/cssref/css3\_pr\_overflow-wrap.asp) | Brauzer uzun so'zli satrlarni, agar ular konteyneridan to'lib toshgan bo'lsa, uzishi mumkinmi yoki yo'qligini belgilaydi |
| [overflow-x](https://www.w3schools.com/cssref/css3\_pr\_overflow-x.asp)       | Kontentning chap/o‘ng qirralari elementning kontent maydonini to‘ldirib yuborsa, nima qilish kerakligini belgilaydi      |
| [overflow-y](https://www.w3schools.com/cssref/css3\_pr\_overflow-y.asp)       | Kontentning yuqori/pastki qirralari elementning kontent maydonini to'ldirib yuborsa, nima qilish kerakligini belgilaydi  |
