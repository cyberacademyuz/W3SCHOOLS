# Box shadow

### CSS box-shadow xususiyati <a href="#css-box-shadow" id="css-box-shadow"></a>

CSSning `box-shadow` xususiyati elementga bir yoki bir nechta soyalar berish uchun ishlatiladi.

### Gorizontal va Vertikal soya yaratish <a href="#gorizontal-va-vertikal-soyani-belgilang" id="gorizontal-va-vertikal-soyani-belgilang"></a>

Eng oddiy soya berish usuli gorizontal va vertikal soyadan foydalanish hisoblanadi. Soyaning standart rangi joriy matn rangi bilan bir xil bo'ladi.

![](<../../../.gitbook/assets/image (350).png>)

```
div {
  box-shadow: 10px 10px;
}
```

### Soya uchun rang berish <a href="#soya-uchun-rang-berish" id="soya-uchun-rang-berish"></a>

rang parametri soyaning rangini belgilaydi.

![](<../../../.gitbook/assets/image (241).png>)

```
div {
  box-shadow: 10px 10px lightblue;
}
```

### Soyaga blur effektini qo'shish <a href="#soyaga-blur-effektini-qoshish" id="soyaga-blur-effektini-qoshish"></a>

Blur parametri blur radiusini belgilaydi. Bunda raqam qanchalik katta bo'lsa, soya shunchalik ko'p  blur effektiga ega bo'ladi.

![](<../../../.gitbook/assets/image (651).png>)

```
div {
  box-shadow: 10px 10px 5px lightblue;
}
```

### Soyaning tarqalish radiusini o'rnatish <a href="#soyaning-tarqalish-radiusini-ornatish" id="soyaning-tarqalish-radiusini-ornatish"></a>

`spread` parametri tarqalish radiusini belgilaydi. Berilgan musbat qiymat soyaning o'lchamini oshiradi, manfiy qiymat esa soyaning o'lchamini kamaytiradi.

![](<../../../.gitbook/assets/image (225).png>)

```
div {
  box-shadow: 10px 10px 5px 12px lightblue;
}
```

### Inset parametrini belgilash <a href="#inset-parametrini-belgilash" id="inset-parametrini-belgilash"></a>

`Inset` parametri soyani tashqi soyadan ichki soyaga o'zgartiradi.

![](<../../../.gitbook/assets/image (240).png>)

```
div {
  box-shadow: 10px 10px 5px lightblue inset;
}
```

### Bir qancha soyalar qo'shish <a href="#bir-qancha-soyalarni-qoshish" id="bir-qancha-soyalarni-qoshish"></a>

Elementda bir nechta soyalar ham bo'lishi mumkin:

```
div {
  box-shadow: 5px 5px blue, 10px 10px red, 15px 15px green;
}
```

### Kartalar <a href="#kartalar" id="kartalar"></a>

Qog'ozga o'xshash kartalar yaratish uchun ham `box-shadow` xususiyatidan foydalanishingiz mumkin:

![](<../../../.gitbook/assets/image (648).png>)                                               ![](<../../../.gitbook/assets/image (221).png>)

```
div.card {
  width: 250px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  text-align: center;
}
```

### CSS Soya Xususiyatlari <a href="#css-soya-xususiyatlari" id="css-soya-xususiyatlari"></a>

Quyidagi jadvalda CSSning soya xususiyatlari haqida ma'lumot ko'rsatilgan:

| Xususiyat                                                                 | Ta'rif                                                             |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| [box-shadow](https://www.w3schools.com/cssref/css3\_pr\_box-shadow.asp)   | Elementga bir yoki bir nechta soyalarni qo'llash uchun ishlatiladi |
| [text-shadow](https://www.w3schools.com/cssref/css3\_pr\_text-shadow.asp) | Matnga bir yoki bir nechta soyalarni qo'llash uchun ishlatiladi    |
