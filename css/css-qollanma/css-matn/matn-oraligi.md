# Matn oralig'i

### Matn oralig'i <a href="#matn-oraligi" id="matn-oraligi"></a>

Ushbu bo'limda quyidagi xususiyatlar haqida bilib olasiz:

* <mark style="color:red;">`text-indent`</mark>
* <mark style="color:red;">`letter-spacing`</mark>
* <mark style="color:red;">`line-height`</mark>
* <mark style="color:red;">`word-spacing`</mark>
* <mark style="color:red;">`white-space`</mark>

### Text indentation <a href="#text-indentation" id="text-indentation"></a>

`text-indent` xususiyati matnning birinchi qatorini xatboshi sifati joy tashlash uchun ishlatiladi:

```
p {
  text-indent: 50px;
}
```

### Letter Spacing

`letter-spacing` xususiyati matndagi belgilar (harflar) orasidagi masofani belgilash uchun ishlatiladi.

Ushbu misolda belgilar orasidagi masofani kattalashtirilish va kichraytirilishni qanday qilish ko'rsatilgan:

```
h1 {
  letter-spacing: 5px;
}

h2 {
  letter-spacing: -2px;
}
```

### Line height <a href="#line-height" id="line-height"></a>

`line-height` xususiyati qatorlar orasidagi masofani belgilaydi:

```
p.small {
  line-height: 0.8;
}

p.big {
  line-height: 1.8;
}
```

### Word spacing <a href="#soz-oraligi" id="soz-oraligi"></a>

`word-spacing` xususiyati matndagi so'zlar oralg'ini belgilash uchun ishlatiladi.

Quyidagi misolda so'zlar orasidagi masofa kattalashtirilish va kichraytirilishni qanday qilish ko'rsatilgan:

```
p.one {
  word-spacing: 10px;
}

p.two {
  word-spacing: -2px;
}
```

### White space <a href="#white-space" id="white-space"></a>

`white-space` xususiyati element matnidagi bo'sh joy va qator tashlashlarni boshqarishga yordam beradi.

Ushbu misolda element ichidagi matnni keyingi qatorga tushishini cheklash ko'rsatiladi:

```
p {
  white-space: nowrap;
}
```

### CSSning barcha matn oraliqlariga aloqador xususiyatlari <a href="#css-barcha-matn-oraligi-xususiyatlari" id="css-barcha-matn-oraligi-xususiyatlari"></a>

| Xususiyat                                                                       | Ta'rif                                                          |
| ------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| [letter-spacing](https://www.w3schools.com/cssref/pr\_text\_letter-spacing.asp) | Matndagi belgilar orasidagi masofani belgilaydi                 |
| [line-height](https://www.w3schools.com/cssref/pr\_dim\_line-height.asp)        | Qatorlar orasidagi masofani belgilaydi                          |
| [text-indent](https://www.w3schools.com/cssref/pr\_text\_text-indent.asp)       | Matn blokidagi birinchi qatorning chekinishini belgilaydi       |
| [white-space](https://www.w3schools.com/cssref/pr\_text\_white-space.asp)       | Element ichidagi bo'sh joy qanday ishlov berilishini belgilaydi |
| [word-spacing](https://www.w3schools.com/cssref/pr\_text\_word-spacing.asp)     | Matndagi so'zlar orasidagi masofani belgilaydi                  |
