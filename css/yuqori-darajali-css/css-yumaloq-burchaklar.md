# CSS Yumaloq burchaklar

<figure><img src="../../.gitbook/assets/image (804).png" alt=""><figcaption></figcaption></figure>

### CSS border-radius xususiyati <a href="#css-border-radius-xususiyati" id="css-border-radius-xususiyati"></a>

CSSning `border-radius` xususiyati elementning burchagi qanchalik dumaloq bo'lishi kerakligini belgilaydi

Bunga 3 ta misol:

1. Background rangga ega element uchun yumaloq burchaklar

![](<../../.gitbook/assets/image (800).png>)



2. Xoshiyali element uchun yumaloq burchaklar:

![](<../../.gitbook/assets/image (791).png>)

3. Background rasmli element uchun yumaloq burchaklar

![](<../../.gitbook/assets/image (779).png>)

Kodlari:

```
#rcorners1 {
  border-radius: 25px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners2 {
  border-radius: 25px;
  border: 2px solid #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners3 {
  border-radius: 25px;
  background: url(paper.gif);
  background-position: left top;
  background-repeat: repeat;
  padding: 20px;
  width: 200px;
  height: 150px;
}
```

{% hint style="warning" %}
**Maslahat:** `border-radius` xususiyati `border-top-left-radius`, `border-top-right-radius`, `border-bottom-right-radius` va `border-bottom-left-radius` xususiyatlari uchun qisqartma hisoblanadi.
{% endhint %}

### CSS border-radius - Har bir burchakni belgilash <a href="#css-border-radius-da-har-bir-burchakni-belgilash" id="css-border-radius-da-har-bir-burchakni-belgilash"></a>

`border-radius` xususiyati 1 tadan 4 tagacha qiymat qabul qilishi mumkin. Quyida qoidalarini keltiramiz:

**To'rtta qiymatli - border-radius: 15px 50px 30px 5px;** (birinchi qiymat tepa chap burchak uchun, ikkinchisi tepa qismdagi o'ng burchak uchun, uchinchi qiymat pastki o'ng burchak uchun va to'rtinchisi pastki chap burchak uchun)

![](<../../.gitbook/assets/image (275).png>)

**Uchta qiymatli - border-radius: 15px 50px 30px;** (birinchi qiymat tepa chap burchak uchun, ikkinchisi tepa o'ng burchak va pastki chap burchak uchun va uchinchi qiymat o'ng tomondagi pastki burchak uchun)

![](<../../.gitbook/assets/image (806).png>)

**Ikkita qiymatli - border-radius: 15px 50px;** (birinchi qiymat tepa qismning chap burchagi va pastki o'ng burchak uchun, ikkinchisi esa tepa tomndagi o'ng burchak hamda pastki chap burchak uchun)

![](<../../.gitbook/assets/image (773).png>)

**Bitta qiymatli - border-radius: 15px;** (barcha burchaklar uchun)

![](<../../.gitbook/assets/image (792).png>)

Mana kodlari:

```
#rcorners1 {
  border-radius: 15px 50px 30px 5px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners2 {
  border-radius: 15px 50px 30px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners3 {
  border-radius: 15px 50px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners4 {
  border-radius: 15px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}
```

Bundan tashqari, elliptik burchaklar yaratishingiz mumkin:

```
#rcorners1 {
  border-radius: 50px / 15px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners2 {
  border-radius: 15px / 50px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners3 {
  border-radius: 50%;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}
```

### CSSning yumaloq burchaklar uchun xususiyatlari <a href="#css-dumaloq-burchaklar-xususiyatlari" id="css-dumaloq-burchaklar-xususiyatlari"></a>

| Xususiyat                                                                                               | Ta'rif                                        |
| ------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| [border-radius](https://www.w3schools.com/cssref/css3\_pr\_border-radius.asp)                           | Barcha to'rtta burchak uchun qisqartma        |
| [border-top-left-radius](https://www.w3schools.com/cssref/css3\_pr\_border-top-left-radius.asp)         | Tepadagi Chap burchakning shaklini belgilaydi |
| [border-top-right-radius](https://www.w3schools.com/cssref/css3\_pr\_border-top-right-radius.asp)       | Tepadagi o'ng burchakning shaklini belgilaydi |
| [border-bottom-right-radius](https://www.w3schools.com/cssref/css3\_pr\_border-bottom-right-radius.asp) | Pastki o'ng burchakning shaklini belgilaydi   |
| [border-bottom-left-radius](https://www.w3schools.com/cssref/css3\_pr\_border-bottom-left-radius.asp)   | Pastki chap burchakning shaklini belgilaydi   |
