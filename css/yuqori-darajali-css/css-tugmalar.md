# CSS Tugmalar

CSS-dan foydalanib tugmalarni qanday yasashni o'rganing.

### Oddiy tugmani stillash

![](<../../.gitbook/assets/image (357).png>)

```
.button {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
```

### Tugma ranglari

Tugmaning orqafon rangini o'zgartirish uchun `background-color` xususiyatidan foydalaning:

![](<../../.gitbook/assets/image (229).png>)

```
.button1 {background-color: #4CAF50;} /* Green */
.button2 {background-color: #008CBA;} /* Blue */
.button3 {background-color: #f44336;} /* Red */
.button4 {background-color: #e7e7e7; color: black;} /* Gray */
.button5 {background-color: #555555;} /* Black */
```

### Tugma o'lchamlari

![](<../../.gitbook/assets/image (359).png>)

Tugmaning shrift o'lchamini o'zgartirish uchun `font-size` xususiyatdan foydalaning:

```
.button1 {font-size: 10px;}
.button2 {font-size: 12px;}
.button3 {font-size: 16px;}
.button4 {font-size: 20px;}
.button5 {font-size: 24px;}
```

Tugma paddingini o'zgartirish uchun `padding` xususiyatidan foydalaning:

![](<../../.gitbook/assets/image (253).png>)

```
.button1 {padding: 10px 24px;}
.button2 {padding: 12px 28px;}
.button3 {padding: 14px 40px;}
.button4 {padding: 32px 16px;}
.button5 {padding: 16px;}
```

### Dumaloq tugmalar

![](<../../.gitbook/assets/image (263).png>)

Tugmaga yumaloq burchaklar qo'shish uchun `border-radius` xususiyatidan foydalaning:

```
.button1 {border-radius: 2px;}
.button2 {border-radius: 4px;}
.button3 {border-radius: 8px;}
.button4 {border-radius: 12px;}
.button5 {border-radius: 50%;}
```

### Tugmaning rangli chegaralari

![](<../../.gitbook/assets/image (115).png>)

Tugmaga rangli chegara qo'shish uchun `border` xususiyatidan foydalaning:

```
.button1 {
  background-color: white;
  color: black;
  border: 2px solid #4CAF50; /* Green */
}
...
```

### Hoverli tugmalar

![](<../../.gitbook/assets/image (655).png>)

Sichqonchani kursorini tugma ustiga olib borganingizda uning tilini o'zgartirish uchun `:hover` selektoridan foydalaning.

**Maslahat:** Hover effektining bajarilish tezligini belgilash uchun `transition-duration` xususiyatidan foydalaning:

```
.button {
  transition-duration: 0.4s;
}

.button:hover {
  background-color: #4CAF50; /* Green */
  color: white;
}
...
```

### Soyali tugmalari

![](<../../.gitbook/assets/image (246).png>)

Tugmaga soya berish uchun `box-shadow` xususiyatidan foydalaning:

```
.button1 {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
}

.button2:hover {
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}
```

### O'chirib qo'yilgan tugmalar

![](<../../.gitbook/assets/image (109).png>)

Tugmaga shaffoflik qo'shish uchun `opacity` xususiyatdan foydalaning ("o'chirilgan" ko'rinish hosil qiladi).

**Maslahat:** Bundan tashqari, `cursor` xususiyatini “not-allowed” qiymati bilan qoʻshishingiz mumkin, bunda sichqoncha kursorini tugma ustiga olib borganingizda “no parking sign” belgisi paydo boʻladi:

```
.disabled {
  opacity: 0.6;
  cursor: not-allowed;
}
```

### Tugma kengligi

<figure><img src="../../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure>

Standart holda, tugma o'lchami uning matn kontenti bilan belgilanadi (kontentning kengligi kabi). Tugmaning kengligini o'zgartirish uchun `width` xususiyatidan foydalaning:

```
.button1 {width: 250px;}
.button2 {width: 50%;}
.button3 {width: 100%;}
```

### Tugma guruhlari

![](<../../.gitbook/assets/image (230).png>)

\
Marginlarni olib tashlang va tugma guruhini yaratish uchun har bir tugmaga `float:left` bering:

```
.button {
  float: left;
}
```

### Chegarali tugma guruhi

![](<../../.gitbook/assets/image (259).png>)

Chegarali tugma guruhini yaratish uchun `border` xususiyatidan foydalaning:

```
.button {
  float: left;
  border: 1px solid green;
}
```

### Vertikal tugmalar guruhi

![](<../../.gitbook/assets/image (395).png>)

\
Tugmalarni yonma-yon emas vertikal tarzda guruhlash uchun `float:left` o'rniga `display:block`dan foydalaning:

```
.button {
  display: block;
}
```

### Rasmdagi tugma

![](<../../.gitbook/assets/image (391).png>)

### Animatsiyali tugmalar

{% hint style="info" %}
Hover bo'lganda strelka qo'shish:\
![](<../../.gitbook/assets/image (479).png>)
{% endhint %}

{% hint style="info" %}
Bosganda "pressed" effektini qo'shish:\
![](<../../.gitbook/assets/image (744).png>)
{% endhint %}

{% hint style="info" %}
Hover bo'lganda yo'qolish effekti:\
![](<../../.gitbook/assets/image (751).png>)
{% endhint %}

{% hint style="info" %}
Bosilganda "ripple" effektini qo'shish:\
![](<../../.gitbook/assets/image (368).png>)
{% endhint %}
