# Font Style

### CSS Shrift stili <a href="#css-font-stili" id="css-font-stili"></a>

`font-style` xususiyati asosan matnni italic (kursiv) qilish uchun ishlatiladi.

Xususiyatni 3 ta qiymati mavjud:

* normal - matn odatiy ko'rinishda bo'ladi
* italic - matn kursiv ko'rinishda bo'ladi
* oblique - matndagi harflarni biroz egilgan holda ko'rsatadi (oblique ham o'zi italic ni bir turi ammo kam ishlatiladi)

```
p.normal {
  font-style: normal;
}

p.italic {
  font-style: italic;
}

p.oblique {
  font-style: oblique;
}
```

### Font Weight <a href="#font-weight" id="font-weight"></a>

`font-weight` xususiyati shriftning qanday "qalinlik"da bo'lishini belgilaydi:

```
p.normal {
  font-weight: normal;
}

p.thick {
  font-weight: bold;
}
```

### Font variant <a href="#font-variant" id="font-variant"></a>

`font-variant` xususiyati matnni small-caps shriftida ko'rsatilishi yoki ko'rsatilmasligini belgilaydi.

small-caps shriftida barcha kichik harflar katta harflarga aylantiriladi. Biroq, aylantirilgan katta harflar matndagi asl katta harflarga qaraganda kichikroq o'lchamda ko'rinadi.

```
p.normal {
  font-variant: normal;
}

p.small {
  font-variant: small-caps;
}
```
